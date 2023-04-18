# List Comprehensions

## List comprehension is a powerful and concise method for creating lists in Python that becomes essential the more you work with lists, and lists of lists.

[click here  to read](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)

### ***What is the basic syntax of Python list comprehension, and how does it differ from using a for loop to create a list? Provide an example of a list comprehension that squares the elements in a given list of integers.***



The basic syntax of Python list comprehension is as follows:

```python
new_list = [expression for item in iterable if condition]

```

List comprehension differs from using a for loop to create a list in that it allows for a more concise and readable syntax. The same result can be achieved using a for loop, but the code is typically longer and more difficult to read.

Here's an example of a list comprehension that squares the elements in a given list of integers:

```python
original_list = [1, 2, 3, 4, 5]
squared_list = [num ** 2 for num in original_list]

print(squared_list)
# Output: [1, 4, 9, 16, 25]
```
This creates a new list squared_list by applying the expression num ** 2 to each element num in the original list [1, 2, 3, 4, 5].

-----------------------------------------------------
# Primer on Decorators

### ***What is a decorator in Python?***
[click here to read](https://realpython.com/primer-on-python-decorators/)

A decorator in Python is a special type of function that can modify the behavior of another function or class. In other words, a decorator can add new functionality to an existing function or class without modifying its source code. Decorators are a powerful feature of Python that allow developers to write reusable code that can be applied to different functions or classes.

A decorator is defined using the @ symbol followed by the name of the decorator function. When a decorator is applied to a function or class, the decorator function is called with the function or class as its argument. The decorator function can modify the function or class in any way it wants, and then return the modified function or class.


----------

# Primer on Decorators

### ***What is a decorator in Python?***
[click here to read](https://realpython.com/primer-on-python-decorators/)

### ***Explain the concept of decorators in Python. How do they work, and what are some common use cases for them? Provide an example of a simple decorator function from the reading.***

Decorators in Python are a way to modify or extend the behavior of a function or class without modifying its source code. They work by wrapping the original function or class with another function that adds new functionality. The decorator function takes the original function as its input and returns a new function that can add new functionality or modify the behavior of the original function.

The syntax for applying a decorator to a function in Python is to place the decorator function above the function definition, and precede it with the @ symbol. When the function is called, it is actually calling the wrapper function that was created by the decorator function.

Common use cases for decorators in Python include logging, timing, authentication, caching, and error handling. Decorators can also be used to add functionality to classes and methods, as well as to create context managers.

ex:
```python
import time

def timing_decorator(func):
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = func(*args, **kwargs)
        end_time = time.time()
        print(f"{func.__name__} took {end_time - start_time} seconds to execute")
        return result
    return wrapper

@timing_decorator
def my_function():
    # do something time-consuming
    time.sleep(2)

my_function()
```

-----
## Things I want to know more about:
