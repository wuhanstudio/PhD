# Week 3

> 2022/10/10 - 2022/10/16

Most experiments were completed.



## 1. Preprocessing

**Experiment Settings:**

- Attacking **1000** images in the ImageNet dataset.

- $L_{\inf}$ = 0.05

- Max number of queries for each image = 1,000



**Model Accuracy** (1000 samples):

| Environment | Inception v3 | Resnet 50 | VGG16  |
| ----------- | ------------ | --------- | ------ |
| Local Model | 75.90%       | 70.90%    | 65.20% |
| DeepAPI     | 75.70%       | 70.80%    | 65.00% |



**Before Preprocessing (Local):**


| Attack  | Avg. Queries |       |        | Attack Success Rate |        |        | Total Queries |        |        |
| :-----: | :----------: | :---: | :----: | :-----------------: | :----: | :----: | :-----------: | :----: | :----: |
|         |      I       |   R   |   V    |          I          |   R    |   V    |       I       |   R    |   V    |
|  SimBA  |              |       |        |                     |        |        |               |        |        |
| Square  |    178.40    | 88.47 | 102.10 |       91.30%        | 97.46% | 95.40% |    135,000    | 62,700 | 66,400 |
| Bandits |              |       |        |                     |        |        |               |        |        |



**After Preprocessing (Cloud):**


| Attack  | Avg. Queries |        |      | Attack Success Rate |        |      | Total Queries |         |      |
| :-----: | :----------: | :----: | :--: | :-----------------: | :----: | :--: | :-----------: | :-----: | :--: |
|         |      I       |   R    |  V   |          I          |   R    |  V   |       I       |    R    |  V   |
|  SimBA  |              |        |      |                     |        |      |               |         |      |
| Square  |    290.50    | 194.15 |      |       83.01%        | 92.15% |      |    222,000    | 138,700 |      |
| Bandits |              |        |      |                     |        |      |               |         |      |





## 2. Distributed Queries

Distributed queries (8 workers):

| Cloud Service  | 1 query   | 2 queries | 10 queries | 20 queries |
| -------------- | --------- | --------- | ---------- | ---------- |
| Cloud Vision   | 446.68ms  | 353.61ms  | 684.25ms   | 1124.82ms  |
| Imagga         | 1688.11ms | 2331.81ms | 10775.75ms | 21971.77ms |
| DeepAPI (ours) | 538.47ms  | 643.17ms  | 1777.81ms  | 1686.36ms  |





## 3. Distributed Attacks

**Experiment Settings:**

- Attacking **100** images in the ImageNet dataset.

- $L_{\inf}$ = 0.05

- max number of queries for each image = 1,000



**3.1 Non-Distributed:**

| Attack  | Avg. Queries |      |      | Attack Success Rate |      |      | Total Queries |      |      | Time (min) |      |      |
| :-----: | :----------: | :--: | :--: | :-----------------: | :--: | :--: | :-----------: | :--: | :--: | :--------: | :--: | :--: |
|         |      I       |  R   |  V   |          I          |  R   |  V   |       I       |  R   |  V   |     I      |  R   |  V   |
|  SimBA  |              |      |      |                     |      |      |               |      |      |            |      |      |
| Square  |              |      |      |                     |      |      |               |      |      |            |      |      |
| Bandits |              |      |      |                     |      |      |               |      |      |            |      |      |



**3.2 Horizontal Distribution:**

| Attack  | Avg. Queries |       |       | Attack Success Rate |        |        | Total Queries |        |        | Time (min) |       |       |
| :-----: | :----------: | :---: | :---: | :-----------------: | :----: | :----: | :-----------: | :----: | :----: | :--------: | :---: | :---: |
|         |      I       |   R   |   V   |          I          |   R    |   V    |       I       |   R    |   V    |     I      |   R   |   V   |
|  SimBA  |              |       |       |                     |        |        |               |        |        |            |       |       |
| Square  |    359.8     | 204.7 | 222.8 |       78.21%        | 93.33% | 90.54% |    28,000     | 15,400 | 16,500 |   48.14    | 24.40 | 57.93 |
| Bandits |              |       |       |                     |        |        |               |        |        |            |       |       |



**3.3 Vertical Distribution:**

| Attack  | Avg. Queries |      |      | Attack Success Rate |      |      | Total Queries |      |      |
| :-----: | :----------: | :--: | :--: | :-----------------: | :--: | :--: | :-----------: | :--: | :--: |
|         |      I       |  R   |  V   |          I          |  R   |  V   |       I       |  R   |  V   |
|  SimBA  |              |      |      |                     |      |      |               |      |      |
| Square  |              |      |      |                     |      |      |               |      |      |
| Bandits |              |      |      |                     |      |      |               |      |      |






## Plan

- Week 4: Draft

- Week 5: Revision and Submission
