# Stacks and Queues

### What are stacks and queues?

* Stacks are a type of data structure that follow a particular order, called LIFO (last in, first out), meaning that the last item added to it is the first one to be removed.
* Queues, on the other hand, follow a different order called FIFO (first in, first out), meaning that the first item added to it is the first one to be removed.
* Both data structures can be represented as abstract classes and can be implemented using different programming languages and algorithms.
* Stacks and queues can hold many different types of data, from simple integers to complex objects.
  
### Why use stacks and queues?

* Stacks and queues are often used in programming as abstract data types to store collections of elements that follow a particular order.
* They provide a way to manage data efficiently and effectively, especially in situations where the order of element access is important.
* Stacks and queues offer a simple and elegant solution to many programming problems and can be used in a variety of contexts.

### How to use stacks and queues?

* To use a stack, push data onto the top of the stack using the <b>push()</b> method, and remove data from the top of the stack using the <b>pop()</b> method.
  
* To use a queue, add data to the end of the queue using the <b>enqueue()</b> method, and remove data from the front of the queue using the <b>dequeue()</b> method.
* Care should be taken when using stacks and queues to avoid overflow and underflow errors, as well as ensuring proper management of memory allocation.
  
-------------------
### Stack Implementation

   In stack, elements are stored and accessed in <b>Last In First Out</b> manner. That is, elements are added to the top of the stack and removed from the top of the stack.
### Queue Implementation

   In queues, elements are stored and accessed in <b>First In First Out</b> manner. That is, elements are added from the behind and removed from the front.

   ![](./assets/stackandqueue.webp)

-----------------------------
### Stack Methods
* push() Method
  <pre> import java.util.Stack;
    class Main {
    public static void main(String[]args) {
        Stack &lt;String&gt;  animals= new Stack<>();
        // Add elements to Stack
        animals.push("Dog");
        animals.push("Horse");
        animals.push("Cat");
        System.out.println("Stack: " + animals);
    } }</pre>
 * pop() Method 
   <pre> import java.util.Stack;
    class Main {
    public static void main(String[] args) {
        Stack &lt;String&gt;  animals= new Stack<>();
        // Add elements to Stack
        animals.push("Dog");
        animals.push("Horse");
        animals.push("Cat");
        System.out.println("Initial Stack: " + animals);
        // Remove element stacks
        String element = animals.pop();
        System.out.println("Removed Element: " + element);
    } }</pre>

    ---------------------------------
### Queue Methods
* Enqueue() Method
   <pre>
    import java.util.Queue;
    import java.util.LinkedList;
    class Main {
    public static void main(String[] args) {
    // create a queue
    Queue &lt;String&gt; fruits = new LinkedList<>();
    // adds "Apple" and "Orange" to the queue
    fruits.add("Apple");
    fruits.add("Orange");
    // print elements of the queue
    for (String item : fruits) {
    System.out.println(item);
    }}}
</pre>

* Dequeue() Method
  <pre>
    import java.util.Queue;
    import java.util.LinkedList; 
    class Main {
    public static void main(String[] args) {
    // create a queue
    Queue<String> colors = new LinkedList<>();
    // adds "Red" and "Blue" to the queue
    colors.add("Red");
    colors.add("Blue");
    // removes element from the beginning of the colors queue
    String removedElement = colors.remove();
    System.out.println("Removed Element: " + removedElement);
  }}
  </pre>

  -------------------------------------
###Quiz
* [quiz](https://quizlet.com/539019766/stacks-queues-and-deques-practice-quiz-flash-cards/)
* [fill-in-the-blank](https://www.pathwalla.com/2020/10/data-structures-stack-and-queues-fill.html)

