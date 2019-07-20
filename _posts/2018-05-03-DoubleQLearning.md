---
layout: posts
title: Deep Double Q Learning
description: Deep reinforcement model that learns how to beat classic control problems
tags: Projects

header:
  teaser: assets/images/DeepQLearningMountainCar.jpg
---

## Q-Learning

In this project, I developed a reinforcement learning neural network model. Specifically, I implemented a Deep Double Q Learning model ([Link to paper](https://arxiv.org/pdf/1509.06461.pdf "Deep Reinforcement Learning with Double Q-learning")) originally produced and published by Google's company, [Deepmind](https://deepmind.com/ "deepmind.com"). 

<p align="center">
	<img src="/assets/images/DoubleQLearningFlowDiagram.png">
</p>
  
The Deep Double Q Learning model extends the idea of a classic reinforcement learning model called Q-Learning. In Q-Learning, the objective is to model every possible action-state pair to a reward. So given a state, and taking a specific action, a corresponding reward can be learned. In this sense, an agent (the model that is trained) can learn what is the best action to take at any given state to receive the highest reward.

<figure class="half">
	<img src="/assets/images/DeepQLearningRoomExample.jpg">
	<img src="/assets/images/DeepQLearningQtable.jpg">
	<figcaption>Intuition example: The objective is to get to state 5</figcaption>
</figure>


This approach is reasonable for environments that have a small, finite number of states, but this approach is not possible for games with an overwhelmingly unkonwn number of states. Essentially, a matrix consisting of rewards for every possible state and every possible action would need to be saved in a computer's memory. 

---

## Deep Q-Learning


This is where Deep Double Q Learning comes in to play. With this model, the action-state reward relationship can be learned through a neural network that learns what the best actions are at any given state. The inputs to the neural network are the states, and the outputs are the possible actions. Again, the objective is to learn what action to take that produces the largest amount of reward. This approximation can be modeled inside the neural network through the weights.


Training the model can be simplified to a 2 step process:

1. Form a memory of previous action-state reward relationships

2. Then update the weights by computing the error between an actual reward (randomly sampled from memory) and the corresponding approximated reward (from online model).
    
<p align="center">
	<img src="/assets/images/DoubleQLearningProcess.png">
</p>

---

## Results

### Training Moutain Car Game:
<video muted controls width="480" height="320">
  <source src="/assets/images/DeepQLearningTrainingMountainCar.mp4" type="video/mp4">
</video>


### Training Pole Cart Game:
<video muted controls width="480" height="320">
  <source src="/assets/images/DeepQLearningTrainingPoleCart.mp4" type="video/mp4">
</video>


While completing this project I was able to experiment with different tools to develop neural networks like:

* Keras
* Cafe
* Tensorflow
* OpenAI Gym

Overall, this project has made me acustomed to NN development tools and excited to see what other challenges can be solved using neural networks.

If you are interested in learning more about Deep Double Q Learning, check out my presentation on the Deepmind's published paper. [Link to presentation](https://github.com/jbocinsky/Big_Data_Project/blob/master/projectDocuments/presentation/DeepDoubleQLearningPaperSummary.pdf)

If you would like to check out the detailed project report, source code, or presentations, please check out my [github repository](https://github.com/jbocinsky/Big_Data_Project "Deep Double Q Learning Repository").


Thanks,  
James

---

