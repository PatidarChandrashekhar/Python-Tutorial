MongoDB - Indexing

sudo rm /var/lib/apt/lists/lock
sudo rm /var/cache/apt/archives/lock
sudo rm /var/lib/dpkg/lock
sudo apt install mongodb-server -y
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.6 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.6.list
sudo apt-get update
sudo apt-get install -y mongodb-org
sudo service mongodb start

-------------

Installing and starting MongoDB :
Click on Install
Now in a terminal type, mongo
Now you have


Successfully running MongoDB environment


a command line shell to interact with MongoDB


This question gives you hands-on experience on Indexes in MongoDB.


1. Use the database local

2. Create Products Collection. Insert the following five documents in to the collection.

db.Products.save({
 _id: 1,
 Fruitname: "Mango",
 Retailer: [
  {ProviderName: "FutureRetail", ProviderKey: "1232"},
  {ProviderName: "More", ProviderKey: "1423"}
 ]
});

db.Products.save({
 _id: 2,
 Fruitname: "Apple",
 Retailer: [
  {ProviderName: "Spencers", ProviderKey: "13443"}
 ]
});

db.Products.save({
 _id: 3,
 Fruitname: "WaterMelon",
 Retailer: [
  {ProviderName: "Hypercity", ProviderKey: "1445345"}
 ]
});

db.Products.save({
 _id: 4,
 Fruitname: "orange",
Retailer: [
  {ProviderName: "v-mart", ProviderKey: "13443"},
  {ProviderName: "HyperCity", ProviderKey: "1768"}
 ]
});

db.Products.save({
 _id: 5,
 Fruitname: "Plum",
 Retailer: [
  {ProviderName: "DMART", ProviderKey: "13443"},
  {ProviderName: "KMART", ProviderKey: "768"}
 ]
});

3. Use Find() method to select a record

Query the Products collection by finding records named 'plum':

`db.Products.find({ "Fruitname": "Plum" }).pretty();`

4. Use Explain() Method

`db.Products.find({ "Fruitname": "Plum" }).explain();`

 
## View:
"winningPlan" : { "stage" : "COLLSCAN"}

5. Create Index for Single Field

## Create Index for Single Field: Fruitname

`db.Products.createIndex({ "Fruitname": 1 });`

6. `db.Products.find({ "Fruitname": "Plum" }).explain();`
 
## View
 
winningPlan" : {
                        "stage" : "FETCH",
                        "inputStage" : {
                                "stage" : "IXSCAN",

7. Create another two indexes 

Create Index for Retailer.ProviderKey and Retailer.ProviderName:
`db.Products.createIndex({ "Retailer.ProviderKey": 1,  "Retailer.ProviderName": 1 }); `

8. Use find and query the records based on conditions  

db.Products.find({ "Retailer.ProviderKey": "1232",  "Retailer.ProviderName": "FutureRetail" });

 ## Perform Execution status for the above query

`db.Products.find({ "Retailer.ProviderKey": "1232",  "Retailer.ProviderName": "FutureRetail" }).explain("executionStats");`

9. Determining the sizes and details of the Indexes 

db.Products.stats();

10.  Find the indexes in the collection 

`db.Products.getIndexes(); `


---------------------------

#!/bin/bash
SCORE=0
PASS=0
TOTAL_TESTS=4


(echo "use local"; echo "show collections" ) | mongo > collection.txt
if(($(grep -io -e "Products" collection.txt | wc -l) ==1)); then PASS=$((PASS+1)); fi;

( echo "use local" ; echo 'db.Products.find({ "Fruitname": "Plum" }).pretty();' ) | mongo > find.txt
if(($(grep -io -e "DMART" -e "KMART" -e "13443" -e "768" find.txt | wc -l) >=4)); then PASS=$((PASS+1)); fi;


( echo "use local" ; echo 'db.Products.find({ "Fruitname": "Plum" }).explain();' ) | mongo > method_after_index.txt
if(($(grep -io -e "FETCH" -e "IXSCAN" method_after_index.txt | wc -l) >=2)); then PASS=$((PASS+1)); fi;


( echo "use local" ; echo "db.Products.getIndexes();" ) | mongo > index.txt
if(($(grep -io -e "Fruitname_1" -e "Retailer.ProviderKey_1_Retailer.ProviderName_1" index.txt | wc -l) >=2)); then PASS=$((PASS+1)); fi;



echo $PASS
SCORE=$(($PASS*100 / $TOTAL_TESTS))
echo "FS_SCORE:$SCORE%"



-----------------------
