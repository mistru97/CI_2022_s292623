# Lab3 report:

## Description:
Solution of the tasks given in the laboratory 3 to develop agents able to solve Nim game.
All the tasks are evaluated vs a pure random agent

## Task1:
As fixed rule agent I use this approach:
- always have a odd number of rows with one object
- if this rows are not odd reduce another row to one object
- else remove another row

this is to achive a fixed finale with the two agents forced to remove one row at each move. If when player have an odd number of active row then automatically has won.

I also implementent my version of nim-sum

Results:

- my fixed rule agent: ```expert player won vs random strategy 93.57% of matches```
- nim-sum agent: ```best strategy won vs random strategy 100.0% of matches```

## Task2:

As evolved rules agent I use this approach:
- a param ```change_strat_p``` to select which strategy use: it is a threshold [0, 1] to choose when to switch from a strategy to delete a number of objects(choosed by the other param) from the longest row and the fixed strategy used before
- a param ```reduce_row_p``` to reduce the longest row of a percentage between 1 and all the objects

The two params are adapted using a genetic algorithm with:
- `POPULATION_SIZE` = 50
- `OFFSPRING_SIZE` = 20

The fitness of the algorithm is the average winrate of ```K=10``` evaluations. An evaluation is the wr vs a pure random agent in ```NUM_MATCHES=100``` games with a ```nim_size``` variable from ```10``` to ```20```

Result:
- ```best param: {'change_strat_p': 0.7606715804580229, 'reduce_row_p': 0.9323175433902825}, wr: 96.5```

## Task3:
Implemented minmax algorithm with alpha beta pruning

Result:
- ```minmax player won vs random strategy 58.5% of matches```

The result is not good if we consider that is between 50-60% of wr versus a random opponent.