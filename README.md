# ☕ Drink Machine – Factory Method Pattern in Java

This repository demonstrates the **Factory Method** design pattern by implementing a drink machine that produces various types of coffee and tea based on user input.

## 🚀 Overview

The project uses the **Factory Method** to delegate the instantiation of drinks to concrete creators:

- `DrinkCreator` is an abstract base class.
- `TeaCreator` and `CoffeeCreator` implement the creation logic for different drink types.
- `Drink` is an interface implemented by drink classes like `Americano`, `MilkOolongTea`, etc.

## 📁 Project Structure

```
factorymethod/
├── DrinkCreators/
│   ├── Abstractions/DrinkCreator.java
│   ├── CoffeeCreator.java
│   └── TeaCreator.java
├── Drinks/
│   ├── Coffee/ (Espresso, Latte, Cappuccino, etc.)
│   ├── Tea/ (BlackTea, GreenTea, etc.)
│   ├── Enums/ (CoffeeTypes.java, TeaTypes.java, DrinkTypes.java)
│   └── Interfaces/Drink.java
DrinkMachine.java
```

## 🧪 Sample Usage (Main)

```java
DrinkCreator teaCreator = new TeaCreator();
teaCreator.pourDrink(); // Default tea
teaCreator.pourDrink(TeaTypes.MILK_OOLQNG); // Specific tea

DrinkCreator coffeeCreator = new CoffeeCreator();
coffeeCreator.pourDrink(); // Default coffee
coffeeCreator.pourDrink(CoffeeTypes.CAPPUCCINO); // Specific coffee
```

## ✅ Output Example

```
Factory Method
Default tea...
Milk Oolong Tea
Default coffee...
Cappuccino
```

## 💡 Benefits

- **Open/Closed Principle**: New drinks can be added with minimal changes.
- **Encapsulation**: Creation logic is hidden from the client.
- **Polymorphism**: Unified interface (`Drink`) allows flexible usage.

## 🧱 Extending the Project

To add a new drink:

1. Implement a new class in `Drinks/Tea/` or `Drinks/Coffee/` that implements `Drink`.
2. Add a new value to the corresponding enum (`TeaTypes` or `CoffeeTypes`).
3. Update the `switch` in `TeaCreator` or `CoffeeCreator` accordingly.

## 📌 Design Pattern Reference

This is a textbook example of the [Factory Method](https://refactoring.guru/design-patterns/factory-method) pattern — a **creational pattern** used to delegate object instantiation.
