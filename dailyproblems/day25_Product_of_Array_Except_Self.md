##### 238\. Product of Array Except Self



Given an integer array nums, return an array answer such that answer\[i] is equal to the product of all the elements of nums except nums\[i].



The product of any prefix or suffix of nums is guaranteed to fit in a 32-bit integer.



You must write an algorithm that runs in O(n) time and without using the division operation.

Example 1:



Input: nums = \[1,2,3,4]

Output: \[24,12,8,6]

Example 2:



Input: nums = \[-1,1,0,-3,3]

Output: \[0,0,9,0,0]

&nbsp;



Constraints:



2 <= nums.length <= 105

-30 <= nums\[i] <= 30

The input is generated such that answer\[i] is guaranteed to fit in a 32-bit integer.



**Solution:**

class Solution {

&nbsp;   public int\[] productExceptSelf(int\[] nums) {

&nbsp;       int n=nums.length;

&nbsp;       int\[] res=new int\[n];

&nbsp;       res\[0]=1;

&nbsp;       for(int i=1;i<n;i++){

&nbsp;          res\[i]=res\[i-1]\*nums\[i-1];

&nbsp;       }

&nbsp;       int right=1;

&nbsp;       for(int i=n-1;i>=0;i--){

&nbsp;           res\[i]\*=right;

&nbsp;           right\*=nums\[i];

&nbsp;       }

&nbsp;       return res;

&nbsp;   }

}

