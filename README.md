# 10-Core-java-solved-problems-

Name: Gayatri Pawar
College: shram sadhana bombay trust college of engineering and technology ,jalgaon.
Branch :Computer engineering
Year: Final Year.


#1.Write a Java program to perform basic Calculator operations.
import java.util.Scanner;
public class BasicCalculator {
  
    public static void main(String[] args)
    {
        // stores two numbers
        double num1, num2;
  
        // Take input from the user
        Scanner sc = new Scanner(System.in);
  
        System.out.println("Enter the numbers");
  
        // take the inputs
        num1 = sc.nextDouble();
  
        num2 = sc.nextDouble();
  
        System.out.println("Enter the operator (+,-,*,/)");
  
        char op = sc.next().charAt(0);
  
        double o = 0;
  
        switch (op) {
  
        // case to add two numbers
        case '+':
  
            o = num1 + num2;
  
            break;
  
        // case to subtract two numbers
        case '-':
  
            o = num1 - num2;
  
            break;
  
        // case to multiply two numbers
        case '*':
  
            o = num1 * num2;
  
            break;
  
        // case to divide two numbers
        case '/':
  
            o = num1 / num2;
  
            break;
  
        default:
  
            System.out.println("You enter wrong input");
  
            break;
        }
  
        System.out.println("The final result:");
  
        System.out.println();
  
        // print the final result
        System.out.println(num1 + " " + op + " " + num2
                           + " = " + o);
    }
}

#2.Write a Java program to calculate Fibonacci Series up to n numbers.

class Main {
  public static void main(String[] args) {

    int n = 10, firstTerm = 0, secondTerm = 1;
    System.out.println("Fibonacci Series till " + n + " terms:");

    for (int i = 1; i <= n; ++i) {
      System.out.print(firstTerm + ", ");

      // compute the next term
      int nextTerm = firstTerm + secondTerm;
      firstTerm = secondTerm;
      secondTerm = nextTerm;
    }
  }
}

#3.Write a Java program to calculate a Factorial of a number.

class FactorialExample{  
 public static void main(String args[]){  
  int i,fact=1;  
  int number=5;//It is the number to calculate factorial    
  for(i=1;i<=number;i++){    
      fact=fact*i;    
  }    
  System.out.println("Factorial of "+number+" is: "+fact);    
 }  
}  

#4.Write a Java program to find out whether the given String is Palindrome or not.

class Main {
  public static void main(String[] args) {

    String str = "amma", reverseStr = "";
    
    int strLength = str.length();

    for (int i = (strLength - 1); i >=0; --i) {
      reverseStr = reverseStr + str.charAt(i);
    }

    if (str.toLowerCase().equals(reverseStr.toLowerCase())) {
      System.out.println(str + " is a Palindrome String.");
    }
    else {
      System.out.println(str + " is not a Palindrome String.");
    }
  }
}

#5.Write a Java program to calculate Permutation and Combination of 2 numbers.

import java.util.Scanner;
class PermutationCombination
{
    static long factorial(int num) {
        int f = 1;
        for (int i = 1; i <= num; i++) {
            f *= i;
        }
        return f;
    }
    
    public static void main(String args[]) {
        Scanner in = new Scanner(System.in);
        System.out.print("Enter the value of n: ");
        int n = in.nextInt();
        System.out.print("Enter the value of r: ");
        int r = in.nextInt();
        int p = (int)(factorial(n) / factorial(n - r));
        int c = (int)(factorial(n) 
                      / (factorial(n - r) * factorial(r)));
        System.out.println("Permutation = " + p);
        System.out.println("Combination = " + c);
    }
}

#6.Write a program in Java to print Diamond Pattern.



