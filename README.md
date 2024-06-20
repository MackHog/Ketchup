# Ketchup
Daily read to ketchup with the inner monkey

## Domain Driven Design
Ubiquitous language - talk the same language as the business, reflect the language in the codes domain.

## SOLID principles

### Single Responsibility Principle (SRP)
Functionality should be related to a single responsibility (and have only one reason for changing).

### Open-Close Principle (OCP)
Software entities such as modules, classes, functions, etc. should be open for extension, but closed for modification

### Liskov Substitution Principle (LSP)
We can successfully replace the object/instance of a parent class with an object/instance of the child class, without affecting the behavior of the base class instance.
(If S is a subtype of T, then objects of type T should be replaced with objects of type S)

### Interface Segregation Principle (ISP)
Clients should not be forced to implement any methods they do not use. Rather than one fat interface, numerous little interfaces are preferred.

### Dependency Inversion Principle (DIP)
High-level modules/classes should not depend on low-level modules/classes. Instead, both should depend upon abstractions

## Rules

### Law of demeter (Principle of Least Knowledge)
Only talk to your immediate friends.
Never go two dots down.

Order have a friend in Items but should not beg Items for more info.
~~~ 
if (order.Items.Count > 0)
~~~ 
Should be
~~~ 
if (order.HasItems)
~~~ 

### Keep it simple, stupid (KISS)

## SQL

Index scan is bad. Index seek is good.

## Algoritm

### Big O notation

O(1) => Constant Time Complexity (same speed independet of number of elements) => array.indexOf
O(log n) => Logarithmic Time Complexity. Execution time increases logarithmically with the size of the input => binary search
O(n) => Linear Time Complexity. Increases proportionally to the size of the input (n = number of elements) => foreach
O(n²) => Quadratic Time Complexity. if the input size increases, the algorithm’s running time increases by the square of that size => foreach in foreach