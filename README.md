[//]: # (Image References)

[image1]: https://upload.wikimedia.org/wikipedia/commons/thumb/e/e8/Udacity_logo.svg/640px-Udacity_logo.svg.png
[image2]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif 
[image3]: https://user-images.githubusercontent.com/10624937/42386929-76f671f0-8106-11e8-9376-f17da2ae852e.png



### ![image1]
# Deep Reinforcement Learning Nanodegree
## Value Based Methods | Project: *Navigation*
### Author : Alberto García García

---

### Introduction


The problem to be solved in this project consists in training an agent through
reinforcement learning algorithms. The goal of the agent is to collect as many yellow bananas as possible while avoiding 
blue bananas in a large, square world. 

![image2]

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around 
agent's forward direction.  Given this information, the agent has to learn how to best select actions. Four discrete 
actions are available, corresponding to:

- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

Yellow bananas provides a reward of +1, while blue ones provide a reward of -1. The problem is considered to be solved 
when the average score of the last 100 episodes is equal or greater than 13 points.  

### Guidelines

The whole training of the agent is implemented in the Solution.ipynb notebook. You can either visualize the last
execution or run it by yourself. To do so, you can take the following steps:

1. Create (and activate) a new environment with Python 3.6.

   - Linux or Mac: 
	```bash
	conda create --name drlnd python=3.6
	source activate drlnd
	```
	- Windows: 
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```

2. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of 
OpenAI gym.
3. Install the dependencies in the `python/` folder.
   ```bash
   cd ./python/
   pip install .
   ```
4. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd`
environment.  
   ```bash
   python -m ipykernel install --user --name drlnd --display-name "drlnd"
   ```
5. Before running the notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. 

   ![image3]


### Results

The agent is able to solve the problem in 395 episodes. The weights of the deep Q-network are stored in 
`solution/agent.pth`. 
