## BLOCK-readText

#### Timeline for the entire topic - 3 hours.

In this topic, you have to build a small web API from scratch for the following user stories.

_Note - This is not fullstack application, you only have to build the API using Node.js, Express.js and MongoDB. Please follow standard web practices._

```
1. There are two kinds of users in our system
  - students
  - mentors
2. A student should be able to signup using following information.
  - Name, Email Id, Password, Batch Number.
3. A student should be able to login using his/her email id and password.
4. Atleast 3 mentors should be automatically seeded into the database and so they don't have to signup. Mentor data should be seeded with the following information.
  - Name, Email Id, Password.
5. A mentor should be able to login using email and password.
6. The identification route for both the types of users has to be the same.
7. A mentor should be able to add a task in a resource called `Todo` with following info.
  - Name of todo, Whether its completed or not.
8. A mentor should be able to see all the tasks.
9. A student should be able to see all the tasks but should not be able to add a new task.
```

## BLOCK-writeTextAnswer

Here write the psuedo code you would follow to build the above API.

1. Models

- students
- mentors
- todo

2. Schema for students will include
   Name - String
   Email Id - String
   Password - String
   BatchNumber - Number

3. Request body for students Login route
   `{ email: "puneet@gmail.com", password: "puneet" }`

4. Schema for mentors
   Name - String
   Email Id - String
   Password - String

   - Have to seed 3 mentors into database

5. Request body for mentors Login route
   `{ email: "puneet@gmail.com", password: "puneet" }`

6. keep identification route same for both mentors and students.

7. Schema for todo
   Name of todo - String
   Completed - Boolean (default: false)

8. A mentor can see and add task in todo.

9. A student can see task but can't add.
