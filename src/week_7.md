# Week 7

> 2022/11/07 - 2022/11/13

## 1. Reinforcement Learning

> Trade-off between exploration and exploitation.

### 1.1 Tabular Solution

> The state and action spaces are **small enough** for the approximate value functions to be represented as arrays or tables.

- Finite Markov Decision Process
- Dynamic Programming
- Monte Carlo Methods

-------------

TD learning combines some of the features of both Monte Carlo and Dynamic Programming (DP) methods.

-------------

- Temporal-Difference Learning
- n-step Bootsrapping

### 1.2 Approximate Solution Methods

> Problems with **arbitrary large** state spaces.

-------------

- **Prediction Task**: Evaluate a given policy by estimating the value of taking actions following the policy.

- **Control Task**: Find the optimal policy that gets most rewards.

-------------

- **On-policy**: Estimate the value of a policy while using it for control.

- **Off-policy**: The policy used to generate behaviour, called the behaviour policy, may be unrelated to the policy that is evaluated and improved, called the estimation policy.

-------------

<!-- Treat the on-policy case with function approximation: -->

- On-policy TD Prediction
    - TD(0)
- On-policy TD Control
    - SARSA

<!-- The extension to function approximation turns out to be significantly di↵erent and harder for o↵-policy learning than it is for on-policy learning.  -->

- Off-policy TD Control
    - Q-Learning
    - Dyna-Q and Dynq-Q+
    - Expected SARSA

-------------

<!-- Methods that instead learn a parameterized policy that can select actions without consulting a value function. -->

- Policy Gradient Methods
    - REINFORCE
    - Actor-Critic
    - Advantage Actor-Critic (A2C)


## 2. Webots Simulator (ROS2)

> Multi-agent Reinforcement Learning.

![](https://raw.githubusercontent.com/cyberbotics/webots/R2021a/docs/automobile/images/titleweb.png)
