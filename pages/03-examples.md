# Python Example: Number Guessing Game

We'll build a simple guessing game that demonstrates several Python features. <sup><Link to="references">6.</Link></sup>

<v-clicks>

- Imports and variables
- Functions
- User input and exception handling
- Lambda expressions and conditionals

</v-clicks>

---

# Number Guessing Game

### Setup
```python {lines:true,startLine:1}
import random

attempts = 7
```

---

# Number Guessing Game

### Functions
```python {lines:true,startLine:6}
def display_rules():
    print("Welcome to Number Guessing Game!\n")
    print("I have selected a number between 1 and 100.")
    print("You have 7 attempts to guess it.\n")
```

---

# Number Guessing Game

### Input & Error Handling
```python {lines:true,startLine:12}
def play_game(number, attempt=1):
    if attempt > attempts:
        print("\nGame Over!")
        print("The correct number was:", number)
        return

    guess = input(f"Attempt {attempt}/7 - Enter your guess: ")

    try:
        guess = int(guess)
    except ValueError:
        print("Please enter a valid number.\n")
        return play_game(number, attempt)

    if guess < 1 or guess > 100:
        print("Please enter a number between 1 and 100.\n")
        return play_game(number, attempt)
```

---

# Number Guessing Game

### Lambda Expressions and Conditionals
```python {lines:true,startLine:30}
check_guess = lambda x, y: "correct" if x == y else (
    "low" if x < y else "high"
)

result = check_guess(guess, number)
```

---

# Number Guessing Game

### Handling the Result
```python {lines:true,startLine:36}
if result == "correct":
    print("\nCongratulations! You guessed the correct number!")
    print("You guessed it in", attempt, "attempt(s).")
    return

if result == "low":
    print("Too Low! Try a higher number.\n")
else:
    print("Too High! Try a lower number.\n")

play_game(number, attempt + 1)
```

---

# Number Guessing Game

### Running the Program
```python {lines:true,startLine:49}
# Start the game
display_rules()

random_number = random.randint(1, 100)

play_game(random_number)
```