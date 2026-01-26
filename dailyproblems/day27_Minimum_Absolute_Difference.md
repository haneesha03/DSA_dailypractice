1200\. Minimum Absolute Difference



Given an array of distinct integers arr, find all pairs of elements with the minimum absolute difference of any two elements.



Return a list of pairs in ascending order(with respect to pairs), each pair \[a, b] follows



a, b are from arr

a < b

b - a equals to the minimum absolute difference of any two elements in arr

&nbsp;



Example 1:



Input: arr = \[4,2,1,3]

Output: \[\[1,2],\[2,3],\[3,4]]

Explanation: The minimum absolute difference is 1. List all pairs with difference equal to 1 in ascending order.

Example 2:



Input: arr = \[1,3,6,10,15]

Output: \[\[1,3]]

Example 3:



Input: arr = \[3,8,-10,23,19,-4,-14,27]

Output: \[\[-14,-10],\[19,23],\[23,27]]

&nbsp;



Constraints:



2 <= arr.length <= 105

-106 <= arr\[i] <= 106



**Solution:**

class Solution {

&nbsp;   public List<List<Integer>> minimumAbsDifference(int\[] a) {

&nbsp;       Arrays.sort(a);

&nbsp;       int n=a.length;

&nbsp;       List<List<Integer>> res=new ArrayList<>();

&nbsp;       int mindiff=Integer.MAX\_VALUE;

&nbsp;       for(int i=1;i<n;i++){

&nbsp;           mindiff=Math.min(mindiff,a\[i]-a\[i-1]);

&nbsp;       }

&nbsp;       for(int i=1;i<n;i++){

&nbsp;           if(mindiff==a\[i]-a\[i-1]){

&nbsp;               List<Integer> al=new ArrayList<>();

&nbsp;               al.add(a\[i-1]);

&nbsp;               al.add(a\[i]);

&nbsp;               res.add(al);

&nbsp;           }



&nbsp;       }

&nbsp;       return res;

&nbsp;   }

}

