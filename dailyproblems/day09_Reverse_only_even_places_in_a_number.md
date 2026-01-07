**Reverse only even places in a number** 

Example:

input:

123456

output:

163452



**Solution:**

import java.util.\*;

public class ReverseEven{

&nbsp;	public static void main(String args\[]){

&nbsp;	Scanner s=new Scanner(System.in);

&nbsp;	System.out.println("enter the number");

&nbsp;	int num=s.nextInt();

&nbsp;	String str=String.valueOf(num);

&nbsp;	char\[] ch=str.toCharArray();

&nbsp;	int n=str.length();

&nbsp;	int i=1,j=n%2==0?n-1:n-2;

&nbsp;	while(i<j){

&nbsp;		char temp=ch\[i];

&nbsp;		ch\[i]=ch\[j];

&nbsp;		ch\[j]=temp;

&nbsp;		i+=2;

&nbsp;		j-=2;

&nbsp;	}

&nbsp;	str=String.valueOf(ch);

&nbsp;	System.out.println(Integer.parseInt(str));

&nbsp;	}

}

