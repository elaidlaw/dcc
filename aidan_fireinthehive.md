Oh no! There's a fire in the hive! Find your way from the top of
the honeycomb to the bottom as fast as you can to make it out before
you get cooked. Be careful! Some cells have more honey than others,
which will slow you down as you make your escape.

Your task will be to, given a honeycomb and the time to move through 
each of its cells, find the time of the fastest route from the top to 
the bottom.

A possible size 3 honeycomb may look like this:

         / \ / \ / \
        | 2 | 1 | 4 |
       / \ / \ / \ / \
      | 3 | 5 | 1 | 1 |
     / \ / \ / \ / \ / \
    | 1 | 6 | 7 | 2 | 4 |
     \ / \ / \ / \ / \ /
      | 8 | 1 | 2 | 3 |
       \ / \ / \ / \ /
        | 1 | 5 | 3 |
         \ / \ / \ /

You may start at any of the cells in the top row, and may finish in any of 
the cells in the bottom row. From each cell, you may move to its left or right
neighbor, or to its diagonally downward neighbors, but you CANNOT ever move 
upwards.

For exmple, on the example honeycomb, the fastest path would be the following:

         / \ / \ / \
        | 2 |*1*| 4 |
       / \ / \ / \ / \
      | 3 | 5 |*1*| 1 |
     / \ / \ / \ / \ / \
    | 1 | 6 | 7 |*2*| 4 |
     \ / \ / \ / \ / \ /
      | 8 |*1*|*2*| 3 |
       \ / \ / \ / \ /
        |*1*| 5 | 3 |
         \ / \ / \ /

The honeycomb will be represented as a list of lists, with each inner list
corresponding to a row, from top to bottom. For example, the above honeycomb
would be represented as follows:

    [[2, 1, 4],
    [3, 5, 1, 1],
    [1, 6, 7, 2, 4],
    [8, 1, 2, 3],
    [1, 5, 3]]

You will write the method run(), which will take in a list of
lists of integers representing the honeycomb and return the time it takes to 
traverse the fastest path.

examples:

    solution.run([[4]]) == 4
    solution.run([[2, 3], [4, 2, 1], [3, 1]]) == 5
    example_comb = [
        [2, 1, 4],
        [3, 5, 1, 1],
        [1, 6, 7, 2, 4],
        [8, 1, 2, 3],
        [1, 5, 3]]
    solution.run(example_comb) == 8

NOTE: Some of the honeycombs your code will be tested on are pretty large. Your
solution needs to run in polynomial time in the size of the input. My solution is
O(n^2) where n is the side length of the honeycomb.