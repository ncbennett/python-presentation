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
```python {lines:true,startLine:1}
import random

moves = {
    "r": "rock",
    "p": "paper",
    "s": "scissors",
}
```

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

---

# Rock, Paper, Scissors

### Run the Functions

```python {lines:true,startLine:25}
player_move = get_move()
computer_move = scissors
determine_winner(player_move, computer_move)
```
