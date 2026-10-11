# Fractional Knapsack
Input: There are  three bags of particular weight an values and there is a limit of total weight u can carry
Task: Maximize the value within limit you can take fraction of one bag too

### Solution
Calculate the value per weight ratio. Keep it in descending order.
Then take the highest ratios in order if possible in full else fractional till you hit the limit
TC: (n log n+ n)
