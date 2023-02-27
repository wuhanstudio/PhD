# Week 7

> 2023/02/20 - 2023/02/26

## Paper Submission

**[IEEE IV]** Decision: 30 March

- Adversarial Driving
- Adversarial Detection

--------------------

**[IEEE ITS]** Submission: 13 May

- Adversarial Driving
- Adversarial Detection

--------------------

**[BMVC]** Submission: 12 May

- Man-in-the-Middle Attack
- Distributed Black Box Attack

--------------------

**[Third-year Report]** Submission: 24 May

--------------------

**[ICLR / CVPR]** Submission: Sep 2024

- Adversarial Tracking
- Physical Patch

## Research Plan

- Jan. Reinforcement Learning  
- Feb. Reinforcement Learning  
<br/>
- Mar. Object Tracking  
- Apr. Object Tracking  
<br/>
- May. WHAT & BAT (Resubmission)

## HPC ( JADE 2 Cluster )

Hartree Centre Login

[https://um.hartree.stfc.ac.uk/hartree/login.jsp](https://um.hartree.stfc.ac.uk/hartree/login.jsp)

The Slurm Scheduler

[https://docs.jade.ac.uk/en/latest/jade/scheduler/](https://docs.jade.ac.uk/en/latest/jade/scheduler/)

<br/>

Allocate a temporary node with 8 GPUS:

```
srun --gres=gpu:8 --pty bash
```

Allocate a small partition with 1 GPU:

```
srun --gres=gpu:1 -p small --pty bash

# 20 CPU Cores / 40 Threads
# 32 GB VRAM / 512 GB RAM
```

Submit and monitor jobs:

```
sbatch
sacct
squeue
scancel
```

## Deep Q Network

- Double DQN
- Dueling DQN
- Prioritized Experience Replay
- Noisy DQN
- N-step DQN
- Distributional DQN


## Reinforcement Learning

[●] Deep SARSA  
[●] Deep Q Network  

[●] REINFORCE  
[●] A2C / A3C  

[●] DDPG  
[●] TRPO & PPO  

[&nbsp; ] SAC  
[&nbsp; ] TD3  
