# Python Example: Rock, Paper, Scissors

<div></div>

We'll build a simple game that demonstrates some basic Python features like:

- Dictionaries
- Conditionals
- Exceptions
- User Input
- Tuples

---

# Rock, Paper, Scissors

### Setup
```python {lines:true}
import random

moves = {
    "r": "rock",
    "p": "paper",
    "s": "scissors",
}
```

<!--
- At the beginning of our program, we will import the random library, part of the Python standard library.
- Then we will define a dictionary, basically a hash table, with the different moves a player can make.
-->

---

# Rock, Paper, Scissors

### Input & Exceptions
```python {lines:true,startLine:8}
def get_move():
    while True:
        try:
            choice = input("Choose rock (r), paper (p), or scissors (s): ").lower()
            return moves[choice]
        except KeyError:
            print("Invalid choice. Please enter r, p, or s.")
```

<!--
- Then we will get user input. This is an example of Python's try and except error catching.
- If the user enters a value not in our dictionary, it will cause an error, and it will ask for input again.
-->

---

# Rock, Paper, Scissors

### Conditionals and Tuples
```python {lines:true,startLine:15}
def determine_winner(player, computer):
    if player == computer:
           return "tie"
       elif (player, computer) in [
           ("rock", "scissors"),
           ("paper", "rock"),
           ("scissors", "paper"),
       ]:
           return "player"
       else:
           return "computer"
```

<!--
- To determine who wins, we'll first check if the computer's choice matches the player's.
- Then, if it doesn't, we'll check if the choices are one of three options.
- These options are represented as tuples, a Python data type.
- If it is one of those options, then the player wins. Otherwise, the computer wins.
-->

---

# Rock, Paper, Scissors

### Run the Code

```python {lines:true,startLine:25}
player_move = get_move()
computer_move = random.choice(list(moves))
determine_winner(player_move, computer_move)
```

<!--
- Finally, we run the code we've written earlier in the program.
- We call the function to get user input, and we randomly assign a move to the computer.
- Then we check the computer's move against the player's move.
-->
