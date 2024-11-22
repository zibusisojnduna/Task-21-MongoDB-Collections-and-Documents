<img src="https://socialify.git.ci/zibusisojnduna/Task-21-MongoDB-Collections-and-Documents/image?language=1&name=1&owner=1&pattern=Circuit%20Board&stargazers=1&theme=Dark" alt="Task-21-MongoDB-Collections-and-Documents" width="640" height="320" />

<h1>Task 21:MongoDB Databases, Collections and Documents</h1>

<p>This document provides step-by-step instructions for using the MongoDB shell (mongosh) to complete the following tasks

Starting the MongoDB shell

Creating databases and collections

Inserting documents

Exporting the database

Starting the MongoDB Shell (mongosh)

Open a terminal or command prompt.</p>

<h1>Features</h1>
<p>Facilitators- A collection with the details of facilitators.</p>
<p>Trainees- A collection with the details of trainees.</p>
<p>Projects- A collections with the details of the projects.</p>

<h1>Prerequisites</h1>
<p>Before you begin, ensure you have met the following requirements:</p>

<p>MongoDB</p>

<p>Mongo Compass</p>

## Run Locally
Clone the project
```bash
  git clone https://github.com/zibusisojnduna/Task-21-MongoDB-Collections-and-Documents
```
Go to the project directory
```bash
  cd Task-21-MongoDB-Collections-and-Documents
```

To start MongosDB Shell
```
mongosh
```

<h1>If the MongoDB server is running on a non-default host or port, specify the connection string. For example:</h1>
```

mongosh "mongodb://localhost:27017"
```

<h1>Switch to the desired database</h1>
```
use codetribe
```

<h1>a. Facilitators Collection:</h1>
Insert a document with the fields Name, Location, and Course:

```
db.Facilitators.insertOne({
  Name: "John Doe",
  Location: "Cape Town",
  Course: "Web Development"
})
```

<h1>b. Trainees Collection:</h1>
Insert a document with the fields Name, Location, and Facilitator:
```

db.Trainees.insertOne({
  Name: "Jane Smith",
  Location: "Johannesburg",
  Facilitator: "John Doe"
})
```

<h1>c. Projects Collection:</h1>
Insert a document with the fields Name, Course, and Lesson:
```

db.Projects.insertOne({
  Name: "Node.js Basics",
  Course: "Backend Development",
  Lesson: "Introduction to Node.js"
})
```
<h1>3. Verify Inserted Documents</h1>
To confirm the documents were inserted, use the find() command:

a. Facilitators:
```
db.Facilitators.find().pretty()
```
b. Trainees:
```
db.Trainees.find().pretty()
```
c. Projects:
```
db.Projects.find().pretty()
```
<h1>4. Export the Database</h1>

To export the database, use the mongodump command. Ensure MongoDB tools are installed and added to your system's PATH.

Open a terminal or command prompt.
Run the following command:
```
mongodump --db=Codetribe --out=./Codetribe_Dump
```
This creates a folder named Codetribe_Dump containing the exported data.

Additional Notes

Ensure the MongoDB server is running before starting the shell or using export commands.

If mongodump is not recognized, ensure MongoDB Database Tools are installed and added to the PATH.


<h1>Usage</h1>
<h2>Connecting to MongoDB</h2>
<p>Your application should now be connected to MongoDB. Ensure that your MongoDB server is running locally or on a remote server. You can check the connection status by looking at the terminal logs.</p>

<h2>Interact with MongoDB</h2>
<p>The MongoDB database can be interacted with directly using a MongoDB client (e.g., MongoDB Compass) or through the application if it provides a UI.</p>



## Tech Stack
**Client:** JavaScript, MongoDB
