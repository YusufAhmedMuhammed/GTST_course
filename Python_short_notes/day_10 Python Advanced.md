
## 1. Functions
Purpose: Reusable blocks of code for specific tasks.

Types:

Built-in: `print(), len(), etc.`

User-defined:

`def greet(name):`
    `return f"Hello {name}!"`
`print(greet("Alice"))  # Output: Hello Alice!`

## 2. Function Features
Arguments: Pass input to a function.

Default Parameters:

`def power(x, n=2):`
    `return x ** n`

`print(power(3))    # Output: 9`
`print(power(3, 3)) # Output: 27`

Return Values: Use return to send output back.

Lambda Functions: Anonymous, single-line functions.

`square = lambda x: x * x`
`print(square(4))  # Output: 16`

## 3. Recursion
A function calling itself to solve subproblems.

Example: Factorial calculation

`def factorial(n):`
    `return 1 if n == 1 else n * factorial(n - 1)`
`print(factorial(5))  # Output: 120`

## 4. Functional Tools
filter(): Filters values based on a condition.

`evens = list(filter(lambda x: x % 2 == 0, [1, 2, 3, 4]))`
`print(evens)  # Output: [2, 4]`

map(): Applies a function to every item in an iterable.

`squares = list(map(lambda x: x ** 2, [1, 2, 3]))`
`print(squares)  # Output: [1, 4, 9]`

## 5. Object-Oriented Programming (OOP)
Class: Blueprint for objects.

Object: An instance of a class.

Constructor: __init__ method initializes data.

Methods: Functions inside classes.

`class Computer:`
    `def __init__(self, name, cpu):`
        `self.name = name`
        `self.cpu = cpu`

    `def info(self):`
        `return f"{self.name} has {self.cpu}"`

`pc = Computer("Dell", "i7")`
`print(pc.info())  # Output: Dell has i7`

## 6. Inheritance
Allows a class to inherit properties/methods from another.

`class Animal:`
    `def eat(self):`
        `print("Eating...")`

`class Dog(Animal):`
    `def bark(self):`
        `print("Barking!")`

`dog = Dog()`
`dog.eat()   # Output: Eating...`
`dog.bark()  # Output: Barking!`

## 7. Packages & Modules
Install external packages:

`pip install package-name`

Import standard libraries:

`import math`
`from datetime import date`

`print(math.sqrt(16))       # Output: 4.0`
`print(date.today())        # Output: 2025-04-16 (example)`

## 🧩 Key Exercises
🔢 Function: Calculate birth year from age.

👤 OOP: Build a Human class with behaviors like walk() and speak().

🔄 Functional Programming: Use map() and filter() on a list of numbers.

🧬 Inheritance Practice: Create a class hierarchy (e.g., Animal → Mammal → Dog).

## 🎯 Pro Tip:
Mastering advanced Python is about writing less code that does more — through abstraction, composition, and efficient data handling.