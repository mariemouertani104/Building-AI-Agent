# Q-Learning GridWorld Agent with Obstacles and Visualization

This project implements a simple AI agent based on the Q-learning algorithm in a 2D grid environment with obstacles.
The objective of the agent is to learn an optimal path to a goal position while avoiding blocked cells.

The project is designed as an educational introduction to reinforcement learning and autonomous agents.

---

## Environment

The environment is a 6x6 grid.

- Start position: (0, 0)
- Goal position: (5, 5)
- Obstacles are fixed cells that the agent cannot enter.

Example obstacle positions:

(1,2), (2,2), (3,2), (4,1), (4,2)

The agent can move in four directions:

- up
- down
- left
- right

If the agent tries to move into an obstacle or outside the grid, it remains in the same cell.

---

## Reward function

- The agent receives a reward of +20 when it reaches the goal.
- The agent receives a reward of -1 at every step.

The episode terminates when the goal is reached.

---

## Agent model

The agent uses the Q-learning algorithm.

A Q-table is maintained for all state-action pairs.

The update rule is:

Q(s,a) = Q(s,a) + α [ r + γ max(Q(s',a')) − Q(s,a) ]

Where:

- α is the learning rate
- γ is the discount factor
- r is the immediate reward
- s' is the next state

---

## Visualization

The learned path is visualized using Matplotlib.

The grid representation is:

- black cells represent obstacles
- the colored path shows the learned trajectory
- the goal cell is displayed at the bottom-right corner

---

## Project structure

The project contains three main components:

1. GridWorld environment  
   Handles the grid, obstacles and agent transitions.

2. Q-learning agent  
   Learns an optimal policy using a Q-table.

3. Training and testing loop  
   Performs the interaction between the agent and the environment and displays the learned path.

---

## How to run

This project runs directly in Google Colab.

Steps:

1. Open a new notebook in Google Colab.
2. Copy the Python code into a single cell.
3. Run the cell.

After training, the learned path and its visualization are displayed.

---

## Possible extensions

- Add moving obstacles
- Introduce a penalty for hitting an obstacle
- Change the reward structure
- Use a larger grid
- Replace Q-learning with a neural network (DQN)

---

## Author

Meriem Ouertani  
First-year ICT Engineering student – INSAT
