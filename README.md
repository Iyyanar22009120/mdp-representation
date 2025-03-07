# MDP REPRESENTATION

## AIM:
To represent a real-world problem in MDP form.

## PROBLEM STATEMENT:

### Problem Description
A student is deciding how to prepare for an exam. They have three strategies to choose from: Self-Study, Group Study, and Online Courses. The student wants to choose the best strategy based on rewards (exam performance).

### State Space
The state space consists of different study strategies available for the student:

State 0: Self-Study
State 1: Group Study
State 2: Online Course

### Sample State
A sample state could be the student currently using Group Study (State 1).

### Action Space
The action space consists of the decisions the student can make:

Action 0: Continue with the current study method.
Action 1: Switch to the next study method.

### Sample Action
A sample action could be the student switching from Self-Study to Group Study.

### Reward Function
The student receives a reward of 0 for staying with the current study method.
If the student switches to Online Course (State 2), they receive a reward of 1 (indicating the best learning outcome).
There are no intermediate rewards for other actions or states.e

### Graphical Representation
![graph of exp](https://github.com/user-attachments/assets/53b6d689-98f6-4159-b78d-a72e517cdca3)


## PYTHON REPRESENTATION:
```
P = {
    0: {  
        0: [(1.0, 0, 0.0, True)],  # Stay in Self-Study
        1: [(1.0, 1, 0.0, True)]   # Switch to Group Study
    },
    1: {  
        0: [(1.0, 1, 0.0, True)],  # Stay in Group Study
        1: [(1.0, 2, 1.0, True)]   # Switch to Online Course (Best choice)
    },
    2: {  
        0: [(1.0, 2, 0.0, True)],  # Stay in Online Course
        1: [(1.0, 2, 0.0, True)]   # Switching has no further effect
    }
}
```


## OUTPUT:
![output re](https://github.com/user-attachments/assets/187fb345-2eee-470b-a33d-d23e40bb6a7a)


## RESULT:
Thus, the given real-world problem of choosing the best study strategy is successfully represented in MDP form.

