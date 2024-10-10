# Java OOP Demonstration Project

## Overview

Welcome to the **Java OOP Demonstration Project**! This project serves as a comprehensive example of **Object-Oriented Programming (OOP)** principles in Java. It showcases various types of classes, including **final classes**, **superclasses**, **base classes**, and **subclasses**, to illustrate key OOP concepts such as **encapsulation**, **inheritance**, **polymorphism**, and **abstraction**.

By exploring this project, you'll gain a deeper understanding of how to structure and organize your Java applications using OOP best practices, making your code more modular, reusable, and maintainable.

---

## Table of Contents

1. [Classes Overview](#classes-overview)
2. [Final Class: `Engine`](#final-class-engine)
3. [Superclass/Base Class: `Vehicle`](#superclassbase-class-vehicle)
4. [Subclass: `Car`](#subclass-car)
5. [Subclass with Additional Functionality: `ElectricCar`](#subclass-with-additional-functionality-electriccar)
6. [Key OOP Concepts](#key-oop-concepts)
7. [Benefits of Using These Class Types](#benefits-of-using-these-class-types)
8. [Getting Started](#getting-started)
9. [Conclusion](#conclusion)

---

## Classes Overview

This project includes the following types of classes:

1. **Final Class**: A class that cannot be extended by any other class.
2. **Superclass/Base Class**: A general-purpose class from which other classes inherit.
3. **Subclass**: A class that extends a superclass, inheriting its properties and methods while adding or modifying functionality.
4. **Subclass with Additional Functionality**: A subclass that not only inherits from a superclass but also introduces new attributes or methods and may override existing ones.

---

## Final Class: `Engine`

### What is a Final Class?

A **final class** in Java is a class that cannot be subclassed. Using the `final` keyword ensures that the class's implementation remains unchanged and cannot be extended, which is useful for creating immutable classes or securing the class's behavior.

### `Engine` Class Example

The `Engine` class represents a vehicle's engine. It is marked as `final` to prevent any subclass from altering its fundamental behavior.

```java
public final class Engine {
    private String engineType;
    private int horsepower;

    public Engine(String engineType, int horsepower) {
        this.engineType = engineType;
        this.horsepower = horsepower;
    }

    public void startEngine() {
        System.out.println("Engine started: " + engineType + " with " + horsepower + " HP.");
    }

    public void stopEngine() {
        System.out.println("Engine stopped.");
    }

    // Getters
    public String getEngineType() {
        return engineType;
    }

    public int getHorsepower() {
        return horsepower;
    }
}
---
## Superclass/Base Class: Vehicle
### What is a Superclass/Base Class?
A **superclass**  is a class that serves as a parent from which other classes (subclasses) inherit properties and behaviors. It encapsulates common attributes and methods that are shared across multiple subclasses, promoting code reuse and reducing duplication..
### `Engine` Class Example
Vehicle Class Example
The Vehicle class serves as the base class for all vehicle types in the project. It contains common attributes like model and year, and methods such as start() and stop().
```java
public class Vehicle {
    protected String model;
    protected int year;

    public Vehicle(String model, int year) {
        this.model = model;
        this.year = year;
    }

    public void start() {
        System.out.println(model + " started.");
    }

    public void stop() {
        System.out.println(model + " stopped.");
    }

    // Getters
    public String getModel() {
        return model;
    }

    public int getYear() {
        return year;
    }
}


