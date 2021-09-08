# DeepRL-UR-motion-planning
Simulate Universal Robot Arm and compare different DeepRL approaches for picking cube

# DDPG
The Q network and policy network is very much like simple Advantage Actor-Critic, but in DDPG, the Actor directly maps states to actions (the output of the network directly the output) instead of outputting the probability distribution across a discrete action space
## Replay Buffer
As used in Deep Q learning (and many other RL algorithms), DDPG also uses a replay buffer to sample experience to update neural network parameters. During each trajectory roll-out, we save all the experience tuples (state, action, reward, next_state) and store them in a finite-sized cache — a “replay buffer.” Then, we sample random mini-batches of experience from the replay buffer when we update the value and policy networks.

For the policy function, our objective is to maximize the expected return

# TD3
TD3 is inspired by double DQN and solves the issue of the overestimation of critic values and has the following changes over DDPG.
* Using Two main critic networks apart from their target networks.
* Delaying update for actor-network.
* Action noise regularisation.

# Experimnet with picking cube
![Alt text](imgs/experiment_1.png?raw=true "Experimnet with picking cube")

# Multi-agent motion colision avoidance
![Alt text](imgs/experiment_2.png?raw=true "Multi-agent motion colision avoidance")
