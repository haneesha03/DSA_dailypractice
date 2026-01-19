#### 345\. Reverse Vowels of a String

Given a string s, reverse only all the vowels in the string and return it.



The vowels are 'a', 'e', 'i', 'o', and 'u', and they can appear in both lower and upper cases, more than once.



&nbsp;



Example 1:



Input: s = "IceCreAm"



Output: "AceCreIm"



Explanation:



The vowels in s are \['I', 'e', 'e', 'A']. On reversing the vowels, s becomes "AceCreIm".



Example 2:



Input: s = "leetcode"



Output: "leotcede"



&nbsp;



Constraints:



1 <= s.length <= 3 \* 105

s consist of printable ASCII characters.



**Solution:**

class Solution {

&nbsp;   public String reverseVowels(String s) {

&nbsp;   char\[] ch=s.toCharArray();

&nbsp;   int i=0,j=ch.length-1;

&nbsp;   String vowels="aeiouAEIOU";

&nbsp;   while(i<j){

&nbsp;       if(vowels.contains(ch\[i]+"") \&\& vowels.contains(ch\[j]+"")){

&nbsp;           char temp=ch\[i];

&nbsp;           ch\[i]=ch\[j];

&nbsp;           ch\[j]=temp;

&nbsp;           i++;j--;

&nbsp;       }

&nbsp;       else if(vowels.contains(ch\[i]+"")){

&nbsp;           j--;

&nbsp;       }

&nbsp;       else if(vowels.contains(ch\[j]+"")){

&nbsp;           i++;

&nbsp;       }

&nbsp;       else{

&nbsp;           i++;j--;

&nbsp;       }

&nbsp;   }

&nbsp;   String str=new String(ch);

&nbsp;   return str;

&nbsp;   }

}

