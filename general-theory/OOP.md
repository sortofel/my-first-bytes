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
- JavaScript uses `extends` keyword.
- To call the parent class constructor, use `super()`.

```js
class Player {
  constructor(name) {
    this.name = name;
  }
}

class SuperPlayer extends Player {
  constructor(name, power) {
    super(name);         // Call parent constructor
    this.power = power;
  }
}
```

---

### 2. Encapsulation

- Keeping related data and methods together inside a **class**.
- Hides internal implementation and exposes only what's necessary.

```js
class BankAccount {
  #balance = 0; // private field

  deposit(amount) {
    this.#balance += amount;
  }

  getBalance() {
    return this.#balance;
  }
}
```

---

### 3. Abstraction

- Hides complex implementation and shows only the interface.
- Makes the code easier to use without knowing internal details.

```js
// User doesn't need to know how the engine works
class Car {
  startEngine() {
    console.log("Vroom!");
  }

  drive() {
    this.startEngine();
    console.log("Driving...");
  }
}
```

---

### 4. Polymorphism

- "Many shapes": Same method name behaves differently in different classes.
- Methods can be **overridden** in child classes.

```js
class Animal {
  speak() {
    console.log("Animal speaks");
  }
}

class Dog extends Animal {
  speak() {
    console.log("Dog barks");
  }
}
```
