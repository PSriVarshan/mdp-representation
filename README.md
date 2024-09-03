### Developed By : Sri Varshan P

### Register No. 212222240104

### Date : 

# MDP REPRESENTATION

## AIM:

### To represent an optimal decision-making strategy for an umpire in a sports game into a Markov Decision Process (MDP) form

## PROBLEM STATEMENT:

### Problem Description

### An umpire in a sports game needs to make decisions based on the current game state, which includes the game score and the number of fouls. The umpire can either provide a score or not and call a foul or not. The aim is to determine the optimal decision-making strategy for the umpire to maximize the reward, where positive rewards are given for correct actions that align with the game rules.

### State Space

The state space consists of all possible combinations of the game score and the foul status. Each state is represented by:

> Game Score: The current score of the game.
<br>

> Foul Status: Indicates whether a foul has occurred

### Sample State

(Game Score = 3, Foul Status = True(1))

### Action Space
The action space consists of the following actions:

1.Provide Score: Update or confirm the game score.

2.Call Foul: Indicate that a foul has occurred.

3.Do Nothing: Take no action.

### Sample Action

Call Foul

### Reward Function

#### Reward of 1: If the umpire calls a foul when a foul has occurred and provides the score.

#### Reward of 0: If the umpire either does not provide the score or fails to call a foul when a foul has occurred.

### Graphical Representation


![Image](https://github.com/user-attachments/assets/264f5588-f2f4-483b-a674-be54de681f6e)




## PYTHON REPRESENTATION:
```py

mdp = {
    0: {  # Initial state with no score and no foul
        1: [(0.8, 2, 1.0, False)],  # Higher chance of scoring with a foul
        0: [(0.2, 1, 0.0, False)]  # Adjusted probability for no foul
    },
    1: {  # Score increased, no foul called
        1: [(1.0, 3, 1.0, True)],  # Moves to terminal state with foul
        0: [(0.0, 1, 0.0, False)]  # No probability to stay in the same state
    },
    2: {  # Score increased with a foul
        1: [(1.0, 3, 1.0, True)],  # Guaranteed transition to terminal state
        0: [(0.0, 2, 0.0, False)]  # No probability to stay in the same state
    },
    3: {  # Terminal state
        1: [(1.0, 3, 1.0, True)],
        0: [(1.0, 3, 0.0, True)]  # Remains in the terminal state
    }
}


```


## OUTPUT:


![image](https://github.com/user-attachments/assets/84ffdf0e-ee1a-44a1-80ce-676bddb22cfe)


## RESULT:

Thus the given real world problem is successfully represented in a MDP form.
