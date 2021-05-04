# Report on description of implementation

## Learning Algorithm
DDPG algorithm is employed to solve the environment. The algorithm was customized to work with 20 agents used to collect experiences in parallel. 
All experiences of the agents are fed to the replay buffer. 
The networks (actor and target) are adjusted 10 times after every 20 timesteps based on a random sample of experiences from the replay buffer.

#### Chosen hyperparameters
* replay buffer size: 1e6
* minibatch size: 1024
* discount factor (gamma): 0.99
* tau for soft update of target parameters: 1e-3
* learning rate actor: 1.5e-3
* learning rate critic: 1e-3
* L2 weight decay: 0
* maximum number of timesteps per episode: 100000

#### Selected neural network architecture
For actor:
* Network input: state-size -> 33 x 1 vector
* Number of nodes in first hidden fully-connected layer with ReLU applied: 400
* Number of nodes in second hidden fully-connected layer with ReLU applied: 300
* Number of nodes in output layer with tanh applied representing the potential actions: 4

For critic:
* Network input: state-size -> 33 x 1 vector
* Number of nodes in first hidden fully-connected layer with ReLU applied: 400
* Number of nodes in second hidden fully-connected layer with ReLU applied: 300
* Number of nodes in output layer representing the potential actions: 4

## Plot of Rewards
The environment was solved within **481 episodes**.
As described in `README.md` the environment was considered to be solved, when the agent got
* an average score of +30 (over 100 consecutive episodes, and over all agents). Specifically,
    * After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. 
    * This yields 20 (potentially different) scores. We then take the average of these 20 scores.

#### The following plot of rewards was obtained during training:
![Alt text](plots/plot_of_rewards.png?raw=true "Title")

## Ideas for future work
Potential future work to be done:
Evaluate... 
* alternative Neural Network architectures
* alternative reinforcement learning algorithms

