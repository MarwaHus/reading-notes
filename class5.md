# class 05

 ### Linked Lists

 ### What is Linked List
   A linked list is a linear data structure, in which the elements are not stored at contiguous memory locations. The elements in a linked list are linked using pointers as shown in the below image:
  >![](R.png)
You have to start somewhere, so we give the address of the first node a special name called HEAD. Also, the last node in the linked list can be identified because its next portion points to NULL.
<br>

  Representation of Linked List
  Let's see how each node of the  linked list is represented. Each node consists: <br>
- A data item<br>
- An address of another node<br>
We wrap both the data item and the next node reference in a struct as:

<pre>struct node
{
  int data;
  struct node *next;
};</pre>
Understanding the structure of a linked list node is the key to having a grasp on it.<br>

### Linked List Implementations in java
>
<pre>
// Linked list implementation in Java

class LinkedList {
  // Creating a node
  Node head;

  static class Node {
    int value;
    Node next;

    Node(int d) {
      value = d;
      next = null;
    }
  }

  public static void main(String[] args) {
    LinkedList linkedList = new LinkedList();

    // Assign value values
    linkedList.head = new Node(1);
    Node second = new Node(2);
    Node third = new Node(3);

    // Connect nodess
    linkedList.head.next = second;
    second.next = third;

    // printing node-value
    while (linkedList.head != null) {
      System.out.print(linkedList.head.value + " ");
      linkedList.head = linkedList.head.next;
    }
  }
}</pre>
  ### What are the types of linked list:
  1. Singly Linked List:<br>
   A singly linked list is a linear data structure in which the elements are not stored in contiguous memory locations and each element is connected only to its next element using a pointer.
   >![](sl.png)


 2. Doubly Linked List:<br>
     A doubly linked list (DLL) is a special type of linked list in which each node contains a pointer to the previous node as well as the next node of the linked list.
     <br>
     >![](DLL1.png)<br>
     
3. Circular Linked List
   A circular linked list is a variation of a linked list in which the last element is linked to the first element. This forms a circular loop.
  > ![](circular-linked-list.webp)

### Linked List Complexity
Time Complexity

|    |Worst case|	Average Case|
|--------------|-----------|----------|
Search	|O(n)| O(n)|
|Insert|	O(1)|	O(1)
|Deletion|	O(1)|	O(1)

### Recommended Readings
1. Tutorials
* [Linked List Operations (Traverse, Insert, Delete)](https://www.programiz.com/dsa/linked-list-operations)
* [Types of Linked List](https://www.programiz.com/dsa/linked-list-types)
* [Java LinkedList](https://www.programiz.com/java-programming/linkedlist)
2. Examples
* [Get the middle element of Linked List in a single iteration](https://www.programiz.com/java-programming/examples/get-middle-element-of-linkedlist)
* [Convert the Linked List into an Array and vice versa](https://www.programiz.com/java-programming/examples/linkedlist-array-conversion)
* [Detect loop in a Linked List](https://www.programiz.com/java-programming/examples/detect-loop-in-linkedlist)

###quiz 
* [quiz](https://www.geeksforgeeks.org/data-structure-gq/top-mcqs-on-linked-list-data-structure-with-answers/)
* [fill-in-the-blank ](https://quizlet.com/204481717/ch-17-linked-lists-fill-in-the-blank-flash-cards/)