###### Count distinct elements in every window



Given an integer array arr\[] and a number k. Find the count of distinct elements in every window of size k in the array.



Examples:



Input: arr\[] = \[1, 2, 1, 3, 4, 2, 3], k = 4

Output: \[3, 4, 4, 3]

Explanation:

First window is \[1, 2, 1, 3], count of distinct numbers is 3.

Second window is \[2, 1, 3, 4] count of distinct numbers is 4.

Third window is \[1, 3, 4, 2] count of distinct numbers is 4.

Fourth window is \[3, 4, 2, 3] count of distinct numbers is 3.

Input: arr\[] = \[4, 1, 1], k = 2

Output: \[2, 1]

Explanation:

First window is \[4, 1], count of distinct numbers is 2.

Second window is \[1, 1], count of distinct numbers is 1.

Input: arr\[] = \[1, 1, 1, 1, 1], k = 3

Output: \[1, 1, 1]

Explanation: Every window of size 3 in the array \[1, 1, 1, 1, 1], contains only the element 1, so the number of distinct elements in each window is 1.

Constraints:

1 ≤ k ≤ arr.size() ≤ 105

1 ≤ arr\[i] ≤ 105



###### Solution:

class Solution {

&nbsp;   ArrayList<Integer> countDistinct(int arr\[], int k) {

&nbsp;       // code here

&nbsp;       ArrayList<Integer> al=new ArrayList<>();

&nbsp;       HashMap<Integer,Integer> hm=new HashMap<>();

&nbsp;       for(int i=0;i<arr.length;i++){

&nbsp;           hm.put(arr\[i],hm.getOrDefault(arr\[i],0)+1);

&nbsp;           if(i>=k-1){

&nbsp;               al.add(hm.size());

&nbsp;               hm.put(arr\[i-k+1],hm.get(arr\[i-k+1])-1);

&nbsp;               if(hm.get(arr\[i-k+1])==0){

&nbsp;                   hm.remove(arr\[i-k+1]);

&nbsp;               }

&nbsp;           }

&nbsp;       }

&nbsp;       return al;

&nbsp;   }

}

