#### 151\. Reverse Words in a String

Given an input string s, reverse the order of the words.



A word is defined as a sequence of non-space characters. The words in s will be separated by at least one space.



Return a string of the words in reverse order concatenated by a single space.



Note that s may contain leading or trailing spaces or multiple spaces between two words. The returned string should only have a single space separating the words. Do not include any extra spaces.



&nbsp;



Example 1:



Input: s = "the sky is blue"

Output: "blue is sky the"

Example 2:



Input: s = "  hello world  "

Output: "world hello"

Explanation: Your reversed string should not contain leading or trailing spaces.

Example 3:



Input: s = "a good   example"

Output: "example good a"

Explanation: You need to reduce multiple spaces between two words to a single space in the reversed string.

&nbsp;



Constraints:



1 <= s.length <= 104

s contains English letters (upper-case and lower-case), digits, and spaces ' '.

There is at least one word in s.



**Solution:**

class Solution {

&nbsp;   public String reverseWords(String s) {

&nbsp;       String str=s.trim();

&nbsp;       String\[] words=str.split("\\\\s+");

&nbsp;       int i=0,j=words.length-1;

&nbsp;       while(i<j){

&nbsp;           String temp=words\[i];

&nbsp;           words\[i]=words\[j];

&nbsp;           words\[j]=temp;

&nbsp;           i++;

&nbsp;           j--;

&nbsp;       }

&nbsp;       return String.join(" ",words);

&nbsp;   }

}

&nbsp;

