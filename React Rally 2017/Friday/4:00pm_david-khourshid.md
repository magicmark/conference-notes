# David Khourshid

DFA = Deterministic Finite Automata

Write UI as a State Transition Diagram
- May already exist as "User Flowcharts" (eg) from design

Codify State Transition Diagram in an object

Function to map current action and event to next "state"
- Pass to setState

Map element contents/states based on state key

Can be represented as a visual graph [insert link here]

Testing *can* more powerful (auto generated tests based on state)

## Downsides
State Explosion: adding one state = more complexity

## Hierarchical States
If can't find the next state, go to the next diagram, which may contain the state

## Concurrent States
Could be in multiple states
Could be orthogonal = managing separate bits of state

## Resources
Constructing the User Interface with Statecharts
Pure UI
