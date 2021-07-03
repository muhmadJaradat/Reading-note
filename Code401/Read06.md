# OOP

## Object

Object can hold two thing state,behavior the state which have a values and behavior to use this values.objects are everywhere in real world example, the car is an object that has state like color,model, weight and a behavior for example you can turn it on and off.

## Class

The class is a blueprint for the object for example cars have many different  types,color,and models.

## Inheritance

* let's say that the cars I mentioned all share color, breakes and weight, but some types of cars have advanced technologies for example speed fixer,auto driver . so you can inherit all the common things from the main superclass (car)   for each subclass (different types of cars).

* In OOP I can have a parent class and as many children classes as i need.

* the parent class also called the super class.

* syntax to inherit from super class: `public class FingerPrintCar extends Car{}` .

## Interface

* objects have methods that allow me to communicate with them.

* for example: In order to work or communicate with T.V I should use buttons, in that sense buttons are methods and the board is the Interface that allow me to talk to the t.v.

* interface is class that contain group of methods.

* it contains methods with empty body.

* To create an interface class use following syntax:

```java
public interface myInterface{

    //  wheel revolutions per minute
    void turnTvOnOff(int newValue);

    void IncreaseVoice(int increment);

    void ChangeChannel(int newValue);

    void decreaseVoice(int decrement);
}
```

implement interface.

* to implement interface i need a class.

* that class should contain keyword implements.

* that class I can have anything I want, but there is a catch.

* The catch is I must implement all methods in the interface class or i will get error.

for example :

```java
public class App implements {
   void turnTvOnOff(int newValue){
       return 0;
   }

    void IncreaseVoice(int increment){
       return 0;
   }

    void ChangeChannel(int newValue){
       return 0;
   }
    void decreaseVoice(int decrement){
       return 0;
   }

}
```

## Package

* package is group of classes logically do common work.

* I should think of packages like I am grouping my classes for organizing them.

* Why I need packages? java is OOP language which means everything should be class, I might use hundreds of class so it's wise to 'package' them.