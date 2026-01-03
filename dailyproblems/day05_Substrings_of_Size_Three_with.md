**1876. Substrings of Size Three with Distinct Characters**

A string is good if there are no repeated characters.



Given a string s​​​​​, return the number of good substrings of length three in s​​​​​​.



Note that if there are multiple occurrences of the same substring, every occurrence should be counted.



A substring is a contiguous sequence of characters in a string.



&nbsp;



Example 1:



Input: s = "xyzzaz"

Output: 1

Explanation: There are 4 substrings of size 3: "xyz", "yzz", "zza", and "zaz". 

The only good substring of length 3 is "xyz".

Example 2:



Input: s = "aababcabc"

Output: 4

Explanation: There are 7 substrings of size 3: "aab", "aba", "bab", "abc", "bca", "cab", and "abc".

The good substrings are "abc", "bca", "cab", and "abc".

&nbsp;



Constraints:



1 <= s.length <= 100

s​​​​​​ consists of lowercase English letters.

**My Solution:**

class Solution {

&nbsp;   public int countGoodSubstrings(String s) {

&nbsp;       int count=0;

&nbsp;       for(int i=0;i<=s.length()-3;i++){

&nbsp;           HashSet<Character> hs=new HashSet<>();

&nbsp;           String sb=s.substring(i,i+3);

&nbsp;           for(int j=0;j<3;j++){

&nbsp;               if(!hs.add(sb.charAt(j))){

&nbsp;               continue;

&nbsp;               }

&nbsp;               else if(hs.size()==3){

&nbsp;                   count++;

&nbsp;               }

&nbsp;           }

&nbsp;       }

&nbsp;       return count;

&nbsp;   }

}



**Optimized Solution:**

class Solution {

&nbsp;   public int countGoodSubstrings(String s) {

&nbsp;       int count=0;

&nbsp;       if(s.length()<3) return count;

&nbsp;       char a=s.charAt(0);

&nbsp;       char b=s.charAt(1);

&nbsp;       char c=s.charAt(2);

&nbsp;       if(a!=b \&\& b!=c \&\& c!=a) count++;

&nbsp;       for(int i=3;i<s.length();i++){

&nbsp;           a=b;

&nbsp;           b=c;

&nbsp;           c=s.charAt(i);

&nbsp;           if(a!=b \&\& b!=c \&\& c!=a) count++;

&nbsp;       }

&nbsp;       return count;

&nbsp;   }

}

