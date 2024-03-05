<h1> PACMAN Q-LEARNING </h1>

<p align="justify">Implementing reinforcement learning for an agent and crawler. Both learn by exploring different paths to reach the goal state. Ultimately, both are able to find optimal paths. We can try both manual paths or simulate a number of episodes.</p>

<p align="justify">The following functions are essential components of the algorithm implemented in qlearningAgents.py file.</p>

<h4>1.getQValue:</h4>
<p align="justify">The getQValue function has been implemented in a way such that at first, we check if the given (state, action) pair is present in qvalues dictionary.  If present, the respective value Q-value is returned. Else, we return 0.0.</p>

![Screenshot 2024-03-05 114717](https://github.com/ChiragRadhakrishna43-7/Pacman_QLearning/assets/121251823/ffe201b8-9256-47fe-b32e-b53db58daf92)

<h4>2.computeValueFromQValues:</h4>
<p align="justify">We have implemented the computeValueFromQValues function as follows:<br/>
Firstly, we call the getLegalActions() method to determine the possible actions that can be performed at the state. If there are no actions then the function call completes by returning 0.0. If actions can be performed, we iterate over all possible actions and track the maximum Q-value. This Q-value is returned which indicates the value of that state.</p>

![image](https://github.com/ChiragRadhakrishna43-7/Pacman_QLearning/assets/121251823/aa517f22-01a7-48bc-871b-0e7f2a95ff64)

<h4>3.computeActionFromQValues:</h4>
<p align="justify">Like the computeValueFromQValues() function, we obtain the actions that can be taken at the state using the getLegalActions() method. The getLegalActions method returns a list of possible actions that can be performed at the state. We iterate through each action and find the maximum value. In this process, we also store the associated action that corresponds to the maximum value found.
When the loop terminates, we have found the action that yields the maximum Q value and return it.</p>

![Screenshot 2024-03-05 115358](https://github.com/ChiragRadhakrishna43-7/Pacman_QLearning/assets/121251823/56f8fcde-9a02-4302-88b4-b7d9968bc3e5)

<h4>4.update:</h4>
<p align="justify">The update function helps update the Q-values. At first, the old Q-value is calculated. The old value is reduced by a factor of (1- self.alpha). We then compute the new Q-value by considering the observed reward and the estimated value of the next state. The Q-value for the (state, action) is obtained by adding the previous and new values.</p>
