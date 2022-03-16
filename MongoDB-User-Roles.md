MongoDB User Role Management

MongoDB shell version v3.6.23

connecting to: mongodb://127.0.0.1:27017/?gssapiServiceName=mongodb

Implicit session: session { "id" : UUID("227b3086-25bc-48b0-9d1a-1cb776bb22cc") }

MongoDB server version: 3.6.23

switched to db admin

system.roles

system.users

system.version



use admin
db.createRole(
   {
     role: "ClusterwideAdmin",
     privileges: [
       { resource: { cluster: true }, actions: [ "addShard" ] },
       { resource: { db: "config", collection: "" }, actions: [ "find", "update", "insert", "remove" ] },
       { resource: { db: "sample", collection: "" }, actions: [ "find", "update", "insert", "remove" ] },
       { resource: { db: "users", collection: "usersCollection" }, actions: [ "update", "insert", "remove" ] },
       { resource: { db: "", collection: "" }, actions: [ "find" ] }
     ],
     roles: [
       { role: "read", db: "admin" }
     ]
   },
   { w: "majority" , wtimeout: 5000 }
)


Installing and starting MongoDB :
Click on Install
Now in a terminal type, mongo
Now you have



Successfully running MongoDB environment
a command line shell to interact with MongoDB
This question gives you hands-on experience on User and Role Management in MongoDB.



1. Create a User with Role

use sample

db.createUser(
   {
     user: "usertest",
     pwd: "usertest123",
     roles: [ "readWrite", "dbAdmin" ]
   }
);


2. Get user


db.getUser("usertest");


3. Drop user


db.dropUser("usertest", {w: "majority",  wtimeout: 2000});


4. Create Role and assign to multiple databases


use admin

db.createRole(
   {
     role: "ClusterwideAdmin",
     privileges: [
       { resource: { cluster: true }, actions: [ "addShard" ] },
       { resource: { db: "config", collection: "" }, actions: [ "find", "update", "insert", "remove" ] },
       { resource: { db: "sample", collection: "" }, actions: [ "find", "update", "insert", "remove" ] },
       { resource: { db: "users", collection: "usersCollection" }, actions: [ "update", "insert", "remove" ] },
       { resource: { db: "", collection: "" }, actions: [ "find" ] }
     ],
     roles: [
       { role: "read", db: "admin" }
     ]
   },
   { w: "majority" , wtimeout: 5000 }
)


5. Revoke User


db.revokeRolesFromUser( "usertest",
                        [ { role: "read", db: "sample" 
                          }, 
                        "readWrite"
                        ],
                        { w: "majority" }
                      )
                      
