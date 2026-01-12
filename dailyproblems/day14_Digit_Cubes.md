### Digit Cubes



Given an integer N, check whether the number is equal to the sum of cubes of its digits.



Input Format

The first and only line of input contains an integer - N.



Output Format

Print "Yes" if the number satisfies the given condition, "No" otherwise.



Constraints

0 <= N <= 109



Example

Input

153



Output

Yes



Explanation



13 + 53 + 33 = 153



**Solution:**

import java.io.\*;

import java.util.\*;



public class Main {



&nbsp;   public static void main(String\[] args) {

&nbsp;       /\* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Main. \*/

&nbsp;       Scanner s=new Scanner(System.in);

&nbsp;       int n=s.nextInt();

&nbsp;       int temp=n;

&nbsp;       int sum=0,rem=0;

&nbsp;       while(n>0){

&nbsp;           rem=n%10;

&nbsp;           sum+=(rem\*rem\*rem);

&nbsp;           n=n/10;

&nbsp;       }

&nbsp;       if(sum==temp){

&nbsp;          System.out.println("Yes");

&nbsp;           return;

&nbsp;       }

&nbsp;       System.out.println("No");



&nbsp;   }

}

