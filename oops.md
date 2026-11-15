###  Object-Oriented Programming (OOPs) 
OOPs stands for Object-Oriented Programming. It is a programming paradigm (approach) that organizes code around objects rather than just functions and logic.

OOPs helps us write code that is:
- Reusable
- Modular
- Maintainable
- Secure
- Easy to extend
Java is a popular object-oriented programming language


1. Class and Object
These are the two fundamental building blocks of OOPs.

### Class
A class is a blueprint or template used to create objects. It defines the properties (data) and behaviors (methods) that its objects will have.


### Object
An object is an instance of a class that has its own state and behavior.

### 2. Four Pillars of OOPs
There are four major principles of object-oriented programming:

### 2.1 Encapsulation
Definition: Encapsulation is the process of wrapping data (variables) and methods into a single unit (class) and restricting direct access to the data.

In simple words: Data hiding and controlled access.


### 2.2 Abstraction
Definition: Abstraction is the process of hiding internal implementation details and exposing only essential functionality to the user.
In simple words: Show what is necessary, hide how it works.

Java supports abstraction through:
1. Abstract classes
2. Interfaces

### 2.3 Inheritance
Definition: Inheritance is a mechanism through which one class acquires the properties and methods of another class.

It promotes code reusability.


### Types of inheritance
1. Single Inheritance - One child inherits from one parent.

2. Multilevel Inheritance - A class inherits from a class that itself inherits from another class.

3. Hierarchical Inheritance - Multiple child classes inherit from one parent.

4. Multiple Inheritance - One child inherits from multiple parents.

Important Java interview point: Java does not support multiple inheritance through classes to avoid ambiguity (diamond problem). However, it supports multiple inheritance of type through interfaces.

### 2.4 Polymorphism
Definition: Polymorphism means one entity can take multiple forms.
In Java, polymorphism allows the same method name or interface to behave differently depending on the situation.

There are two main types:
1. Compile-time polymorphism (Method Overloading)
2. Runtime polymorphism (Method Overriding)

A. Method Overloading
When multiple methods have the same name but different parameter lists within a class, it is called method overloading.

Important: Changing only the return type does not constitute method overloading.

B. Method Overriding
When a child class provides its own implementation of a method already defined in its parent class, it is called method overriding.

### Overloading vs Overriding
Overloading	Overriding
Same method name	Same method signature
Different parameters	Same parameters
Usually within the same class	Requires inheritance
Compile-time polymorphism	Runtime polymorphism
Return type can differ if parameters differ	Return type must be compatible


### 3. Important OOPs Concepts for Interviews
Apart from the four pillars, understand these concepts as well.
3.1 Constructor
A constructor is a special member of a class used to initialize objects.

Important properties:
- Constructor name must be the same as the class name.
- It does not have a return type.
- It is automatically called when an object is created.

Types:
- Default constructor
- No-argument constructor
- Parameterized constructor

Note: If you don't declare any constructor, Java provides a default constructor. Once you declare a constructor, Java does not automatically provide one.

### 3.2 Interface
An interface defines a contract that implementing classes must follow.

### Important:
- A class uses implements to implement an interface.
- A class can implement multiple interfaces.
- Interfaces can contain abstract methods, default methods, static methods and other supported members.

### 3.3 Abstract Class vs Interface
Abstract Class                  	        Interface
Declared using abstract	                     Declared using interface
Can have constructors	                      Cannot have constructors
Can have instance variables 	            Fields are implicitly public, static and final
Can have abstract and concrete methods	    Can have abstract, default, static and private methods
A class extends one class                   	A class can implement multiple interfaces

### 3.4 Access Modifiers
Access modifiers control the visibility of classes, variables, constructors and methods.
Modifier	Accessibility
private	Within the same class
default	Within the same package
protected	Same package and subclasses
public	Accessible from anywhere, subject to module/package accessibility


## 3.5 Static Keyword
The static keyword means a member belongs to the class rather than individual objects.

### 3.6 this and super
Keyword	Meaning
this	Refers to the current object
super	Refers to the immediate parent class

###  Static vs Final
Static	                                                 Final
Belongs to the class    	                    Restricts modification or extension
Can be used with variables and methods  	Can be used with variables, methods and classes
Static variables are shared             	Final variables cannot be reassigned
Static methods can be hidden                	Final methods cannot be overridden and extended

### finally block
The finally block is used in exception handling to execute cleanup code.
It normally executes whether an exception occurs or not.

### finalize 
Historically, it was intended to give an object an opportunity to perform cleanup before garbage collection. 
In latest versions it is discontinued



