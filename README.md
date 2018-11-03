# Mind-The-Gap

## Problem

This is a whiteboard coding challenge that I recently attempted. The task is to sort a calculate the number of cycles that are required to process an array. 

## Set up
There is one input variable for this problem:
  * *cycles* - an array of integers that represent cycles

## Problem
A computer is given an array of processes to run. Running each cycle consume one cycle. So for example, the array of 
[0, 1, 2, 3] will return the integer 4 denoting four cycles to run the five different processes. 

However, the computer cannot run the same process in sequence. There must be a gap of at least five spaces since the last time it ran that process.  So if the user inputs the array of processes of [0, 1, 2, 3, 3] the computer will have to inject a *gap* of five between the first and second running of 3. In this scenario, the computer can only process the array of [0, 1, 2, 3] as [0, 1, 2, 3, -, -, -, -, -, 3], which equals 9 cycles for a four process array. 

## assumptions
 The array contains unsorted, non-zero, non-unique elements. (Don't sort the array or you'll screw everything up).
 
 ## example
 To solve this problem, I created the following example.
 * cycles = [0,1,2,3,3,1,0,4,3,2,4]
 * output = 20
 
 The desired output should be 20 - 1 cycle for each of the 11 processes in the array, plus 5 more for the imposed gap between the first and second 3s, plus 2 more for the imposed gap between the second and third 3s, and plus 3 more for the gap between the first and second 4s. 


## Added Wrinkle
For an extra challenge, solve the problem where the gap is variably. Instead of a hard-set 5 cycle gap, derive a 
function where the user can set the gap length.


## solution 
My solution is in the other file in this repository. There is a functioning Python function along with comments that explain my thought process. Best case runtime is O(n) and space complexity is O(n). If you come up with something better, please let me know.