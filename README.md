Download Link: https://assignmentchef.com/product/solved-jac444-assignment-7-paradigm-of-programming-added-to-java
<br>
This assignment lets you practice functional programming as the new paradigm of programming added to Java 8. It includes concepts such as Generics, Functional Interfaces, Lambda Expressions, Method References, Streams, and Collections.

Functional Programming allows you to write programs more concise, and in many cases (like working with collections), faster and with fewer bugs. Mostly, in Functional Programming, you specify what you want to do (not how you want it to be done, as it’s the case in non-functional programming paradigms.) Therefore, in this assignment, you should do all the tasks without using the traditional control statements (for, while, do/while, if/else, switch/case and even recursion) and just by using Functional Programming facilities provided in Java 8.

(<em>the only exception is inside the equals, constructor, and setter methods of class Student </em>

<em>(discussed below); which you could use the </em><em>if/else</em><em> control structure!</em>)




Two basic elements of Functional Programming are Lambda Expressions (which are anonymous methods) and Method References, that have had them in the course (Week 7). Java 8 also introduces <a href="https://docs.oracle.com/javase/8/docs/api/java/util/stream/package-summary.html">Streams</a> (hint: don’t mix them up with IO Streams! They are new beasts!) Lambda Expressions and Streams let you do variety of tasks on the elements of a collection with great ease.




In this assignment, you should first define a class <strong>Student</strong> which has four fields in this order:

firstName as a String, lastName as a String, grade as a double, and department as a

String. Provide one constructor for the class (which takes all the fields), setter and getter methods for all fields, a getName method which returns the full name of the student (<em>ex. “John White”</em>), toString, and equals methods.

We assume that there has been a contest among students of different departments and the results have been gathered as grades. Therefore, in a second class, <strong>StudentProcess</strong>, you are supposed to use functional programming to do various tasks on a collection of <strong>Student</strong>s.

You might want to have a look at the following classes/interfaces, as you will need them while doing the assignment:

<ul>

 <li>util.Arrays;</li>

 <li>util.Comparator;</li>

 <li>util.List;</li>

 <li>util.Map;</li>

 <li>util.TreeMap;</li>

 <li>util.function.Consumer;</li>

 <li>util.function.BiConsumer;</li>

 <li>util.function.Function;</li>

 <li>util.function.Predicate;</li>

 <li>util.stream.Stream;</li>

 <li>util.stream.Collectors;</li>

 <li>util.Optional;</li>

</ul>




<u>Task 1:</u> Create an array of Students in the beginning of your implementations, populate it with some Students, make a list out of your array, and print all its elements. You could create your own Student objects, hard-coded into your program and I will test your code run, against my input (use arbitrary values for first names, last names, grades – between 0.0 and 100.0 – and departments.) There is no need to read data from the file in this assignment (<em>hint: have a look at List&lt;E&gt; class and don’t forget to use method references to do this task and this assignment.</em>)




<u>Task 2:</u> Display Students with grades in the range 50.0-100.0, sorted into ascending order by grade. (<em>hint: you need to return a Stream&lt;Student&gt; out of your List&lt;Student&gt; first, and then use Stream and Comparator classes’ methods classes’ methods.</em>)

<u>Task 3:</u> Display the first student in the collection with grade in the range 50.0-100.0 (<em>hint: you need to return a Stream&lt;Student&gt; out of your List&lt;Student&gt; first, and then use Stream and Optional classes’ methods.</em>)

<u>Task 4:</u> Sort the Students (a)by their last names, and then their first names in ascending and (b)by their last names, and then their first names in descending orders and display the students after each of these two processes. (<em>hint: you need to return a Stream&lt;Student&gt; out of your List&lt;Student&gt; first, and then use Stream and Comparator classes’ methods.</em>)

<u>Task 5:</u> Display unique Student last names, sorted. (<em>hint: you need to return a Stream&lt;Student&gt; out of your List&lt;Student&gt; first, and map it to a Stream&lt;String&gt;, and use its methods.</em>)

