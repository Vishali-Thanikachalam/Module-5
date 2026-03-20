
# 1. Constructors in Python: Welcome Message with Student Name

## 🎯 Aim
To write a Python program that creates a **Student** class with a **default constructor** and a method to display a welcome message along with the student’s name provided by the user.

## 🧠 Algorithm
1. **Get user input**: Accept the student's name from the user.
2. **Define the class**: Create a class `Student` with a default constructor (`__init__`).
3. **Default Constructor**: In the constructor, assign the user input (student name) to an instance variable `self.a`.
4. **Display Message**: Define a method `show` that prints "This is non-parameterized constructor" and a welcome message with the student’s name.
5. **Execute the Program**: Instantiate the `Student` class and call the `show` method.

## 🧾 Program
```
name = input("Enter the student's name: ")

class Student:
   
    def __init__(self):
        self.a = name  # assign user input to instance variable

    def show(self):
        print("This is a non-parameterized constructor")
        print("Welcome,", self.a)

s = Student()
s.show()
```

## Output
<img width="530" height="152" alt="image" src="https://github.com/user-attachments/assets/30e8d348-56b8-4693-8790-54c8904af1fd" />

## Result
Thus, the program was executed successfully.

 
# 2. Destructor in Python

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
<img width="597" height="152" alt="image" src="https://github.com/user-attachments/assets/ce14e753-fd80-4ecc-809b-b3c3377625a6" />

## Result
Thus, the program was executed successfully.


# 3. Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
```
class Details:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def getName(self):
        return self.name

    def getAge(self):
        return self.age


class Employee(Details):
    def __init__(self, name, age, employee_id, department):
        super().__init__(name, age)
        self.employee_id = employee_id
        self.department = department

    def getEmployeeDetails(self):
        print("\n--- Employee Details ---")
        print("Name:", self.getName())
        print("Age:", self.getAge())
        print("Employee ID:", self.employee_id)
        print("Department:", self.department)


class Patient(Details):
    def __init__(self, name, age, patient_id, disease):
        super().__init__(name, age)
        self.patient_id = patient_id
        self.disease = disease

    def getPatientDetails(self):
        print("\n--- Patient Details ---")
        print("Name:", self.getName())
        print("Age:", self.getAge())
        print("Patient ID:", self.patient_id)
        print("Disease:", self.disease)


# Get input for Employee
ename = input("Enter Employee Name: ")
eage = int(input("Enter Employee Age: "))
eid = input("Enter Employee ID: ")
edept = input("Enter Department: ")

# Create Employee object and display details
emp = Employee(ename, eage, eid, edept)
emp.getEmployeeDetails()

# Get input for Patient
pname = input("\nEnter Patient Name: ")
page = int(input("Enter Patient Age: "))
pid = input("Enter Patient ID: ")
pdisease = input("Enter Disease: ")

# Create Patient object and display details
pat = Patient(pname, page, pid, pdisease)
pat.getPatientDetails()

```
## Sample Output
<img width="458" height="666" alt="image" src="https://github.com/user-attachments/assets/3d786b5b-4cbc-4db4-b6dd-9ee981d6d3fa" />

## Result
Thus, the program was executed successfully.


# 4. Multilevel Inheritance Example in Python

This Python project demonstrates the concept of **Multilevel Inheritance** to collect and display the **name**, **age**, and **location** of a person.

## 🎯 Aim

To write a Python program that uses multilevel inheritance to get and display a person’s name, age, and location.

## 🧠 Algorithm

1. **Parent Class**  
   - `__init__(name)` initializes the `name` attribute.  
   - `getName()` returns the `name`.

2. **Child Class (inherits Parent)**  
   - `__init__(name, age)` initializes `name` using `super()` and adds `age`.  
   - `getAge()` returns the `age`.

3. **Grandchild Class (inherits Child)**  
   - `__init__(name, age, location)` initializes `name` and `age` using `super()` and adds `location`.  
   - `getLocation()` returns the `location`.

4. **Input & Output**  
   - Take user input for name, age, and location.  
   - Create an instance of `Grandchild`.  
   - Print all details using class methods.

## Program
```
class Person:
    def __init__(self, name):
        self.name = name

    def getName(self):
        return self.name


class Student(Person):
    def __init__(self, name, age):
        super().__init__(name)
        self.age = age

    def getAge(self):
        return self.age


class Resident(Student):
    def __init__(self, name, age, location):
        super().__init__(name, age)
        self.location = location

    def getLocation(self):
        return self.location


# Input from user
name = input("Enter Name: ")
age = int(input("Enter Age: "))
location = input("Enter Location: ")

# Creating object of Grandchild class
r = Resident(name, age, location)

# Display details
print("\n--- Person Details ---")
print("Name:", r.getName())
print("Age:", r.getAge())
print("Location:", r.getLocation())

```

## Sample Output
<img width="453" height="279" alt="image" src="https://github.com/user-attachments/assets/695fcb79-764d-4474-b20e-1a7fa23e7533" />

## Result
Thus, the program was executed successfully.

# 5. Arithmetic Operations Using Multiple Inheritance in Python

This Python program demonstrates **multiple inheritance** by performing basic arithmetic operations — Addition, Subtraction, and Division — using three classes.

## 🎯 Aim

To write a Python program to calculate **Add, Sub & Division** using **Multiple Inheritance**.

## 🧠 Algorithm

1. **Define `Calculation1` class**
   - Contains `Summation(a, b)` method to return the sum of two numbers.
2. **Define `Calculation2` class**
   - Contains `Subtraction(a, b)` method to return the difference of two numbers.
3. **Define `Derived` class**
   - Inherits from both `Calculation1` and `Calculation2`.
   - Contains `Division(a, b)` method to return the division result.
4. **Input**
   - Prompt the user to enter two numbers.
5. **Process**
   - Create an object of the `Derived` class.
   - Call `Summation`, `Subtraction`, and `Division` methods.
6. **Output**
   - Display the results of the three operations.

## 💻 Program 
```
class Calculation1:
    def Summation(self, a, b):
        return a + b


class Calculation2:
    def Subtraction(self, a, b):
        return a - b


class Derived(Calculation1, Calculation2):
    def Division(self, a, b):
        return a / b


# Input from user
a = float(input("Enter first number: "))
b = float(input("Enter second number: "))

# Create object of Derived class
d = Derived()

# Perform operations
print("\n--- Arithmetic Operations ---")
print("Addition:", d.Summation(a, b))
print("Subtraction:", d.Subtraction(a, b))
print("Division:", d.Division(a, b))

```
## Output Example
<img width="475" height="268" alt="image" src="https://github.com/user-attachments/assets/5ecbdf44-ed00-45ad-b202-e6692de8a7db" />

## Result
Thus, the program was executed successfully.
