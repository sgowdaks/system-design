## 1. The Core Pillars of LLD

Before you touch a design pattern, you need to master the fundamental principles. These are the "rules of the road" for clean code.

### SOLID Principles

These five principles are the bread and butter of LLD. You should be able to explain them and, more importantly, identify when they are being violated.

* **S:** Single Responsibility (A class should have one reason to change).
* **O:** Open/Closed (Open for extension, closed for modification).
* **L:** Liskov Substitution (Subtypes must be substitutable for their base types).
* **I:** Interface Segregation (Don't force a class to implement methods it doesn't use).
* **D:** Dependency Inversion (Depend on abstractions, not concretions).

### Object-Oriented Programming (OOP)

You need a deep comfort level with **Inheritance, Encapsulation, Polymorphism, and Abstraction**. Practice mapping real-world objects into class hierarchies.

---

## 2. Design Patterns (The "Cheat Codes")

Design patterns are proven solutions to recurring problems. You don't need to know all 20+, but you must master these "Must-Haves":

| Category | Patterns to Master |
| --- | --- |
| **Creational** | Singleton, Factory, Abstract Factory, Builder |
| **Structural** | Adapter, Decorator, Facade, Proxy |
| **Behavioral** | Strategy, Observer, State, Command |

---

## 3. The LLD Interview Workflow

In an interview, don't jump straight into coding. Follow this structured approach:

1. **Clarify Requirements:** Ask questions to define the scope. (e.g., "For a Parking Lot, do we need to support electric vehicle charging stations?")
2. **Define Entities/Classes:** Identify the "nouns" in your requirements.
3. **Class Diagram (UML):** Map out the relationships (Is-a vs. Has-a).
4. **Define APIs/Methods:** What are the entry points for the user?
5. **Code Implementation:** Write the core logic, focusing on the interfaces and patterns you chose.

---

## 4. Practice Projects

The best way to learn LLD is by building "Mini-Systems." Try designing these from scratch:

* **Parking Lot:** Classic for practicing inheritance and strategy patterns.
* **Logging Framework:** Great for Singleton and Chain of Responsibility.
* **Snake and Ladder / Chess:** Perfect for state management and game logic.
* **Vending Machine:** The ultimate test for the **State Pattern**.
* **Stack Overflow / Movie Booking System:** Excellent for entity relationship and concurrency basics.

