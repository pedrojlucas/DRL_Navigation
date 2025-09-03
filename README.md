# Description of the environment
This environment created by Unity ML is one of the nice playgrounds to test Deep Reinforcement learning algorithms. We are going to solve it using an implementation of DQN.

![banana](https://github.com/user-attachments/assets/0d857db8-e934-4967-ba42-725068c9ae50)

Animated scene of a virtual environment with scattered yellow and purple objects resembling bananas.

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:

0 - move forward.
1 - move backward.
2 - turn left.
3 - turn right.
The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

# How to prepare your system to execute

## Clone the github repository

git clone https://github.com/pedrojlucas/DRL_Navigation

## Install all the dependencies in a Anaconda or miniconda environment

$ conda create -n dqn python=3.6
$ conda activate dqn
$ pip install -r requirements.txt

## Install Unity environment

For this project, you will not need to install Unity - this is because we have already built the environment for you, and you can download it from one of the links below. You need only select the environment that matches your operating system:

* Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
* Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
* Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
* Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

Then, place the file in the cloned repository folder in your local machine, and unzip (or decompress) the file.

You will need to change the target folder in the Jupyter notebook file before executing it.
