**Interchange Diagonals**



Given a matrix A of size NxN, interchange the diagonal elements from top to bottom and print the resultant matrix.



Input Format

First line of input contains N - the size of the matrix. It is followed by N lines each containing N integers - elements of the matrix.



Output Format

Print the matrix after interchanging the diagonals.



Constraints

1 <= N <= 100

1 <= A\[i]\[j] <= 104



Example

Input

4

5 6 7 8

13 14 15 16

1 2 3 4

9 10 11 12



Output

8 6 7 5 

13 15 14 16 

1 3 2 4 

12 10 11 9 



**Solution:**



import java.io.\*;

import java.util.\*;



public class Main {



&nbsp;   public static void main(String\[] args) {

&nbsp;       /\* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Main. \*/

&nbsp;       Scanner s=new Scanner(System.in);

&nbsp;       int n=s.nextInt();

&nbsp;       int\[]\[] a=new int\[n]\[n];

&nbsp;       for(int i=0;i<n;i++){

&nbsp;           for(int j=0;j<n;j++){

&nbsp;               a\[i]\[j]=s.nextInt();

&nbsp;           }

&nbsp;       }

&nbsp;       for(int i=0;i<n;i++){

&nbsp;           for(int j=n-1;j>=0;j--){

&nbsp;               if(i==n-j-1){

&nbsp;               int temp=a\[i]\[i];

&nbsp;               a\[i]\[i]=a\[i]\[j];

&nbsp;               a\[i]\[j]=temp;

&nbsp;               }

&nbsp;           }

&nbsp;       }

&nbsp;       for(int i=0;i<n;i++){

&nbsp;           for(int j=0;j<n;j++){

&nbsp;               System.out.print(a\[i]\[j]+" ");

&nbsp;           }

&nbsp;           System.out.println();

&nbsp;       }



&nbsp;   }

}



