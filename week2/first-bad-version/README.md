1. Problem
   The task is to find the first bad version among n versions.
   Versions are ordered from 1 to n. Once a version becomes bad, all following versions are also bad. The goal is to find the first bad version while making as few calls to isBadVersion() as possible.
2. Approach
   I use binary search.

   I keep two boundaries:

   left - the beginning of the search range;
   right - the end of the search range.

   For each iteration, I calculate the middle version.
   If isBadVersion(mid) returns true, mid can be the first bad version, so I move the right boundary to mid.
   If isBadVersion(mid) returns false, mid and all versions before it are good, so I move the left boundary to mid + 1.
   The search continues until left and right become equal. At that point, this position is the first bad version.
3. Time Complexity
   Time Complexity: O(log n)
   Binary search eliminates approximately half of the remaining versions after each check. Therefore, the number of checks grows logarithmically as the number of versions increases.
4. Space Complexity
   Space Complexity: O(1)
   The algorithm uses only a few variables (left, right, and mid). It does not create any additional data structures, so the extra memory remains constant.
5. Reflection / Improvement
   Binary search already achieves O(log n) time complexity and O(1) additional space.

   To improve the solution further, the problem itself would need to provide additional information about which versions are bad. Without such information, reducing the number of checks below logarithmic complexity is not possible with this approach.