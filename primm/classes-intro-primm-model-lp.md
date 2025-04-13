Okay, here is an updated lesson plan incorporating code snippets for each stage of the PRIMM model, designed to guide students in learning about Python classes:

## Lesson Plan: Exploring Python Classes with PRIMM

**Objective:** Students will learn the fundamental concepts of Python classes and object-oriented programming through the Predict, Run, Investigate, Modify, and Make (PRIMM) model.

**Materials:** Computer with Python interpreter, internet access (optional for documentation).

**Duration:** 2-3 class periods (depending on student pace and complexity of the "Make" stage).

**Procedure:**

### Introduction (Brief Review - 10 minutes)

* Briefly review the concepts of functions, variables, and data types in Python.
* Introduce the idea of organizing code and data into reusable "objects" that model real-world entities. Explain that classes are blueprints for creating these objects.

### PRIMM Activities

#### Step 1: Predict (15 minutes)

* **Task:** Before running any code, students will examine the provided class definitions and predict their behavior based on the attributes and methods.
* **Provide the following code snippets (one at a time or all together):**

```python
# Class Example 1: Dog
class Dog:
    def __init__(self, name, breed):
        self.name = name
        self.breed = breed
        self.is_hungry = True

    def bark(self):
        return "Woof!"

    def eat(self):
        self.is_hungry = False
        return f"{self.name} is now full."

# Class Example 2: Circle
class Circle:
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14159 * self.radius ** 2

    def describe(self):
        return f"This is a circle with a radius of {self.radius}."
```

* **Guiding Questions for Students:**
    * For the `Dog` class:
        * What information (attributes) do you think a `Dog` object will store?
        * What actions (methods) can a `Dog` object perform? What do you think these methods will do?
        * What do you think the initial value of `is_hungry` will be when a new `Dog` is created?
    * For the `Circle` class:
        * What information does a `Circle` object store?
        * What calculations do you think the `area()` method will perform?
        * What kind of string do you expect the `describe()` method to return?

#### Step 2: Run (15 minutes)

* **Task:** Provide students with the following starter code that creates instances of the `Dog` and `Circle` classes and calls their methods. Students will run this code to observe the output.

```python
# Running the Dog class
my_dog = Dog("Buddy", "Golden Retriever")
print(f"{my_dog.name} says: {my_dog.bark()}")
print(f"Is {my_dog.name} hungry? {my_dog.is_hungry}")
print(my_dog.eat())
print(f"Is {my_dog.name} hungry now? {my_dog.is_hungry}")

print("-" * 20)

# Running the Circle class
my_circle = Circle(5)
print(my_circle.describe())
print(f"The area of the circle is: {my_circle.area()}")
```

* **Instructions for Students:**
    * Copy and paste this code into a Python interpreter or a Python script and run it.
    * Observe the output carefully. Does the output match your predictions from the previous step? Note any discrepancies.

#### Step 3: Investigate (30 minutes)

* **Task:** Students will now investigate how the classes work by creating their own instances, accessing attributes directly, and experimenting with the methods.

```python
# Investigation with Dog
another_dog = Dog("Lucy", "Poodle")
print(f"Another dog's name: {another_dog.name}")
another_dog.is_hungry = False # Directly changing an attribute
print(f"Is {another_dog.name} hungry? {another_dog.is_hungry}")
print(another_dog.bark())

print("-" * 20)

# Investigation with Circle
small_circle = Circle(2)
large_circle = Circle(10)
print(f"Small circle radius: {small_circle.radius}, Area: {small_circle.area()}")
print(f"Large circle radius: {large_circle.radius}, Area: {large_circle.area()}")
```

* **Guiding Questions and Tasks for Students:**
    * **Dog:**
        * Create a third `Dog` object with a different name and breed. Print its name and make it bark.
        * What happens if you try to access an attribute that wasn't defined in the `__init__` method (e.g., `my_dog.owner = "You"`)? (Lead them to understand dynamic attribute assignment).
        * Can you make a dog hungry again after it has eaten? How would you do that? (Introduce the idea of adding a new method or directly modifying the attribute).
    * **Circle:**
        * Create a circle with a radius of 7. Calculate and print its area.
        * Add a new attribute to the `Circle` class called `color` in the `__init__` method. How would you then access and print the color of a `Circle` object? (Guide them to modify the `__init__` and create new instances).
        * Write code to change the radius of an existing `Circle` object and then recalculate its area.

