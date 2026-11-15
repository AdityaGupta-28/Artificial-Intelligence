

 #### ############################ JAVA

### Throwable
"Throwable is the root superclass of Java's exception-handling mechanism. Both Error and Exception inherit from Throwable.

1. What is an exception?
An exception is an unwanted event that occurs during program execution and disrupts the normal flow of the program.

2. Error is unwanted interupt in program execution and it can't be handle


### 4. Important keywords related to Throwable
Keyword                         	Meaning
try	                        Contains code that may cause an exception
catch	                Handles an exception
finally	                Executes after try/catch in normal completion and most control-flow cases
throw	                 Explicitly throws a throwable object
throws	                Declares possible exceptions in a method signature


1. What is the Java Collections Framework?
The Java Collections Framework is a set of interfaces, classes and algorithms provided by Java to store, manage and manipulate groups of objects efficiently.

Instead of implementing data structures from scratch, we can use ready-made classes such as ArrayList, LinkedList, HashSet and HashMap.

### 1. What is HashMap?
HashMap is a class in Java that implements the Map interface. It stores data in the form of key-value pairs.

Important characteristics:
- Keys must be unique.
- Duplicate keys overwrite their previous values.
- Multiple keys can have the same value.
- It allows one null key and multiple null values.
- It does not guarantee insertion order.
- It is not synchronized by default.

### Internal Working of HashMap in Java
HashMap internally uses an array of buckets, where each bucket stores key-value entries.

When we insert a key-value pair using put():
1. Hashing: HashMap calls hashCode() on the key to calculate its hash.
2. Index calculation: It calculates the bucket index using the hash and array capacity.
3. Storage: The key-value pair is stored in the calculated bucket.
4. Collision handling: If two keys map to the same bucket, Java handles the collision using linked nodes. In Java 8+, heavily populated buckets can be converted into Red-Black Trees.
5. Retrieval: When get() is called, HashMap calculates the bucket index and uses equals() to identify the correct key and return its value.

## Important interview points
- Default initial capacity: 16
- Default load factor: 0.75
- Average time complexity of put() and get(): O(1)
- Collision resolution: Linked nodes / Red-Black Tree.
- hashCode() calculates the hash; equals() checks key equality.


###  HashMap vs Hashtable
Feature         	HashMap	            Hashtable
Synchronization	    Not synchronized	Synchronized
Thread safety	    Not thread-safe	    Thread-safe for individual operations
Performance	        Generally faster	Generally slower
Null key	        Allows one	        Not allowed
Null values	        Allowed	            Not allowed
Introduced	        Java 1.2	        Java 1.0
Legacy status	    Modern collection	Legacy class

### 2. Internal working of HashSet
The most important interview point:

HashSet internally uses a HashMap to store elements.

When you add an element:
1. HashSet calls add(element).
2. Internally, it stores the element as a key in a HashMap.
3. It uses a dummy constant object as the value.
4. HashMap calculates the hash using hashCode().
5. If a collision occurs, equals() checks whether the element already exists.
6. If the element already exists, it is not added again.

