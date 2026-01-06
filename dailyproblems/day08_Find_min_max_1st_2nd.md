**Find 1st minimum 2nd minimum ,1st maximum,2nd maximum int the given array**



**Solution:**



public class MinMax{

&nbsp;   public static void main(String args\[]){

&nbsp;       int\[] a={2,10,20,40,71,43,71,0,5,99,204,0,434};

&nbsp;       int n=a.length;

&nbsp;       int max1=a\[0],max2=Integer.MIN\_VALUE;

&nbsp;       int min1=a\[0],min2=Integer.MAX\_VALUE;

&nbsp;       for(int i=1;i<n;i++){

&nbsp;           if(a\[i]>=max1){

&nbsp;               max2=max1;

&nbsp;		        max1=a\[i];

&nbsp;           }

&nbsp;	        else if(a\[i]>max2){

&nbsp;		        max2=a\[i];

&nbsp;	        }

&nbsp; 	        if(a\[i]<=min1){

&nbsp;		        min2=min1;

&nbsp;		        min1=a\[i];

&nbsp;	        }

&nbsp;	        else if(a\[i]<min2){

&nbsp;	        	min2=a\[i];

&nbsp;	        }

&nbsp;       }

&nbsp;	System.out.println(max1+" "+max2);

&nbsp;	System.out.println(min1+" "+min2);

&nbsp;   }

}



