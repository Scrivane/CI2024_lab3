# CI2024_lab3
thanks to Emanumele Carelli for the help , he gave me the the base fuction to calculate linear conflict distance 


To solve the n-puzzle problem , it's implemented A* alghorithm using as heuristic for the cost the linear conflict distance.
Sometimes it took to long to run and vscode would crash before a good solution was found. To impove that for big puzzle , the alghorithm first finds the moves to get to first row(or column) in current state equal to the solution , then it resizes the problem by not moving in that row (or column) anymore.
As you can see in the table this Firstcut alghorithm maneged to find the solution where normal A* didn't . Where both alghoritm works ,A* finds a solution with less moves but with more evaluated states then using Firstcut .


results 

| Dimension | Number of Random Steps | Seed  | Firstcut | Moves | Evaluated |
|-----------|-------------------------|-------|----------|------|-----------|
| 3x3       | 100003                 | 43242 | no       | 24   | 679       |
| 4x4       | 100003                 | 43242 | yes      | 69   | 230221    |
| 4x4       | 100003                 | 43242 | no       | *    | *        |
| 4x4       | 100003                 | 4     | no       | 47   | 1003783   |
| 4x4       | 100003                 | 4     | yes      | 51   | 63216     |

* = vscode crashes before it finds a solution

With higher dimensions , it works only if Number of Random Steps is low . It also works for non quadratic puzzles for examples 4x3 or 3x4.