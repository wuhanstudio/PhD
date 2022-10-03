# Week 1

> 2022/09/26 - 2022/10/02

Whether black-box attacks are real threats or just research stories?

## MLSys 2023:

- Paper Submission: Friday, **October 28**, 2023 4pm ET
- Page Length: Up to **10 pages** long, not including references (10 + n)

## Survey

Black-box attacks rely on queries but attacking real-world image classification models in cloud services could cost **20,000 to 50,000 queries** for a single attack, which means attacking **a single image** could cost **\$480 - $1200** and **5-14 hours** ([Ilyas et al.](https://arxiv.org/abs/1804.08598)) and the attack is not guaranteed to succeed (the success rate is not 100%).

The following evaluation metrics are important for black-box attacks:

- **Success Rate**: Initial research focused on improving the success rate.
- **Number of Queries**: Recent research interests shifted to reducing the number of queries. 
- **Time Cost**: I notice that reducing the number of queries is not the only way to accelerate black-box attacks (also possible via distributed queries).

In a survey paper ([Bhambri et al.](https://arxiv.org/abs/1912.01667)), black-box attacks are classified into:

- **Gradient-based Methods**
- **Local Search**
- Combinatorics
- Transferability

## Problems

For black-box attacks against cloud services:

- The more queries we sent simultaneously, the faster the attack is.
- Do we need to start from scratch every time we attack the same model? 
- Experiments: we shouldn't assume access to pre-processing methods.

## Plan

> Week 1 - Week 5 (Total: 5 weeks)

**Week 1**:

- Local Search

  - SimBA (2019)
  - Square Attack (2020)

**Week 2**:

- Gradient Estimation

    - Limited Query (2018)
    - Bandits (2019)

- The Draft for MLSys 2023. (Introduction)

**Week 3**: The Draft for MLSys 2023. (Methodology)

**Week 4**: The Draft for MLSys 2023. (Experiment)

**Week 5**: Revision & Submission.
