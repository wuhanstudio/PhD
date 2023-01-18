# Week 16

> 2023/01/09 - 2023/01/15


## Multi-Agent Connected Autonomous Driving (MACAD)

- A Review: [https://arxiv.org/abs/2203.07676](https://arxiv.org/abs/2203.07676)
- An RL env: [https://github.com/praveen-palanisamy/macad-gym](https://github.com/praveen-palanisamy/macad-gym)


### OpenAI Gym environment

- Environments: 

  - Hete Ncom | Inde | PO Intrx MA | TLS 1B2C1P TWN3-v0

  - **Homo Ncom | Inde | PO Intrx MA | SS 3C TWN3-v0**

- Observation Space: Images (168 x 168 x 3).

- Action Space: 9 discrete actions.


![](imgs/macad-gym.png)


## RL Methods

### Baseline

Discrete Action Space:

- [Deep Q (2013)](https://arxiv.org/abs/1312.5602)
- [A2C / A3C (2016)](https://arxiv.org/abs/1602.01783)

Continuous Action Space:

- [DDPG (2015)](https://arxiv.org/abs/1509.02971)
- [TRPO & PPO (2017)](https://www.andrew.cmu.edu/course/10-703/slides/Lecture_NaturalPolicyGradientsTRPOPPO.pdf)

### Advanced

Continuous Action Space:

- [SAC (2018)](https://proceedings.mlr.press/v80/haarnoja18b)
- [TD3 (2019)](https://spinningup.openai.com/en/latest/algorithms/td3.html)

<!-- - [HER (2017)](https://arxiv.org/abs/1707.01495) -->

## Other Platforms

- [https://github.com/oxwhirl/smac](https://github.com/oxwhirl/smac)
- [https://github.com/facebookresearch/nocturne](https://github.com/facebookresearch/nocturne)
