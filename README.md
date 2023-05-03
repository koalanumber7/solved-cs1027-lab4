Download Link: https://assignmentchef.com/product/solved-cs1027-lab4
<br>
<ul>

 <li>Develop a generic class so that it works with any type</li>

 <li>Examine the structure of singly- and doubly- linked lists and their respective nodes</li>

 <li>Modify existing loops to work more robustly and efficiently with linked lists</li>

 <li>Identify the various cases in removing a node from a list</li>

 <li>Program a removal method that handles each of the identified cases</li>

</ul>

<h1>Pre-Lab</h1>

<ul>

 <li>Create a new Java project called Lab4</li>

 <li>Download the files: <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab04/Person.java">java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab04/Person.java">,</a> <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab04/TestReverse.java">TestReverse.java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab04/TestReverse.java">,</a> <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab04/LinearNode.java">LinearNode.java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab04/LinearNode.java">,</a> <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab04/BuildLinkedList.java">BuildLinkedList.java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab04/BuildLinkedList.java">,</a> <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab04/DoubleLinkedNode.java">DoubleLinkedNode.java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab04/DoubleLinkedNode.java">,</a> and <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab04/BuildDLL.java">BuildDLL.java</a>  Save these downloaded files into the Lab4 src folder</li>

</ul>

<h1>Exercise 1 – Creating a class with generics</h1>

<ol>

 <li>Create a new class called ReversibleArray.</li>

 <li>In the class header, add the code &lt;T&gt; immediately to the right of the class name.</li>

 <li>Give this class two private instance variables: T[] array and int count</li>

 <li>Create a constructor which takes in one parameter of type T[] and assign that parameter’s value into array. Set count as the length of the array.</li>

 <li>Add a toString() method that outputs the array values in the format: elem0, elem1, elem2, etc. (hint: add the comma and space only if you are not on the final iteration of the loop).</li>

 <li>Create the most important function in this class: public void reverse () { }

  <ol>

   <li>This method must swap elements within the array, without making a new array or other collection.</li>

   <li>The swaps should be made symmetrically about the middle of the array. This means array[0] swaps with array[n-1], array[1] swaps with array[n-2], etc.</li>

   <li>Use a temp variable to help with these swaps. What variable type should this temp variable be?</li>

   <li>How many swaps must be made to correctly reverse the array?</li>

  </ol></li>

 <li>Open TestReverse.java and read over the code in its main()</li>

 <li>Run TestReverse to see the output. If your output is incorrect, then debug the program until it works properly. It should print out the following text:</li>

</ol>

atom, breeze, clock, daydream, energy energy, daydream, clock, breeze, atom

11, 22, 33, 44, 55, 66, 77 77, 66, 55, 44, 33, 22, 11

Jerry Seinfeld, Salma Hayek, Reese Witherspoon, Vince Vaughn

Vince Vaughn, Reese Witherspoon, Salma Hayek, Jerry Seinfeld




<h1>Exercise 2 – Singly Linked Lists</h1>




<ol>

 <li>Open LinearNode.java and BuildLinkedList.java in Eclipse and examine the code in both classes.</li>

 <li>The main() method in BuildLinkedList created a list with 10 nodes, each storing an integer value from 1 to 10. The printList() method prints out this list. Run the program to see the list elements printed out.</li>

 <li>The problem is that printList() is “hard-coded” to loop through 10 elements in the for-loop so this method will not work for any other size of list. Modify this method so that it works for any list length (i.e. not hard-coded). You <strong>cannot</strong> change the method signature (parameters). You also <strong>cannot</strong> add instance variables to the class.</li>

 <li>In the main() method, change the for-loop to create a list of 20 nodes and run the program to ensure that it correctly creates and prints out those 20 nodes.</li>

 <li>Change it again, this time to 7 and check that it works properly with the 7 nodes.</li>

</ol>




<h1>Exercise 3 – Doubly Linked Lists</h1>




<ol>

 <li>Open DoubleLinkedNode.java and BuildDLL.java in Eclipse and examine the code in both classes.</li>

 <li>The DoubleLinkedNode class is complete and does not have to be modified.</li>

 <li>The BuildDLL class has some provided methods for creating a doubly linked list with a sequence of letters (note that we are using the Character class for this, which is a wrapper for the primitive char type) and printing out the list from front to rear. Run the program to see the default output.</li>

 <li>Notice that the original list is printing correctly, but the remove() method is not provided so subsequent list outputs are incorrect.</li>

 <li>You must fill in the code for removing an element from the linked list using the following rules and hints:

  <ul>

   <li>Loop through the list until you find the correct node (how can you tell if the node is the one for which we are searching?)</li>

   <li>We will assume that the input parameter ‘elem’ will always be a valid element that is contained in the list. Normally we would have to account for elements that are not found in the list, but you may ignore this possibility for this lab.</li>

   <li>What are the 3 possible cases of the node’s location in the list? How must each of these cases be handled?</li>

   <li>Make the appropriate connections with the previous and/or next node based on its position in the list. (Hint: remember front’s previous is null and rear’s next is null).</li>

  </ul></li>

 <li>Run the program and check that the output is correct. The list after each step should be:</li>

</ol>

<table width="272">

 <tbody>

  <tr>

   <td width="144">K T E N P A L</td>

   <td width="128">(original)</td>

  </tr>

  <tr>

   <td width="144">K T E P A L</td>

   <td width="128">(after removing ‘N’)</td>

  </tr>

  <tr>

   <td width="144">T E P A L</td>

   <td width="128">(after removing ‘K’)</td>

  </tr>

  <tr>

   <td width="144">T E P A</td>

   <td width="128">(after removing ‘L’)</td>

  </tr>

 </tbody>

</table>