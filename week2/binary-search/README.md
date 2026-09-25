1. Problem
   We are given a sorted array and a target value; using binary search, we need to find the target and output its index, or output -1 if it is not found.
2. Approach
   The solution uses binary search: first, we define the boundaries (start and end),
   int start = 0, end = nums.length - 1;
   then we set up a loop that continues as long as there are numbers to check.
   while (start <= end) {
   If the middle element matches the target, we finish; otherwise, we proceed—moving to the right half if the target is greater than the middle element, 
   or to the left half if it is smaller.
   if (nums[mid] == target) {
   return mid;
   }
   if (nums[mid] < target) {
   start = mid + 1;
   } else {
   end = mid - 1;
   }
3. Time Complexity
   Time Complexity: O(log n)
   The algorithm uses binary search. On each iteration, it checks the middle element and eliminates half of the remaining search range.
   The number of iterations grows logarithmically with the number of elements. Therefore, the time complexity is O(log n).
4. Space Complexity
   The algorithm uses only a fixed number of variables:
   Therefore, the space complexity is O(1).
5. Reflection / Improvement
   I think the solution is already optimal; making it more complex would result in worse performance.
