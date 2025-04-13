Certainly! Here’s the revised four-day lesson plan focused on teaching Python classes using the PRIMM model, including an activity to help students understand the `self` keyword.

### Four-Day Lesson Plan: Introduction to Python Classes Using PRIMM

**Grade Level:** 11th and 12th Grade  
**Duration:** 4 class periods (90 minutes each)  
**Objective:** Students will learn the concept of classes in Python, how to create and use them, and apply this knowledge to build a simple program.

---

#### Day 1: Introduction to Classes and the `self` Keyword

**1. Introduction to Classes (15 minutes)**
   - Explain what a class is in Python and its importance in object-oriented programming (OOP).
   - Discuss real-world analogies (e.g., a blueprint for a house).

**2. Predict (15 minutes)**
   - Present a simple class definition without implementation. Ask students to predict what the code will do.

   ```python
   class Dog:
       def __init__(self, name):
           self.name = name
   ```

   **Discussion Questions:**
   - What do you think this class represents?
   - What attributes or methods might a `Dog` class have?

**3. Run (15 minutes)**
   - Have students run a code snippet that creates an instance of the `Dog` class and prints its name.

   ```python
   my_dog = Dog("Buddy")
   print(my_dog.name)
   ```

**4. Investigate the `self` Keyword (30 minutes)**
   - **Activity:** In pairs, students will explore the purpose of the `self` keyword by modifying the `Dog` class to include a method that returns the dog's name. They will create a second instance of the `Dog` class to see how `self` differentiates between instances.

   ```python
   class Dog:
       def __init__(self, name):
           self.name = name

       def get_name(self):
           return self.name
   ```

   - Students will create two instances of the `Dog` class and call the `get_name` method on both.

   ```python
   dog1 = Dog("Buddy")
   dog2 = Dog("Max")

   print(dog1.get_name())  # Should print "Buddy"
   print(dog2.get_name())  # Should print "Max"
   ```

   **Discussion Questions:**
   - How does `self` help differentiate between the attributes of different instances?
   - What would happen if we didn’t use `self` in the method?

**5. Modify (15 minutes)**
   - Students will modify the `Dog` class to include additional attributes (e.g., age) and methods (e.g., a method to bark).

---

#### Day 2: Working with Multiple Classes

**1. Review (15 minutes)**
   - Recap the previous lesson and discuss what students learned about classes, methods, and the `self` keyword.

**2. Predict (15 minutes)**
   - Present a code snippet that defines a `Person` class and a `Dog` class. Ask students to predict how these classes might interact.

   ```python
   class Person:
       def __init__(self, name):
           self.name = name
   ```

**3. Run (15 minutes)**
   - Have students run a code snippet that creates instances of both classes.

   ```python
   my_person = Person("Alice")
   my_dog = Dog("Buddy")
   ```

**4. Investigate (30 minutes)**
   - In pairs, students will investigate how to create a relationship between the `Person` and `Dog` classes, such as having a person own a dog.

   ```python
   class Person:
       def __init__(self, name):
           self.name = name
           self.dog = None

       def adopt_dog(self, dog):
           self.dog = dog
   ```

**5. Modify (15 minutes)**
   - Students will modify the `Person` class to include a method that displays the person’s dog’s name.

   ```python
   def show_dog(self):
       if self.dog:
           return f"{self.name} has a dog named {self.dog.name}."
       else:
           return f"{self.name} has no dog."
   ```

---

#### Day 3: Inheritance and Polymorphism

**1. Review (15 minutes)**
   - Discuss the concepts of inheritance and polymorphism in OOP.

**2. Predict (15 minutes)**
   - Present a code snippet that defines a subclass of `Dog`, such as `ServiceDog`. Ask students to predict how this subclass might differ from the base class.

Certainly! Here’s the continuation of the lesson plan starting from Day 3, focusing on inheritance and polymorphism in Python classes.

### Day 3: Inheritance and Polymorphism

**1. Review (15 minutes)**
   - Discuss the concepts of inheritance and polymorphism in object-oriented programming (OOP).
   - Explain how subclasses can inherit attributes and methods from parent classes.

**2. Predict (15 minutes)**
   - Present a code snippet that defines a subclass of `Dog`, such as `ServiceDog`. Ask students to predict how this subclass might differ from the base class.

   ```python
   class ServiceDog(Dog):
       def __init__(self, name, service_type):
           super().__init__(name)
           self.service_type = service_type
   ```

   **Discussion Questions:**
   - What additional attributes or methods do you think a `ServiceDog` might have?
   - How does the `super()` function work in this context?

**3. Run (15 minutes)**
   - Have students run a code snippet that creates an instance of the `ServiceDog` class and prints its name and service type.

   ```python
   my_service_dog = ServiceDog("Max", "Guide")
   print(f"{my_service_dog.name} is a {my_service_dog.service_type} dog.")
   ```

