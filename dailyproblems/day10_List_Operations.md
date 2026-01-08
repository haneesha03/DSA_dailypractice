**List Operations** 

You are tasked with implementing a program that manipulates an empty list based on a series of commands.



Input Format

The first line of input contains an integer N, indicating the number of commands to follow. The next N lines contains any of the following commands:append X: Appends the integer X to the end of the list.count X: Count the number of occurrences of the integer X in the list.reverse: Reverses the order of elements in the list.insert Pos X: Inserts the integer X at the position Pos in the list.sort: Sorts the elements of the list in ascending order.index X: Gives the index of the first occurrence of the integer X in the list, or -1 if X is not found.length: Gives the length of the list.extend: Extends the list by appending it's current elements to itself.Output Format

For count, index, and length command, print the result. For the remaining commands, print the updated list separated by spaces.



Constraints

1 <= N <= 50

1 <= X <= 100

0 <= Pos < length of the list



Example

Input

10

append 13

append 7

insert 1 6

extend

index 2

reverse

index 7

length

sort

count 6



Output

13

13 7

13 6 7

13 6 7 13 6 7

-1

7 6 13 7 6 13

0

6

6 6 7 7 13 13

2



**Solution:**

import java.io.\*;

import java.util.\*;



public class Main {

&nbsp;   public static void command(String cmd,ArrayList<Integer> al){

&nbsp;       String\[] part=cmd.split(" ");

&nbsp;       String option=part\[0];

&nbsp;       switch(option){

&nbsp;           case "append":

&nbsp;               int x=Integer.parseInt(part\[1]);

&nbsp;               al.add(x);

&nbsp;               print(al);

&nbsp;               break;

&nbsp;           case "insert":

&nbsp;               int index=Integer.parseInt(part\[1]),ele=Integer.parseInt(part\[2]);

&nbsp;               al.add(index,ele);

&nbsp;               print(al);

&nbsp;               break;

&nbsp;           case "extend":

&nbsp;               ArrayList<Integer> copy=new ArrayList<>(al);

&nbsp;               al.addAll(al);

&nbsp;               print(al);

&nbsp;               break;

&nbsp;           case "index":

&nbsp;               int search=Integer.parseInt(part\[1]);

&nbsp;               int ind=al.indexOf(search);

&nbsp;               System.out.println(ind);

&nbsp;               break;

&nbsp;           case "reverse":

&nbsp;               Collections.reverse(al);

&nbsp;               print(al);

&nbsp;               break;

&nbsp;           case "length":

&nbsp;               System.out.println(al.size());

&nbsp;               break;



&nbsp;           case "count":

&nbsp;               int target=Integer.parseInt(part\[1]);

&nbsp;               int count=Collections.frequency(al,target);

&nbsp;               System.out.println(count);

&nbsp;               break;



&nbsp;           case "sort":

&nbsp;               Collections.sort(al);

&nbsp;               print(al);

&nbsp;               break;

&nbsp;       }

&nbsp;   }

&nbsp;   public static void print(ArrayList<Integer> al){

&nbsp;       for(int ele:al){

&nbsp;           System.out.print(ele+" ");

&nbsp;       }

&nbsp;       System.out.println();

&nbsp;   }

&nbsp;   public static void main(String\[] args) {

&nbsp;       /\* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Main. \*/

&nbsp;       Scanner s=new Scanner(System.in);

&nbsp;       int n=s.nextInt();

&nbsp;       s.nextLine();

&nbsp;       String\[] commands=new String\[n];

&nbsp;       ArrayList<Integer> al=new ArrayList<>();

&nbsp;       for(int i=0;i<n;i++){

&nbsp;           commands\[i]=s.nextLine();

&nbsp;           command(commands\[i],al);

&nbsp;       }

&nbsp;   }

}

