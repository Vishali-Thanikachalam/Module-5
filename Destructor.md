# Destructor in Python

This project demonstrates how to implement a **destructor** in Python using a simple class.

## 🚀 Overview

The program defines a class `Demo` with:

- A **constructor** `__init__` that initializes an instance variable and prints a message.
- A **destructor** `__del__` that prints a message when the object is destroyed.

## 🧠 Algorithm

1. Define a class named `Demo`.
2. Inside the class, define the `__init__` method:
   - Initialize an instance variable `status` with the value `"Alive"`.
   - Print the value of `status`.
3. Define the `__del__` method:
   - Print a message indicating the object is being destroyed.
4. Outside the class:
   - Create an instance of the `Demo` class.
   - Delete the object using the `del` keyword.
## Program
```
class Demo:
    def __init__(self):
        self.status = "Alive"
        print("Object status:", self.status)

    def __del__(self):
        print("Destructor called... Object is being destroyed.")

d = Demo()
del d
```

## 🧪 Output
<img width="597" height="152" alt="image" src="https://github.com/user-attachments/assets/603a523b-426a-4988-9f0b-04f7ca635af1" />

## Result
Thus, the program has been executed successfully.