**4. Investigate (30 minutes)**
   - In pairs, students will investigate how to override methods in the `ServiceDog` class to provide specific behavior, such as a specialized bark method.

   ```python
   class ServiceDog(Dog):
       def __init__(self, name, service_type):
           super().__init__(name)
           self.service_type = service_type

       def bark(self):
           return f"{self.name} the {self.service_type} dog says Woof!"
   ```

   - Students will create an instance of `ServiceDog` and call the `bark` method.

**5. Modify (15 minutes)**
   - Students will modify the `ServiceDog` class to include additional methods or attributes, such as a method that describes the service the dog provides.

   ```python
   def describe_service(self):
       return f"{self.name} is trained to assist as a {self.service_type}."
   ```

---

### Day 4: Applying Knowledge and Project Work

**1. Review (15 minutes)**
   - Recap the concepts of classes, inheritance, and polymorphism. Discuss any questions students may have.

**2. Predict (15 minutes)**
   - Present a scenario where students need to create a new class, such as `Cat`, that inherits from a base class `Animal`. Ask students to predict what attributes and methods might be included.

   ```python
   class Animal:
       def __init__(self, name):
           self.name = name
   ```

**3. Run (15 minutes)**
   - Have students run a code snippet that creates an instance of the `Animal` class and prints its name.

   ```python
   my_animal = Animal("Leo")
   print(my_animal.name)
   ```

**4. Investigate (30 minutes)**
   - In pairs, students will create a `Cat` class that inherits from `Animal` and includes specific attributes and methods, such as `meow`.

   ```python
   class Cat(Animal):
       def meow(self):
           return f"{self.name} says Meow!"
   ```

   - Students will create an instance of `Cat` and call the `meow` method.

**5. Project Work (15 minutes)**
   - Introduce a mini-project where students will create their own classes based on a theme of their choice (e.g., vehicles, characters, etc.). They should include attributes, methods, and demonstrate inheritance if applicable.
   - Allow students to work in pairs or small groups to brainstorm and start coding their projects.

---

### Assessment and Wrap-Up
- At the end of the four days, consider assessing students through a quiz on class concepts, or have them present their mini-projects to the class.
- Encourage students to reflect on what they learned about classes, the `self` keyword, inheritance, and polymorphism.
---

## Part Two / Python Classes LP

Yes, I understand what station rotations are! They involve setting up different stations around the classroom, each focusing on a specific topic or activity. Students rotate through these stations, allowing them to engage with various aspects of the lesson in a hands-on and collaborative manner.

Here’s a revised four-day lesson plan for teaching Python classes that incorporates more opportunities for research and includes station rotation activities.

### Four-Day Lesson Plan: Introduction to Python Classes Using PRIMM

**Grade Level:** 11th and 12th Grade  
**Duration:** 4 class periods (90 minutes each)  
**Objective:** Students will learn the concept of classes in Python, how to create and use them, and apply this knowledge to build a simple program.

---

#### Day 1: Introduction to Classes and the `self` Keyword

**1. Introduction to Classes (15 minutes)**
   - Explain what a class is in Python and its importance in object-oriented programming (OOP).
   - Discuss real-world analogies (e.g., a blueprint for a house).

**2. Station Rotation Activity (60 minutes)**
   - Set up three stations, each focusing on a different aspect of classes in Python. Students will rotate through each station in pairs.

   **Station 1: Class Basics**
   - Research the basic structure of a class in Python. Students will read a short article or watch a video and summarize the key points.
   - **Output:** Create a simple class definition (e.g., `Dog`) and share it with the class.

   **Station 2: The `self` Keyword**
   - Research the purpose of the `self` keyword in Python classes. Students will find examples of how `self` is used in methods.
   - **Output:** Write a method that uses `self` to access an instance variable and share it with the class.

   **Station 3: Attributes and Methods**
   - Research the difference between attributes and methods in a class. Students will look for examples of each.
   - **Output:** Create a class with at least one attribute and one method, and present it to the class.

**3. Class Discussion (15 minutes)**
   - Have students share their findings from each station. Discuss the importance of the `self` keyword and the roles of attributes and methods.

---

#### Day 2: Working with Multiple Classes

**1. Review (15 minutes)**
   - Recap the previous lesson and discuss what students learned about classes, methods, and the `self` keyword.

**2. Station Rotation Activity (60 minutes)**
   - Set up three new stations focusing on relationships between classes and object-oriented principles.

   **Station 1: Class Relationships**
   - Research how classes can interact with each other (e.g., composition and aggregation).
   - **Output:** Create a simple example of two classes that interact (e.g., `Person` and `Dog`).

   **Station 2: Inheritance**
   - Research the concept of inheritance in Python. Students will find examples of how inheritance is used in real-world applications.
   - **Output:** Create a subclass (e.g., `ServiceDog` inheriting from `Dog`) and explain the relationship.

   **Station 3: Polymorphism**
   - Research polymorphism and how it allows methods to be used in different ways across different classes.
   - **Output:** Write a method that demonstrates polymorphism (e.g., a `speak` method in both `Dog` and `Cat` classes).

