# Dunder Methods

## Overall, learning about dunder methods is an important part of becoming a proficient Python developer and will help you write more effective, maintainable, and Pythonic code.

[click here  to read](https://dbader.org/blog/python-dunder-methods)

### ***What is the purpose of dunder methods in Python? Provide an example of a commonly used dunder method.***

Dunder methods are special methods in Python with a naming convention that starts and ends with two underscores. They are used to define behaviors and operations for classes and objects. One commonly used dunder method is __init__, which is used to initialize an object's attributes when the object is created. Other commonly used dunder methods include __str__ for defining how an object should be printed as a string and __eq__ for defining how two objects should be compared for equality.

```python
class Person:
    def __init__(self, name):
        '''
        Initialize a new Person object
        '''
        self.name = name

    def __str__(self):
        '''
        Define how Person objects should be printed as strings
        '''
        return f"Person named {self.name}"

    def __eq__(self, other):
        '''
        Define how Person objects should be compared for equality
        '''
        return self.name == other.name
```

-----------------------------------------------------
# Ethical issues

### ***In the video “AI Guru makes $238,800 with misleading paid course,” what was the main ethical issue raised concerning the use of developers’ work, and how might this have been avoided?***
[click here to watch](https://www.youtube.com/watch?v=7jmBE4yPrOs)

The main ethical issue raised in the video was that the AI Guru was using other developers' work without their permission and without giving them credit. This could have been avoided by asking for permission to use the developers' work and giving them credit for their work.

----------

# statistics — Mathematical statistics functions

### ***Describe the Python statistics module and give an example of a function within the module that can be used to perform a common statistical operation.***
[click here to read](https://docs.python.org/3/library/statistics.html)


The Python statistics module provides functions for calculating mathematical statistics of numeric data. One function within the module that can be used to perform a common statistical operation is mean, which calculates the arithmetic mean of a list of numbers.

example:
```python
>>> from statistics import mean
'''
Calculate the arithmetic mean of a list of numbers
'''
>>> mean([1, 2, 3, 4, 4])
2.8
```
-----------------------------------------------------


## Things I want to know more about:
