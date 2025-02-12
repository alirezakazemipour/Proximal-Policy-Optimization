# PPO

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)  

Implementation of the proximal policy optimization on Atari environments. All hyper-parameters have been chosen based on the paper.
> For continuous domain (Mujoco) [look at this](https://github.com/alirezakazemipour/Mujoco-PPO).

## Dependencies
- gym == 0.17.2  
- numpy == 1.19.1  
- opencv_contrib_python == 3.4.0.12  
- torch == 1.4.0  
- tqdm == 4.47.0  

## Installation
```shell
pip3 install -r requirements.txt
```

## Usage
The training requires a suitable (not necessarily a 1080 Ti or a 2080 RTX Nvidia gpu :grin:) gpu-enabled machine. Google Colab provides what is enough to train such an algorithm but if you a more powerful free online gpu provider, take a look at: [paperspace.com](paperspace.co).  
- **To run the code**:  
```shell
python3 main.py
```
- **If you want continue the previous training procedure, turn `LOAD_FROM_CKP` to `True` otherwise, the training would be restarted from scratch**.  
- **If you want to test the agent, simply turn `Train` flag to `False`**. There is a pre-trained model in the _Pre-trained models_ directory that you may use to see agent plays.  

## Environments tested
- [x] Pong
- [x] Breakout 
- [x] SuperMarioBros-1-1 [mario branch.](https://github.com/alirezakazemipour/Proximal-Policy-Optimization/tree/mario)
- [ ] MsPacman

## Demo
Breakout | Mario
:-------------:|:---------:
![](demo/Breakout.gif)| ![](demo/mario.gif)

## Result
- **Following graphs are breakout environment's result**.  
<p align="center">
  <img src="Results/Result.jpg" height=600s>
</p>  

## Reference
[_Proximal Policy Optimization Algorithms_, Schulman et al., 2017](https://arxiv.org/abs/1707.06347)

## Acknowledgement
[@OpenAI](https://github.com/openai) for [Baselines](https://github.com/openai/baselines).  
[@higgsfield](https://github.com/higgsfield) for [his ppo code](https://github.com/higgsfield/RL-Adventure-2/blob/master/3.ppo.ipynb).  
[@upiven](https://github.com/uvipen) for [mario-ppo](https://github.com/uvipen/Super-mario-bros-PPO-pytorch).  
[@roclark](https://github.com/roclark) for [custom reward wrapper](https://github.com/roclark/super-mario-bros-dqn).