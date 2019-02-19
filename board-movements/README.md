**Problem**: Given a board of length D and N moves, calculate the number of possible solutions when you are allowed to move forward one step or stay in place (at the end of your last move, you want to be at the last position).

**Solution:** solution will be given recursively. We have a few base cases to take care of here: when the size of the board is 0, no matter how many moves we have, we only have the option to syau in place, and there is only one way to do that. If the board size is equal to the number of moves, there is also only one way to play—that is, to move forward at each step. However, if the number of moves is smaller than board length, there is no way to actually get to the end of the board, so the answer is 0. Other than that, the number of possible solutions is in the form (n, d) (n choose d), which can be written recursively as (n, d) = (n - 1, d) + (n - 1, d - 1). This will be the recursive step in our function.