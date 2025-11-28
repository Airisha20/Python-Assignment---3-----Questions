# Python-Assignment---3-----Questions

Q1- Differentiate between method overriding and method overloading with an example.
A1- Method overloading refers to the ability to define multiple methods within the same class that share the same name but have different parameters. Method         overriding occurs in the context of inheritance, where a subclass provides its own specific implementation for a method that is already defined in its           superclass. The overridden method in the subclass must have the exact same name and signature (parameters) as the method in the superclass.

    1. Method overloading:
    class Calculator:
        def add(self, a, b=None, c=None):
            if c is not None:
                return a + b + c
            elif b is not None:
                return a + b
            else:
                return a
    
    calc = Calculator()
    print(calc.add(10))
    print(calc.add(10, 20))
    print(calc.add(10, 20, 30))

    2. Method overriding:
    class Animal:
    def speak(self):
        print("Animal makes a sound")

    class Dog(Animal):
        def speak(self):
            print("Woof!")
    
    class Cat(Animal):
        def speak(self):
            print("Meow!")
    
    animal = Animal()
    dog = Dog()
    cat = Cat()
    
    animal.speak()
    dog.speak()
    cat.speak()

Q2- Describe the role and types of constructors in Python with a suitable example.
A2- In Python, a constructor is a special method that is called automatically when an object is created from a class. Its main role is to initialize the          object by setting up its attributes or state. Constructors can be of two types:
    1. Default Constructor - A default constructor does not take any parameters other than self. It initializes the object with default attribute values.
    2. Parameterized Constructor - A parameterized constructor accepts arguments to initialize the object's attributes with specific values.
    
