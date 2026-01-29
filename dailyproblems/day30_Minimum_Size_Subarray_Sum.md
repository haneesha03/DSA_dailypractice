###### 209\. Minimum Size Subarray Sum

Solved

Medium

Topics

premium lock icon

Companies

Given an array of positive integers nums and a positive integer target, return the minimal length of a subarray whose sum is greater than or equal to target. If there is no such subarray, return 0 instead.



&nbsp;



Example 1:



Input: target = 7, nums = \[2,3,1,2,4,3]

Output: 2

Explanation: The subarray \[4,3] has the minimal length under the problem constraint.

Example 2:



Input: target = 4, nums = \[1,4,4]

Output: 1

Example 3:



Input: target = 11, nums = \[1,1,1,1,1,1,1,1]

Output: 0

&nbsp;



Constraints:



1 <= target <= 109

1 <= nums.length <= 105

1 <= nums\[i] <= 104



###### Solution:

class Solution {

&nbsp;   public int minSubArrayLen(int target, int\[] nums) {

&nbsp;       int minlen=Integer.MAX\_VALUE;

&nbsp;       int sum=0;

&nbsp;       int l=0;

&nbsp;       for(int r=0;r<nums.length;r++){

&nbsp;           sum+=nums\[r];

&nbsp;           while(sum>=target \&\& l<=r){

&nbsp;               minlen=Math.min(minlen,r-l+1);

&nbsp;               sum-=nums\[l];

&nbsp;               l++;

&nbsp;           }

&nbsp;       }

&nbsp;       return minlen==Integer.MAX\_VALUE?0:minlen;

&nbsp;   }

}

