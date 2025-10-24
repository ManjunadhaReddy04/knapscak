AIM
To Implement 0/1 Knapsack problem using Dynamic Programming and find its complexity.

ALGORITHM

1.	Consider the same cases as mentioned in the recursive approach. 
2.	In a DP[][] table let’s consider all the possible weights from ‘1’ to ‘W’ as the columns and weights that can be kept as rows. 
3.	The state DP[i][j] will denote the maximum value of ‘j-weight’ considering all values from ‘1 to ith’. So if we consider ‘wi’ (weight in ‘ith’ row) we can fill it in all columns which have ‘weight values > wi’. Now two possibilities can take place: 
a.	Fill ‘wi’ in the given column.
b.	Do not fill ‘wi’ in the given column.
4.	Now we have to take a maximum of these two possibilities, formally if we do not fill the ‘ith’ weight in the ‘jth’ column then the DP[i][j] state will be the same as DP[i-1][j] but if we fill the weight, DP[i][j] will be equal to the value of ‘wi’+ value of the column weighing ‘j-wi’ in the previous row. 
5.	So we take the maximum of these two possibilities to fill the current state.