<u>Task 6:</u> Display Student full names, sorted in order by last name then first name. (<em>hint: you need to return a Stream&lt;Student&gt; out of your List&lt;Student&gt; first, use Stream class’s methods, and map it to a Stream&lt;String&gt; somewhere along the way.</em>)

<u>Task 7:</u> Display Students, grouped by their departments. (<em>hint: you need to have an object of Map&lt;String, List&lt;Student&gt;&gt; and first populate it using Stream class’s methods, and second, display the desired output using Map class’s methods. You should also use Collectors for this task.</em>)

<u>Task 8:</u> Count and display the number of Students in each department. (<em>hint: you need to have an object of Map&lt;String, Long&gt; and first populate it using Stream class’s methods, and second, display the desired output using Map class’s methods. You should also use Collectors for this task.</em>)

<u>Task 9:</u> Calculate and display the sum of all Students’ grades. (<em>hint: you need to return a Stream&lt;Student&gt; out of your List&lt;Student&gt; first, and then use Stream class’s methods to map it to a DoubleStream, and then, use DoubleStream methods to do the task.) </em>




<u>Task 10:</u> Calculate and display the average of all Students’ grades. (<em>hint: you need to return a Stream&lt;Student&gt; out of your List&lt;Student&gt; first, and then use Stream class’s methods to map it to a DoubleStream, and then, use DoubleStream methods to do the task.) </em>

<strong> </strong>

<strong>Typical Output:  </strong>

For a typical input such as:

Student[] students = {

<table width="51">

 <tbody>

  <tr>

   <td width="51">StudentStudentStudentStudentStudentStudentStudent</td>

  </tr>

 </tbody>

</table>

<strong>new</strong> (“Jack”, “Smith”, 50.0, “IT”),          <strong>new</strong> (“Aaron”, “Johnson”, 76.0, “IT”),          <strong>new</strong> (“Maaria”, “White”, 35.8, “Business”),          <strong>new</strong> (“John”, “White”, 47.0, “Media”),          <strong>new</strong> (“Laney”, “White”, 62.0, “IT”),          <strong>new</strong> (“Jack”, “Jones”, 32.9, “Business”),          <strong>new</strong> (“Wesley”, “Jones”, 42.89, “Media”)};

<strong> </strong>

The output could be:




Task 1:




Complete Student list:

Jack     Smith       50.00   IT

Aaron    Johnson     76.00   IT

Maaria   White       35.80   Business

John     White       47.00   Media

Laney    White       62.00   IT

Jack     Jones       32.90   Business

Wesley   Jones       42.89   Media







Task 2:




Students who got 50.0-100.0 sorted by grade:

Jack     Smith       50.00   IT

Laney    White       62.00   IT

Aaron    Johnson     76.00   IT







Task 3:




First Student who got 50.0-100.0:

Jack     Smith       50.00   IT







Task 4:




Students in ascending order by last name then first:

Aaron    Johnson     76.00   IT

Jack     Jones       32.90   Business

Wesley   Jones       42.89   Media Jack     Smith       50.00   IT

John     White       47.00   Media

Laney    White       62.00   IT

Maaria   White       35.80   Business




Students in descending order by last name then first:

Maaria   White       35.80   Business

Laney    White       62.00   IT

John     White       47.00   Media Jack     Smith       50.00   IT

Wesley   Jones       42.89   Media

Jack     Jones       32.90   Business

Aaron    Johnson     76.00   IT




Task 5:




Unique Student last names:

Johnson

Jones

Smith

White




Task 6:




Student names in order by last name then first name:

Aaron Johnson

Jack Jones

Wesley Jones

Jack Smith

John White

Laney White

Maaria White




Task 7:




Students by department:

Media

John     White       47.00   Media

Wesley   Jones       42.89   Media

IT

Jack     Smith       50.00   IT

Aaron    Johnson     76.00   IT

Laney    White       62.00   IT

Business

Maaria   White       35.80   Business

Jack     Jones       32.90   Business




Task 8:




Count of Students by department:

Business has 2 Student(s)

IT has 3 Student(s)

Media has 2 Student(s)




Task 9:




Sum of Students’ grades: 346.59




Task 10:

Average of Students’ grades: 49.51

<strong> </strong>