#### Step 4: Modify (45 minutes)

* **Task:** Students will now modify the existing classes by adding new attributes and methods to extend their functionality.
* **Modification Challenges for Students:**
    * **Dog:**
        * Add an `age` attribute to the `Dog` class (in the `__init__` method). Modify the `describe()` method (or create a new `describe()` method) to include the dog's name, breed, and age.
        * Add a new method called `play(toy)` that takes a `toy` (string) as an argument and returns a message like "{dog\_name} is playing with their {toy}."
    * **Circle:**
        * Add a new attribute called `color` to the `Circle` class (in the `__init__`).
        * Add a new method called `circumference()` that calculates and returns the circumference of the circle ($2 \pi r$). You can use `math.pi` for a more accurate value.

```python
# Modified Dog class (example - students will implement)
class Dog:
    def __init__(self, name, breed, age):
        self.name = name
        self.breed = breed
        self.is_hungry = True
        self.age = age

    def bark(self):
        return "Woof!"

    def eat(self):
        self.is_hungry = False
        return f"{self.name} is now full."

    def describe(self):
        return f"{self.name} is a {self.breed} and is {self.age} years old."

    def play(self, toy):
        return f"{self.name} is playing with their {toy}."

# Modified Circle class (example - students will implement)
import math

class Circle:
    def __init__(self, radius, color):
        self.radius = radius
        self.color = color

    def area(self):
        return math.pi * self.radius ** 2

    def circumference(self):
        return 2 * math.pi * self.radius

    def describe(self):
        return f"This is a {self.color} circle with a radius of {self.radius}."

# Example usage of modified classes
my_new_dog = Dog("Max", "Labrador", 3)
print(my_new_dog.describe())
print(my_new_dog.play("ball"))

my_new_circle = Circle(8, "blue")
print(my_new_circle.describe())
print(f"The circumference is: {my_new_circle.circumference()}")
```

* **Instructions for Students:**
    * Implement the modifications described above for either the `Dog` or the `Circle` class (or both, if time allows).
    * Test your changes by creating new instances of the modified class and calling the new methods and accessing the new attributes.

#### Step 5: Make (Remaining Time - 45-60 minutes)

* **Task:** Students will now apply their understanding of Python classes to create their own class that models a different real-world object or concept of their choosing.
* **Instructions for Students:**
    * Choose a new real-world object or concept (different from `Dog` and `Circle`).
    * Define a new Python class for your chosen object.
    * Give your class a descriptive name.
    * Include at least two relevant attributes in the `__init__` method.
    * Implement at least one meaningful method that operates on the attributes of your class.
    * Demonstrate the creation of at least two instances of your class and show how to use its method(s) and access its attributes.
    * Provide a brief explanation (comments in the code or a short paragraph) of what your class represents, its attributes, and what its method does.

* **Possible Student Projects (Encourage creativity!):**
    * `Book` class with attributes like `title`, `author`, `pages` and methods like `read_page()`.
    * `Car` class with attributes like `make`, `model`, `speed` and methods like `accelerate()`, `brake()`.
    * `Student` class with attributes like `name`, `grades` and methods like `add_grade()`, `get_average()`.
    * `Rectangle` class with attributes like `length`, `width` and methods like `calculate_area()`, `calculate_perimeter()`.

### Conclusion (10 minutes)

* Have students briefly share the classes they created in the "Make" stage.
* Discuss the benefits of using classes to organize code and model real-world entities.
* Briefly introduce the concepts of inheritance and polymorphism (as a preview for future lessons).

### Assessment

* Observe student participation and engagement during each stage of the PRIMM activity.
* Evaluate the code produced during the "Modify" and "Make" stages based on correctness, functionality, and adherence to the requirements.
* Collect the code files from the "Make" stage for a more formal assessment.

---
