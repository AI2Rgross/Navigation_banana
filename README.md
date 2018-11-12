# Navigation Project


## Introduction
In this project, I trained an agent to navigate and collect bananas in a large, square world.

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of my agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:

    0 - move forward.
    1 - move backward.
    2 - turn left.
    3 - turn right.

The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.


## Requirement

As I am working under ubuntu 16.04, I will give you a few tips to make it run smoothly. But, I recommand you to follow the instruction on the Udacity DRL github: https://github.com/udacity/deep-reinforcement-learning/blob/master/p1_navigation/README.md. Especially, if you work under a different OS.

You can also have a look at:
https://github.com/udacity/deep-reinforcement-learning/blob/master/README.md
 

### For ubuntu 16.04

dowload the repo:
https://github.com/AIRgr/Navigation

dowload the file https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip
Place the file in the GitHub repository, in the Navigation/ folder, and unzip the file.


### Tips to prepare the environement
 
- Python 3
Check if you have a one of the following python versionn: 3.5.x or 3.6.x
If not, it s time to install it using the "sudo apt-get install" command.

- pip 3
You will also need to install pip for python 3. 
sudo apt-get install python3-pip

- Pytorch:
check this link https://pytorch.org and get the command to install pytorch

- Ml agents for unity
First dowmload Ml agent ripo on https://github.com/Unity-Technologies/ml-agents.git

- Install ml agent:
pip3 install .

if there is any trouble have a look at:
https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Installation.md

- Install unity
pip3 install unity

- ipython
In order to run the notebook with python 3 also install ipyton.
sudo pip3 install ipython[all]


### Requirements for the navigation project
 
Go inside the Navigation repo, and open a terminal in order to install the requirements:
pip3 install -r requirements.txt
Then run the next command to open a notebook:
ipython3 notebook

click on Navigation.ipynb to open it.
Try to run the first cell where the libraries are imported to check if UnityEnvironment is well installed.

Then, in the next cell correct the path of the Banana.x86_64 and try running it.
env = UnityEnvironment(file_name="the_path_here/Banana_Linux/Banana.x86_64")

Now everything is ready to either train your own solution or run the pre-computer solution.


## My files

Main files of the repository:

    - The main part of the code: point for starting the environment, train the agent or test a solution.
        Navigation.ipynb

    - the Agent class with dqn, ddqn, and othes basic functions to interact with the environment. The Replay buffer class.
        agent.py

    - The Pytorch neural networks and dueling network used to approximate the Q-value functions used by the agent.
        model.py

    - the weights of the pytorch model for dqn,ddqn, dueling dqn and dueling ddqn of the solved environment.
        dqn_checkpoint.pth  (dqn)
        ddqn_checkpoint.pth (ddqn)
        duel_dqn_checkpoint.pth (dqn + dueling network)
        duel_ddqn_checkpoint.pth (ddqn + dueling network)
 
    - Installation notes and tips, brief description of the project
        README.md

    - Udacity original readme for instalation of the envirionment.
        Udacity_README.md

    - My notes about DQN, DDQN, Duelling network
        Report.pdf

The code I developped to solve the banana environement is based on the dqn exercice from the UDACITY DRL github available here: https://github.com/udacity/deep-reinforcement-learning. 