import java.util.Scanner;
 class Diamond 
{
 
 
public static void main(String[] args)
{
 
Scanner sc=new Scanner(System.in);
System.out.println("Enter N : ");
int n=sc.nextInt(); 
System.out.print("Enter Symbol : ");
 
char c = sc.next().charAt(0);
int i=1;
int j;
while(i<=n)
{
j=1;
while(j++<=n-i)
 
{
System.out.print(" ");
 
}
j=1;
while(j++<=i*2-1)
 
{
System.out.print(c);
 
}
 
System.out.println();
i++;
} 
i=n-1;
while(i>0)
{
j=1;
while(j++<=n-i)
 
{
System.out.print(" ");
 
} 
j=1;
while(j++<=i*2-1)
 
{
System.out.print(c);
 
}
 
System.out.println();
i--;
}
 
}
}



7.Write a Java Program to reverse the letters present in the given String.

public class Example
{
   public void reverseWordInMyString(String str)
   {
	/* The split() method of String class splits
	 * a string in several strings based on the
	 * delimiter passed as an argument to it
	 */
	String[] words = str.split(" ");
	String reversedString = "";
	for (int i = 0; i < words.length; i++)
        {
           String word = words[i]; 
           String reverseWord = "";
           for (int j = word.length()-1; j >= 0; j--) 
	   {
		/* The charAt() function returns the character
		 * at the given position in a string
		 */
		reverseWord = reverseWord + word.charAt(j);
	   }
	   reversedString = reversedString + reverseWord + " ";
	}
	System.out.println(str);
	System.out.println(reversedString);
   }
   public static void main(String[] args) 
   {
	Example obj = new Example();
	obj.reverseWordInMyString("hi my name is gayatri ");
	obj.reverseWordInMyString("This is an easy Java Program");
   

   8.Write a Java Program to check whether the given array is Mirror Inverse or not.



   
// Java implementation of the approach
public class Gayatri {
 
    // Function that returns true if
    // the array is mirror-inverse
    static boolean isMirrorInverse(int arr[])
    {
        for (int i = 0; i < arr.length; i++) {
 
            // If condition fails for any element
            if (arr[arr[i]] != i)
                return false;
        }
 
        // Given array is mirror-inverse
        return true;
    }
 
    // Driver code
    public static void main(String[] args)
    {
        int arr[] = { 1, 2, 3, 0 };
        if (isMirrorInverse(arr))
            System.out.println("Yes");
        else
            System.out.println("No");
    }
}

9.Write a Java program to remove elements from an ArrayList

// Importing required classes
import java.util.ArrayList;
import java.util.List;
  
// Main class
public class Gayatri {
    // Main driver method
    public static void main(String[] args)
    {
        // Creating an object of List interface with
        // reference to ArrayList class
        List<Integer> al = new ArrayList<>();
  
        // Adding elements to our ArrayList
        // using add() method
        al.add(10);
        al.add(20);
        al.add(30);
        al.add(1);
        al.add(2);
  
        // Printing the current ArrayList
        System.out.println(al);
  
        // This makes a call to remove(int) and
        // removes element 20
        al.remove(1);
  
        // Now element 30 is moved one position back
        // So element 30 is removed this time
        al.remove(1);
  
        // Printing the updated ArrayList
        System.out.println(al);
    }
}

10.Write a Java Program to find the Transpose of a given Matrix.

public class MatrixTransposeExample{  
public static void main(String args[]){  
//creating a matrix  
int original[][]={{1,3,4},{2,4,3},{3,4,5}};    
    
//creating another matrix to store transpose of a matrix  
int transpose[][]=new int[3][3];  //3 rows and 3 columns  
    
//Code to transpose a matrix  
for(int i=0;i<3;i++){    
for(int j=0;j<3;j++){    
transpose[i][j]=original[j][i];  
}    
}    
  
System.out.println("Printing Matrix without transpose:");  
for(int i=0;i<3;i++){    
for(int j=0;j<3;j++){    
System.out.print(original[i][j]+" ");    
}    
System.out.println();//new line    
}    
System.out.println("Printing Matrix After Transpose:");  
for(int i=0;i<3;i++){    
for(int j=0;j<3;j++){    
System.out.print(transpose[i][j]+" ");    
}    
System.out.println();//new line    
}    
}} 
