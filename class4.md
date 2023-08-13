# class 04

### Java OO Tutorial (only the Object and Class ones)

1. Explain the difference between an object and a class.<br>
   An object is an instance of a class. In other words, a class is a blueprint or template for creating objects that share similar characteristics and behaviors. Objects are created from classes and can be thought of as individual entities with their own state and behavior.

   For example, a class called "Car" might have properties such as "make," "model," and "color," as well as methods such as "drive," "stop," and "accelerate." An object created from this class might be a specific car with a make of "Honda," a model of "Civic," and a color of "blue." The object would have its own behavior based on the methods defined in the class, such as the ability to drive and stop.

   In summary, a class is a blueprint or template used to create objects, while an object is an instance of a class that has its own state and behavior.
<br>
2. Name two types of state that a Student object might have.<br>
   -  Name
   -  GPA
   -  ID
  <br>
3. Name two types of behaviours that a student object might have.<br>
   - Attend Class: The `Student` object might have the behavior of attending a class. This behavior might be represented by a method called `attendClass()` that updates the attendance record for the student.
   - Study: The `Student` object might have the behavior of studying for a test or exam. This behavior might be represented by a method called `study()` that updates the knowledge of the student.

------------------------------------------
### Java Classes 
1. Explain the significance of a constructor for a class.<br>
   A constructor is a special method that is called when an object is created from a class. The purpose of a constructor is to initialize the state of the object. In other words, a constructor is used to set the initial values of the properties of an object so that it is ready for use.

   The significance of a constructor for a class is that it ensures that every object created from that class has a consistent and valid state. The constructor can take in arguments to customize the creation of each object, such as setting the initial value of a property to a specific value passed as a parameter. By providing a constructor, it can help ensure that a programmer does not accidentally create an object with invalid or missing data.

   In summary, a constructor is important because it is responsible for initializing an object's state with valid, consistent data necessary for the object to function appropriately.
   <br>
2. Write the declaration statement for a class named “Student” (do not fill it with fields and methods).
   
   <pre> public class Student {
    // Declaring instance variables
    private String name;
    private int age;
    private float gpa;
    
    // Constructor
    public Student(String name, int age, float gpa) {
        this.name = name;
        this.age = age;
        this.gpa = gpa;
    }
    // declaring methods
    }</pre>

---------------------------
### Binary, Decimal and Hexadecimal Numbers

1. What is the value of the binary number 1101?<br>
 <pre>1x2^3 + 1x2^2 + 0x2^1 + 1x2^0 = 8 + 4 + 0 + 1 = 13</pre>
3. Write the number 52 in binary. Write it in hexidecimal.<br> 
 <pre>52 / 2 = 26  remainder 0
 26 / 2 = 13  remainder 0
 13 / 2 = 6   remainder 1
  6 / 2 = 3   remainder 0
  3 / 2 = 1   remainder 1
  1 / 2 = 0   remainder 1
  52 in binary is 110100.</pre>