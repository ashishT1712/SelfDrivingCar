# SelfDrivingCar
# Artificial Intelligence- Basic Model of Self Driving Car using Q-Learning
## Introduction
We introduced a deep Q- network (DQN) agent to perform the task of self-driving car. We evaluated our car model’s performance with standard agents in a racing simulation environment. Our results indicate that our DQN agent is capable of successfully controlling a car to navigate around a simulation environment. The idea of this research is to make an intelligent control system that uses the concepts of deep learning with q learning to increase the efficiency of self-driving car. The plan is to use the concept of neural networks and other Artificial Intelligence techniques and algorithms to create the intelligent system.

## Problem Description
Our problem is formulated as a Markov Decision Process (MDP) in which at each timestep t, an agent observes a state st and performs an action at that leads it to a new state st+1 and observes a corresponding reward rt = R (st, at). We will use of reinforcement learning approaches and thus do not assume a transition model T (st, at, st+1) between the states st and then next state st+1. 
Q-Learning Approach
The Q-Learning algorithm was proposed as a way to optimize solutions in Markov decision process problems.  The feature of Q-Learning is in its capacity to choose between immediate rewards and delayed rewards.  At each step of time, an agent observes the vector of state xt, then chooses and applies an action ut. As the process moves to state xt+1, the agent receives a reinforcement r (xt, ut).  The goal of the training is to find the order of actions in sequence which maximizes the sum of the future reinforcements, thus leading to the shortest path from start to finish[4].

The transition rule of Q learning is a very simple formula:
Q (state, action) = R (state, action) + gamma * Max [Q (next state, all actions)]

The gamma parameter has a range of 0 to 1 (0 <= gamma > 1) and ensures the convergence of the sum.  If gamma is closer to zero, the agent will tend to consider only immediate rewards.  If gamma is closer to one, the agent will consider future rewards with greater weight, willing to delay the reward.

The Q-Learning algorithm goes as follows:
1. We need to set the gamma parameter, and environment rewards in matrix R.
2. Initialize matrix Q to zero.
3. For each episode:
Select a random initial state.
Do While the goal state hasn't been reached.
•	Select one among all possible actions for the current state.
•	Using this possible action, consider going to the next state.
•	Get maximum Q value for this next state based on all possible actions.
•	Compute: Q (state, action) = R (state, action) + gamma * Max [Q (next state, all actions)]
•	Set the next state as the current state.
End Do
End For
