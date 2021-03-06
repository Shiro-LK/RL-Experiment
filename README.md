# RL-Experiment
Reproduce simple experiment with gym for RL algorithm. All these algorithms are based on the Bellman Equation where : 
- <img src="https://render.githubusercontent.com/render/math?math=V^\pi(s)"> is the state-value function of MDP (Markov Decision Process). It's the expected return starting from state s following policy <img src="https://render.githubusercontent.com/render/math?math=\pi">. 
- <img src="https://render.githubusercontent.com/render/math?math=Q^\pi(s)">is the action-value function. It is the expected return starting from state s, following policy <img src="https://render.githubusercontent.com/render/math?math=\pi">, taking action <img src="https://render.githubusercontent.com/render/math?math=a">

The Bellman Equations are : 

<img src="https://render.githubusercontent.com/render/math?math=V_{\pi}(s)=\sum_{a \in \mathcal{A}} \pi(a \mid s)\left(R_{s}^{a}+\sum_{s^{\prime} \in S} \gamma \mathcal{P}_{s s^{\prime}}^{a} V_{\pi}\left(s^{\prime}\right)\right)"> with <img src="https://render.githubusercontent.com/render/math?math=R"> the reward, <img src="https://render.githubusercontent.com/render/math?math=\gamma"> the discount, <img src="https://render.githubusercontent.com/render/math?math=P"> the transition matrix probability, <img src="https://render.githubusercontent.com/render/math?math=V"> the value function, <img src="https://render.githubusercontent.com/render/math?math=s"> the state, <img src="https://render.githubusercontent.com/render/math?math=a"> the action and <img src="https://render.githubusercontent.com/render/math?math=\pi"> the probability of making the decision in state <img src="https://render.githubusercontent.com/render/math?math=s"> (policy).

<img src="https://render.githubusercontent.com/render/math?math=q_{\pi}(s, a)=R_{s}^{a}+\sum_{s^{\prime} \in \mathcal{S}} \gamma \mathcal{P}_{s s^{\prime}}^{a} \underset{a \in \mathcal{A}}{\pi\left(a \mid s^{\prime}\right)} q_{\pi}\left(s^{\prime}, a\right)"> with <img src="https://render.githubusercontent.com/render/math?math=a"> the action, and <img src="https://render.githubusercontent.com/render/math?math=P">  the probability that action <img src="https://render.githubusercontent.com/render/math?math=a"> in state <img src="https://render.githubusercontent.com/render/math?math=s"> time t will lead to state s'  at time <img src="https://render.githubusercontent.com/render/math?math=t">+1.

0 - Value Iteration and policy iteration : [0-ValueIteration-PolicyIteration](0-ValueIteration-PolicyIteration.ipynb)

1- Monte Carlo with MoutainCar : [1-Model-free-MonteCarlo](1-Model-free-MonteCarlo.ipynb)
![MountainCar with Monte Carlo](gif/monte_carlo_moutaincar.gif)

2 - SARSA and Q-Learning Cartpole-v0 :[2-Model-free-Cartpole-SARSA-QLearning](2-Model-free-Cartpole-SARSA-QLearning.ipynb)
![Q-Learning_CartPole](gif/qlearning_cartpole.gif)

3 - DQN Cartpole-v0 : [3-Model-free-Cartpole-Deep-QLearning(DQN)](3-Model-free-Cartpole-Deep-QLearning(DQN).ipynb)
![DQN CartPole](gif/DQN_cartpole.gif)

4- Double DQN : ongoing