# LMS-OOP
Design Pattern Analysis

We could have used a Factory Design pattern. Factory pattern is used to create objects using a common interface. We could have used this pattern for creating different types of book objects like Textbook, Magazine, Journals etc. A library factory can be created which will make these objects based on input. This would help us promote loose coupling in the system and also make it easier while testing.

Strategy Design Pattern could have been used in our project. In this design pattern, we use an interface to apply an algorithm. For example, our code has a searchBook() function for both student and librarian. So, the User class could have been made as an interface and Student and Librarian class can implement this interface thus implementing various common methods like searchBook() or viewAllBooks()



















SOLID Principles


1) Single Responsibility

This principle is not incorporated in our code. In our code, a single class has many responsibilities. The student class contains various methods such as searchBook(), issueBook(), renewBook(), returnBook() and viewDues(). Apart from this, the Librarian class deals with methods namely removeBook(), searchBook(), displayAllBooks(), editBookDetails(), searchStudent(), displayAllStudents(), editStudentDetails(), and settleDues().

Consequences:
a) Both student class and librarian class have a lot of test cases. It is also difficult to debug runtime behavior because a single class contains a lot of functionalities.
b) There are few places in which code indicates high coupling because of large dependencies.


2) Open for extension, closed for modification
  
 This principle is not incorporated in our code. The LibraryDataBase class is connected with every function. Whenever we implement any feature/functionality, LibraryDataBase needs to be modified as well.

Consequences:
a) As LibraryDataBase  is linked with a lot of methods, we won’t be able to test a single functionality. The entire flow will be tested.
b) It breaks the single responsibility principle as well. Both the principles are interrelated.



3) Liskov Substitution
   
Our code is following this principle. All the derived classes that are Librarian and the student class can be substituted with the super class. Objects of subclasses (student) behave the same way as the object of the superclass.

Advantages: Our code encourages code reusability.

4) Interface Segregation
   
We have not implemented any large interface in our code.

5) Dependency Inversion
   
This principle is not incorporated in our code. All our classes and functions are highly coupled. Also, the LibraryDatabase class is dependent upon Student class and Librarian class. All three are not linked by abstractions.

Consequences:
a) This limits the reuse of higher level components that is LibraryDatabase class.
b) All the functions will remain tightly coupled until we follow dependency inversion principle.












UML Diagrams:
