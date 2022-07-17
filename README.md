# Top-Java-Programming-Interview-Questions
Java Programming Interview Questions are always the deciding factor in any Java interview. Whether you are a beginner in Java or an expert programmer, you will be tested for your coding skills in the interview. So, it’s a good idea to brush up your coding skills before you face the interview.

## 1. Program to Print Hello World in Java.
```java
class HelloWorld
{
    public static void main(String args[])
    {
        System.out.println("Hello World!!");
    }
} 
```

## 2. Program to Accept values of Two Numbers and print their Addition in Java.
```java
import java.util.Scanner;

class AddNumbers
{
    public static void main(String args[])
    {
        int x, y, z;
        System.out.print("Enter two integers to calculate their sum : ");
        Scanner in = new Scanner(System.in);
        x = in.nextInt();
        y = in.nextInt();
        z = x + y;
        System.out.println("Sum of entered integers = " + z);
    }
}
```



## 3. Program to accept three Number and Print Largest among them in Java.
```Java
class CommandLineArgs 

{
    public static void main(String args[]) 
    {
        int a, b, c;
        
        a = Integer.parseInt(args[0]);
        b = Integer.parseInt(args[1]);
        c = Integer.parseInt(args[2]);

        if (a > b && a > c) {
            System.out.println("Largest Number is : " + a);
        } else if (b > c) {
            System.out.println("Largest Number is : " + b);
        } else {
            System.out.println("Largest Number is : " + c);
        }
    }
}

```