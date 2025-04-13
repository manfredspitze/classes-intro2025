Here are three examples of Python classes that your students can create as part of a PRIMM (Predict, Run, Investigate, Modify, Make) activity. The classes are `Book`, `Car`, and `Student`. Each class will help students understand different aspects of object-oriented programming.

### Class Examples

1. **Book Class**
   - Attributes: `title`, `author`, `pages`, `is_read`
   - Methods: 
     - `read()`: Marks the book as read.
     - `get_info()`: Returns a string with the book's details.

2. **Car Class**
   - Attributes: `make`, `model`, `year`, `mileage`
   - Methods:
     - `drive(miles)`: Increases the mileage by the number of miles driven.
     - `get_info()`: Returns a string with the car's details.

3. **Student Class**
   - Attributes: `name`, `age`, `grades`
   - Methods:
     - `add_grade(grade)`: Adds a grade to the student's list of grades.
     - `get_average()`: Returns the average of the student's grades.

### PRIMM Activity Instructions

**Objective:** Students will create and use the `Book`, `Car`, and `Student` classes to understand the principles of object-oriented programming in Python.

#### Step 1: Predict

- **Task:** Before writing any code, ask students to predict what each class will do based on its attributes and methods. 
- **Questions to Consider:**
  - What information do you think each class will store?
  - How do you think the methods will interact with the attributes?
  - What kind of output do you expect from the methods?

#### Step 2: Run

- **Task:** Provide students with starter code for each class. They will run the code to see if it works as expected. 

**Starter Code:**

```python
# Book Class
class Book:
    def __init__(self, title, author, pages):
        self.title = title
        self.author = author
        self.pages = pages
        self.is_read = False

    def read(self):
        self.is_read = True

    def get_info(self):
        return f"{self.title} by {self.author}, {self.pages} pages. Read: {self.is_read}"

# Car Class
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.mileage = 0

    def drive(self, miles):
        self.mileage += miles

    def get_info(self):
        return f"{self.year} {self.make} {self.model}, Mileage: {self.mileage} miles"

# Student Class
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age
        self.grades = []

    def add_grade(self, grade):
        self.grades.append(grade)

    def get_average(self):
        return sum(self.grades) / len(self.grades) if self.grades else 0
```

- **Expected Output:** Students should run the code and see that no errors occur. They can create instances of each class and call the methods to see the results.

#### Step 3: Investigate

- **Task:** Students will investigate how the classes work by creating instances and calling methods. They should explore the following:

```python
# Create instances
my_book = Book("1984", "George Orwell", 328)
my_car = Car("Toyota", "Camry", 2020)
my_student = Student("Alice", 17)

# Call methods
my_book.read()
print(my_book.get_info())  # Should show that the book has been read

my_car.drive(150)
print(my_car.get_info())  # Should show the updated mileage

my_student.add_grade(90)
my_student.add_grade(85)
print(my_student.get_average())  # Should show the average of grades
```

- **Discussion Questions:**
  - What happens when you call the `read()` method on the `Book` instance?
  - How does the `drive()` method affect the `Car` instance?
  - What is the output of the `get_average()` method for the `Student` instance?
Certainly! Here’s the continuation of the PRIMM activity instructions starting from Step 4: Modify.

### Step 4: Modify

- **Task:** Students will modify the classes to add new features or change existing ones. Here are some suggestions for modifications:

  - **Book Class:** Add a method to check if the book is a bestseller.
  - **Car Class:** Add a method to reset the mileage.
  - **Student Class:** Add a method to display all grades.

- **Example Modifications:**

```python
# Book Class Modification
def is_bestseller(self):
    return self.pages > 300  # Example condition for a bestseller

# Car Class Modification
def reset_mileage(self):
    self.mileage = 0  # Resets the mileage to zero

# Student Class Modification
def display_grades(self):
    return f"{self.name}'s grades: {', '.join(map(str, self.grades))}"
```

- **Instructions for Students:**
  - Implement the suggested modifications in your existing class definitions.
  - Test the new methods by creating instances of each class and calling the new methods to see if they work as expected.

- **Example Usage of Modified Methods:**

```python
# Testing the modified Book class
my_book.is_bestseller = is_bestseller
print(f"Is '{my_book.title}' a bestseller? {my_book.is_bestseller()}")

# Testing the modified Car class
my_car.reset_mileage()
print(my_car.get_info())  # Should show mileage reset to 0

# Testing the modified Student class
my_student.display_grades = display_grades
print(my_student.display_grades())  # Should show the grades list
```

### Step 5: Make

- **Task:** Students will create a small project that utilizes the classes they have worked on. They can choose a theme or scenario that interests them, such as a library system, a car dealership, or a school management system.

- **Instructions for Students:**
  - Choose a theme for your project that incorporates the `Book`, `Car`, and `Student` classes.
  - Create instances of each class and demonstrate how they interact with each other.
  - Use the methods you have created and modified to showcase the functionality of your classes.
  - Prepare a short presentation or a report explaining your project, the classes you used, and how they work together.

- **Example Project Ideas:**
  - **Library System:** Create a system where students can borrow books. Use the `Book` class to represent books and the `Student` class to represent students who borrow them.
  - **Car Dealership:** Simulate a car dealership where customers can view cars and their details. Use the `Car` class to represent the cars available for sale.
  - **School Management System:** Create a simple system to manage students and their grades. Use the `Student` class to track student information and grades.
---
