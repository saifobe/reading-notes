# Classes and Objects
Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. Classes are essentially a template to create your objects.

Ex) 
```
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class")
```

You can create multiple different objects that are of the same class(have the same variables and functions defined). However, each object contains independent copies of the variables defined in the class. For instance, if we were to define another object with the "MyClass" class and then change the string in the variable above:

Ex) 
```
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

myobjectx = MyClass()
myobjecty = MyClass()

myobjecty.variable = "yackity"

# Then print out both values
print(myobjectx.variable)
print(myobjecty.variable)
```
## init()
The __init__() function, is a special function that is called when the class is being initiated. It's used for assigning values in a class.

Ex)
```
class NumberHolder:

   def __init__(self, number):
       self.number = number

   def returnNumber(self):
       return self.number

var = NumberHolder(7)
print(var.returnNumber()) #Prints '7'

```

# Thinking Recursively in Python
Thinking recursively means breaking a problem down into smaller, more manageable sub-problems, and solving each sub-problem using the same approach until the solution is found. In Python, we can implement recursive solutions using functions that call themselves.

## Recursive Functions in Python
Recursive functions are functions that call themselves in order to solve a problem. They are useful when the problem can be broken down into smaller, similar sub-problems.

Ex)
```
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)

```
## Maintaining State
When dealing with recursive functions, keep in mind that each recursive call has its own execution context, so to maintain state during recursion you have to either:

- Thread the state through each recursive call so that the current state is part of the current call’s execution context
- Keep the state in global scope

## Recursive Data Structures in Python
A data structure is recursive if it can be deﬁned in terms of a smaller version of itself. A list is an example of a recursive data structure. Let me demonstrate. Assume that you have only an empty list at your disposal, and the only operation you can perform on it is this:

```
# Return a new list that is the result of
# adding element to the head (i.e. front) of input_list
def attach_head(element, input_list):
    return [element] + input_list
```

# Python Testing with pytest: Fixtures and Coverage
pytest is a popular testing framework for Python that makes it easy to write and run tests. pytest provides a lot of features that make testing easier, such as fixtures and coverage.

Fixtures are functions that provide data to tests. They are used to set up the test environment, provide data for tests to use, and clean up after the tests are run. Fixtures are defined using the @pytest.fixture decorator.

## About fixtures
In testing, a fixture provides a defined, reliable and consistent context for the tests. This could include environment (for example a database configured with known parameters) or content (such as a dataset).

Fixtures define the steps and data that constitute the arrange phase of a test (see Anatomy of a test). In pytest, they are functions you define that serve this purpose. They can also be used to define a test’s act phase; this is a powerful technique for designing more complex tests.

## Questions

### 1- What are the key differences between classes and objects in Python, and how are they used to create and manage instances of a class?
- A class is a blueprint for creating objects, while an object is an instance of a class.
- A class is defined using the class keyword, while an object is created using the name of the class followed by parentheses.
- A class is used to create objects, which are used to access the attributes and methods of the class.

### 2- Explain the concept of recursion and provide an example of how it can be used to solve a problem in Python. What are some best practices to follow when implementing a recursive function?
- Recursion is a programming technique where a function calls itself to solve a problem by dividing it into smaller subproblems of the same type.
- A recursive function should always include a base case, make sure that the recursion eventually reaches the base case, and use clear and descriptive variable names.
- Recursion should be used only when necessary and when it simplifies the solution to a problem.

### What is the purpose of pytest fixtures and code coverage in testing Python code? Explain how they can be used together to improve the quality and maintainability of a project?

- Pytest fixtures provide a way to set up and tear down objects or resources that are required for testing, while code coverage measures how much of the code has been executed during testing.
- Using fixtures and code coverage together can improve the quality and maintainability of a project by isolating the code being tested, identifying untested parts of the code, and making it easier to refactor and modify the code while ensuring that the tests provide adequate coverage.

## Things I want to know more about
- Pytest Fixtures

