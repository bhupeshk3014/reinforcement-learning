
# Week 1 – Class Activity: Introduction to Reinforcement Learning

This class activity complements the Week 1 lecture content of CSCN8020 by visualizing and modeling RL concepts like **state machines**, **Markov Decision Processes (MDPs)**, and the **exploration-exploitation tradeoff**, especially using real-world analogies like finance.

---

## 🎯 Learning Objective
Understand reinforcement learning through:
- Modeling environments as state machines
- Visualizing MDP transitions
- Practicing state-action mapping
- Exploring tradeoffs in decision-making (exploration vs exploitation)

---

## 🧠 Visualizing Learning Paradigms (Page 2)
A comparative image illustrates:
- **Supervised Learning:** Learns from (X, Y) label pairs (e.g., predicting house price from features)
- **Unsupervised Learning:** Identifies structure in unlabeled data (e.g., shopping categories)
- **Reinforcement Learning:** Learns via interaction, using state-action-reward feedback loops (maze-solving robot)

---

## 🧩 State Machine Setup (Pages 4–6)
### Scenario:
A robot moves through a maze.

- **Actions (A)** = {Up, Down, Left, Right}
- **States (S)** = Set of locations at time steps: \( S = \{S_1, S_2, ..., S_t\}, t=11 \)
- **Transition Function:** \( \partial(S_1, A_1) = S_2 \)

This means: given state \( S_1 \) and action \( A_1 \), the next state will be \( S_2 \).

### Grid-based representation:
- Current location: (1, 2)
- Previous location: (1, 3)
- Grid boundaries and walls constrain allowed actions

---

## 🔁 State Diagram (Page 7)
This diagram shows directional transitions:
```
S1 --up--> S2 --right--> S3 --up--> S4 --left--> S5 --up--> S6
                                      \
                                      down
```
It models how a robot agent can reach a goal by transitioning between defined states using allowed actions.

---

## 🥤 State Machine Exercise: Vending Machine (Page 8)
Teams were asked to model a vending machine using a state machine:

### States:
- Idle
- Coin Inserted
- Selection Made
- Dispensing

### Inputs:
- Insert coin
- Make selection
- Dispense item
- Return to idle

### Task:
- Define states and transition triggers
- Draw a labeled state diagram with arrows

This reinforces how state machines underpin RL environments.

---

## 💸 Exploration vs Exploitation in Finance (Pages 10–11)
Explained with a real-world analogy:

### Exploration:
- Try new investments (e.g., AI startups, ETFs)
- High potential reward but risky

### Exploitation:
- Stick with known safe stocks (e.g., Apple)
- Lower risk but may miss out on gains

> **Tradeoff**: Must balance curiosity vs certainty to maximize long-term returns.

---

## 🔄 MDP Transition Function (Pages 13–14)
### Formula:
\[
p(s', r | s, a) = P(S_t = s', R_t = r | S_{t-1} = s, A_{t-1} = a)
\]

This defines the **probability of moving to state s' and receiving reward r**, given current state and action.

### Conservation Rule:
\[
\sum_{s'} \sum_r p(s', r | s, a) = 1
\]

Meaning: The sum of probabilities for all possible outcomes after an action must equal 1.

### Maze Analogy:
- States: grid positions
- Actions: {left, right, up, down}
- Rewards: assigned to specific cells or transitions

---

## 🧪 Try-at-Home Tasks (Page 15)
1. **Maze Navigation:**
   - Build a grid with assigned transition probabilities and rewards
2. **Hands-On MDP Math:**
   - Calculate \( p(s', r | s, a) \) for given state-action pairs
   - Ensure the total probability for transitions from any state sums to 1

---

## 🎥 Suggested Videos (Pages 17–19)
Explore deeper with visual demos and explanations:
- [Reinforcement Learning with Gymnasium](https://youtu.be/vufTSJbzKGU?si=5Mn5FuXlyPbi5LOf)
- [Intro to Q-Learning](https://youtu.be/vw0Zy_oCWxE?si=wasqU0gpbvLeI1pH)
- [Multi-Armed Bandit Problem](https://youtu.be/bkw6hWvh_3k?si=jQBl9Aejj_fE63VL)
- [Agent-Environment Interface by IIT](https://youtu.be/CHpR3KVMLzU)

---

## ✅ Summary
This activity bridged theory with hands-on design:
- Mapped real-world systems to RL models (state machines, MDPs)
- Practiced transition logic and diagrams
- Applied the **exploration vs exploitation** dilemma to real finance
- Set up for deeper RL math and coding in upcoming weeks
