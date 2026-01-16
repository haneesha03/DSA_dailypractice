#### Compress String 

Given a string, compress the given string. See the example for more details.



Input Format

Input contains a string S, consisting of lowercase and uppercase characters.



Output Format

Print the compressed string.



Constraints

1 <= len(S) <= 100



Example

Input

aaabbbbhhheaaAsssssss



Output

a3b4h3e1a2A1s7



Explanation



In the given string, a is repeating for 3 times - after compression a3.

Similarly,

b is repeating for 4 times - b4

h is repeating for 3 times - h3

e is repeating for 1 time - e1

a is repeating for 2 times - a2

A is repeating for 1 time - A1

s is repeating 7 times - s7



**Solution:**

import java.io.\*;

import java.util.\*;



public class Main {



&nbsp;   public static void main(String\[] args) {

&nbsp;       /\* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Main. \*/

&nbsp;       Scanner s=new Scanner(System.in);

&nbsp;       String str=s.next();

&nbsp;       StringBuffer sb=new StringBuffer();

&nbsp;       int i=0;

&nbsp;       int count=0;

&nbsp;       char ch=str.charAt(0);

&nbsp;       while(i<str.length()){

&nbsp;           char c=str.charAt(i);

&nbsp;           if(ch==c){

&nbsp;               count++;

&nbsp;           }

&nbsp;           else{

&nbsp;               sb.append(ch);

&nbsp;               sb.append(count);

&nbsp;               ch=c;

&nbsp;               count=1;

&nbsp;           }

&nbsp;           i++;

&nbsp;       }

&nbsp;       sb.append(ch);

&nbsp;       sb.append(count);

&nbsp;       System.out.println(sb);



&nbsp;   }

}

