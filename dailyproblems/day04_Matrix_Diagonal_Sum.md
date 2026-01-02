**1572. Matrix Diagonal Sum**



Given a square matrix mat, return the sum of the matrix diagonals.



Only include the sum of all the elements on the primary diagonal and all the elements on the secondary diagonal that are not part of the primary diagonal.



&nbsp;



Example 1:





Input: mat = \[\[1,2,3],

&nbsp;             \[4,5,6],

&nbsp;             \[7,8,9]]

Output: 25

Explanation: Diagonals sum: 1 + 5 + 9 + 3 + 7 = 25

Notice that element mat\[1]\[1] = 5 is counted only once.

Example 2:



Input: mat = \[\[1,1,1,1],

&nbsp;             \[1,1,1,1],

&nbsp;             \[1,1,1,1],

&nbsp;             \[1,1,1,1]]

Output: 8

Example 3:



Input: mat = \[\[5]]

Output: 5

&nbsp;



Constraints:



n == mat.length == mat\[i].length

1 <= n <= 100

1 <= mat\[i]\[j] <= 100



**Solution:**

class Solution {

&nbsp;   public int diagonalSum(int\[]\[] mat) {

&nbsp;       int n=mat.length;

&nbsp;       int sum=0;

&nbsp;       for(int i=0;i<n;i++){

&nbsp;           for(int j=0;j<n;j++){

&nbsp;               if(i==j){

&nbsp;                   sum+=mat\[i]\[j];

&nbsp;               }

&nbsp;               else if(i+j==n-1){

&nbsp;                   sum+=mat\[i]\[j];

&nbsp;               }

&nbsp;           }

&nbsp;       }

&nbsp;       return sum;

&nbsp;   }

}

**Optimized Solution:**

class Solution {

&nbsp;   public int diagonalSum(int\[]\[] mat) {

&nbsp;       int n=mat.length;

&nbsp;       int sum=0;

&nbsp;       for(int i=0;i<n;i++){

&nbsp;           sum=sum+mat\[i]\[i]+mat\[i]\[n-1-i];

&nbsp;       }

&nbsp;       if(n%2==1){

&nbsp;           sum-=mat\[n/2]\[n/2];

&nbsp;       }

&nbsp;       return sum;

&nbsp;   }

}

