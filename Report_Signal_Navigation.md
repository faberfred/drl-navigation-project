[//]: # (Image References)

# Navigation by Signals - Report
The following report displays the results for the Agent trained by the *37 input signals* of the Unity environment. 
### Settings

- Python version: 3.6
- PyTorch: 1.4.0 / 1.5.0
- Cuda: CUDAToolkit 10.1
- Operating system: ubuntu 18.04 / 20.04
- Unity environment: Banana.x86_64 provided by Udacity can be downloaded [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip).

### Model

The project has been solved with the help of a deep neural network consisting of **5 linear layers**:

- one input layer of size 37 (=size of the state space).
- three hidden layers of size 128 each.
- one output layer of size 4 (= size of the action space).
The activateion function is **Relu**.
The **dropout probability is 0,1** (=10%).

### Agent

The project has been solved with a **Double-DQN** agent. 

- The replay buffer size is 100000
- The batch size is 32
- Gamma = 0.99
- Tau = 0.01 (for soft update of target parameters)
- Learning rate = 0.0005
- The weights will be updated every 4 steps
The Implementation of the Double-DQN agent is done according to [`Mnih et al., 2015`](https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf) and  [`van Hasselt et al., 2015`](https://arxiv.org/pdf/1509.06461.pdf)

### Training

The maximum number of training episodes is 2000.
The maximum number of timesteps per episode is 1000.
The starting value of epsilon, for epsilon-greedy action selection is 1.0.
The minimum value of epsilon is 0.1
The multiplicative factor (per episode) for decreasing epsilon is 0.995.

### Result

The result of the training is shown in the plot below: 

![Training results](./images/training_results_ddqn_128_128_128.png  "Training results")

For training purposses the score has been raised to +14.

### Further improvements

The agent can be further improved by incorporating the Dueling Double-DQN and the Prioritized Experience Replay techniques. 
