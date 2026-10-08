# Interesting Features of Python

<div v-click>


# Interesting Features of Python

### Generators

```python {none|1-3|5-6}{lines:true}
def countdown(n):
    while n > 0:
        yield n
        n -= 1

for number in countdown(3):
    print(number)
```

<!--
- Generators look like ordinary functions, but use the yield keyword instead of return to produce values.
- Unlike normal functions, generators can pause execution and resume where they left off.
- Each time the generator is advanced, it runs until the next yield.
- This allows us to process large amounts of data without storing every value in memory, making them useful for processing large files or streams of data.
-->


---


# Interesting Features of Python

### Decorators

```python {none|1-4|6-8|10}{lines:true}
def uppercase(func):
    def wrapper():
        return func().upper()
    return wrapper

@uppercase
def greet():
    return "Hello Bob"

print(greet())  # Output: HELLO BOB
```

<!--
- Decorators allow us to extend or modify a function's behavior without changing the function's original definition.
- In Python, functions are objects, meaning they can be passed as arguments and returned from other functions.
- For example, our decorator accepts a function and returns a new function that converts its result to uppercase.
- The @uppercase syntax applies that decorator to greet.
- Decorators are commonly used to add third-party functionality to your functions.
-->


---


# Interesting Features of Python

### Dictionary Comprehensions

```python {none|1|3|4}{lines:true}
moves = ["rock", "paper", "scissors"]

lengths = {move: len(move) for move in moves}
print(lengths) # Output: {'rock': 4, 'paper': 5, 'scissors': 8}
```

<!--
- Another interesting Python feature is dictionary comprehensions.
- Python dictionaries are data structures that map keys to values, similar to a hash table.
- Dictionary comprehensions provide an easy way to construct dictionaries from other collections.
- Here, we iterate through our list of moves, using each move as a key and its character count as the value, letting us replace a normal loop and repeated dictionary assignments with a single expression.
-->

