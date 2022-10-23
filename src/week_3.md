# Week 3

> 2022/10/10 - 2022/10/16

Most experiments were completed.



## 1. Pre-processing

**Experiment Settings:**

- Attacking **1000** images in the ImageNet dataset.

- $L_{\inf}$ = 0.05

- Max number of queries for each image = 1,000



**Model Accuracy** (1000 samples):

| Environment | Inception v3 | Resnet 50 | VGG16  |
| ----------- | ------------ | --------- | ------ |
| Local Model | 75.90%       | 70.90%    | 65.20% |
| DeepAPI     | 75.70%       | 70.80%    | 65.00% |



**Before Pre-processing (Local):**


| Attack  | Avg. Queries |        |        | Attack Success Rate |        |        | Total Queries |         |         |
| :-----: | :----------: | :----: | :----: | :-----------------: | :----: | :----: | :-----------: | :-----: | :-----: |
|         |      I       |   R    |   V    |          I          |   R    |   V    |       I       |    R    |    V    |
|  SimBA  |    745.40    | 690.50 | 630.75 |        3.04%        | 4.33%  | 5.13%  |    745,000    | 691,000 | 631,000 |
| Square  |    178.40    | 88.47  | 102.10 |       91.30%        | 97.46% | 95.40% |    135,000    | 62,700  | 66,400  |
| Bandits |    520.40    | 403.00 | 382.10 |       41.37%        | 55.01% | 57.52% |    520,000    | 403,000 | 382,000 |



**After Pre-processing (Cloud):**


| Attack  | Avg. Queries |        |        | Attack Success Rate |        |        | Total Queries |         |         |
| :-----: | :----------: | :----: | :----: | :-----------------: | :----: | :----: | :-----------: | :-----: | :-----: |
|         |      I       |   R    |   V    |          I          |   R    |   V    |       I       |    R    |    V    |
|  SimBA  |    744.75    | 697.60 | 633.25 |        3.33%        | 3.64%  |  8.9%  |    745,000    | 697,000 | 633,000 |
| Square  |    290.50    | 194.15 | 223.60 |       83.01%        | 92.15% | 88.30% |    222,000    | 138,700 | 145,100 |
| Bandits |    683.35    | 639.55 |        |       10.80%        | 11.17% |        |    681,000    | 639,000 |         |





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

| Attack  | Avg. Queries |        |        | Attack Success Rate |        |        | Total Queries |        |        | Time (min) |      |      |
| :-----: | :----------: | :----: | :----: | :-----------------: | :----: | :----: | :-----------: | :----: | :----: | :--------: | :--: | :--: |
|         |      I       |   R    |   V    |          I          |   R    |   V    |       I       |   R    |   V    |     I      |  R   |  V   |
|  SimBA  |    775.10    | 739.60 | 729.70 |        2.56%        | 4.00%  | 2.70%  |    77,500     | 74,000 | 73,000 |    662     | 638  | 657  |
| Square  |    359.80    | 200.10 | 227.60 |       78.21%        | 93.33% | 91.89% |    28,100     | 15,400 | 16,800 |    301     |  81  | 175  |
| Bandits |    730.30    | 688.30 | 697.70 |        7.69%        | 9.33%  | 6.76%  |    73,000     | 68,800 | 69,800 |    758     | 629  | 670  |



**3.2 Horizontal Distribution:**

| Attack  | Avg. Queries |        |        | Attack Success Rate |        |        | Total Queries |        |        | Time (min) |      |      |
| :-----: | :----------: | :----: | :----: | :-----------------: | :----: | :----: | :-----------: | :----: | :----: | :--------: | :--: | :--: |
|         |      I       |   R    |   V    |          I          |   R    |   V    |       I       |   R    |   V    |     I      |  R   |  V   |
|  SimBA  |    772.50    | 738.80 | 727.70 |        2.56%        | 2.67%  | 2.70%  |    77,300     | 73,900 | 72,800 |    148     | 133  | 226  |
| Square  |    359.80    | 204.70 | 222.80 |       78.21%        | 93.33% | 90.54% |    28,100     | 15,400 | 16,500 |     48     |  24  |  58  |
| Bandits |    740.50    | 672.60 | 706.80 |        5.13%        | 10.67% | 5.41%  |    73,700     | 67,000 | 70,400 |    221     | 202  | 292  |



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
