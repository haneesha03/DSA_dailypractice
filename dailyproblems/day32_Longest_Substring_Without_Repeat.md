###### 3\. Longest Substring Without Repeating Characters



Given a string s, find the length of the longest substring without duplicate characters.

Example 1:



Input: s = "abcabcbb"

Output: 3

Explanation: The answer is "abc", with the length of 3. Note that "bca" and "cab" are also correct answers.

Example 2:



Input: s = "bbbbb"

Output: 1

Explanation: The answer is "b", with the length of 1.

Example 3:



Input: s = "pwwkew"

Output: 3

Explanation: The answer is "wke", with the length of 3.

Notice that the answer must be a substring, "pwke" is a subsequence and not a substring.

&nbsp;



Constraints:



0 <= s.length <= 5 \* 104

s consists of English letters, digits, symbols and spaces.



###### Solution:

class Solution {

&nbsp;   public int lengthOfLongestSubstring(String s) {

&nbsp;       int maxlen=0;

&nbsp;       HashSet<Character> hs=new HashSet<>();

&nbsp;       int l=0;

&nbsp;       for(int i=0;i<s.length();i++){

&nbsp;           while(!hs.add(s.charAt(i))){

&nbsp;               hs.remove(s.charAt(l++));

&nbsp;           }

&nbsp;           maxlen=Math.max(maxlen,i-l+1);

&nbsp;       }

&nbsp;       return maxlen;

&nbsp;   }

}

