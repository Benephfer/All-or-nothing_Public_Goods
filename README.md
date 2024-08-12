# All-or-nothing_Public_Goods
Data for project on All-or-nothing Public Goods Game on Networks

The Model:
In this project we simulate the behaviour of 50 agents on a random (connected) geometric network playing an all-or-nothing public goods game.

Each agent that is in the game observes (privately) a random variable which is to be their payofff if all the agents in the game contribute to the public good. If even one agent does not contribute then no agents get this reward and instead get zero. An agent can secure a payoff of one by not contributing to the public good (defecting).

Agents track an estimate of how likely other agents are to contribute to the public good. They use simple exponential smoothing (also known as exponential moving average). Their action in a turn then simply is the myopic action maximising their one-turn expected reward.

The Data:
Each setting (radius in geometric random network model) was simulated 500 times and the agents belief averaged at the end of 10^7 rounds or until all agents beliefs are < 0.0001 or > 1-0.0001. For each simulation run under a setting (given in the name n = number of players (always 50), rad = radius in random geometric graph model, a = learning rate alpha of the simple exponential smoothing rule) we track the following statistics.

Est: Average estimate of the beliefs of all agents at the termination of the simulation
time: The number of rounds simulated (max 10^7 -1 because we start counting at 0)
max_d: maximum node degree in the graph instance
mean_d: average node degree in the graph instance
triangles: number of triangles in the graph instance
