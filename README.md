# Mind-The-Gap

## Problem

This is a whiteboard coding challenge that I recently attempted. The task is to calculate the number of "cycles" that are required to run an array of processes. 

## Set up
There is one input for this problem:
  * *processes* - an array of integers that represent computer processes

## Problem
A computer is given an array of processes to run. Running each cycle consume one cycle. So for example, the array of 
[0, 1, 2, 3] will return the integer 4 denoting four cycles to run the four different processes. 

However - and this is the catch of the entire problem - the computer cannot run the exact same process unless there is a minimum gap between the last and current instance. There must be a gap of at least five spaces since the last time it ran that process.  So if the user inputs the array of processes of [0, 1, 2, 3, 3] the computer will have to inject a *gap* of five between the first and second running of 3. In this scenario, the computer will process the array of [0, 1, 2, 3, 3] as [0, 1, 2, 3, -, -, -, -, -, 3], which equals 10 cycles for a five process array. 

There doesn't need to be a gap injected if it is the *first* time the computer runs a process or if there is already 
a minimum of five spaces between the last and current instance. So the array of [3, 4, 1, 2, 9, 7, 3] will not 
require additional cycles because there is already a five-space gap between the 3s. The function will return 7 in
this example. 

## assumptions
 The array contains unsorted, non-unique elements. (Don't sort the array or you'll screw everything up).
 
 ## example
 To solve this problem, I created the following example.
 * processes = [0,1,2,3,3,1,0,4,3,2,4]
 * expected output = 19
 * Illustrating the extra cycles injected into this array: [0, 1, 2, 3, -, -, -, -, -, 3, 1, 0, 4, -, -. 3, 2, -, 4]
 
 The desired output should be 19 - 1 cycle for each of the 11 processes in the array, plus 5 more for the imposed gap between the first and second 3s, plus 2 more for the imposed gap between the second and third 3s, and plus 1 more for the gap between the first and second 4s. 

 The solution does not need to return the modified array, only the integer of the total number of cycles required. 


## Added Wrinkle
For an extra challenge, solve the problem where the gap is variable. Instead of a hard-set 5 cycle gap, modify the function so the user can set the gap length as an input.


## solution 
My solution is in the other file in this repository. There is a working Python function along with comments that explain my thought process. Best case runtime is O(n) and space complexity is O(n). If you come up with something better, please let me know.
