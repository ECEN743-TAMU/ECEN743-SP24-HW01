# ECEN 743: Reinforcement Learning - Assignment 1

## Overview

1. You have to submit a PDF report and your code to Canvas.
2. Put all your files (PDF report and code) into a **single compressed folder** named `Lastname_Firstname_A1.zip`.
3. Your PDF report should include answers and plots to all the questions. This can be achieved through:
    * If you are proficient with `matplotlib` and `LaTex`, you can export all your plots and write a report in `LaTex` (Microsoft Word is also fine). The university provides free premium Overleaf service to students.
    * You can learn about `nbconvert` which is a python package that helps convert jupyter notebook to other format (including PDF). Here is the [**link**](https://github.com/jupyter/nbconvert).
    * As a last resort, you can also save the Jupyter Notebook as an `html` file. Open it using your favorite browser and print to PDF.
4. This homework is self-containted in one Jupyter notebook. In your `zip`, we expect only your PDF report and **one** Jupyter notebook.

## Installation Intructions

1. If you wish to complete this assignment locally (not on Google Colab), you need to install Jupyter Notebook. You can do  
```
pip install jupyter notebook
```
2. In this assignment, you will play around with the famous `FrozenLake` environment. Please install Gymnasium (you can read more about Gymnasium [here](https://gymnasium.farama.org/)).
```
pip install gymnasium
```
3. It is strongly advised that you learn how to use virtual environment for Python. It creates an isolated environment from the system Python or other Python releases you have installed system-wide. It helps you manage Python packages in a clean fashion and allow you to only install necessary packages for particular projects. An exemplary, lightweight virtual environment module is `venv` [(link)](https://docs.python.org/3/library/venv.html). Your python distribution is likely to include it by default. If not, for example on Ubuntu, you can install it by
```
sudo apt-get install python3-venv
```

## Assignment
In this assignment, you will implement planning (dynamic programming)  algorithms on the `FrozenLake` environment from Gymnasium [(Link)](https://gymnasium.farama.org/environments/toy_text/frozen_lake/).

1. **Q-Value Iteration (QVI):** Implement Q-value iteration on the frozen lake environment.  
    (a). What is the optimal policy and value function?  
    (b). Plot $U_k = ||Q_k-Q_{k-1}||,$ where $Q_k$ is the Q-value during the $k^{\mathrm{th}}$ iteration.  
    (c). Use the `fancy_visual` function to plot the heat maps of the optimal policy and value function.  

2. **Policy Evaluation:** Consider the following polices: $(i)$ the optimal policy obtained from  QVI, and $(ii)$ a uniformly random policy where each action is taken with equal probability. Compute the value of the  these polices using:  
    (a). By solving a linear systems of equations.  
    (b). By the iterative approach.    
    (c). Which method is better and why?  

3. **Policy Iteration (PI):** Implement policy iteration on the frozen lake environment.  
    (a). What is the optimal policy and value function?  
    (b). Compare the convergence of QVI and PI.   
