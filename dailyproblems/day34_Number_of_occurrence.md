###### Number of occurrence



Given a sorted array, arr\[] and a number target, you need to find the number of occurrences of target in arr\[]. 



Examples :



Input: arr\[] = \[1, 1, 2, 2, 2, 2, 3], target = 2

Output: 4

Explanation: target = 2 occurs 4 times in the given array so the output is 4.

Input: arr\[] = \[1, 1, 2, 2, 2, 2, 3], target = 4

Output: 0

Explanation: target = 4 is not present in the given array so the output is 0.

Input: arr\[] = \[8, 9, 10, 12, 12, 12], target = 12

Output: 3

Explanation: target = 12 occurs 3 times in the given array so the output is 3.

Constraints:

1 ≤ arr.size() ≤ 106

1 ≤ arr\[i] ≤ 106

1 ≤ target ≤ 106



###### Solution:

class Solution {

&nbsp;   public static int firstocc(int\[] a,int key){

&nbsp;       int n=a.length;

&nbsp;       int fo=-1;

&nbsp;       int l=0,h=n-1;

&nbsp;       while(l<=h){

&nbsp;           int mid=(l+h)/2;

&nbsp;           if(a\[mid]==key){

&nbsp;               fo=mid;

&nbsp;               h=mid-1;

&nbsp;           }

&nbsp;           else if(a\[mid]>key){

&nbsp;               h=mid-1;

&nbsp;               

&nbsp;           }

&nbsp;           else{

&nbsp;               l=mid+1;

&nbsp;           }

&nbsp;       }

&nbsp;       return fo;

&nbsp;       

&nbsp;   }

&nbsp;   public static int lastocc(int\[] a,int key){

&nbsp;       int n=a.length;

&nbsp;       int l=0,h=n-1;

&nbsp;       int lc=-1;

&nbsp;       while(l<=h){

&nbsp;           int mid=(l+h)/2;

&nbsp;           if(a\[mid]==key){

&nbsp;               lc=mid;

&nbsp;               l=mid+1;

&nbsp;           }

&nbsp;           else if(a\[mid]>key){

&nbsp;               h=mid-1;

&nbsp;           }

&nbsp;           else{

&nbsp;               l=mid+1;

&nbsp;           }

&nbsp;       }

&nbsp;       return lc;

&nbsp;   }

&nbsp;   int countFreq(int\[] arr, int target) {

&nbsp;       // code here

&nbsp;       int fo=firstocc(arr,target);

&nbsp;       int lo=lastocc(arr,target);

&nbsp;       if(fo==-1){

&nbsp;           return 0;

&nbsp;       }

&nbsp;       return lo-fo+1;

&nbsp;   }

}



