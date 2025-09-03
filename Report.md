# Environment details

The state space has 37 dimensions and consists of:

* The agent's velocity.
* Ray based objects position in the agents forward field of view.

The agent receives a reward of +1 for a yellow banana, and -1 for blue banana. The goal is therefore to maximize the collection of yellow bananas while minimizing / avoiding blue ones.

The action space for the agent consists of the following four possible actions:

0 - walk forward  
1 - walk backward  
2 - turn left  
3 - turn right  
The agent must collect a reward of +13 or more in over 100 consecutive episodes to solve the problem.  

# Learning algorithm
Q-Learning is an approach which generates a Q-table that is used by an agent to determine best action for a given state. This technique becomes difficult and inefficient in environments that have a large state space. Deep Q-Networks on the other hand makes use of a neural network to approximate Q-values for each action based on the input state.

However, there are drawbacks in Deep Q-Learning. A common issue is that the reinforcement learning tends to be unstable or divergent when a non-linear function approximator such as neural networks are used to represent Q. This instability comes from the correlations present in the sequence of observations, the fact that small updates to Q may significantly change the policy and the data distribution, and the correlations between Q and the target values.

To overcome this, experience replay is a technique that was used in this solution that uses the biologically inspired approach of replaying a random sample of prior actions to remove correlations in the observation sequence and smooth changes in the data distribution.

# Model architecture and hyperparameters

Fully connected layer 1: Input 37 (state space), Output 64, RELU activation.  
Fully connected layer 2: Input 64, Output 64, RELU activation.  
Fully connected layer 3: Input 64, Output 4 (action space).  

The hyperparameters for tweaking and optimizing the learning algorithm were:

max_t (1000): maximum number of timesteps per episode.  
eps_start (1.0): starting value of epsilon, for epsilon-greedy action selection.  
eps_end (0.01): minimum value of epsilon.  
eps_decay (0.995): multiplicative factor (per episode) for decreasing epsilon.  

# Plot of rewards
Below is a training run of the above model architecture and hyperparameters:

Number of agents: 1  
Number of actions: 4  
Episode 100	Average Score: 0.98  
Episode 200	Average Score: 3.66  
Episode 300	Average Score: 7.27  
Episode 400	Average Score: 10.19  
Episode 500	Average Score: 12.66  
Episode 518	Average Score: 13.02  
The plot of rewards for this run is as follows:

<img width="356" height="236" alt="Trend_solucionDQNBanana" src="https://github.com/user-attachments/assets/72085674-89f1-4fff-89f9-c67ccac8abb4" />

# References

1.- [DQN Paper] (https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf)
