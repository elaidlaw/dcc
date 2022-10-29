Problem: how many swaps will insertion sort take?

I hope you are all familiar with insertion sort. If not, just google it, it’s just a sorting technique. Sometimes arrays are too large to insertion sort because they are slow. Is there some way to check the number of swaps required? That is the problem we are trying to answer.

For example, on the input array [4, 3, 2, 1], we use 6 shifts to sort the array.

 Array     Shifts
[4,3,2,1]
[3,4,2,1]   1
[2,3,4,1]   2
[1,2,3,4]   3

Total shifts = 1 + 2 + 3 = 6