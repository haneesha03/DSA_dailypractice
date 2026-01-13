### Toggle Case

Given a string, toggle the case of each character in the given string.



Input Format

The first and only input line contains a string S, consisting of lowercase and uppercase characters.



Output Format

Print the toggled string.



Constraints

1 <= len(S) <= 100



Example

Input

SMartINTERviewS



Output

smARTinterVIEWs



**Solution:**

import java.io.\*;

import java.util.\*;



public class Main {



&nbsp;   public static void main(String\[] args) {

&nbsp;       /\* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Main. \*/

&nbsp;       Scanner s=new Scanner(System.in);

&nbsp;       String str=s.next();

&nbsp;       StringBuffer sb=new StringBuffer();

&nbsp;       for(int i=0;i<str.length();i++){

&nbsp;           char ch=str.charAt(i);

&nbsp;           if(Character.isLowerCase(ch)){

&nbsp;               sb.append(Character.toUpperCase(ch));

&nbsp;           }

&nbsp;           else{

&nbsp;               sb.append(Character.toLowerCase(ch));

&nbsp;           }

&nbsp;       }

&nbsp;       System.out.println(sb.toString());

&nbsp;   }

}

