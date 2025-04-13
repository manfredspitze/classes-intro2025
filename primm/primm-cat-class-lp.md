Okay, here's the PRIMM lesson plan updated with examples and code snippets specifically focused on domestic cats:

## Lesson Plan: Exploring Python Classes with PRIMM - Focus on Cats!

**Objective:** Students will learn the fundamental concepts of Python classes and object-oriented programming through the Predict, Run, Investigate, Modify, and Make (PRIMM) model, using the domestic cat as a central theme.

**Materials:** Computer with Python interpreter, internet access (optional for documentation).

**Duration:** 2-3 class periods (depending on student pace and complexity of the "Make" stage).

**Procedure:**

### Introduction (Brief Review - 10 minutes)

* Briefly review the concepts of functions, variables, and data types in Python.
* Introduce the idea of organizing code and data into reusable "objects" that model real-world entities. Explain that classes are blueprints for creating these objects, and today we'll focus on our feline friends!

### PRIMM Activities

#### Step 1: Predict (15 minutes)

* **Task:** Before running any code, students will examine the provided class definition for a `Cat` and predict its behavior based on the attributes and methods.
* **Provide the following code snippet:**

```python
# Class Example: Cat
class Cat:
    def __init__(self, name, breed, age):
        self.name = name
        self.breed = breed
        self.age = age
        self.is_sleeping = False

    def meow(self):
        return "Meow!"

    def sleep(self):
        self.is_sleeping = True
        return f"{self.name} is now sleeping."

    def wake_up(self):
        self.is_sleeping = False
        return f"{self.name} woke up!"
```

* **Guiding Questions for Students:**
    * What information (attributes) do you think a `Cat` object will store?
    * What actions (methods) can a `Cat` object perform? What do you think these methods will do?
    * What do you think the initial value of `is_sleeping` will be when a new `Cat` is created?
    * Based on the method names, what kind of output do you expect from `meow()`, `sleep()`, and `wake_up()`?

#### Step 2: Run (15 minutes)

* **Task:** Provide students with the following starter code that creates instances of the `Cat` class and calls its methods. Students will run this code to observe the output.

```python
# Running the Cat class
my_cat = Cat("Whiskers", "Siamese", 5)
print(f"{my_cat.name} says: {my_cat.meow()}")
print(my_cat.sleep())
print(f"Is {my_cat.name} sleeping? {my_cat.is_sleeping}")
print(my_cat.wake_up())
print(f"Is {my_cat.name} sleeping now? {my_cat.is_sleeping}")

print("-" * 20)

another_cat = Cat("Patches", "Calico", 2)
print(f"{another_cat.name} is a {another_cat.breed} who is {another_cat.age} years old.")
```

* **Instructions for Students:**
    * Copy and paste this code into a Python interpreter or a Python script and run it.
    * Observe the output carefully. Does the output match your predictions from the previous step? Note any discrepancies.

#### Step 3: Investigate (30 minutes)

* **Task:** Students will now investigate how the `Cat` class works by creating their own instances, accessing attributes directly, and experimenting with the methods.

```python
# Investigation with Cat
yet_another_cat = Cat("Shadow", "Bombay", 7)
print(f"This cat's breed: {yet_another_cat.breed}")
yet_another_cat.is_sleeping = True # Directly changing an attribute
print(f"Is {yet_another_cat.name} sleeping? {yet_another_cat.is_sleeping}")
print(yet_another_cat.meow()) # Even sleeping cats can meow!

print("-" * 20)

young_cat = Cat("Kitten", "Tabby", 0.5) # Age in years
print(f"{young_cat.name} is {young_cat.age} years old.")
```

* **Guiding Questions and Tasks for Students:**
    * Create a fourth `Cat` object with a different name, breed, and age. Print its name and make it meow.
    * What happens if you try to access an attribute that wasn't defined in the `__init__` method (e.g., `my_cat.favorite_toy = "mouse"`)? (Lead them to understand dynamic attribute assignment).
    * Can you make a cat wake up even if it wasn't sleeping? What happens when you call `wake_up()` on a cat where `is_sleeping` is already `False`?
    * Add a new attribute to the `Cat` class called `color` in the `__init__` method. How would you then create a `Cat` object with a specific color and print that color? (Guide them to modify the `__init__` and create new instances).
    * Write code to change the age of an existing `Cat` object and then print its updated age.

#### Step 4: Modify (45 minutes)

