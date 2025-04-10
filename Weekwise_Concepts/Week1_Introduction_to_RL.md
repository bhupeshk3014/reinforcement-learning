
# Week 1: Introduction to Reinforcement Learning (CSCN8020)

---

## What is Reinforcement Learning (RL)?

Reinforcement Learning (RL) is a subfield of machine learning focused on how an **agent** learns to make **sequential decisions** by **interacting with an environment** to **maximize a cumulative reward**.

### 🔹 Definitions:
- **Definition 1:** RL is about learning what to do—how to map situations to actions—to maximize a **numerical reward signal**.
- **Definition 2:** RL is learning through **trial-and-error**, where the agent receives **rewards or penalties** after taking actions in an environment.

### Key Characteristics:
- Learning from **interaction**
- **Delayed feedback** (not immediate)
- Decisions affect **future outcomes**
- Goal is to **maximize long-term rewards**

---

## Key Components of RL

| Component   | Description |
|-------------|-------------|
| **Agent**        | The decision-maker (e.g., robot, program) that learns and acts |
| **Environment**  | The world or system with which the agent interacts |
| **State (s)**     | Current situation the agent observes from the environment |
| **Action (a)**    | The possible moves/choices the agent can make in a given state |
| **Reward (r)**    | Feedback from the environment based on the agent's action |

### Interaction Loop:
At each time step `t`:
1. Agent observes **state** \( S_t \)
2. Takes **action** \( A_t \)
3. Receives **reward** \( R_{t+1} \)
4. Transitions to **next state** \( S_{t+1} \)

This forms a feedback loop:  
**State → Action → Reward → Next State**

---

## RL vs Other Learning Paradigms

| Paradigm          | How it Learns                  | Feedback Style       | Interaction |
|------------------|-------------------------------|----------------------|-------------|
| Supervised       | From labeled data             | Direct, explicit     | Passive     |
| Unsupervised     | Finds patterns in unlabeled data | Indirect, intrinsic  | Passive     |
| Reinforcement    | Learns by interacting with environment | Delayed, scalar reward | **Active**     |

---

## Advantages of RL
- Supports **long-term goal** optimization
- Enables **learning through interaction**
- Can operate in **uncertain, dynamic environments**
- Useful for **sequential decision-making**
- No need for labeled datasets (unlike supervised learning)

---

## The Reinforcement Learning Problem

The RL problem is defined by how an **agent** interacts with an **environment** over time to **maximize cumulative rewards**.

### Core Elements:
- **Policy (\(\pi\))**: A mapping from states to actions.
- **Value Function (\(V(s)\))**: Expected cumulative reward from state \(s\) under policy \(\pi\).
- **Model (optional)**: Predicts next state and reward; used in model-based RL.

---

## Exploration vs Exploitation

A central challenge in RL is the **exploration-exploitation trade-off**:

| Strategy        | Description |
|----------------|-------------|
| **Exploration** | Trying new actions to discover better rewards |
| **Exploitation**| Choosing the known best action to get the highest immediate reward |

The agent must **balance** both to perform optimally in the long run.

---

## Applications of RL

| Domain     | Example Use-Cases |
|------------|-------------------|
| **Gaming**   | Playing chess, Go, Pong, Donkey Kong |
| **Robotics** | Path planning, pick-and-place tasks |
| **Finance**  | Portfolio optimization |
| **Healthcare** | Personalized treatment recommendations |

---

## Markov Decision Process (MDP)

> A Markov Decision Process (MDP) provides the mathematical framework to describe RL problems involving **sequential decision-making**.

### MDP Defined:
\[ \text{MDP} = (S, A, P, R) \]
Where:
- \(S\): Set of states
- \(A\): Set of actions
- \(P(s'|s,a)\): Transition probabilities
- \(R(s,a)\): Reward function

### Markov Property:
> The **future is conditionally independent of the past given the present**.  
This means the **current state contains all necessary information**.

---

## MDP Agent-Environment Interaction (Trajectory)

At each time step \( t = 0,1,2,... \):
1. Agent observes state \( S_t \)
2. Chooses action \( A_t \)
3. Receives reward \( R_{t+1} \)
4. Moves to next state \( S_{t+1} \)

### Trajectory Format:
\[ S_0, A_0, R_1, S_1, A_1, R_2, S_2, ... \]

This interaction forms the **experience** from which the agent learns.

---

## Finite MDPs

In a **finite MDP**, the number of states, actions, and rewards is finite.
- Transition and reward functions are defined as:
\[ p(s', r | s, a) = P(S_t = s', R_t = r | S_{t-1} = s, A_{t-1} = a) \]
- These probabilities **sum to 1** for all \( s \) and \( a \).

---

## Example: Simple Maze

### Problem Setup:
- **Agent**: Blue circle that moves on a grid
- **Environment**: Maze grid
- **States**: Each grid cell
- **Actions**: {Up, Down, Left, Right}
- **Goal**: Reach the green circle (reward = +1)

### Finite MDP Modeling:
- Each position = a state \(s_{i,j}\)
- Actions change the state depending on allowed movement
- Transition probabilities can be defined based on walls and blocked cells
- Rewards are usually 0 for every move, +1 at goal

---

## Summary

- RL is a trial-and-error learning paradigm to maximize long-term rewards
- Key components: Agent, Environment, State, Action, Reward
- MDPs formalize the interaction between the agent and the environment
- The Markov property allows simplification by considering only the present state
- Applications range from games to healthcare to robotics
