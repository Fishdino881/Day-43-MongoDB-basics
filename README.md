# Day-43-MongoDB-basics

Overview

MongoDB is a NoSQL, document-oriented databas designed for scalability, flexibility, and high performance.
Unlike relational databases (SQL), MongoDB stores data in JSON-like documents, making it ideal for modern applications and large-scale systems.

This day focuses on building a strong foundation in MongoDB fundamentals.



What is MongoDB?

 NoSQL database (non-relational)
 Stores data as **documents** inside **collections**
 Schema-less and flexible
 Designed for horizontal scaling
 Uses BSON (Binary JSON) format

---

SQL vs MongoDB

| SQL          | MongoDB                         |
| ------------ | ------------------------------- |
| Tables       | Collections                     |
| Rows         | Documents                       |
| Columns      | Fields                          |
| Fixed schema | Flexible schema                 |
| JOINs        | Embedded documents / references |

---

Core Concepts

Database

A container that holds multiple collections.

```js
use myDatabase
```

---

Collection

A group of documents (similar to a table in SQL).

```js
db.createCollection("users")
```

---

Document

A single record stored as key-value pairs.

```js
{
  "name": "Kunal",
  "age": 20,
  "role": "Data Science Student"
}
```

---

## 🔄 CRUD Operations

Create (Insert)

```js
db.users.insertOne({ name: "Alice", age: 22 })
db.users.insertMany([
  { name: "Bob", age: 25 },
  { name: "Charlie", age: 30 }
])
```

---

Read (Find)

```js
db.users.find()
db.users.find({ age: 25 })
db.users.findOne({ name: "Alice" })
```

---

Update

```js
db.users.updateOne(
  { name: "Alice" },
  { $set: { age: 23 } }
)
```

---

Delete

```js
db.users.deleteOne({ name: "Bob" })
db.users.deleteMany({ age: { $gt: 30 } })
```

---

Query Operators

* `$eq` – equals
* `$gt` – greater than
* `$lt` – less than
* `$gte` – greater than or equal
* `$lte` – less than or equal

```js
db.users.find({ age: { $gt: 21 } })
```


Tools Used

 MongoDB
 MongoDB Shell
 MongoDB Compass


Key Learnings

 Understood NoSQL and document-based databases
 Learned how MongoDB stores and retrieves data
 Practiced essential CRUD operations
 Compared MongoDB with relational databases
 Built a strong base for aggregations and indexing


Use Cases

 Backend development
 Real-time applications
 Data engineering pipelines
 Scalable systems
 AI & ML data storage
