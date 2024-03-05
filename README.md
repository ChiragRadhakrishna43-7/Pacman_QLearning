<p align="justify">Implementing reinforcement learning for an agent and crawler. Both learn by exploring different paths to reach the goal state. Ultimately, both are able to find optimal paths. We can try both manual paths or simulate a number of episodes.</p>

<p align="justify">The following functions are essential components of the algorithm implemented in qlearningAgents.py file.</p>

<h1>1.getQValue:</h1>
<p align="justify">The getQValue function has been implemented in a way such that at first, we check if the given (state, action) pair is present in qvalues dictionary.  If present, the respective value Q-value is returned. Else, we return 0.0.</p>
