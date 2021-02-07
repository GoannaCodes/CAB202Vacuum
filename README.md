# CAB202Vacuum
Using QUT CAB202 C Graphics library to create a simulation of a roomba cleaning trash off the floor.

`coll.c` contains code relating to pixel collision with several sprites\
`helpers.c` contains a small collection of helper functions to draw rectangles, formatted lines and sprites, obtain input (char & int) and erase rows if needed.

`Scratch.c` contains the main code so that all components can interact with one another
  - displays battery % of vacuum, time elapsed, current load in vacuum & total number of trash on screen
  - key shortcuts to pause, quit & reset simulation, tell vacuum to return to base, drop a piece of trash on screen, move vacuum to a specified location as well as change load & battery level of the vacuum
  - simulation behaviour based on certain conditions i.e. when the vacuum battery = 0, the game is paused & game over screen is displayed
`trashRestart.c` contains sprites for 3 different types of trash, as well as functions for:
  - clearing sprites off screen (when collected by vacuum)
  - drawing a certain number of each trash type
  - determining a random location for trash to be drawn
  - collision code to ensure trash doesn't overlap 
  - user prompt for how many of each trash item to be generated

`vacuumRestart.c` contains sprites for vacuum & based, as well as functions for:
  - random movement of the vacuum when not controlled
  - battery depletion
  - pausing vacuum movement 
  - manual vacuum movement with 'jkli' keys
  - drawing base & vacuum on screen
  
`coll.h`, `helpers.h`, `trash.h`, `vacuum.h` are helper files and contains function definitions to be used by other classes\
`makefile` executes object files (i.e. coll.o, Scratch.o), which are all used to run the simulation

`vacuum_test.bash` aides in testing expected behaviour of vacuum simulation. No manual input is required as inputs are provided in each test case. 
