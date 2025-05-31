# Object Oriented Programming
### :link: OOP
- [1. Inheritance](#1-inheritance)
- [2. Encapsulation](#2-encapsulation)
- [3. Abstraction](#3-abstraction)
- [4. Polymorphism](#4-polymorphism)
---
## OOP 4 Pillars
### 1. Inheritance
- Allows one class to inherit properties and methods from another.
- Java uses `extends` keyword.
- To call the parent class constructor, use `super()`.
- Like how specialized cells (muscle, nerve) inherit basic cellular structures but add their own functions.
```java
public class Player {
    public String name;
    
    public Player(String name) {
        this.name = name;
    }
}
```
```java
public class SuperPlayer extends Player {
    public int power;
    
    public SuperPlayer(String name, int power) {
        super(name);
        this.power = power;
    }
}
```
---
### 2. Encapsulation
- Keeping related data and methods together inside a **class**.
- Hides internal implementation and exposes only what's necessary.
- Like a cell membrane that protects internal components and controls what enters/exits.
```java
public class BankAccount {
    private double balance = 0;
    
    public void deposit(double amount) {
        this.balance += amount;
    }
    
    public double getBalance() {
        return this.balance;
    }
}
```
---
### 3. Abstraction
- Hides complex implementation and shows only the interface.
- Like how you don't need to understand cellular respiration to know that cells produce energy.
- In Java, use `abstract` keyword to create abstract classes that cannot be instantiated.
- **Abstract vs Interface**: Abstract classes can have concrete methods and fields, interfaces only define method signatures.
```java
abstract class Animal {
    protected String species;
    
    public void breathe() {
        System.out.println("Breathing oxygen");
    }
    
    public abstract void makeSound();
}
```
```java
public class GuineaPig extends Animal {
    public void makeSound() {
        System.out.println("Guinea pig squeaks");
    }
}
```
```java
interface Flyable {
    protected int mile = 1; //non-changeable

    void fly();
    void land();
}
```
---
### 4. Polymorphism
- "Many shapes": Same method name behaves differently in different classes.
- Methods can be **overridden** in child classes.
- Like how different cell types respond differently to the same hormone signal.
```java
public class Animal {
    public void speak() {
        System.out.println("Animal speaks");
    }
}
```
```java
public class Dog extends Animal {
    @Override
    public void speak() {
        System.out.println("Dog barks");
    }
}
```
