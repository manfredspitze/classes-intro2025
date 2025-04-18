Four-day lesson plan on Python classes based on the PRIMM (Predict, Run, Investigate, Modify, Make) model:

---

### **Unit Name**
Python Classes: Building Blocks of Object-Oriented Programming

### **Unit Objective(s)**
- Students will understand the structure and purpose of Python classes and their components: methods, attributes, the `self` keyword, and instances.
- Students will apply these concepts to create and interact with their own Python classes.

---

### **Day 1: Introduction to Python Classes & Attributes**
**Time Allocation**  
- Introduction (10 min)  
- Predict & Run Activities (30 min)  
- Investigate (20 min)  
- Modify (20 min)  
- Wrap-Up Discussion (10 min)

**Focus Concept:** Attributes  
**Activities:**  
1. **Predict & Run:** Introduce a simple class and its attributes:  

```python
class Car:
    brand = "Toyota"
    color = "red"
```  

- Predict: Ask students to guess what `Car.brand` and `Car.color` will output when printed.  
- Run: Execute the code and verify predictions.  

**Example 2:** Demonstrate assigning attributes through the constructor method `__init__`.  

```python
class Dog:
    def __init__(self, name, breed):
        self.name = name
        self.breed = breed
```  

**Discussion Questions**  
1. *What are attributes in a class?*  
   - **Answer:** Attributes store data about an object and define its properties.  
2. *How can we initialize attributes in a class?*  
   - **Answer:** Using the `__init__` method.  

**Mastery Check 1:**  
- Quiz: *What is the difference between class-level attributes and instance attributes?*  
- Application: Write a class `Book` with attributes `title`, `author`, and `year_published`.

---

### **Day 2: Methods**
**Time Allocation**  
- Review (10 min)  
- Predict & Run Activities (30 min)  
- Investigate (25 min)  
- Modify (15 min)  
- Wrap-Up Discussion (10 min)

**Focus Concept:** Methods  
**Activities:**  
1. **Example 1:** Define and run a method in a class:  

```python
class Calculator:
    def add(self, a, b):
        return a + b
```  

2. **Example 2:** Introduce class-level methods using `@classmethod`.  

```python
class MathTools:
    @classmethod
    def multiply(cls, x, y):
        return x * y
```  

**Discussion Questions**  
1. *What is the difference between instance methods and class methods?*  
   - **Answer:** Instance methods operate on specific objects; class methods operate on the class as a whole.  
2. *Why do we use the `self` keyword in methods?*  
   - **Answer:** To refer to the specific instance of the class.  

**Mastery Check 2:**  
- Quiz: Apply your understanding by writing a method to calculate the area of a rectangle.  
- Application: Modify the `Calculator` class to include a `subtract` method.

---

### **Day 3: The Keyword `self` & Instances**
**Time Allocation**  
- Review (10 min)  
- Predict & Run Activities (30 min)  
- Investigate (25 min)  
- Modify (15 min)  
- Wrap-Up Discussion (10 min)

**Focus Concepts:** `self`, Instances  
**Activities:**  
1. **Example 1:** Demonstrate the use of `self` to differentiate between instance attributes:  

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```  

2. **Example 2:** Create multiple instances of a class and access their attributes.  

```python
person1 = Person("Alice", 25)
person2 = Person("Bob", 30)
```  

**Discussion Questions**  
1. *Why is the keyword `self` important?*  
   - **Answer:** It allows methods to refer to the instance they are being called on.  
2. *How do we create instances of a class?*  
   - **Answer:** By calling the class as if it were a function (e.g., `Person("Alice", 25)`).  

**Mastery Check:**  
- Quiz: Create an instance of a class `Animal` and set attributes `species` and `habitat`.  
- Application: Write a class `Student` and create three instances with different names and grades.

---

### **Day 4: Putting It All Together**
**Time Allocation**  
- Review (15 min)  
- Make Activity (50 min)  
- Mastery Check (20 min)  
- Wrap-Up (5 min)

**Focus Concept:** Integrating Classes, Methods, Attributes, `self`, and Instances  

**Activities:**  
1. **Make:** Task students with designing a class `BankAccount` with the following:  
   - Attributes: `account_holder`, `balance`  
   - Methods: `deposit(amount)`, `withdraw(amount)`, `get_balance()`  

2. Students will create and test instances of their class.  

**Discussion Questions**  
1. *How do all the components of a class work together?*  
   - **Answer:** Attributes store data, methods define behavior, `self` links methods/attributes to instances, and instances represent specific objects.  

**Final Mastery Check:**  
- Quiz: Explain the purpose of the `__init__` method and the `self` keyword.  
- Application: Extend the `BankAccount` class to include a method for transferring money between two accounts.

---

