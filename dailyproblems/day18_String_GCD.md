#### String GCD 

Given two strings, P and Q, your task is to find the largest common divisor string S, such that both P and Q are divisible by S. In other words, there exists a string 'S' for which P = S + S + ... + S and Q = S + S + ... + S. If such a string S exists, output the largest possible S, otherwise, print -1.



Note: A string X is divisible by string Y if and only if X can be obtained by concatenating Y with itself one or more times.



Input Format

The first line of input contains the string P. The Second line of input contains string Q.



Output Format

Print the largest string S.



Constraints

1 ≤ len(P), len(Q) ≤ 1000

'A' <= P\[i],Q\[i] <= 'Z'



Example

Input

ABABAB

ABAB



Output

AB



**Solution:**

import java.io.\*;

import java.util.\*;



public class Main {



&nbsp;   public static void main(String\[] args) {

&nbsp;       /\* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Main. \*/

&nbsp;       Scanner s=new Scanner(System.in);

&nbsp;       String x=s.next(),y=s.next();

&nbsp;       if(!(x+y).equals(y+x)){

&nbsp;           System.out.println(-1);

&nbsp;           return;

&nbsp;       }

&nbsp;       while(!x.equals(y)){

&nbsp;           if(x.length()>y.length()){

&nbsp;               x=x.substring(y.length());

&nbsp;           }

&nbsp;           else if(y.length()>x.length()){

&nbsp;               y=y.substring(x.length());

&nbsp;           }

&nbsp;       }

&nbsp;       System.out.println(x);

&nbsp;   }

}

