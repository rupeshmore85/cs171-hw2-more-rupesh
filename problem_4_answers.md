1. Briefly explain your technical choices. 
Your final visualization may differ significantly from you original sketch or only implement a subset of it, 
but ensure you document the tradeoffs you faced and the reasoning behind your choices.

Solution:

Reason behind the choice of Chord Layout:

1. Chord diagrams show relationships among a group of entities.
2. A chord diagram visualizes these relationships by drawing quadratic Bézier curves between arcs.
3. The chord layout is designed to work in conjunction with the chord shape and the arc shape. 
The layout is used to generate data objects which describe the chords, serving as input to the chord shape. 
The layout also generates descriptions for the groups, which can be used as input to the arc shape.

Technical choice: 
1. The implementation was much simpler and visualization is more appealing to the eye due to the interactions.
2. Less performance issue.