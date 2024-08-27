# MDP REPRESENTATION

## AIM:
Write your aim here

## PROBLEM STATEMENT:

### Problem Description
Write your answer here

### State Space
Write your answer here

### Sample State
Write your answer here

### Action Space
Write your answer here

### Sample Action
Write your answer here

### Reward Function
Write your answer here

### Graphical Representation


![Img](https://github.com/user-attachments/assets/23c283e1-dc60-4a6f-b942-efd0b7d60d66)




## PYTHON REPRESENTATION:
```py

mdp = {
    0: {  # Initial state with no score and no foul
        1: [(0.8, 2, 1.0, False)],  # Higher chance of scoring with a foul
        0: [(1.0, 1, 0.0, False)]  # Guaranteed transition to state 1
    },
    1: {  # Score increased, no foul called
        1: [(1.0, 3, 1.0, True)],  # Moves to terminal state with foul
        0: [(1.0, 1, 0.0, False)]  # Stays in the same state
    },
    2: {  # Score increased with a foul
        1: [(1.0, 3, 1.0, True)],  # Guaranteed transition to terminal state
        0: [(1.0, 2, 0.0, False)]  # Stays in the same state
    },
    3: {  # Terminal state
        1: [(1.0, 3, 1.0, True)],
        0: [(1.0, 3, 0.0, True)]
    }
}

```


## OUTPUT:

![image](https://github.com/user-attachments/assets/d26e9339-886c-457d-9d87-9d3c4c8a5779)


## RESULT:

Thus the given real world problem is successfully represented in a MDP form.
