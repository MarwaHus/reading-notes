# Class 6

### Java OO Tutorial (review Object and Class, read the rest)

1. What is the difference between an Object and a Class in Java?<br>
   
    An object is an instance of a class. In other words, a class is a blueprint or template for creating objects that share similar characteristics and behaviors. Objects are created from classes and can be thought of as individual entities with their own state and behavior.

   For example, a class called "Car" might have properties such as "make," "model," and "color," as well as methods such as "drive," "stop," and "accelerate." An object created from this class might be a specific car with a make of "Honda," a model of "Civic," and a color of "blue." The object would have its own behavior based on the methods defined in the class, such as the ability to drive and stop.

   In summary, a class is a blueprint or template used to create objects, while an object is an instance of a class that has its own state and behavior.<br>

2. Explain to a non-technical friend the concept of inheritance in Java.<br>
   Inheritance in Java is like having a family tree where one person inherits certain traits or characteristics from their parents. In Java, classes can also have relationships and inherit properties and behaviors from a parent class. This allows for code to be organized and re-used so that a sub-class (child) inherits all the methods and variables from the super-class (parent) and can add their own unique methods and variables. This approach saves time and effort because new sub-classes can be created quickly by inheriting the properties of a parent class.
----------------------------------------------
### Java Static Keyword

 1. Static methods are also called what? Why?<br>
   Static methods are also called class methods because they belong to the class rather than to an instance of the class. The main reason for this is that static methods do not require any object of the class to be created to run, unlike non-static methods, which need the object to be instantiated first. Static methods can be accessed by using the class name followed by the dot operator and then the method name. This makes it easy to use them for common utility functions that do not require any specific object state, or for operations that apply to all objects of a class. Because they belong to the class and not to a specific instance of the class, static methods are useful for managing global functionalities.<br>
   
 2. How can you access a variable of a class without instantiating an object from that class?  <br>
   You can access a variable of a class without instantiating an object from that class by using the "static" keyword in the variable declaration. This creates a static variable, which belongs to the class rather than to any object instance of the class, meaning that it can be accessed without an object instance being created. To access the static variable, you can use the class name followed by the dot operator and then the variable name.

-----------------------------------------------------
### Java Singleton Class

1. What is a Design Pattern? Describe one or two with analogies from your previous work experience.<br>
   A design pattern is a general reusable solution to a commonly occurring problem within a given context in software design. Essentially, a design pattern provides a proven and tested template that can be used to solve a particular type of problem or to achieve a specific outcome in software development.One example of a design pattern is the Singleton pattern, where a class has only one instance and provides a global point of access to that instance. 
   
2. What is a Singleton?<br>
   Singleton pattern is a design pattern which restricts a class to instantiate its multiple objects. It is nothing but a way of defining a class. Class is defined in such a way that only one instance of the class is created in the complete execution of a program or project. It is used where only a single instance of a class is required to control the action throughout the execution. A singleton class shouldn’t have multiple instances in any case and at any cost. Singleton classes are used for logging, driver objects, caching and thread pool, database connections.

  ### Things I want to know more about 

  - Software Design Patterns