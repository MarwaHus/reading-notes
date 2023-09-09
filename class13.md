# Class 13

### Related data in Spring (One-to-Many Relationship)
1. Name a few real life examples of “One To Many” relatioships.<br>
   Real-life examples of a "One to Many" relationship include:
   * One teacher can have many students in a classroom.
   * One company can have many employees in various departments.
   * One author can have written many books.
2. Given two entities, one named Player and one named Team, if you wanted to create a one to many relationship with those entities which would be the one and which would be the many?<br>
   In a relationship between Player and Team, Team would be the "one" and Player would be the "many". This is because one team can have many players on its roster.

3. Explain one to many relationships to a non-technical friend.<br>A one to many relationship is a type of relationship where one entity can be associated with multiple instances of another entity. For example, one school can have many students enrolled in it. In this relationship, the entity that can have multiple instances (e.g. students) is considered the "many" side, while the entity that can have only one instance (e.g. school) is considered the "one" side. The relationship between the entities is established by adding a foreign key in the "many" entity table that points to the primary key of the "one" entity table. This allows us to easily retrieve all the associated instances of the "many" entity for a given instance of the "one" entity.

### Baeldung: Spring Integration Testing.
1. Describe the difference between a unit test and an integration test.<br>
   A unit test is a test that focuses on testing a single unit of code, such as a method or function, in isolation. It typically involves mocking dependencies and doesn't involve testing the integration with other components or systems. On the other hand, an integration test is a test that verifies the interaction between different components or systems in a larger system. It typically involves testing the end-to-end behavior of the system and can involve multiple layers of the application.
2. What is the object that provides support for Sprin MVC Testing?<br>
   `MockMvc` provides support for Spring MVC testing. It encapsulates all web application beans and makes them available for testing.

        Let’s see how to use it:

        private MockMvc mockMvc;
        @BeforeEach
        public void setup() throws Exception {
            this.mockMvc = MockMvcBuilders.webAppContextSetup(this.webApplicationContext).build();
        }
3. What does the “perform()” method do in a Spring integration test?<br>The `perform()` method in a Spring integration test is used to perform an HTTP request to a particular endpoint and obtain a result object, which can then be transformed and analyzed using various methods provided by the MockMvcResultMatchers class. It's typically used to test the behavior of controllers and their interactions with the rest of the application.