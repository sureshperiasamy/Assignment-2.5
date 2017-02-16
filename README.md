# Assignment-2.5
a. Write a Java code with the class name, “acad,” and a method called “main.” Hard code the program with two integers and print the sum of those two integers.

import java.util.Scanner;


public class acad {
public static void main(String args[])
{
	Scanner s=new Scanner(System.in);
	int a=5,b=6; //initializing two variables with value
	int sum;
	sum=a+b;  //adding a and b storing result in sum
	System.out.println("Sum of "+a+" and "+b+" is "+sum);
}
}

b. Rewrite the above code, wherein the inputs are provided by the user at runtime and the output is printed.

import java.util.Scanner;


public class acad {
public static void main(String args[])
{
	Scanner s=new Scanner(System.in);
	int a,b;
	System.out.println("Enter the first number:");
	a=s.nextInt();  //getting first number from user
	System.out.println("Enter the second number");
	b=s.nextInt();   //getting second number from user
	int sum;
	sum=a+b;  //adding a and b storing result in sum
	System.out.println("Sum of "+a+" and "+b+" is "+sum);
}
}

c. Write a program with the method name, “sum()” that accepts two parameters from the user and print the sum of those two numbers. The output format should be:
First number is:
Second number is:
Sum is:


import java.util.Scanner;


public class acad {
public static void main(String args[])
{
	Scanner s=new Scanner(System.in);
	int a,b;
	System.out.println("Enter the first number");
	a=s.nextInt();  //getting first number from user
	System.out.println("Enter the second number:");
	b=s.nextInt();   //getting second number from user
	sum(a,b); //passing value of a and b to method sum
}
public static void sum(int a,int b)
{
	System.out.println("First number is:"+a);
	System.out.println("Second number is:"+b);
	System.out.println("Sum is: "+(a+b));  //printing the sum of a and b
	
}
}

	
d. Write a program to accept two numbers from “stdin” and find all the odd as well as even numbers present in between them

import java.util.Scanner;


public class acad {
public static void main(String args[])
{
	Scanner s=new Scanner(System.in);
	int a,b;
	System.out.println("Enter the first number");
	a=s.nextInt();  //getting first number from user
	System.out.println("Enter the second number:");
	b=s.nextInt();   //getting second number from user
	System.out.println("The even numbers are");
	for(int i=a;i<=b;i++)
	{
	    if(i%2==0)
	    	System.out.println(i);
	}
	System.out.println("The odd numbers are");
	for(int i=a;i<=b;i++)
	{
		if(i%2!=0)
			System.out.println(i);
	}
}
}

e. Joe is scared to go to school. When her dad asked for the reason, Joe said that she was unable to complete the task given to her by her teacher. The task was to find the “first 10 multiples” of the number entered from “stdin”. 

import java.util.Scanner;


public class acad {
public static void main(String args[])
{
	Scanner s=new Scanner(System.in);
	int a;
	System.out.println("Enter the number");
	a=s.nextInt();   //getting the number from user
	for(int i=1;i<=10;i++) //defining a loop to execute for 10 times
	{
		System.out.println(a+" * "+i+" = "+(a*i)); //printing the multiplication value
	}
}
}

	
f. Write a program consisting the method “sum()” and demonstrate the concept of method overloading using this method.



import java.util.Scanner;


public class acad {
public static void main(String args[])
{
	Scanner s=new Scanner(System.in);
System.out.println("1.Sum of two numbers \n2.Sum of three numbers");  
int a =s.nextInt();
switch (a){
case 1 : System.out.println("Enter two numbers");
int x=s.nextInt();
int y=s.nextInt();
sum(x,y);  //calling the method sum which accepts two integers
break;
case 2 : System.out.println("Enter three numbers");
int b=s.nextInt();
int c=s.nextInt();
int d=s.nextInt();
sum(b,c,d);  //calling the method sum which accepts three integers
break;
}}
public static void sum(int a,int b)  //creating a method sum which accepts two integer
{
	System.out.println("Sum of two numbers are "+(a+b));
}
public static void sum(int a,int b,int c) //creating a method sum which accepts three integer
{
	System.out.println("Sum of three numbers are "+(a+b+c));
}
}

g. Can you overload a method with the same return type? Explain your answer with proper logic.

YES I CAN OVERLOAD METHOD WITH SAME RETURN TYPE.AS,OVERLOADING DEPENDS ONLY ON THE NUMBER AND TYPE OF ARGUMENTS PASSED TO THE METHOD AND IT IS INDEPENDENT ON  THE RETURN TYPE

import java.util.Scanner;


public class acad {
public static void main(String args[])
{
	Scanner s=new Scanner(System.in);
System.out.println("1.Sum of two numbers \n2.Sum of three numbers");  
int a =s.nextInt();
switch (a){
case 1 : System.out.println("Enter two numbers");
int x=s.nextInt();
int y=s.nextInt();
int q=sum(x,y);  //calling the method sum which accepts two integers
System.out.println("Sum of two numbers : "+q);
break;
case 2 : System.out.println("Enter three numbers");
int b=s.nextInt();
int c=s.nextInt();
int d=s.nextInt();
int p=sum(b,c,d);  //calling the method sum which accepts three integers
System.out.println("Sum of three numbers : " +p);
break;
}}
public static int sum(int a,int b)  //creating a method sum which accepts two integer
{
	return a+b; return int type
}
public static int sum(int a,int b,int c) //creating a method sum which accepts three integer 
{
	return a+b+c; //return int type
}
}

	
h. Write a program in Java using Arrays, that sorts the element in a descending order.
import java.util.Arrays;
import java.util.Scanner;


public class acad {
public static void main(String args[])
{
	Scanner s=new Scanner(System.in);
System.out.println("Enter the number of elements in array ");
int n=s.nextInt(); //getting the size of the array
System.out.println("Enter the elements in array");
int[] a=new int[n];  //defining an integer array of size n
for(int i=0;i<n;i++)
{
 	a[i]=s.nextInt();   //getting the value from user for the array
}
Arrays.sort(a);  //this line sort the elements present in the array in ascending order
System.out.println("Array in descending order");
for(int i=n-1;i>=0;i--)     //loop which is used to print it in a reverse order
{
	System.out.println(a[i]);
}
}
}

	

