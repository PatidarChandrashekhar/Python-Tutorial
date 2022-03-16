MongoDB - Query Optimization

sudo rm /var/lib/apt/lists/lock
sudo rm /var/cache/apt/archives/lock
sudo rm /var/lib/dpkg/lock
sudo apt install mongodb-server -y
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.6 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.6.list
sudo apt-get update
sudo apt-get install -y mongodb-org
sudo service mongodb start


----------------

Installing and starting MongoDB :
Click on Install
Now in a terminal type, mongo
Now you have


Successfully running MongoDB environment


a command line shell to interact with MongoDB



1. Lets evaluate performance of query

Consider 'School' is a collection which contains student documents. Each document consists of Full name of student, subject studied, and marks scored in a particular subject.

try {
   db.school.insertMany( [
{ "_id" :"1", "Fullname" :"Mridhula", "subject" : "Science", "score" : 680 },
{ "_id" : "2", "Fullname" : "Mridhula", "subject" : "Mathematics", "score" : 980 },
{ "_id" : "3", "Fullname" : "Mridhula", "subject" : "English", "score" : 770 },
{ "_id" :"4", "Fullname" : "Akhila", "subject" : "science", "score" : 670 },
{ "_id" : "5", "Fullname" : "Akhila", "subject" : "Mathematics", "score" : 870},
{ "_id" : "6", "Fullname" : "Akhila", "subject" : "English", "score" : 890 },
{ "_id" :"7", "Fullname" : "Abhilasha", "subject" : "Science", "score" : 670 },
{ "_id" :"8", "Fullname" : "Abhilasha", "subject" : "Mathematics", "score" : 780 },
{ "_id" :"9", "Fullname" : "Abhilasha", "subject" : "English", "score" : 900 }
   ] );
} catch (e) {
   print (e);
};

2. use find() command

Find details of students whose score is greater than 670 by using the following command:

db.school.find( { score: { $gt: 670 } } ) ;

3. Use Explain() method and find the output with out creating Index
db.school.find( { score: { $gt: 670 } } ).explain("executionStats");

queryPlanner.winningPlan.inputStage.stage :
COLLSCAN to indicate that there is no index use.

executionStats.nReturned:
7 to indicate that the query matches and returns seven documents.

executionStats.totalKeysExamined:
Displays 0 to indicate that MongoDB scanned the entire document with the absence of a key.

executionStats.totalDocsExamined:
Displays 9 to indicate that MongoDB scanned 9 documents.

4. Create Indexes
Create a single-field Index on the field 'Score': db.school.createIndex( { score:1} );

5. use Explain () and find the output after creating Index
db.school.find( { score: { $gt: 670 } } ).explain("executionStats");

queryPlanner.winningPlan.inputStage.stage:
Displays IXSCAN to indicate index use.

executionStats.nReturned:
Displays 7 to indicate that the query matches and returns 7 documents.

executionStats.totalKeysExamined:
Displays 7 to indicate that MongoDB scanned 7 index entries. The number of keys examined match the number of documents returned, meaning that the MongoDB only had to examine index keys to return the results. The MongoDB did not have to scan all the documents, and only the 7 matching documents had to be moved into the memory. This ensures results in a very efficient manner.

executionStats.totalDocsExamined:
Displays 7 to indicate that MongoDB scanned 7 documents.


6. Find the indexes created
db.school.getIndexes();


7. Find the students with more condition
Find details of students whose score is greater than 670, and subject is sports:

db.school.find( { score: { $gt: 670 }, subject: "sports" } );

8. Use explain () and find the output.
db.school.find( { score: { $gt: 670 }, subject: "sports" } ).explain("executionStats");

9. Create Compound Indexes
Create Compound Indexes for the fields 'Score' and 'Subjects':

db.school.createIndex( { score: 1, subject: 1 } );

10. Check after creating Compound Index
db.school.find( { score: { $gt: 670 }, subject: "sports" } ).explain("executionStats");

Examine
"keysExamined" : 7, and "nReturned" : 3

7 records are verified to find 3 records.

11. Create Compound Indexes by changing the order
Change the order of the Index:

db.school.createIndex( { subject: 1 ,score: 1,} )

12. Use explain and find the output of the Compound Index by changing the order
db.school.find( { score: { $gt: 670 }, subject: "sports" } ).explain("executionStats");

Examine
"keysExamined" : 3, and "nReturned" : 3

In this example query, the Compound Index {subject: 1, score: 1} is more efficient than the compound index {score: 1, subject: 1}. In Compound Indexes, the order of the fields affect the performance of the query.

--------------
