# Menace

Menace is a tic-tac-toe (noughts and crosses) machine-learning system designed
to learn how to play. I first came across it on Matt Parker's [StandupMaths
YouTube channel here](https://www.youtube.com/watch?v=R9c-_neaxeU). Links to
more details are there.

The machine in the video can only play first. For the machine to play second,
an entirely different set of board states and matchboxes are needed.

It struck me that you could set up two machines, one to go first and one to go
second, and play them against so they both learn how to play. In this
implementation the machines play each other 1000 times, and then play the human
twice, once as machine first, once as human first.

## Learning summary

The short description is:
- There is a matchbox for each possible board state
- Beads in the matchbox represent each possible move the machine can make
- To make a move, a random bead is chosen
- If there are no beads left in the box the machine resigns
- At the end of the game, beads are added or removed from all matchboxes
  involved:
    - For a win, add three more beads of the colour that led to a win
    - For a draw, add one bead of the colour that led to a win
    - For a loss, remove a bead of the colour that led to the loss

## Statistics

After the initial training sequence, statistics are printed showing the numbers
of wins, losses and draws. During the game the machine displays a summary of the
virtual beads in the boxes before it makes its choice.
