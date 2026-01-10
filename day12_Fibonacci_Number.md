**Fibonacci Number** 

For a given positive integer - N, compute Nth Fibonacci number.



Input Format

The first and only line of input contains a positive number - N.



Output Format

Print the Nth fibonacci number.



Constraints

0 <= N <= 20



Example

Input

4



Output

3



Explanation



The fibonacci series:

0, 1, 1, 2, 3, 5, 8,......

At 4th position, we have 3.



**Solution:**

import java.io.\*;

import java.util.\*;



public class Main {

&nbsp;   public static int fibonacii(int n){

&nbsp;       if(n==0){

&nbsp;           return 0;

&nbsp;       }

&nbsp;       else if(n==1){

&nbsp;           return 1;

&nbsp;       }

&nbsp;       return fibonacii(n-1)+fibonacii(n-2);

&nbsp;   }

&nbsp;   public static void main(String\[] args) {

&nbsp;       /\* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Main. \*/

&nbsp;       Scanner s=new Scanner(System.in);

&nbsp;       int n=s.nextInt();

&nbsp;       System.out.println(fibonacii(n));

&nbsp;   }

}

