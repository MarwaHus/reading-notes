# class 02

### Primitives vs. Objects

1. Explain the difference between an “int” and an “Integer” in Java.

   The difference between "int" and "Integer" in Java is that "int" is a primitive data type that stores numerical values, while "Integer" is a class that wraps the "int" primitive type into an object and provides additional utility methods. "int" has a default value of 0, while "Integer" has a default value of null. The primitive data type "int" is used for simple numerical operations, while "Integer" is used when an object is needed, such as when working with collections or third-party libraries that require objects instead of primitives.

 2. What is the default value for ints? Integers?
   
     In Java, the default value of an "int" primitive is 0, and the default value of an "Integer" object is "null".

   3. What is autoboxing? Unboxing?
    Autoboxing converts primitive data types to their corresponding wrapper classes, while unboxing converts wrapper classes to their corresponding primitive data types. These features in Java make it easier to switch between primitive types and wrapper types without having to write explicit conversion code. Autoboxing and unboxing are widely used in Java collections and arraylists, allowing the code to be simpler and more concise
------------------------------
### Exceptions in Java

1. List the three basic categories of exceptions.
   -  Checked Exceptions.
   -  Unchecked Exceptions.
   -  Errors.
  
2. What type of statement can you use to handle an exception?
   In Java, you can handle an exception using a try-catch block. 
   Here's an example of a try-catch block:
try {
   //code that might throw an exception
} catch (Exception e) {
    // Code to handle the exception
}.

----------------------------------

### Using Scanner to read in a file in Java.
1. Describe a situation where you think it would be useful to have a program that scans text.
Describe a situation where you think it would be useful to have a program that scans text. in two lines
Delete
A program that scans text could be helpful in monitoring customer feedback in real-time. It can analyze customer reviews, comments, and social media posts, identify common themes and topics, and provide insights to improve products and services.
2. What is input from a Scanner broken down into?
Input from a Scanner is broken down into tokens, where each token represents a sequence of characters that ends with a delimiter (e.g., whitespace or a specific character).