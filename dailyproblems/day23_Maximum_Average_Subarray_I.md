##### 643\. Maximum Average Subarray I

You are given an integer array nums consisting of n elements, and an integer k.



Find a contiguous subarray whose length is equal to k that has the maximum average value and return this value. Any answer with a calculation error less than 10-5 will be accepted.



&nbsp;



Example 1:



Input: nums = \[1,12,-5,-6,50,3], k = 4

Output: 12.75000

Explanation: Maximum average is (12 - 5 - 6 + 50) / 4 = 51 / 4 = 12.75

Example 2:



Input: nums = \[5], k = 1

Output: 5.00000

&nbsp;



Constraints:



n == nums.length

1 <= k <= n <= 105

-104 <= nums\[i] <= 104

**Solution:**

class Solution {

&nbsp;   public double findMaxAverage(int\[] nums, int k) {

&nbsp;       int sum=0;

&nbsp;       for(int i=0;i<k;i++) {

&nbsp;           sum+=nums\[i];

&nbsp;       }

&nbsp;       int max=sum;

&nbsp;       for(int i=k;i<nums.length;i++){

&nbsp;           sum=sum+nums\[i]-nums\[i-k];

&nbsp;           max=Math.max(sum,max);

&nbsp;       }

&nbsp;       return (double)max/(double)k;

&nbsp;   }

}

