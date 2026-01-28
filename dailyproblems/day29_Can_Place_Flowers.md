###### 605\. Can Place Flowers

Solved

Easy

Topics

premium lock icon

Companies

You have a long flowerbed in which some of the plots are planted, and some are not. However, flowers cannot be planted in adjacent plots.



Given an integer array flowerbed containing 0's and 1's, where 0 means empty and 1 means not empty, and an integer n, return true if n new flowers can be planted in the flowerbed without violating the no-adjacent-flowers rule and false otherwise.



&nbsp;



Example 1:



Input: flowerbed = \[1,0,0,0,1], n = 1

Output: true

Example 2:



Input: flowerbed = \[1,0,0,0,1], n = 2

Output: false

&nbsp;



Constraints:



1 <= flowerbed.length <= 2 \* 104

flowerbed\[i] is 0 or 1.

There are no two adjacent flowers in flowerbed.

0 <= n <= flowerbed.length

###### Solution:

class Solution {

&nbsp;   public boolean canPlaceFlowers(int\[] fb, int n) {

&nbsp;       int m=fb.length;

&nbsp;       for(int i=0;i<m;i++){

&nbsp;           if(fb\[i]==0){

&nbsp;               boolean lemp= (i==0)|| fb\[i-1]==0;

&nbsp;               boolean remp=(i==m-1)||fb\[i+1]==0;

&nbsp;               if(lemp \&\& remp){

&nbsp;                   fb\[i]=1;

&nbsp;                   i++;

&nbsp;                   n--;

&nbsp;               }

&nbsp;               if(n<=0){

&nbsp;               return true;

&nbsp;               }

&nbsp;           }

&nbsp;       }

&nbsp;       return n<=0;



&nbsp;   }

}

