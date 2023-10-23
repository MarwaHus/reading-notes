# class 29

#### What database engine is Room wrapped around? Do you think this is a good choice? Why or why not?<br>
Room is wrapped around SQLite - a lightweight and efficient database engine. SQLite is a popular choice for embedded and mobile applications, as it requires minimal setup and resource usage while still providing a full-featured SQL database engine.

I think SQLite is a good choice for Room to be wrapped around, considering the primary use case of Room is for local, on-device data storage. SQLite has been widely used in this context and has proven to be reliable and performant.

#### Do Rooms have any similarities to JPA?<br>
Yes, Rooms have similarities to JPA (Java Persistence API), specifically to its Java Persistence Query Language (JPQL).
Both Room and JPA are object-relational mapping (ORM) frameworks that provide a layer of abstraction between the application and the database. They allow developers to interact with the database using Java objects and abstract away the underlying SQL queries.
Similar to JPQL, Room has its own query language called SQLite Query Language (SQL), which is a subset of SQL. Both allow developers to execute queries against a database, and Room's SQL syntax is designed to be similar to JPQL.

#### Describe a DAO in your own words.<br>
DAO stands for "Data Access Object". It is an object that encapsulates the database queries used to access and manipulate data. DAOs serve as an abstraction layer between the database and the application, allowing developers to perform database operations using an object-oriented API that’s easier to work with and maintain.
DAOs are typically used in conjunction with an ORM (Object-Relational Mapping) framework. The ORM maps database tables to Java objects and uses DAOs to interact with those objects. DAOs can be thought of as a collection of methods that are responsible for performing CRUD (Create, Read, Update, Delete) operations on database tables.
One of the main benefits of using a DAO is that it helps to separate concerns in an application. The database operations are abstracted away from the main application logic, which makes it easier to change the underlying data model without affecting the rest of the application.
