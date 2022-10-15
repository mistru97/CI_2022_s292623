# Lab1 report:

## State:

- State._data is a tuple like: ```(set, list)```
  - ```set``` is a set that contains the number between 0 and N - 1 that has been found.
  - ```list``` is a list of the remaining possible P lists of integers.

## Results

| N    | # of elements Ls | # of nodes | Algorithm   |
| :--- | :--------------: | :--------: | :---------- |
| 5    |        5         |     21     | A*          |
| 10   |        10        |    257     | A*(beam=15) |
| 20   |        24        |    1975    | A*(beam=20) |
| 100  |       271        |    412     | Depth first |
| 500  |        x         |     x      | x           |
| 1000 |        x         |     x      | x           |

