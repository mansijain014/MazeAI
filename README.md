# MazeAI

### About
It is an application that uses AI to solve a maze using a reinforcement learning technique i.e. Q-Learning.
You can change the theme of the maze, customize the maze and choose the location of the goal as well.

### Required Packages
The application requirements are present in <code>requirements.txt</code>
If you have pip installed (which is there, if you installed python from the official website), install the packages using these commands in the command prompt.

    pip install pyglet
    pip install tkinter
    pip install matplotlib
    pip install numpy
    pip install threading
    pip install random
    pip install time

### What is Q-Learning?
Q-learning is an off policy reinforcement learning algorithm that seeks to find the best action to take given the current state. It’s considered off-policy because the q-learning function learns from actions that are outside the current policy, like taking random actions, and therefore a policy isn’t needed. More specifically, q-learning seeks to learn a policy that maximizes the total reward.

### Q-Table
A q-table is a matrix that follows the shape of [state, action] and we initialize our values to zero. We then update and store our q-values after an episode. This q-table becomes a reference table for our agent to select the best action based on the q-value.

### 3 Basic steps involved in updating the q-values
- The agent starts in a state (s1) takes an action (a1) and receives a reward (r1)
- The agent selects action by referencing Q-table with the highest value (max) OR by random (epsilon, ε)
- Update q-values in the q-table.

### The Formula Used
Q[state, action] = Q[state, action] + lr * (reward + gamma * np.max(Q[new_state, :]) — Q[state, action])

- Learning Rate: lr often referred to as alpha, can be defined as how much you accept the new value vs the old value. Above we are taking the difference between new and old and then multiplying that value by the learning rate. This value then gets added to our previous q-value which essentially moves it in the direction of our latest update.
- Gamma: It is a discount factor. It’s used to balance immediate and future rewards. From our update rule above you can see that we apply the discount to the future reward. Typically this value can range anywhere from 0.8 to 0.99.
- Reward: It is the value received after completing a certain action at a given state.

### Demo Screenshots

![](/demo/window1.png)
![](/demo/window2.png)
![](/demo/window3.png)
![](/demo/window4.png)
