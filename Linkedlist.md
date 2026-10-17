# Reverse the Linkedlist
Input: A Linkedlist
Output: Head of the Linkedlist while being rotated k times
### Brute
For k times you will traverse through the linkedlist then point out the last element pointer to head and gthe second last poiner to null then make the last element new head
TC: O(n^2)

### Optimal
Go through one iteration and find the length of the linkedlist 
at the end point the last element pointer to the head and make it circular linkedlist
then find out k%length (in some case k an be more than length too)
l=length-(k%length)
now from the head go to lth node 
head=node.next
node.next=null
now return the head
TC:O(n)