* **Task:** Students will now modify the `Cat` class by adding new attributes and methods to extend its functionality.
* **Modification Challenges for Students:**
    * Add a `weight_kg` attribute to the `Cat` class (in the `__init__` method).
    * Add a new method called `purr()` that returns a string like "{cat\_name} is purring."
    * Add a new method called `eat(food)` that takes a `food` (string) as an argument and returns a message like "{cat\_name} is eating their {food}." This method could also potentially change the `is_sleeping` attribute (e.g., cats often get sleepy after eating!).

```python
# Modified Cat class (example - students will implement)
class Cat:
    def __init__(self, name, breed, age, weight_kg):
        self.name = name
        self.breed = breed
        self.age = age
        self.weight_kg = weight_kg
        self.is_sleeping = False

    def meow(self):
        return "Meow!"

    def sleep(self):
        self.is_sleeping = True
        return f"{self.name} is now sleeping."

    def wake_up(self):
        self.is_sleeping = False
        return f"{self.name} woke up!"

    def purr(self):
        return f"{self.name} is purring."

    def eat(self, food):
        self.is_sleeping = True # Cats often nap after eating
        return f"{self.name} is eating their {food} and is now feeling sleepy."

    def describe(self): # Optional: Modify describe to include weight
        return f"{self.name} is a {self.breed}, {self.age} years old, and weighs {self.weight_kg} kg."

# Example usage of modified class
my_fluffy_cat = Cat("Fluffy", "Persian", 8, 4.5)
print(my_fluffy_cat.purr())
print(my_fluffy_cat.eat("salmon"))
print(f"Is {my_fluffy_cat.name} sleeping? {my_fluffy_cat.is_sleeping}")
```

* **Instructions for Students:**
    * Implement the modifications described above for the `Cat` class.
    * Test your changes by creating new instances of the modified `Cat` class and calling the new methods and accessing the new attributes.

#### Step 5: Make (Remaining Time - 45-60 minutes)

* **Task:** Students will now apply their understanding of Python classes to create their own class that models a different aspect of the domestic cat or a related concept.
* **Instructions for Students:**
    * Choose a new aspect related to cats (e.g., a `LitterBox`, a `CatToy`, a `CatShelter`, a `CatOwner`).
    * Define a new Python class for your chosen object.
    * Give your class a descriptive name (e.g., `LitterBox`).
    * Include at least two relevant attributes in the `__init__` method (e.g., for `LitterBox`: `is_clean`, `last_cleaned`).
    * Implement at least one meaningful method that operates on the attributes of your class (e.g., for `LitterBox`: `scoop()`).Assume the role of high school computer programming teacher.  You will help me with tasks such as unit and daily lesson planning, creating course content, writing code, debugging code, and understanding the code I use in class.

When writing code and providing sample code, please relate your suggestions and responses to all the previous sections of the conversation I am having with you.

When providing code solutions, give me a clear, succinct overview of what the code will do and how it will work.  Present the code in a format that's easy to copy and paste, and explain your reasoning and any variables or parameters that could be adjusted in the code.  Clearly explain how to use the code within a larger coding project.
    * Demonstrate the creation of at least two instances of your class and show how to use its method(s) and access its attributes.
    * Provide a brief explanation (comments in the code or a short paragraph) of what your class represents, its attributes, and what its method does.

* **Possible Student Projects (Encourage creativity!):**
    * `LitterBox` class with attributes like `is_clean` (Boolean), `last_cleaned` (string or date) and methods like `scoop()`, `needs_cleaning()`.
    * `CatToy` class with attributes like `name`, `material` and methods like `play_with()`.
    * `CatShelter` class with attributes like `capacity`, `current_occupants` (list of `Cat` objects) and methods like `admit_cat(cat)`, `adopt_cat(cat_name)`.
    * `CatOwner` class with attributes like `name`, `owned_cats` (list of `Cat` objects) and methods like `feed_cats()`, `play_with_cats()`.

### Conclusion (10 minutes)

* Have students briefly share the classes they created in the "Make" stage, perhaps even describing how their cats might interact with these new objects.
* Discuss how classes help model complex systems by breaking them down into interacting objects.
* Briefly reiterate the core concepts of classes, attributes, and methods.

### Assessment

* Observe student participation and engagement during each stage of the PRIMM activity.
* Evaluate the code produced during the "Modify" and "Make" stages based on correctness, functionality, and adherence to the requirements.
* Collect the code files from the "Make" stage for a more formal assessment.

This updated lesson plan uses the engaging theme of domestic cats to illustrate the concepts of Python classes within the PRIMM framework, providing concrete examples and encouraging students to build upon their understanding in a relatable context.
