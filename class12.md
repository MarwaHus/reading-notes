# Class 12

### Spring guide: Accessing Data with JPA

1. How are query methods defined when using Spring Data JPA?<br>
   Query methods are defined in an interface that extends a Spring Data repository interface. The method names follow the convention "findBy" followed by the entity property name and optional comparison operators. The query methods can be further customized using additional keywords, such as "Distinct", "IgnoreCase", and "OrderBy". Spring Data JPA generates the necessary query at runtime based on the method signature.
2. Which dependencies will you need in order to complete the Spring guide?<br>
   To complete the Spring guide, you will need the following dependencies:

   - Spring Boot
   - Spring Data JPA
   - H2 Database (embedded database for testing and development)

3. What annotations are used to specify an auto generated identification number for an Entity?<br>
   To specify an auto generated identification number for an Entity, we can use the `@GeneratedValue` and `@Id` annotations in Java Persistence API (JPA):

- `@Id`: Specifies the primary key of an entity. It can be applied on a field or a property. It should be used in conjunction with either the `@GeneratedValue` annotation or manually assigning a value to it in code.

- `@GeneratedValue`: Specifies the strategy for the generation of primary keys. It can be applied on a field or a property. The `strategy` attribute defines the type of generation strategy to be used, such as `GenerationType.AUTO`, `GenerationType.IDENTITY`, `GenerationType.SEQUENCE`, or `GenerationType.TABLE`. 

For example, the following code adds an auto generated identification number for an Entity using JPA annotations:

```java
@Entity
public class Person {

   @Id
   @GeneratedValue(strategy = GenerationType.IDENTITY)
   private Long id;
   private String name;
   private int age;

   // getters and setters
}
```
### Baeldung: Comparing repositories
 1. Which of the Spring Data Repositories covered in the readings has the most methods available to it?<br>
   The `CrudRepository` covered in the readings has the most methods available to it. It provides generic CRUD (Create, Read, Update, Delete) operations for any entity, as well as additional methods for querying entities based on specific criteria. Here are some of the methods available in `CrudRepository`:

     - `save()`: saves an entity to the database
     - `findById()`: finds an entity by its primary key
     - `findAll()`: returns all entities in the database
     - `count()`: returns the number of entities in the database
     - `delete()`: deletes an entity from the database
     - `deleteAll()`: deletes all entities from the database

     Other Spring Data repositories, such as `PagingAndSortingRepository` and `JpaRepository`, extend `CrudRepository` and therefore also have the same methods available. However, they provide additional methods for pagination, sorting, and working with JPA-specific features, such as caching and auditing.
2. Name a downstide of a Spring Data Repository.<br>One downside of a Spring Data Repository is that it may not be suitable for complex queries or data access scenarios that require more fine-grained control than what the generic methods provided by a repository can offer. In such cases, it may be necessary to write custom SQL queries or use a more advanced approach, such as using the `JdbcTemplate` or implementing a DAO (Data Access Object) layer.
   
3. How would you define an operation to find a student based on their name in a repo named StudentRepository which extends JpaRepository?<br>
  To define an operation to find a student based on their name in a repo named `StudentRepository` which extends `JpaRepository`, we can add a new method with the following signature in the repository interface:

```java
public interface StudentRepository extends JpaRepository<Student, Long> {

    Student findByName(String name);

}
```

This method uses the naming convention of Spring Data JPA to generate a query method based on the name of the method. In this case, the `findByName` method will find a `Student` entity based on their `name` property.

The return type of the method is `Student`, which represents the result of the query. The parameter of the method is `name`, which is the value we want to search for.

We can then use this method in our code to find a student based on their name, like this:

```java
Student student = studentRepository.findByName("John Doe");
```