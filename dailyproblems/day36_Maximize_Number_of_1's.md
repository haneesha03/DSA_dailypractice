###### Maximize Number of 1's

Given a binary array arr\[] containing only 0s and 1s and an integer k, you are allowed to flip at most k 0s to 1s. Find the maximum number of consecutive 1's that can be obtained in the array after performing the operation at most k times.



Examples:



Input: arr\[] = \[1, 0, 1], k = 1

Output: 3

Explanation: By flipping the zero at index 1, we get the longest subarray from index 0 to 2 containing all 1’s.

Input: arr\[] = \[1, 0, 0, 1, 0, 1, 0, 1], k = 2

Output: 5

Explanation: By flipping the zeroes at indices 4 and 6, we get the longest subarray from index 3 to 7 containing all 1’s.

Input: arr\[] = \[1, 1], k = 2

Output: 2

Explanation: Since the array is already having the max consecutive 1's, hence we dont need to perform any operation. Hence the answer is 2.

Constraints:

1 ≤ arr.size() ≤ 105

0 ≤ k ≤ arr.size()

0 ≤ arr\[i] ≤ 1

###### Solution:

class Solution {

&nbsp;   public int maxOnes(int a\[], int k) {

&nbsp;       // code here

&nbsp;       int l=0,maxlen=0;

&nbsp;       int n=a.length,count=0;

&nbsp;       for(int i=0;i<n;i++){

&nbsp;           if(a\[i]==0){

&nbsp;               count++;

&nbsp;           }

&nbsp;           while(count>k){

&nbsp;               if(a\[l]==0){

&nbsp;                   count--;

&nbsp;               }

&nbsp;               l++;

&nbsp;           }

&nbsp;           maxlen=Math.max(maxlen,i-l+1);

&nbsp;       }

&nbsp;       return maxlen;

&nbsp;   }

}

