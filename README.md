# DDPG

End to End Mobile Robot Navigation using DDPG 
(Continuous Control with Deep Reinforcement Learning) based on Tensorflow + Gazebo

Goal: Let robot(turtlebot) navigate to the target(enter green circle)

Input: 10 laser finding
Output: 2 action (linear velocity [0 - 1] / angular velocity [-1 - 1]) (action_dimension = 2)

Algorithm: DDPG (Actor with batch normlization Critic without batch normlization)
Training env: gazebo

Source code: https://github.com/floodsung/DDPG

Testing result:

Following video is my testing result when action dimension = 1 (only control angular velocity / linear velocity = o.5 m/s)

result is good enough
![image](https://github.com/m5823779/DDPG/blob/master/github.gif)

Following video is my testing result when action dimension = 2 (control both linear velocity and angular velocity)

result is quite bad
output will saturate
![image](https://github.com/m5823779/DDPG/blob/master/github2.gif)


Following vedio is output
First is linear velocity, second is angular velocity
the output is always converge to 0


![image](https://github.com/m5823779/DDPG/blob/master/github3.gif)


Problem:

When action dimension = 2
action will be saturate(can't navigation)


"Have anyone meet this problem and already solved it?"




reference:

https://arxiv.org/pdf/1703.00420.pdf

https://github.com/floodsung/DDPG
