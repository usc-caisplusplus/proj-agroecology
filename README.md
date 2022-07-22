# Project Agroecology #
---
Modern western agriculture heavily relies on monocrops, where a singular crop is grown in a field. These practices require widespread clearing of local wildlife, leave soil malnourished and lead to lower yields over time. Polycultures, where multiple crops symbiotically grow together, leverage microclimates to produce a more sustainable food system long-term. However, knowledge surrounding polycultures are localized to indigenous knowledge systems. Project Agroecology aims to build a reinforcement learning (RL) agent to systematically predict crop placement and determine optimal polyculture composition. This project is in collaboration with Dr. Barath Raghavan and has been active since Spring 2022. Currently, a separate team is developing a 3D plant simulator environment. CAIS++'s role is to develop RL agents that will eventually interface with this environment.
## Summary of Progress Spring 2022 ##
- Gained experiece applying reinforcement learning techniques
- Developed intuition on nature of problem

## Sandbox Environment ##
We have defined a `Plant` class that has the following attributes:
- Type (corn, beans, squash, etc.)
- Age (squash~60 days, corn > 60)

The environment, `Field`, displays crops on 2D field once plant maturity is reached.
The reward function determines the calorie reward at end of the season using the following factors. The end goal is to plant bean, maize, and squash (Three Sisters) within proximity of each other:
- caloric intake of plants
- Small crowding penalty
- Reward for planting squash, bean, and maize in proximity

Each action is determed by planting a specified number of crops at one time step.

## Models ##
We have deployed the following models.
- `DQN` - Deep Q Network
- `QL` - Q Learning 
- `MCTS` - Monte Carlo Tree Search
- `Genetic` - Genetic algorithm

## Future Steps ##
- Literature review to find more complex environment
- Test `Stable-Baselines3` on `Field` 
- Explore using RL on 3D environment


