# AI-Reinforcement-Learning-08-Model-Free-Control
Lecture 5: Model-Free Control by David Silver

Website: http://www0.cs.ucl.ac.uk/staff/D.Silver/web/Teaching.html

Videos: https://www.bilibili.com/video/av32149008/?p=4

For most of these problems, either:
  - MDP model is unknown, but experience can be sampled
  - MDP model is known, but is too big to use, except by samples
Model-free control can solve these problems

- On and Off-Policy Learning
  - On-policy learning
    - “Learn on the job”
    - Learn about policy π from experience sampled from π
  - Off-policy learning
    - “Look over someone’s shoulder”
    - Learn about policy π from experience sampled from µ

## On policy

- Generalised Policy Iteration (Refresher)
  - Policy evaluation Estimate vπ
    - e.g. Iterative policy evaluation
  - Policy improvement Generate π' ≥ π
    - e.g. Greedy policy improvement
    
### Monte-Carlo
- Policy Iteration With **Monte-Carlo Evaluation**
  - Policy evaluation: Monte-Carlo policy evaluation V = vπ
  - Policy improvement: Greedy policy improvement
- Model-Free Policy Iteration Using **Action-Value Function**
  - Policy evaluation: Monte-Carlo policy evaluation Q = qπ
  - Policy improvement: Greedy policy improvement
  
- e-Greedy Exploration
  - Simplest idea for ensuring continual exploration
  - All m actions are tried with non-zero probability
  - With probability 1 − e choose the greedy action
  - With probability e choose an action at random

- Monte-Carlo Policy Iteration
  - Policy evaluation Monte-Carlo policy evaluation, Q = qπ
  - Policy improvement e-greedy policy improvement
  
- Monte-Carlo Control
  - Every episode:
    - Policy evaluation Monte-Carlo policy evaluation, Q ≈ qπ
    - Policy improvement e-greedy policy improvement
    
- Greedy in the Limit with Infinite Exploration (GLIE)
  - Definition
     - All state-action pairs are explored infinitely many times
     - The policy converges on a greedy policy
     
- GLIE Monte-Carlo Contro

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-08-Model-Free-Control/blob/master/readme_img/GLIE%20Monte-Carlo%20Control.png" width = "70%" height = "70%" div align=center />

### Temporal-difference (TD)

- Temporal-difference (TD) learning has several advantages over Monte-Carlo (MC)
  - Lower variance
  - Online
  - Incomplete sequences
  
- On-Policy Control With Sarsa
  - Every time-step:
    - Policy evaluation Sarsa, Q ≈ qπ
    - Policy improvement e-greedy policy improvement

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-08-Model-Free-Control/blob/master/readme_img/n-Step%20Sarsa.png" width = "70%" height = "70%" div align=center />

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-08-Model-Free-Control/blob/master/readme_img/Forward%20View%20Sarsa(%CE%BB).png" width = "70%" height = "70%" div align=center />

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-08-Model-Free-Control/blob/master/readme_img/Backward%20View%20Sarsa(%CE%BB).png" width = "70%" height = "70%" div align=center />

<img src="https://github.com/ChenBohan/AI-Reinforcement-Learning-08-Model-Free-Control/blob/master/readme_img/Sarsa(%CE%BB)%20Algorithm.png" width = "70%" height = "70%" div align=center />
    
## Off-Policy Learning

TODO...

