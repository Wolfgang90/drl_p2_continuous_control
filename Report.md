# Report on description of implementation

## Learning Algorithm
DDPG algorithm is employed to solve the environment. The algorithm was customized to work with 20 agents used to collect experiences in parallel. 
All experiences of the agents are fed to the replay buffer. 
The networks (actor and target) are adjusted 10 times after every 20 timesteps based on a random sample of experiences from the replay buffer.

#### Chosen hyperparameters

#### Selected neural network architecture

## Plot of Rewards

#### The following plot of rewards was obtained during training:

## Ideas for future work
Potential future work to be done:
Evaluate... 
* alternative Neural Network architectures
* alternative reinforcement learning algorithms

