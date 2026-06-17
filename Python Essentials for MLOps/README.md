# Python Essentials for MLOps

## Key Points

*	Lists store ordered, mutable items
+	Dictionaries map unique keys to values
-	Sets contain only unique elements
-	Lists index starting at 0 and preserve order when appending items
-	Dictionaries map keys to values for efficient lookup time
-	Tuples act like immutable lists useful when data shouldn't change
-	Sets only allow unique elements, automatically removing duplicates
-	**Append** - Adds an item to the end of a list
-	**Insert** - Inserts an item at a specified index in a list
-	**Extend** - Appends all items from one list onto another
-	**Pop** - Removes and returns an item at a specified index
-	**Get** - Safely gets a dictionary value falling back to a default
-	Append new elements to the end of lists with .append()
- Insert items at any index by passing index to .insert()
-	Combine lists while avoiding nested sub-lists using .extend()
-	Retrieve dicts safely with .get() and default values
-	**Function:** A reusable block of code that performs a specific task. Defined using the def keyword.
-	**Arguments:** Values passed into a function when calling it. Allows customizing behavior.
*	**Variable Arguments:** Allows passing an arbitrary number of arguments to a function.
* **Keyword Arguments:** Arguments passed by name rather than position. Can have default values.

## Using IPython

Very similar to Jupyter, but run from terminal:
  - IPython predates Jupyter
  - Both Jupyter and IPython accept <ins>!ls -l</ins> format to execute shell commands.

## Colab Notebook Key Features

-	Can enable both TPU and GPU runtimes
*	Can upload regular Jupyter Notebooks into colab
*	Can have a Google Drive Full of Colab Notebooks
*	Can sync colab notebooks to Github. Here is an example of a [gist of this notebook](https://gist.github.com/noahgift/c69200e05c057cf239fc7ea0be62e043)
*	Can connect to a [local runtime](https://research.google.com/colaboratory/local-runtimes.html)
*	Can create forms in [Colab](https://colab.research.google.com/notebooks/forms.ipynb)











## Key Points

*	**Class:** Blueprint for creating objects. Defines attributes and methods.
* **Instance:** Object that is created from a class. Has access to class attributes and methods.
*	**Method:** Function that belongs to a class. Accessed via instance or class name.
*	**Constructor:** Special method that runs when an instance is created. Used to initialize attributes.
*	**Inheritance:** Creating a child class from parent class. Child inherits attributes and methods.


## Example

```
class Vehicle:
    wheels = 4 # Class attribute
    
    def __init__(self, make, model):
        self.make = make # Instance attribute
        self.model = model
        
    def description(self): # Method
        return f"The {self.make} {self.model}"

car = Vehicle("BMW", "i3") # Instance created
print(car.wheels) # Access class attribute
print(car.description()) # Call instance method
```
**Output**
> 4

> The BMW i3

## Example

```
class Pet:
    def eat(self):
        print("Chomp")
        
class Dog(Pet):
    def bark(self):
        print("Bark!")
        
dog = Dog()
dog.eat() # Inherited method
dog.bark() # Dog specific method
```

**Output**
> Chomp

Bark!


