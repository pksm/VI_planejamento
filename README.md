## Probabilistic Planning
### Value Iteration Algorithm

Value Iteration (VI) is a method of computing an optimal Markov Decison Process (MDP) policy and its value.

Along with the algorithm and parser, two test domains are provided, Navigation and Tireworld.

#### Usage
```
python3 valueiteration.py navigation_instances/navigation01.net
```

#### Sample output
```
>> Policy
robot-at-x01y01 -> move-north
robot-at-x01y02 -> move-north
robot-at-x01y03 -> move-east
robot-at-x02y01 -> move-west
robot-at-x02y02 -> move-north
robot-at-x02y03 -> move-east
robot-at-x03y01 -> move-west
robot-at-x03y02 -> move-north
robot-at-x03y03 -> move-east
robot-at-x04y01 -> move-west
robot-at-x04y02 -> move-north
robot-at-x04y03 -> move-south
broken-robot -> move-south

>> Time: parsing = 0.0030, solving = 0.1391
```

### LRTDP Algorithm

Labeled Real-Time Dynamic Programming (LRTDP) is an asynchronous value iteration algorithm in which a single state is selected for update in each iteration, we keep track of the states over which the value function has converged and avoid visiting those states again.

Along with the algorithm and parser, two test domains are provided, Navigation and Tireworld.

#### Usage
```
python3 lrtdp.py navigation_instances/navigation01.net
```

#### Sample output
```
>> Policy
robot-at-x04y01 -> move-west
robot-at-x04y02 -> move-north
broken-robot -> move-south
robot-at-x03y01 -> move-west
robot-at-x02y01 -> move-west
robot-at-x01y01 -> move-north
robot-at-x01y02 -> move-north
robot-at-x01y03 -> move-north
robot-at-x02y03 -> move-north
robot-at-x02y02 -> move-north
robot-at-x03y03 -> move-north
robot-at-x03y02 -> move-north

>> Time: parsing = 0.0000, solving = 0.1000
```