**3. Class Discussion (15 minutes)**
   - Have students present their work from each station. Discuss the importance of class relationships, inheritance, and polymorphism in OOP.

---

#### Day 3: Advanced Class Concepts

**1. Review (15 minutes)**
   - Discuss the concepts of inheritance and polymorphism in object-oriented programming (OOP).

**2. Station Rotation Activity (60 minutes)**
   - Set up three stations focusing on advanced class concepts.

   **Station 1: Class Methods and Static Methods**
   - Research the difference between class methods, static methods, and instance methods.
   - **Output:** Create a class that includes both a class method and a static method, and explain their uses.

   **Station 2: Encapsulation**
   - Research the concept of encapsulation and how it is implemented in Python.
   - **Output:** Modify a class to include private attributes and provide getter/setter methods.

   **Station 3: Abstract Classes and Interfaces**
   - Research abstract classes and interfaces in Python. Discuss their purpose and how they differ from regular classes.
   - **Output:** Create an abstract class and a concrete class that implements it.

**3. Class Discussion (15 minutes)**
   - Have students share their findings and examples from each station. Discuss how these advanced concepts enhance the design of Python programs.

---

Certainly! Here’s the updated lesson plan starting from Day 3, focusing on advanced class concepts and incorporating station rotation activities for research and collaboration.

### Day 3: Advanced Class Concepts

**1. Review (15 minutes)**
   - Discuss the concepts of inheritance and polymorphism in object-oriented programming (OOP).
   - Recap the importance of class methods, static methods, encapsulation, and abstract classes.

**2. Station Rotation Activity (60 minutes)**
   - Set up three stations focusing on advanced class concepts. Students will rotate through each station in pairs.

   **Station 1: Class Methods and Static Methods**
   - **Research Task:** Students will research the difference between class methods, static methods, and instance methods. They should look for examples of each.
   - **Output:** Create a class that includes both a class method and a static method. For example:

   ```python
   class MathOperations:
       @classmethod
       def add(cls, a, b):
           return a + b

       @staticmethod
       def multiply(a, b):
           return a * b
   ```

   - Students will explain the purpose of each method type.

   **Station 2: Encapsulation**
   - **Research Task:** Students will research the concept of encapsulation and how it is implemented in Python. They should find examples of private attributes and getter/setter methods.
   - **Output:** Modify a class to include private attributes and provide getter/setter methods. For example:

   ```python
   class BankAccount:
       def __init__(self, balance):
           self.__balance = balance  # Private attribute

       def get_balance(self):
           return self.__balance

       def deposit(self, amount):
           self.__balance += amount
   ```

   - Students will discuss the benefits of encapsulation.

   **Station 3: Abstract Classes and Interfaces**
   - **Research Task:** Students will research abstract classes and interfaces in Python. They should discuss their purpose and how they differ from regular classes.
   - **Output:** Create an abstract class and a concrete class that implements it. For example:

   ```python
   from abc import ABC, abstractmethod

   class Animal(ABC):
       @abstractmethod
       def sound(self):
           pass

   class Dog(Animal):
       def sound(self):
           return "Woof!"
   ```

   - Students will explain how abstract classes enforce a contract for subclasses.

**3. Class Discussion (15 minutes)**
   - Have students share their findings and examples from each station. Discuss how these advanced concepts enhance the design of Python programs.

---

### Day 4: Applying Knowledge and Project Work

**1. Review (15 minutes)**
   - Recap the concepts learned over the week, including classes, inheritance, polymorphism, encapsulation, and abstract classes.

**2. Project Introduction (15 minutes)**
   - Introduce a mini-project where students will create their own classes based on a theme of their choice (e.g., vehicles, characters, or a simple game).
   - Explain that they should incorporate the concepts learned throughout the week, such as inheritance, encapsulation, and methods.

**3. Station Rotation Activity (45 minutes)**
   - Set up three stations to help students brainstorm and develop their projects.

   **Station 1: Brainstorming Ideas**
   - **Task:** Students will brainstorm project ideas and outline the classes they plan to create. They should consider how to use inheritance and encapsulation in their designs.
   - **Output:** Create a project outline that includes class names, attributes, and methods.

   **Station 2: Coding Assistance**
   - **Task:** Students will work on coding their classes. They can ask for help from peers or the teacher as needed.
   - **Output:** Write the initial code for their classes, focusing on implementing the core functionality.

   **Station 3: Testing and Debugging**
   - **Task:** Students will test their classes and methods, looking for any bugs or issues. They should also write test cases to ensure their methods work as expected.
   - **Output:** Create a simple test script that calls methods from their classes and checks for expected outputs.

**4. Project Presentations (15 minutes)**
   - Allow students to present their projects to the class. They should explain their class designs, how they implemented the concepts learned, and any challenges they faced.

---

### Assessment and Wrap-Up
- At the end of the four days, consider assessing students through a quiz on class concepts or evaluating their mini-projects based on creativity, implementation of concepts, and presentation.
- Encourage students to reflect on what they learned about classes, the `self` keyword, inheritance, encapsulation, and polymorphism.

