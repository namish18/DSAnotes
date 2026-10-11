# Sort an array consisting of 0s 1s and 2s
Input: An array consisting of only integers of 0,1 and 2
Task: Sort the array
### Brute 
Use any standard sorting algo like merge sort
TC: O(N log N)
SC: O(N)

### Better
Do one iteration and count the no. of 0s,1s and 2s
Then run the loop again as per the counts first put 0, then 1 and then 2s in the array
TC: O(2N)=O(N)

### Optimal (Dutch National Flag Algorithm)
We keep three variables low, mid and high
So we will have an initial condition in the array which we will follow to make the array sorted.
[0, low-1] -> 0s
[low,mid-1] -> 1s
[mid,high-1] -> unsorted
[high,n-1] -> 2s
We will initialize low and mid at 0 and high at n-1. 
Terminating condition: mid>high
the iteration will happen through mid variable
if(a[mid]=0) then swap(a[low],a[mid]) and low++ and mid++;
if(a[mid]=1) then mid++;
if(a[mid]=2) then  swap(a[mid],a[high-1]) and high --;


# Set Matrix Zeros
Input: Matrix of m,n size consisting of 0s and 1s
Task:  The cells which have 0s in it(initially), the entire row and column of those will be converted to 0

### Brute
Iterate through the matrix and then find the cells which have 0 then convert the 1s of the rows and columns of the cell to -1 (Converting it into 0 will confuse it with initial 0). then after make another iteration and convert the -1 into 0 now

TC: O(n^3) n^2 for iterating through the matrix and another n for converting rows or columns

### Better
keep two arrays as variables of m,n size for rows and columns respectively then change the flag of respective row and column variable. At the end iterate again and convert the 1s to 0s as per the variables

TC: O(n^2)
SC: O(n)

# Two Sum
Input: Array of integers
Task: Return the indexes of two elements which sums up to the target element

### Brute
For each element iterate through the array and find if the sum is same as targer element or not
TC: O(n^2)

### Better
Store a map and start iterating through the array. check if the (target - current element) integer is present in map or not. if not store the integer and its index. if its present then return the current index and the index present in the map
TC: O(n log n)
SC: O(n)


# Majority element (n/3 times)
Input: Array of n integers
Task: Return the integers which appear floor of n/3 times

### Brute
For every element iterate through the array and keep the counter and if the counter is more than the n/3 then add the integer to the solution list

### Better
Keep the hashmap and store the integer and counter in it. when the counter of an integers exceeds the n/3  then add it to the solution list.


# Find the missing and repeating numbers
Input: An array of n integers where all elements are from 1 to n and among them one element is repeated twice and one element is missing
Task: Find the repeating and missing elements

### Brute
Iterate through the entire array for each element and keep a counter for it. At the end counter will be 2 for repeating number and 0 for missing number
TC: O(n^2)

### Better
Keep an hasharray and store the counter on the indexes as you iterate through the array and at the check the indexes and return the index number which has 2 and 0 values in it
TC: O(n logn)
SC: O(n)

### Optimal
Take X and Y as repeating and missing number
find the sum and squared sum of elements from 1 to n.
Find the sum and squared sum of array elements.
The difference between each sum and squared sum will give two equations and then it is just two variables two equation problem.
TC: O(n)