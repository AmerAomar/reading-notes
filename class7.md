# Python Scope

## why should I learn that?

Learning about variable scope in Python is important because it affects how you write and use variables in your code. By understanding variable scope, you can avoid common errors such as accidentally modifying a global variable from within a function or trying to access a local variable outside of its scope. Knowing how variable scope works in Python can also help you write more efficient and organized code. A short and simple explanation of variable scope can help you quickly grasp the concept and start using it effectively in your code.

[read article](https://realpython.com/python-scope-legb-rule/)

### ***Explain the concept of variable scope in Python and describe the difference between local and global scope. Provide an example illustrating the usage of both.***

Variable scope in Python refers to the part of a program where a variable can be accessed. A local variable is defined within a function or block and can only be accessed within that function or block. A global variable is defined outside of any function or block and can be accessed from anywhere in the program.

ex:

```python
x = 1     # global variable

def my_func():
    y = 2     # local variable
    print(x)  # prints 1
    print(y)  # prints 2

my_func()
print(x)      # prints 1
print(y)      # NameError: name 'y' is not defined
```

---
# Python Scope and Keywords

## why should I learn that?

learning global and nonlocal keywords in Python is important because it allows you to modify variables in different scopes. However, it is recommended to use these keywords sparingly and with clear justification, as overuse can make your code more complex and harder to read and maintain. Having a good understanding of these keywords can help you write efficient and organized code and avoid common errors.

[read article](https://realpython.com/python-scope-legb-rule/)


### ***How do the global and nonlocal keywords work in Python, and in what situations might you use them?***
In Python, the global keyword is used to access and modify global variables from within a function, while the nonlocal keyword is used to access and modify variables in the outer scope of a nested function.

global variables can be accessed and modified from anywhere in the program, while nonlocal variables can be accessed and modified from within the inner nested function.

Use global when you want to modify a variable that is defined in the global scope, and use nonlocal when you want to modify a variable that is defined in an outer scope, such as a nested function.

It is generally recommended to use global and nonlocal variables sparingly and with caution, as they can make your code harder to read and maintain.

ex:

```python
x = 0    # global variable

def outer_func():
    y = 1    # outer function variable
    
    def inner_func():
        nonlocal y    # use nonlocal to modify outer function variable
        global x      # use global to modify global variable
        y = 2
        x = 3
    
    inner_func()
    print("y =", y)   # prints 2
    print("x =", x)   # prints 3

outer_func()
print("x =", x)       # prints 3

```

---

# Big O notation is simpler than you might think

## why should I learn that?

Learning about Big O notation is important for anyone interested in computer science, programming, or software engineering. It allows you to evaluate the performance of algorithms, understand their scalability, and choose the best algorithm for a specific task.

Having a good understanding of Big O notation can help you write efficient code and optimize your algorithms, leading to faster execution times and better performance. It is an important concept to know for technical interviews, as interviewers often ask questions related to algorithm analysis and time complexity.

[watch here](https://www.youtube.com/watch?v=dNorFNlDbX0)

### ***In your own words, describe the purpose and importance of Big O notation in the context of algorithm analysis.***

Big O notation is a way of describing the time complexity of an algorithm, which is important for optimizing and improving the performance of the code. It allows us to compare different algorithms and choose the most efficient one for a specific problem by analyzing how much time an algorithm takes to execute as the size of the input data grows.

---
# Rolling Dice Examples

### ***Based on the Rolling Dice Example, explain how you would simulate a dice roll using Python. Describe how you would use code to calculate the probability of rolling a specific number (e.g., the probability of rolling a 6) over a large number of trials.***


use the random module which provides functions to generate random numbers. Specifically, the randint() function can be used to generate a random integer between two given numbers, which can be used to simulate a dice roll. 
```python
import random

# Simulate a dice roll
dice_roll = random.randint(1, 6)

print("The dice roll is:", dice_roll)

```

To calculate the probability of rolling a specific number over a large number of trials, we can use a loop to run the dice roll simulation multiple times and count the number of times the desired outcome occurs. We can then calculate the probability as the number of successful outcomes divided by the total number of trials.

```python
import random

# Number of trials
num_trials = 100000

# Desired outcome
outcome = 6

# Counter for successful outcomes
success_count = 0

# Run simulation for the given number of trials
for i in range(num_trials):
    dice_roll = random.randint(1, 6)
    if dice_roll == outcome:
        success_count += 1

# Calculate the probability
probability = success_count / num_trials

print("The probability of rolling a", outcome, "is:", probability)

```