The remaining figures resulting from all the simulation runs are hosted in this folder. 

The figures are named by their iteration number as well as the time at which the simulation stopped. 
The simulation starts at t=0, and ends either when convergence is reached (by proxy of all beliefs being in either [0,epsilon] or [1-epsilon,1]) or after 10^7 rounds. 
This means that figures with 't9999999' in the name indicate that those runs did not reach consensus in simulated time. 


n50 means that 50 agents were simulated
a30 means that the agents used a learning rate of alpha = 30
rad{x} means that the geometric random graph model used a radius = {x}

