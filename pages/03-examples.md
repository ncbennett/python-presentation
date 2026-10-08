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
```python {none|1|3-7}{lines:true}
import random

moves = {
    "r": "rock",
    "p": "paper",
    "s": "scissors",
}
```

<!--
- At the beginning of our program, we will import the random library, making its functionality available in this program.
- Then we'll define a dictionary, which maps keys to values, with the possible moves you can make.
-->

---

# Rock, Paper, Scissors

### Input & Exceptions
```python {none|8|9|10-12|13-14}{lines:true,startLine:8}
def get_move():
    while True:
        try:
            choice = input("Choose rock (r), paper (p), or scissors (s): ").strip().lower()
            return moves[choice]
        except KeyError:
            print("Invalid choice. Please enter r, p, or s.")
```

<!--
- Then we use a loop to continually get user input until they enter a valid value.
- We use the strip() and lower() methods to remove whitespace and capitalization.
- A keyerror occurs when a requested dictionary key doesn't exist.
-->

---

# Rock, Paper, Scissors


### Conditionals and Tuples

```python {none|16-17|18-23|24-25}{lines:true,startLine:15}
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
- To determine who wins, we'll first use a Python if statement to check if the computer's choice matches the player's, which would lead to a tie.
- Then, if it doesn't, we'll compare the (player, computer) tuple to the three combinations for the player to win.
- These options are represented as tuples, an ordered, immutable collection.
- If it is one of those options, then the player wins. Otherwise, the computer wins.
-->

---

# Rock, Paper, Scissors

### Run the Code

```python {none|27|28|29,30}{lines:true,startLine:27}
player_move = get_move()
computer_move = random.choice(list(moves.values()))
print(f"Computer chose: {computer_move}")
print(f"The winner is: {determine_winner(player_move, computer_move)}")
```

<!--
- Finally, we run the code we've written earlier in the program.
- First, we'll call our function to get the player's move.
- Then, we'll randomly select a move for the computer out of our dictionary's values.
- Then we'll compare the moves and print the results with a Python f-string.
-->
