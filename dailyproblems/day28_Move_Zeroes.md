###### 283\. Move Zeroes



Given an integer array nums, move all 0's to the end of it while maintaining the relative order of the non-zero elements.



Note that you must do this in-place without making a copy of the array.



&nbsp;



Example 1:



Input: nums = \[0,1,0,3,12]

Output: \[1,3,12,0,0]

Example 2:



Input: nums = \[0]

Output: \[0]

&nbsp;



Constraints:



1 <= nums.length <= 104

-231 <= nums\[i] <= 231 - 1

**Solution:**

class Solution {

&nbsp;  

&nbsp;   public void moveZeroes(int\[] a) {

&nbsp;       int n=a.length;

&nbsp;       int j=0;

&nbsp;       for(int i=0;i<n;i++){

&nbsp;           if(a\[i]!=0){

&nbsp;               int temp=a\[i];

&nbsp;               a\[i]=a\[j];

&nbsp;               a\[j]=temp;

&nbsp;               j++;

&nbsp;           }

&nbsp;       }

&nbsp;       



&nbsp;   }

}

