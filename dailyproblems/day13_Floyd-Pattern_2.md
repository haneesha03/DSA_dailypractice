#### **Floyd Pattern - 2** 

Print a right-angled triangle pattern. See the example for more details.



Input Format

The first and only line of input contains a single integer N - the size of the triangle.



Output Format

For the given integer, print the right-angled triangle pattern.



Constraints

1 <= N <= 50



Example

Input

5



Output

1

2 6

3 7 10

4 8 11 13

5 9 12 14 15



**Solution:**

import java.io.\*;

import java.util.\*;



public class Main {



&nbsp;   public static void main(String\[] args) {

&nbsp;       /\* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Main. \*/

&nbsp;       Scanner s=new Scanner(System.in);

&nbsp;       int n=s.nextInt();

&nbsp;       for(int i=1;i<=n;i++){

&nbsp;           int num=i,red=n-1;

&nbsp;           for(int j=1;j<=i;j++){

&nbsp;               System.out.print(num+" ");

&nbsp;               num+=red;

&nbsp;               red--;

&nbsp;           }

&nbsp;           System.out.println();

&nbsp;       }

&nbsp;   }

}

