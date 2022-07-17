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

## 4. Program to Accept value of Radius and Calculate Area of Circle in Java.

```java
class CalculateCircleAreaExample
{

    public static void main(String[] args)
    {

        int radius = 3;
        System.out.println("The radius of the circle is " + radius);

 /*
         * Area of a circle is pi * r * r where r is a radius of a circle.
  */

        // NOTE : use Math.PI constant to get value of pi
        double area = Math.PI * radius * radius;

        System.out.println("Area of a circle is " + area);
    }
}
```

## 5. Program to Accept value of length & width and Calculate Area of Rectangle in Java.

```java
import java.util.Scanner;

class AreaOfRectangle
{
    public static void main(String[] args)
    {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter the length of Rectangle:");
        double length = scanner.nextDouble();

        System.out.println("Enter the width of Rectangle:");
        double width = scanner.nextDouble();

        //Area = length*width;
        double area = length * width;

        System.out.println("Area of Rectangle is:" + area);
    }
}
```

## 6. Program to Accept value of the side of Square and Calculate Area of Square in Java.
```java
import java.util.*;

class AreaOfSquare
{
    public static void main(String args[])
    {
        int side, area;

        Scanner sc = new Scanner(System.in);

        System.out.println("Enter value of the sides of square");
        side = sc.nextInt();

        area = side * side;

        System.out.println("Area of Square : " + area);
    }
}
```

## 7. Program to Calculate Area's in Java.
```java
import java.util.Scanner;

class AreaCalculator
{

    float l, b, h, r, ba, s, c;
    float result = 0f;
    float pi = 3.14f;
    int var;
    public static void main(String[] args)
    {
        AreaCalculator ar = new AreaCalculator();
        ar.options();
    }

    public void options()
    {
        Scanner a = new Scanner(System.in);
        System.out.println("Enter the Object of which Area is to be calculated \n1:square \n2:rectangle \n3:Triangle\n4:circle\n5:Trapezoid\n6:Repeat\n7:Exit");

        var = a.nextInt();
        Area a1 = new Area();

        if (var == 1)
        {
            System.out.println("Enter the Side of Square");
            s = a.nextFloat();
            a1.square(s);
            options();
        }

        else if (var == 2)
        {
            System.out.println("Enter the Length of Rectangle");
            l = a.nextFloat();
            System.out.println("Enter the Breadth of Rectangle");
            b = a.nextFloat();
            a1.rectangle(l, b);
            options();
        }

        else if (var == 3)
        {
            System.out.println("Enter the Height of Triangle");
            h = a.nextFloat();
            System.out.println("Enter the Base of Triangle");
            ba = a.nextFloat();
            a1.triangle(h, ba);
            options();
        }

        else if (var == 4)
        {
            System.out.println("Enter the Radius of Circle");
            r = a.nextFloat();
            a1.circle(r);
            options();
        }

        else if (var == 5)
        {
            System.out.println("Enter the A side of Trapezoid");
            b = a.nextFloat();
            System.out.println("Enter the B side of Trapezoid");
            c = a.nextFloat();
            System.out.println("Enter the Height of Trapezoid");
            h = a.nextFloat();
            a1.trapezoid(b, c, h);
            options();
        }
    }
}

class Area
{
    public void square(float s)
    {
        float result = 0f;
        result = s * s;
        System.out.println("The Area of Square is :" + result);
    }

    public void rectangle(float l, float b)
    {
        float result = 0f;
        result = l * b;
        System.out.println("The Area of Rectangle is :" + result);
    }

    public void triangle(float h, float ba)
    {
        float result = 0f;
        result = 0.5f * h * ba;
        System.out.println("The Area of Triangle is :" + result);
    }

    public void circle(float r)
    {
        float result = 0f;
        result = 3.14f * (r * r);
        System.out.println("The Area of Circle is :" + result);
    }

    public void trapezoid(float b, float c, float h)
    {
        float result = 0f;
        result = (((b + c) / 2) * h);
        System.out.println("The Area of Trapezoid is :" + result);
    }
}
```

## 8. Program to Find Simple Interest and Compound Interest in Java.

```java
import java.lang.*;
import java.util.Scanner;

class CalculateInterest
{
    public static void main(String[] args)
    {
        double p, n, r, si, ci;

        Scanner s = new Scanner(System.in);

        System.out.print("Enter the amount : ");
        p = s.nextDouble();

        System.out.print("Enter the No.of years : ");
        n = s.nextDouble();

        System.out.print("Enter the Rate of interest : ");
        r = s.nextDouble();

        si = (p * n * r) / 100;
        ci = p * Math.pow(1.0 + r / 100.0, n) - p;

        System.out.println("\nAmount : " + p);
        System.out.println("No. of years : " + n);
        System.out.println("Rate of interest : " + r);
        System.out.println("Simple Interest : " + si);
        System.out.println("Compound Interest : " + ci);
    }
}
```

