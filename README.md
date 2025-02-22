# Codetribe Database with MongoDB

Welcome to the **Codetribe Database** project! 🎉 This guide will help you set up and manage a MongoDB database using the MongoDB shell (`mongosh`). Our database consists of three collections: **Facilitators**, **Trainees**, and **Projects**, each filled with useful data.

---

## 🌟 Features

- **Database Name**: Codetribe
- **Collections**:
  - **Facilitators**: Details about facilitators.
  - **Trainees**: Information on trainees.
  - **Projects**: Project-related details.
- **What You'll Learn**:
  - How to create a database
  - How to create collections
  - How to insert and manage data

---

## 🔧 Installation & Setup

### Prerequisites
1. Install MongoDB on your system. [Download Here](https://www.mongodb.com/try/download/community).
2. Ensure `mongosh` is installed and accessible from your terminal.
3. Start the MongoDB server:
   ```bash
   mongod
   ```

### Starting the MongoDB Shell
1. Open your terminal and type:
   ```bash
   mongosh
   ```
2. Verify that MongoDB is running by listing available databases:
   ```bash
   show dbs
   ```

---

## 📌 Step-by-Step Guide

### 1️⃣ Create the Database
To create or switch to the **Codetribe** database:
```bash
use Codetribe
```
MongoDB will create it automatically once data is inserted.

### 2️⃣ Create Collections & Insert Data

#### 📁 Facilitators Collection
1. Insert a facilitator into the database:
   ```bash
   db.Facilitators.insertOne({
       Name: "John Doe",
       Location: "Johannesburg",
       Course: "Web Development"
   })
   ```
2. Verify the entry:
   ```bash
   db.Facilitators.find().pretty()
   ```

#### 📁 Trainees Collection
1. Add a trainee:
   ```bash
   db.Trainees.insertOne({
       Name: "Jane Smith",
       Location: "Cape Town",
       Facilitator: "John Doe"
   })
   ```
2. Check if the trainee was added:
   ```bash
   db.Trainees.find().pretty()
   ```

#### 📁 Projects Collection
1. Insert a project:
   ```bash
   db.Projects.insertOne({
       Name: "E-commerce Website",
       Course: "Web Development",
       Lesson: "Building RESTful APIs"
   })
   ```
2. Verify the data:
   ```bash
   db.Projects.find().pretty()
   ```

---

## 🔥 Handy MongoDB Commands

💡 Keep these commands handy for quick database management:

- **Show all databases**:
  ```bash
  show dbs
  ```
- **Switch to a specific database**:
  ```bash
  use <database_name>
  ```
- **List all collections in a database**:
  ```bash
  show collections
  ```
- **Insert a document into a collection**:
  ```bash
  db.<collection_name>.insertOne({ key: value })
  ```
- **View all documents in a collection**:
  ```bash
  db.<collection_name>.find().pretty()
  ```
- **Delete a database**:
  ```bash
  use <database_name>
  db.dropDatabase()
  ```

---

## ✅ Verifying Your Setup

To confirm everything is working:
1. **Check if the database exists**:
   ```bash
   show dbs
   ```
2. **Switch to the Codetribe database**:
   ```bash
   use Codetribe
   ```
3. **List all collections**:
   ```bash
   show collections
   ```
4. **View stored data**:
   - Facilitators:
     ```bash
     db.Facilitators.find().pretty()
     ```
   - Trainees:
     ```bash
     db.Trainees.find().pretty()
     ```
   - Projects:
     ```bash
     db.Projects.find().pretty()
     ```

---

## 🖼️ Database Overview

![Mongod](https://github.com/user-attachments/assets/61aabe80-cb05-435c-9aee-5ef643b3128d)
![Mongod2](https://github.com/user-attachments/assets/8fcc6cdb-d145-480b-83e0-df7bb31eb5a0)


🎯 **You're all set!** You've successfully created a database, added collections, and inserted data. Happy coding! 🚀

