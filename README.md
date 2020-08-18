[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"
[image2]: 

# DRL-continuous-control

![Trained Agent][image1]

 
## Objective

To train a [DDPG](https://arxiv.org/abs/1509.02971) agent to control a double-jointed robotic arm to move to target locations. 

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"


## Background

**Environment**: UnityML [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment. In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

**Observation Space**: The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm.

**Action Space**: Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

**Reward**: +0.1 point is provided for each step that the agents's hand is in the goal location.

To consider the problem to be solved, the agent need to get an average of 30+ over 100 consecutive episodes.

## Getting Start

### Repository

Clone the repository

```
https://github.com/wjlgatech/DRL-continuous-control.git .
```

### Unity Environment

1. Download the environment that match your system:


- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)


2.  Put the file in the `DRL-continuous-control/` folder, and unzip the file

### Jupyter Notebook

Open the Continuous-control.ipynb notebook

```
jupyter notebook Continuous-control.ipynb
```

## Code Overview

The code consists of the following modules

```
Continuous_Control.ipynb - the main notebook
ddpg_agent.py - defines the Agent that is to be trained
model.py - defines the ddpg model for the Actor and the Critic network
checkpoint_actor.pth - is the final trained Actor network
checkpoint_critic.pth - is the final trained Critic network
train.py - train the ddpg agent
test.py - test the performance of the trained agent
```

## Results
Environment is solved in 273 Episodes with	Average Score: 30.03. The average reward collected over 100 episodes is plotted as follow. 
![cont_control_scores](image2)
