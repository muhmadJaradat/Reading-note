# Object Oriented Design

## The First 5 Principles of Object Oriented Design

* principles that take into consideration when i am designing my project is to be maintained and can grow in the future without problems or code debugging and very important for agile software development.

* the 5 principles:

1. single responsibility Principle.

2. open closed principle.

3. Liskov. substituion principle.

4. interface segeration principle.

5. dependency inversion principle.

### single responsibility principle

* `Each class should do only one job.`

 For example lets say I want a class to calculate the area of a shape.if the class calculate and output result as multi form e.g. html or json it would be violation for the `SRP`.
 to solve this, i will first calculate the shape and create a class that handle outputing whatever recieve, the way the user want it.

### open closed principle

* `Objects should be open for extension but closed for modification.`

meaning the class should be extendable but should not be modified.
and example: let's say the area calculator that accept any shape and calculateit's area, if I want to think how to do it, I will create if else statement for each shape. but what if I want to add new shape ?

Here I voilate the open closed principle. so to solve this I will create class for each shape and claculate the area in each class. now the code can be expanded without modification. when i want to add a new shape I will create a class for that shape.

### Liskov subsition principle

`Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T. Resource`

This means that every subclass or derived class should be substitutable for their base or parent class.

### Interface Segregation Principle

`A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to depend on methods they do not use.`

when i create the interface and create a class implementation for it. and some of my inherited class will be forced to use it since they implement that interface, this voilate the interface segreation principle. to solve this create another interface that implement methods fit it's functionality.now the user won't use the old interface thus will not use it's method.

### Dependency inversion principle

`Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions.`

like principle said it should depend on abstraction not concretions.

 to do that, i would create an interface class and force low level class to implement it.
