# Continuous-control-Agent

## 1. Project overview : 
A reinforcement learning agent( double-jointed arm) trained to maintain its position toward a target in a continuous environment.

<img src ="reacher.gif"/>

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

## 2.Task Description :
### 2.1 Environement : 


For this project, there are two separate versions of the Unity environment:
- The first version contains a single agent.
- The second version contains 20 identical agents, each with its own copy of the environment.  

The second version is useful for algorithms like [PPO](https://arxiv.org/pdf/1707.06347.pdf), [A3C](https://arxiv.org/pdf/1602.01783.pdf), and [D4PG](https://openreview.net/pdf?id=SyZipzbCb) that use multiple (non-interacting, parallel) copies of the same agent to distribute the task of gathering experience.  

#### 1: First Version

The task is episodic, and in order to solve the environment, your agent must get an average score of +30 over 100 consecutive episodes.

#### 2: Second Version

The barrier for solving the second version of the environment is slightly different, to take into account the presence of many agents.  In particular, agents must get an average score of +30 (over 100 consecutive episodes, and over all agents).  Specifically,
- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent.  This yields 20 (potentially different) scores.  We then take the average of these 20 scores. 
- This yields an **average score** for each episode (where the average is over all 20 agents).



## 2.2 Solving the environement: 
This taks is considered solved if we reach an average reward of +30.0 over 100 episodes or more.

## 3. Getting started 
If you wish to reproduce this work you need to setup the enviornement by following this section :

### 3.1 Clone this repository :
`
git clone https://github.com/kukeshajanth/Continous_Control_Project.git
`
### 3.2 Set up the environment : 

Please follow instructions from this [repo](https://github.com/udacity/deep-reinforcement-learning#dependencies)

### 3.3 Download the Unity Environment :

Select the Unity environement based on your opertaing system :

- Linux: click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
- Mac OSX: click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
- Windows (32-bit): click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
- Windows (64-bit): click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

Check out [this](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) link if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

(For AWS) If you'd like to train the agent on AWS (and have not enabled a virtual screen), then please use this [link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux_NoVis.zip) to obtain the "headless" version of the environment. You will not be able to watch the agent without enabling a virtual screen, but you will be able to train the agent. (To watch the agent, you should follow the instructions to enable a virtual screen, and then download the environment for the Linux operating system above.)

==> Place the downloaded file into your cloned project file .


## 4.  Project's structure :

- The agent.py file contains the general structure of the Reinforcement learning agent .
- The ddpg_model.py contains the actor's network code and the critic's network code.
- Continuous_control.ipynb  is the notebook used to train and evaluate the agent.
- Continuous Control Project.pdf is a report about the different aspects of this project.
