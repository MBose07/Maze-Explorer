# Maze-Explorer
# Overview
[t2c_maze_explorer.v] (https://github.com/MBose07/Maze-Explorer/blob/main/code/t2c_maze_explorer.v) implements a hardware-based maze exploration controller in Verilog. The design models a maze-solving bot that navigates using three wall sensors (left, mid, right) and outputs movement commands. The control logic is built as a finite state machine (FSM) with internal position tracking and visited-cell marking to ensure systematic exploration and dead-end handling.

# Core Logic - Dead-End Filling with DFS Navigation
The maze solver uses a DFS-based traversal strategy augmented with dead-end filling. Whenever the robot encounters a dead end, it reverses direction and marks each visited cell along the backtracking path as a dead end until it reaches a junction. This guarantees that fully explored paths are pruned from future decisions, enabling efficient and loop-free maze exploration.