## 9. Program to Calculate Binary Number Calculation in Java.

```java
import java.util.*;

class BinaryCalculator
{
    public static void main(String[] args)
    {
        Scanner in = new Scanner(System.in);

        System.out.print("First Binary:  ");
        String binOne = in.next();

        System.out.print("Second Binary: ");
        String binTwo = in.next();

        int left = Integer.parseInt(binOne, 2);
        int right = Integer.parseInt(binTwo, 2);

        System.out.println("Sum of the binary numbers : " + Integer.toBinaryString(left + right));
        System.out.println("Difference of the binary numbers : " + Integer.toBinaryString(left - right));
        System.out.println("Product of the binary numbers : " + Integer.toBinaryString(left * right));
        System.out.println("Quotient of the binary numbers : " + Integer.toBinaryString(left / right));
    }
}
```

## 10. Program to Convert Celsius to Fahrenheit in Java.

```java
import java.util.*;

class CelsiustoFahrenheit
{
    public static void main(String[] args)
    {
        double temperature;
        Scanner in = new Scanner(System.in);

        System.out.println("Enter temperature in Celsius");
        temperature = in.nextInt();

        temperature = (temperature * 9 / 5.0) + 32;
        System.out.println("Temperature in Fahrenheit = " + temperature);
    }
}
```

## 11. Program to Create a Simple Calculator in Java.

```java
import java.util.Scanner;
import java.io.*;
class Calculator
{
    public static void main(String[] args)
    {
        int choice;
        int x = 0;
        int y = 0;
        int sum;
        PrintStream out;
        Scanner input;
        Calculator calc = new Calculator();
        try
        {
            out = new PrintStream("calclog.txt");
            do
            {
   System.out.println("Calculator Program"); System.out.println("--------------------\n");
                System.out.println("1. Add");
                System.out.println("2. Subtract");
                System.out.println("3. Multiply");
                System.out.println("4. Divide");
                System.out.println("5. Mod");
                System.out.println("6. Power");
                System.out.println("99. End Program\n");
            System.out.println("Enter Choice: ");
                input = new Scanner(System.in);
                choice = input.nextInt();
                while ((choice < 1 || choice > 6) && choice != 99)
                {
  System.out.println("Please enter 1, 2, 3, 4, 5, or 6: ");
                    choice = input.nextInt();
                }
                if (choice != 99)
                {
          System.out.println("Please enter 2 numbers only: ");
                    x = input.nextInt();
                    y = input.nextInt();
                }
                switch (choice)
                {
                    case 1:
                        sum = calc.add(x, y);
                 System.out.printf("The sum is %d\n\n", sum);
                        out.println(x + "+" + y + "=" + sum);
                        break;
                    case 2:
                        sum = calc.sub(x, y);
                System.out.printf("The answer is %d\n\n", sum);
                        out.println(x + "-" + y + "=" + sum);
                        break;
                    case 3:
                        sum = calc.multi(x, y);
                System.out.printf("The answer is %d\n\n", sum);
                        out.println(x + "*" + y + "=" + sum);
                        break;
                    case 4:
                        try
                        {
                            sum = calc.div(x, y);
               System.out.printf("The answer is %d\n\n", sum);
                            out.println(x + "/" + y + "=" + sum);
                        }
                      catch (Exception e)
                        {
     System.out.println("\nError: Cannot Divide by zero\n\n");
                        }
                        break;
                    case 5:
                  sum = calc.mod(x, y);
 System.out.printf("The mod is %d\n\n", sum);
out.println(x + "%" + y + "=" + sum);
                        break;
                    case 6:
                   sum = calc.pow(x, y)
            System.out.printf("The answer is %d\n\n", sum);
                        out.println(x + "^" + y + "=" + sum);
                        break;
                }
            }
            while (choice != 99);
            input.close();
        System.out.println("Ending program...");
        }
        catch (Exception e){
        System.out.println("ERROR: Some error occured");
            e.printStackTrace();
        }
    }
    public int add(int num1, int num2)
    {int sum;
        sum = num1 + num2;
        return sum;
    }
    public int sub(int num1, int num2)
    { int sum;
        sum = num1 - num2;
        return sum;
    }
    public int multi(int num1, int num2)
    { int sum;
        sum = num1 * num2;
        return sum;
    }
    public int div(int num1, int num2)
    {int sum;
        sum = num1 / num2;
        return sum;
    }
    public int mod(int num1, int num2)
    {int sum;
        sum = num1 % num2;
        return sum;
    }
    public int pow(int base, int exp)
    {int sum = 1;
if (exp == 0)
        {sum = 1;
        }
        while (exp > 0)
        {sum = sum * base;
            exp--;
}
        return sum;
    }
}
```