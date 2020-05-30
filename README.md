[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

# Deep-Reinforcement-Learning Projects - Navigation

### Introduction & goal of the project

The objective of this project is to *implement* and *compare* different agents (with different value functions) that navigate and collect bananas in a large, square world. The Unity environment is provided by [**Udacity**](https://www.udacity.com/). This is an extension of a project of the [Deep Reinforcement Learning Nanodegree](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893).

![Trained Agent][image1]

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

### Setup
The setup description applies to *Linux Ubuntu 18.04 / 20.04* with pre-installed *Anaconda*.

Create and activate a new conda environment named *drlnd* with *Python 3.6*:
```python
conda create --name drlnd python=3.6
conda activate drlnd
```
Clone the *Udacity Deep-Reinforcement-Learning-Nanodegree* GitHub repository:
```python
git clone https://github.com/udacity/deep-reinforcement-learning.git
```
Move into the python folder and install several dependencies:
```python
cd deep-reinforcement-learning/python
pip install .
```
This will install among others *unityagents* and *tensorflow 1.7.1*.

Now install the latest *PyTorch* version together with the *CudaToolkit 10.1*:
```python
conda install pytorch torchvision cudatoolkit=10.1 -c pytorch
```

To use *Jupyter Notebook* run the following code:
```python
conda install ipykernel jupyter
jupyter notebook
```

The Unity environment is provided by Udacity and can be downloaded [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip).

#### Setup conclusion

The project is implemented in `python 3.6` within a `jupyter notebook`. 

* ML framework: **`Pytorch 1.4.0`**
* CUDA: **`CUDAToolkit 10.1`**
* Operating system: **`ubuntu 18.04`**
* Unity environment: **`Banana_Linux/Banana.x86_64`** provided by Udacity

