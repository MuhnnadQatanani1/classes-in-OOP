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
5. [Key OOP Concepts](#key-oop-concepts)
6. [Benefits of Using These Class Types](#benefits-of-using-these-class-types)
7. [Getting Started](#getting-started)
8. [Conclusion](#conclusion)

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

### Why Use a Final Class?
**Security**: Prevents unauthorized extension and modification of the class.
**Immutability**: Ideal for creating immutable objects where state should not change after creation.
**Performance**: The JVM can optimize calls to final classes since it knows they won’t be overridden.
### When to Use a Final Class

1-When you want to create immutable classes (e.g., String in Java).

2-When designing utility or helper classes that should not be extended.

3-To ensure the integrity and security of critical classes.


---
## Superclass/Base Class: Vehicle
### What is a Superclass/Base Class?
A **superclass**  is a class that serves as a parent from which other classes (subclasses) inherit properties and behaviors. It encapsulates common attributes and methods that are shared across multiple subclasses, promoting code reuse and reducing duplication.
### Why Use a Superclass/Base Class?
**Code Reusability**: Common functionalities are defined once and reused by multiple subclasses.
**Maintainability**: Easier to manage and update shared features in one place.
**Logical Hierarchy**: Establishes a clear and logical relationship between classes.

### When to Use a Superclass/Base Class

1-When multiple classes share common attributes and behaviors.
2-To establish a hierarchical relationship between classes.
3-To implement shared functionalities that can be overridden or extended by subclasses.
---
## Subclass: Car
### What is a Subclass?
A **subclass**   is a class that inherits from a superclass. It inherits the superclass's attributes and methods while adding its own unique features or behaviors. Subclasses can also override methods to provide specific implementations.
### Why Use a Subclass?
**Specialization**: Allows subclasses to specialize and extend the functionality of the superclass.
**Flexibility**: Enables the creation of more specific classes based on general-purpose superclasses.
**Polymorphism**:  Facilitates dynamic method binding and flexible code design.

### When to Use a Subclass

1-When creating a more specific version of a general-purpose class.
2-To add or modify functionalities that are unique to the subclass.
3-When leveraging polymorphism to handle objects of different subclasses uniformly.
---
## Subclass: Car
### What is a Subclass?
A **subclass**   is a class that inherits from a superclass. It inherits the superclass's attributes and methods while adding its own unique features or behaviors. Subclasses can also override methods to provide specific implementations.
### Why Use a Subclass?
**Specialization**: Allows subclasses to specialize and extend the functionality of the superclass.
**Flexibility**: Enables the creation of more specific classes based on general-purpose superclasses.
**Polymorphism**:  Facilitates dynamic method binding and flexible code design.

### When to Use a Subclass

1-When creating a more specific version of a general-purpose class.
2-To add or modify functionalities that are unique to the subclass.
3-When leveraging polymorphism to handle objects of different subclasses uniformly.
---

## Key OOP Concepts
**Encapsulation**: Bundling data and methods that operate on the data within classes.
**Inheritance**: Mechanism where one class (subclass) inherits properties and behaviors from another (superclass).
**Polymorphism**: Ability to treat objects of different subclasses through a common superclass interface.
**Abstraction**: Hiding complex implementation details and exposing only the necessary parts of an object.
---

## Benefits of Using These Class Types
**Code Reusability**: Superclasses allow defining common functionalities once and reusing them across multiple subclasses.
**Maintainability**: Centralizing shared code in superclasses makes it easier to manage and update functionalities.
**Flexibility and Scalability**: Subclasses can extend and customize base functionalities.
**Security and Integrity**: Final classes ensure critical classes remain unaltered.
**Improved Organization**: Clear hierarchical structures make the codebase more organized and easier to navigate.
---

## Getting Started
**Prerequisites**
Java Development Kit (JDK): Ensure that JDK 8 or higher is installed on your machine.
IDE or Text Editor: Use an IDE like IntelliJ IDEA, Eclipse, or a text editor like VS Code.
---

## Conclusion
This Java OOP Demonstration Project effectively illustrates how to implement and leverage various class types to build a well-structured and maintainable codebase. By understanding and applying concepts like final classes, superclasses, base classes, and subclasses, you can create flexible and scalable applications that adhere to OOP best practices.

### Muhnnad Qatanani

**the Example is below**

```java
//`Engine` Class Example
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
//Vehicle Class Example(Superclass) 

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
//Car Class Example(Subclass) 

public class Car extends Vehicle {
    private String fuelType;

    public Car(String model, int year, String fuelType) {
        super(model, year); // Call the constructor of the superclass
        this.fuelType = fuelType;
    }

    public void refuel() {
        System.out.println(model + " is refueling with " + fuelType + ".");
    }

    // Getter
    public String getFuelType() {
        return fuelType;
    }
}


