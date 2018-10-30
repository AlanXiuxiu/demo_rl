##用深度强化学习方法玩Flappy Bird（利用DQN）

此前 DeepMind 在论文 Human-level Control Through Deep Reinforcement Learning 中提出 Deep Q-Network 的改良版本算法，本程序就是利用DQN训练模型，使其能够自主进行Flappy Bird游戏。

代码来自https://github.com/floodsung/DRL-FlappyBird，实现DQN网络只用了160行。只需要在程序目录内打开终端，输入

`python FlappyBirdDQN.py`

就可以运行已经训练好的模型，在玩游戏的同时，模型会进行强化学习并强化自己的能力。


## 环境配置

- Python 2.7 or 3
- Tensorflow 1.11.0
- Pygame
- Opencv-python

## 运行

`python FlappyBirdDQN.py`

## 模型保存

模型默认保存在saved_networks文件夹中。

此外，DQN网络默认选择Nature Version，可修改代码选择NIPS 2013 Version。通过修改DQN网络代码中的超参数，可以对模型进行调整。

