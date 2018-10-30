# demo_rl

此demo包含两个小游戏，一个是OpenAI Gym里的Cartpole，一个是FlappyBird。

## 强化学习方法玩Cartpole小游戏

OpenAI Gym是一个开发和测试强化学习算法的工具包，本程序简单利用DQN算法实现了自主玩OpenAI Gym环境下的Cartpole小游戏。

Cartpole游戏环境包括一个沿水平轴移动的车和一个固定在车上的杆子。 在每个时间步，你可以观察它的位置（x），速度（x_dot），角度（theta）和角速度（theta_dot）。 这是这个世界的可观察的状态。 在任何状态下，车只有两种可能的行动：向左移动或向右移动。游戏的目的是通过微调移动小车，使得杆子不倒下来，并且过程中小车不能移动出屏幕外。

从强化学习的角度来分析，Cart-Pole的状态空间有四个维度的连续值，行动空间有一个维度的两个离散值。

### 环境配置

- Python 2.7
- Tensorflow 1.11.0
- Gym

### 运行

`python run.py`

### 代码说明

`dqn.py`是DQN网络部分，是强化学习agent 的大脑，搭建神经网络利用了Tensorflow框架。而`run.py`定义了游戏以及训练的过程，同时强化学习的反馈reward也可在此代码中设置。



## 用深度强化学习方法玩Flappy Bird（利用DQN）

此前 DeepMind 在论文 Human-level Control Through Deep Reinforcement Learning 中提出 Deep Q-Network 的改良版本算法，本程序就是利用DQN训练模型，使其能够自主进行Flappy Bird游戏。

代码来自https://github.com/floodsung/DRL-FlappyBird，实现DQN网络只用了160行。只需要在程序目录内打开终端，输入

`python FlappyBirdDQN.py`

就可以运行已经训练好的模型，在玩游戏的同时，模型会进行强化学习并强化自己的能力。

### 环境配置

- Python 2.7 or 3
- Tensorflow 1.11.0
- Pygame
- Opencv-python

### 运行

`python FlappyBirdDQN.py`

### 模型保存

模型默认保存在saved_networks文件夹中。

此外，DQN网络默认选择Nature Version，可修改代码选择NIPS 2013 Version。通过修改DQN网络代码中的超参数，可以对模型进行调整。

