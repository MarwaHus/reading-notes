# Class 01

### Java Basics

1. What does “strong typed” mean?
   "Strong typed" means that a programming language enforces strict rules about the type of data that can be used in a program. This means that variables and expressions must have a specific data type, and that data types cannot be mixed in an operation or assignment.
2. What are the primitive data types?
   The primitive data types in programming include:

   - Integer (int): used for whole numbers without a decimal point
   - Floating point (float): used for decimal numbers
   - Boolean (bool): used for true/false values
   - Character (char): used for individual characters or symbols
   - String (string): used for a sequence of characters or symbols.

---------------------

### XKCD: Compiling

1. Explain to a non-technical friend the difference in how compilation works in Java and JavaScript.
   When explaining the difference in compilation between Java and JavaScript to a non-technical friend:

Java:
In Java, the code is first written in a human-readable form called source code. This source code is then compiled into a bytecode format, which is a low-level representation of the code. The bytecode is later executed by a Java Virtual Machine (JVM) that runs on the user's computer. So, the compilation process in Java happens before the code is actually executed on the user's machine.

JavaScript:
Contrary to Java, JavaScript is an interpreted language. This means that the code is executed directly without a separate compilation step. The JavaScript code you write is directly interpreted by the browser or the JavaScript engine without the need for any explicit compilation. As a result, the code is executed on-the-fly as it is encountered by the browser.

2. Does code complining mean that it works correctly?
   Compilation is an important part of producing working code, but it doesn't guarantee correctness by itself. Compiling code transforms it into a lower-level representation that can be understood and executed by the computer. However, errors or mistakes in the code logic can still occur, even after successful compilation. So, while correct compilation is a crucial step, it is not a guarantee that the code will work flawlessly. Additional factors like proper coding practices, logical correctness, and comprehensive testing are also necessary to ensure that the code works correctly.
----------------------
### Reading Java Documentation

1. How many keywords does Java have?
   Java has 52 keywords.
2. How do you print words to the console in Java?
   To print words to the console in Java, you need to use the System.out.println() method. Here's an example:

public class HelloWorld {
   public static void main(String[] args) {
      System.out.println("Hello, World!");
   }
}