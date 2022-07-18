# Top Java Programming Interview Questions

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

## 12. Program to Calculate Mean in Java.

```java
import java.util.Scanner;

class CalculateMean
{

    public static void main(String[] args)
    {

        int sum = 0, inputNum;
        int counter;
        float mean;
        Scanner NumScanner = new Scanner(System.in);

        System.out.println("Enter the total number of terms whose mean you want to calculate");

        counter = NumScanner.nextInt();

        System.out.println("Please enter " + counter + " numbers:");

        for (int x = 1; x <= counter; x++)
        {
            inputNum = NumScanner.nextInt();
            sum = sum + inputNum;
            System.out.println();
        }

        mean = sum / counter;
        System.out.println("The mean of the " + counter + " numbers you entered is " + mean);
    }
}
```

## 13. Program to Convert Binary to Decimal in Java.

```java
import java.io.*;

class BinaryToDecimal
{
    public static void main(String[] args) throws Exception
    {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        System.out.print("Enter Binary no. to convert in Decimal : ");
        String number = br.readLine();

        /*
          to convert Binary number to decimal number use,
          int parseInt method of Integer wrapper class.

          Pass 2 as redix second argument.
         */

        int decimalNumber = Integer.parseInt(number, 2);
        System.out.println("Binary number converted to decimal number");
        System.out.println("Decimal number is : " + decimalNumber);

    }
}
```

## 14. Program to Convert Binary to Octal in Java.

```java
import java.io.*;

class BinaryToOctal
{
    public static void main(String[] args) throws Exception
    {
        String num = null;
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        System.out.print("Enter binary number : ");
        num = br.readLine();
        int dec = Integer.parseInt(num, 2);

        String oct = Integer.toOctalString(dec);

        System.out.println("Binary " + num + " in Octal is " + oct);

    }
}
```

## 15. Program to Convert Decimal to Binary in Java.

```java
import java.util.Scanner;

class DecimalToBinary
{

    public String toBinary(int n)
    {
        if (n == 0)
        {
            return "0";
        }

        String binary = "";
        while (n > 0)
        {
            int rem = n % 2;
            binary = rem + binary;
            n = n / 2;
        }

        return binary;
    }

    public static void main(String[] args)
    {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int decimal = scanner.nextInt();

        DecimalToBinary decimalToBinary = new DecimalToBinary();
        String binary = decimalToBinary.toBinary(decimal);

        System.out.println("The binary representation is " + binary);
    }
}
```

## 16. Program to Find Fraction Addition in Java.

```java
import java.util.*;

class FractionAdding
{
    public static void main(String args[])
    {
        float a, b, c, d;
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a : ");
        a = scanner.nextFloat();
        System.out.print("Enter b : ");
        b = scanner.nextFloat();
        System.out.print("Enter c : ");
        c = scanner.nextFloat();
        System.out.print("Enter d : ");
        d = scanner.nextFloat();

        // fraction addition formula ((a*d)+(b*c))/(b*d)
        System.out.print("Fraction Addition : [( " + a + " * " + d + " )+( " + b + " * " + c + " ) / ( " + b + " * " + d + " )] = " + (((a * d) + (b * c)) / (b * d)));
    }
}
```

## 17. Program to Find Fraction Subtraction in Java.

```java
import java.util.*;

class FractionSubtraction
{
 public static void main(String args[])
 {
  float a,b,c,d;
  Scanner scanner = new Scanner(System.in);
  System.out.print("Enter a : ");
  a = scanner.nextFloat();
  System.out.print("Enter b : ");
  b = scanner.nextFloat();
  System.out.print("Enter c : ");
  c = scanner.nextFloat();
  System.out.print("Enter d : ");
  d = scanner.nextFloat();

  // fraction addition formula ((a*d)-(b*c))/(b*d)
  System.out.print("Fraction subtraction : [( "+a+" * "+d+" )-( "+b+" * "+c+" ) / ( "+b+" * "+d+" )] = "+(((a*d)-(b*c))/(b*d)));
 }
}
```

## 18. Program to Find GCDLCM in Java.

```java
import java.util.Scanner;

class GCDLCM
{
    public static void main(String args[])
    {
        int x, y;
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter the two numbers: ");
        x = sc.nextInt();
        y = sc.nextInt();

        System.out.println("GCD of two numbers is : " + gcd(x, y));
        System.out.println("LCM of two numbers is : " + lcm(x, y));
    }

    static int gcd(int x, int y)
    {
        int r = 0, a, b;
        a = (x > y) ? x : y; // a is greater number
        b = (x < y) ? x : y; // b is smaller number

        r = b;
        while (a % b != 0)
        {
            r = a % b;
            a = b;
            b = r;
        }
        return r;
    }

    static int lcm(int x, int y)
    {
        int a;
        a = (x > y) ? x : y; // a is greater number
        while (true)
        {
            if (a % x == 0 && a % y == 0)
            {
                return a;
            }
            ++a;
        }
    }
}
```

## 19. Program to Find Harmonic Series in Java.

```java
import java.util.*;

class HarmonicSeries
{

    public static void main(String args[])
    {

        int num, i = 1;
        double rst = 0.0;

        Scanner in = new Scanner(System.in);
        System.out.println("Enter the number for length of series");
        num = in.nextInt();

        while (i <= num)
        {

            System.out.print("1/" + i + " +");
            rst = rst + (double) 1 / i;

            i++;
        }

        System.out.println("\n\nSum of Harmonic Series is " + rst);
    }
}
```

## 20. Program to Create Multiplication Table in Java.

```java
import java.util.Scanner;

class MultiplicationTable
{

    public static void main(String args[])
    {

        int n, c;
        System.out
                .println("Enter an integer to print it's multiplication table");

        Scanner in = new Scanner(System.in);
        n = in.nextInt();
        System.out.println("Multiplication table of " + n + " is :-");

        for (c = 1; c <= 10; c++)
        {
            System.out.println(n + "*" + c + " = " + (n * c));
        }

    }
}
```

## 21. Alphabet Pattern in Java.

<pre>
A 
BB 
CCC
DDDD
EEEEE
</pre>

```java
import java.util.*;

class AlphabetPattern
{
    public static void main(String[] arg)
    {
        int line, row, col;
        char ch = 'A';
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter number of lines : ");
        line = scanner.nextInt();

        for (row = 1; row <= line; row++)
        {
            for (col = 1; col <= row; col++)
            {
                System.out.print("" + ch);
            }
            System.out.println();
            ch++;
        }
    }
}
```

## 22. Binary pattern in Java.

<pre>
1
01
101
0101
10101 
</pre>

```java
       class BinaryPattern
{
    public static void main(String s[])
    {
        int i, j;
 int count = 1;
        for (i = 1; i <= 5; i++)
        {
            for (j = 1; j <= i; j++)
            {
                System.out.format("%d", count++ % 2);
                if (j == i && i != 5)
                    System.out.println("");
            }

            if (i % 2 == 0)
                count = 1;
            else
                count = 0;
        }
    }
}
```

## 23. Christmas tree in Java.

```java
class ChristmasTree
{
    public static final int segments = 4;
    public static final int height = 4;

    public static void main(String[] args)
    {
        makeTree();
    }

    public static void makeTree()
    {
        int maxStars = 2 * height + 2 * segments - 3;
        String maxStr = "";
        for (int l = 0; l < maxStars; l++)
        {
            maxStr += " ";
        }

        for (int i = 1; i <= segments; i++)
        {
            for (int line = 1; line <= height; line++)
            {
                String starStr = "";
                for (int j = 1; j <= 2 * line + 2 * i - 3; j++)
                {
                    starStr += "*";
                }

                for (int space = 0; space <= maxStars - (height + line + i); space++)
                {
                    starStr = " " + starStr;
                }
                System.out.println(starStr);
            }
        }

        for (int i = 0; i <= maxStars / 2; i++)
        {
            System.out.print(" ");
        }

        System.out.println(" " + "*" + " ");

        for (int i = 0; i <= maxStars / 2; i++)
        {
            System.out.print(" ");
        }

        System.out.println(" " + "*" + " ");

        for (int i = 0; i <= maxStars / 2 - 3; i++)
        {
            System.out.print(" ");
        }

        System.out.println(" " + "*******");
    }
}
```

## 24. Christmas tree pattern in Java.

  <pre>
      X
      X
     XXX
      X
    XXXXX
      X
     XXX
   XXXXXX 
</pre>

```java
class ChristmasTreePattern
{
    public static void main(String[] arg)
    {
        drawChristmasTree(4);
    }

    private static void drawChristmasTree(int n)
    {
        for (int i = 0; i < n; i++)
        {
            triangle(i + 1, n);
        }
    }

    private static void triangle(int n, int max)
    {
        for (int i = 0; i < n; i++)
        {
            for (int j = 0; j < max - i - 1; j++)
            {
                System.out.print(" ");
            }

            for (int j = 0; j < i * 2 + 1; j++)
            {
                System.out.print("X");
            }

            System.out.println("");
        }
    }
}
```
## 25. Floyd Triangle in Java.
<pre>
1
2 3 
4 5 6 
7 8 9 10
11 12 13 14 15 
</pre>

```java
import java.util.Scanner;

class FloydTriangle
{
    public static void main(String args[])
    {
        int n, num = 1, c, d;
        Scanner in = new Scanner(System.in);

        System.out.print("Enter the number of rows of floyd's triangle : ");
        n = in.nextInt();

        System.out.println("Floyd's triangle :-");

        for (c = 1; c <= n; c++)
        {
            for (d = 1; d <= c; d++)
            {
                System.out.print(num + " ");
                num++;
            }

            System.out.println();
        }
    }
}
```

## 26. Number pattern 1 in Java.
<pre>
1
12
123
1234
12345
</pre>

```java
class NumberPat1
{

    public static void main(String arg[])
    {

        for (int i = 1; i <= 5; i++)
        {

            for (int j = 1; j <= i; j++)
            {

                System.out.print(j);

            }

            System.out.println();
        }
    }
}
```

## 27. Number pattern 2 in Java.

```java
class NumberPat2
{

    public static void main(String arg[])
    {

        for (int i = 1; i <= 5; i++)
        {

            for (int j = 5; j >= i; j--)
            {

                System.out.print(j);

            }

            System.out.println();
        }
    }
}
```

## 28. Number pattern 3 in Java.
<pre>
12345
1234
123
12
1
</pre>

```java
class NumberPat3
{

    public static void main(String arg[])
    {

        for (int i = 1, r = 5; i <= 5; i++, r--)
        {

            for (int j = 1; j <= r; j++)
            {

                System.out.print(j);

            }

            System.out.println();
        }
    }
}
```

## 29. Number pattern 4 in Java.
<pre>
1
12
123
1234
12345
1234
123
12
1
</pre>

```java
class NumberPat4
{

    public static void main(String arg[])
    {

        int ck = 0, c = 2;

        while (c > 0)
        {

            if (ck == 0)
            {

                for (int i = 1; i <= 5; i++)
                {

                    for (int j = 1; j <= i; j++) 
                    {

                        System.out.print(j);

                    }

                    System.out.println();

                }

                ck++;

            }
            else
            {

                for (int i = 1, r = 5 - 1; i <= 5 - 1; i++, r--)
                {

                    for (int j = 1; j <= r; j++)
                    {

                        System.out.print(j);

                    }

                    System.out.println();
                }
            }

            c--;
        }

    }
}
```

## 30. Number pattern 5 in Java.
<pre>
12345
1234
123
12
1
12
123
1234
12345
</pre>

```java
class NumberPat5
{

    public static void main(String arg[])
    {

        int ck = 0, c = 2;

        while (c > 0)
        {

            if (ck == 0)
            {

                for (int i = 1, r = 5; i <= 5; i++, r--)
                {

                    for (int j = 1; j <= r; j++)
                    {

                        System.out.print(j);

                    }

                    System.out.println();

                }

                ck++;

            }
            else
            {

                for (int i = 2; i <= 5; i++)
                {

                    for (int j = 1; j <= i; j++)
                    {

                        System.out.print(j);

                    }

                    System.out.println();
                }
            }

            c--;
        }

    }
}
```

## 31. Number pattern 6 in Java.
<pre>
1 
22 
333 
4444 
55555
</pre>

```java
class NumberPat6
{

    public static void main(String arg[])
    {

        for(int i=1;i<=5;i++)
        {
            for(int j=1;j<=i;j++)
            {
                System.out.print(i);
            }

            System.out.println();
        }
    }
}
```


## 32. Number pattern 7 in Java.
<pre>
1
23
456
7890
12345
</pre>

```java
class NumberPat7
{

    public static void main(String arg[])
    {

        int t = 1;
        for (int i = 1; i <= 5; i++)
        {
            for (int j = 1; j <= i; j++)
            {
                if (t == 10)
                    t = 0;
                System.out.print(t++);
            }
            System.out.println();
        }
    }
}
```

## 33. Number pattern 8 in Java.

<pre>
5
11111 
0000 
111 
00 
1
</pre>

```java
import java.util.Scanner;

class Pattern
{
    public static void main(String args[])
    {
        int n, i, j;
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter the number of rows ");
        n = sc.nextInt();

        for (i = 1; i <= n; i++)
        {
            for (j = i; j <= n; j++)
            {
                if (i % 2 == 0)
                    System.out.print("0");
                else
                    System.out.print("1");
            }
            System.out.println();
        }
    }
}
```

## 34. Number pattern 9 in Java.
<pre>
        1 
      1 2 1 
    1 2 3 2 1 
  1 2 3 4 3 2 1 
1 2 3 4 5 4 3 2 1
</pre>

```java
class PrintPattern
{
    public static void main(String args[])
    {
        int n = 5;
        for (int i = 1; i <= n; i++)
        {
            int j = n - i;
            while (j > 0)
            {
                System.out.print("  ");
                j--;
            }

            j = 1;
            while (j <= i)
            {
                System.out.print(" " + j);
                j++;
            }

            j = i - 1;
            while (j > 0)
            {
                System.out.print(" " + j);
                j--;
            }

            j = n - i;
            while (j > 0)
            {
                System.out.print("  ");
                j--;
            }
            System.out.println();
        }
    }
}
```

## 35. Number pattern 10 in Java.
<pre>
1 
121 
12321 
1234321 
123454321 
12345654321 
1234567654321
</pre>

```java
import java.util.*;

class Pattern
{
    public static void main(String[] args)
    {
        int i, j, k = 1, l, n;
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter the number of levels of pattern");
        n = sc.nextInt();

        System.out.println("\nPattern is : \n");

        for (i = 1; i <= n; i++)
        {
            l = i;

            for (j = 1; j <= k; j++)
            {
                if (j >= i + 1)
                {
                    System.out.print(--l);
                }

                else
                {
                    System.out.print(j);
                }
            }

            k = k + 2;
            System.out.println(" ");
        }
    }
}
```

## 36. Star Pattern 1 in Java.
<pre>
****
*** 
**
*
</pre>

```java
class StarPattern1
{

    public static void main(String arg[])
    {

        for (int i = 1; i <= 5; i++)
        {

            for (int j = i; j <= 5; j++)

            {

                System.out.print("*");

            }

            System.out.println();
        }
    }
}
```

## 37. Star Pattern 2 in Java.

<pre>
* 
**
***
****
*****
</pre>

```java
class StarPattern2
{

    public static void main(String arg[])
    {

        for (int i = 1; i <= 5; i++)
        {
            for (int j = 1; j <= i; j++)

            {
                System.out.print("*");
            }

            System.out.println();
        }
    }
}
```

## 38. Star Pattern 3 in Java.
<pre>
*****
****
***
**
*
*
**
***
****
*****
</pre>
```java
class StarPattern3
{

    public static void main(String arg[])
    {

        for (int i = 1; i <= 5; i++)
        {
            for (int j = i; j <= 5; j++)

            {
                System.out.print("*");
            }

            System.out.println();
        }

        for (int i = 1; i <= 5; i++)
        {
            for (int j = 1; j <= i; j++)

            {
                System.out.print("*");
            }

            System.out.println();
        }

    }
}
```
## 39. Star Pattern 4 in Java.
<pre>
**
****
******
********
**********
</pre>
```java
class StarPattern4
{

    public static void main(String arg[])
    {

        int num = 12;
        int f = 2;
        int g = num - 1;

        for (int i = 1; i <= (num / 2); i++)
        {

            for (int j = 1; j <= num; j++)
            {

                if (j >= f && j <= g)
                {

                    System.out.print(" ");

                }
                else
                {

                    System.out.print("*");

                }
            }

            f = f + 1;
            g = g - 1;

            System.out.println();
        }
    } 
}
```

## 40. Star Pattern 5 in Java.

<pre>
*
**
***
****
*****
*****
****
***
**
*
</pre>

```java
class StarPattern5
{

    public static void main(String arg[])
    {

        for (int i = 1; i <= 5; i++)
        {

            for (int j = 1; j <= i; j++)

            {
                System.out.print("*");
            }

            System.out.println();
        }

        for (int i = 1; i <= 5; i++)
        {

            for (int j = i; j <= 5; j++)

            {
                System.out.print("*");
            }

            System.out.println();
        }
    }
}
```

## 41. Triangle Pattern in Java.

```java
import java.io.*;

class Triangle
{
    public static void main(String arg[])
    {
        InputStreamReader istream = new InputStreamReader(System.in);
        BufferedReader read = new BufferedReader(istream);
        System.out.println("Enter Triangle Size : ");
        int num = 0;
        try
        {
            num = Integer.parseInt(read.readLine());
        }
        catch (Exception Number)
        {
            System.out.println("Invalid Number!");
        }

        for (int i = 1; i <= num; i++)
        {
            for (int j = 1; j < num - (i - 1); j++)
            {
                System.out.print(" ");
            }

            for (int k = 1; k <= i; k++)
            {
                System.out.print("*");
                for (int k1 = 1; k1 < k; k1 += k)
                {

                    System.out.print("*");
                }
            }

            System.out.println();
        }
    }
}
```

## 42. Add two Matrix in Java.

```java
import java.util.*;

class AddTwoMatrix
{
    int m, n;
    int first[][] = new int[m][n];
    int second[][] = new int[m][n];

    AddTwoMatrix(int[][] first, int[][] second, int m, int n)
    {
        this.first = first;
        this.second = second;
        this.m = m;
        this.n = n;
    }

    public static void main(String[] args)
    {
        int m, n, c, d;

        Scanner in = new Scanner(System.in);

        System.out.println("Enter the number of rows and columns of matrix");
        m = in.nextInt();
        n = in.nextInt();

        int first[][] = new int[m][n];
        int second[][] = new int[m][n];

        System.out.println("Enter the elements of first matrix");

        for (c = 0; c < m; c++)
        {
            for (d = 0; d < n; d++)
            {
                first[c][d] = in.nextInt();
            }
        }

        System.out.println("Enter the elements of second matrix");

        for (c = 0; c < m; c++)
        {
            for (d = 0; d < n; d++)
            {
                second[c][d] = in.nextInt();
            }
        }

        System.out.println("\nElements of First matrix is : ");

        for (c = 0; c < m; c++)
        {
            for (d = 0; d < n; d++)
            {
                System.out.print(first[c][d] + "\t");
            }
            System.out.println();
        }

        System.out.println("\nElements of Second matrix is : ");

        for (c = 0; c < m; c++)
        {
            for (d = 0; d < n; d++)
            {
                System.out.print(second[c][d] + "\t");
            }
            System.out.println();
        }

        AddTwoMatrix a = new AddTwoMatrix(first, second, m, n);
        //call by reference
        a.addmatrix(a); //Passing Object
    }

    //Function for Adding two matrix and storing in third matrix 
    public void addmatrix(AddTwoMatrix a)
    {
        int c, d;
        int sum[][] = new int[a.m][a.n];

        for (c = 0; c < a.m; c++)
        {
            for (d = 0; d < a.n; d++)
            {
                sum[c][d] = a.first[c][d] + a.second[c][d];
            }
        }

        System.out.println("\nSum of the two matrices is : ");

        for (c = 0; c < a.m; c++)
        {
            for (d = 0; d < a.n; d++)
            {
                System.out.print(sum[c][d] + "\t");
            }
            System.out.println();
        }
    }
}
```

## 43. Array of Arrays.

```java
class ArrayOfArraysAnimalDemo
{
    public static void main(String[] args)
    {
        String[][] animals = {{"DanaDog", "WallyDog", "JessieDog", "AlexisDog", "LuckyDog"}, {"BibsCat", "DoodleCat", "MillieCat", "SimonCat"}, {"ElyFish", "CloieFish", "GoldieFish", "OscarFish", "ZippyFish", "TedFish"}, {"RascalMule", "GeorgeMule", "GracieMule", "MontyMule", "BuckMule", "RosieMule"}};

        for (int i = 0; i < animals.length; i++)
        {
            System.out.print(animals[i][0] + ": ");

            for (int j = 1; j < animals[i].length; j++)
            {
                System.out.print(animals[i][j] + " ");
            }

            System.out.println();
        }
    }
}
```

## 44. Array operations.
```java
class ArrayOperations
{
    public static void main(String[] args)
    {
        double[] myList = {1.9, 2.9, 3.4, 3.5};

        // Print all the array elements
        for (int i = 0; i < myList.length; i++)
        {
            System.out.println(myList[i] + " ");
        }
        // Summing all elements
        double total = 0;
        for (int i = 0; i < myList.length; i++)
        {
            total += myList[i];
        }

        System.out.println("Total is " + total);

        // Finding the largest element
        double max = myList[0];
        for (int i = 1; i < myList.length; i++)
        {
            if (myList[i] > max)
                max = myList[i];
        }

        System.out.println("Max is " + max);
    }
}
```

## 45. Array Sort.
```java
import java.util.Arrays;

class ArraySort
{
    // This program is the example of  array sorting
    public static void main(String[] args)
    {
        // TODO Auto-generated method stub
        // initializing unsorted  array
        String iArr[] = {"Programming", "Hub", "Alice", "Wonder", "Land"};

        // sorting array
        Arrays.sort(iArr);

        // let us print all the elements available in list
        System.out.println("The sorted array is:");
        for (int i = 0; i < iArr.length; i++)
        {
            System.out.println(iArr[i]);
        }
    }
}
```
## 46. Array Sum and Average.
```java
import java.io.*;

class ArrayAverage
{
    public static void main(String[] args)
    {
        //define an array
        int[] numbers = new int[]{10, 20, 15, 25, 16, 60, 100};

        int sum = 0;

        for (int i = 0; i < numbers.length; i++)
        {
            sum = sum + numbers[i];
        }

        double average = sum / numbers.length;
        System.out.println("Sum of array elements is : " + sum);
        System.out.println("Average value of array elements is : " + average);
    }
}
```

## 47. Basic Array.
```java
import java.util.*;

class ArrayBasic
{
    public static void main(String[] args)
    {
        int[] arr;
        int size, i;

        Scanner sc = new Scanner(System.in);

        System.out.println("Enter size of array");
        size = sc.nextInt();

        arr = new int[size];

        System.out.println("\nEnter array elements");
        for (i = 0; i < size; i++)
        {
            arr[i] = sc.nextInt();
        }

        System.out.println("\nElements in the Array are : ");
        for (i = 0; i < size; i++)
        {
            System.out.print(arr[i] + " ");
        }
    }
}
```

## 48. Create & Display Matrix.
```java
import java.util.Scanner;
 
 class Matrix_Create {
 
 Scanner scan;
 int matrix[][];
 int row, column;
 
 void create() {
  
  scan = new Scanner(System.in);
  
  System.out.println("Matrix Creation");
  
  System.out.println("\nEnter number of rows :");
  row = Integer.parseInt(scan.nextLine());
  
  System.out.println("Enter number of columns :");
  column = Integer.parseInt(scan.nextLine());
  
  matrix = new int[row][column];
  System.out.println("Enter the data :");
 
  for(int i=0; i<row ; i++) {
   
   for(int j=0; j
    <column ; j++) {
    
    matrix[i][j] =scan.nextInt();
     }
  }
 }
 
 void display() {
  
  System.out.println("\nThe Matrix is :");
  
  for(int i=0; i <row ; i++) {
   
   for(int j=0; j <column ; j++) {
    
    System.out.print("\t" + matrix[i][j]);
   }
   System.out.println();
  }
 }
}
 
  class CreateAndDisplayMatrix {
 
 public static void main(String
     args[]) {
  
  Matrix_Create obj=new Matrix_Create();
  
  obj.create();
  obj.display();
 }
}
```

## 49. Display Array using for-each loop.
```java
class DisplayArrayForEach
{
    public static void main(String[] args)
    {
        double[] myList = {1.9, 2.9, 3.4, 3.5};

        // Print all the array elements
        for (double element : myList)
        {
            System.out.println(element);
        }
    }
}
```

## 50. Double Matrix.
```java
import java.util.*;
import java.text.DecimalFormat;

class DoubleMatrix
{
    public static void main(String[] args)
    {
        double[][] a;
        double[] s;
        int row, col, k = 0, i, j;
        double sum = 0.0;

        DecimalFormat f = new DecimalFormat("##.####");
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter size of row and column");
        row = sc.nextInt();
        col = sc.nextInt();

        a = new double[row][col];
        s = new double[col];

        System.out.println("Enter elements of matrix");
        for (i = 0; i < row; i++)
        {
            for (j = 0; j < col; j++)
            {
                a[i][j] = sc.nextDouble();
            }
        }

        System.out.println("Double Matrix is : ");
        for (i = 0; i < row; i++)
        {
            for (j = 0; j < col; j++)
            {
                System.out.print(" " + a[i][j]);
            }
            System.out.println();
        }

        //sum of the elements of double matrix

        for (i = 0; i < col; i++)
        {
            for (j = 0; j < row; j++)
            {
                sum = sum + a[j][i];
            }
            s[k] = sum;
            k++;
            sum = 0;
        }

        for (i = 0; i < col; i++)
        {
            System.out.println("Sum of Column " + (i + 1) + " is : " + f.format(s[i]));
        }
    }
}
```

## 51. Example to Pass Arrays to function.
```java
import java.util.*;
class PassingArraystoFunction 
{
    public static void main(String[] args) 
    {
        int[] a;
        int size;
        
        Scanner sc = new Scanner(System.in);
        
        System.out.println("Enter size of array");
        size = sc.nextInt();
        
        a = new int[size];
        
        System.out.println("Enter elements in the array");
        for(int i = 0 ;i < size; i++)
        {
            a[i] = sc.nextInt();
        }

        System.out.println("The Elements of the array are : ");
        for(int i = 0 ;i < size; i++)
        {
            System.out.print(a[i] + " ");
        }

        //Passing array to the function
        addElements(a, size);
    }
    
    public static void addElements(int[] a , int size)
    {
        int sum = 0;
        
        for(int i = 0; i < size; i++)
        {
            sum += a[i];
        }

        System.out.println("\nSum of the elements of arrays is : "+sum);
    }
}
```

## 52. Find closest value of a number in an Array.
```java
import java.util.*;

class ClosestValue
{
    public static void main(String[] args)
    {
        int a[];
        int find;
        int closest = 0;

        Scanner sc = new Scanner(System.in);

        System.out.println("Enter size of array");
        int size = sc.nextInt();

        a = new int[size];

        System.out.println("Enter numbers in array");
        for (int i = 0; i < size; i++)
        {
            a[i] = sc.nextInt();
        }

        System.out.println("Numbers are : ");
        for (int i = 0; i < size; i++)
        {
            System.out.print(a[i] + " ");
        }

        System.out.println();
        System.out.println("Enter Number to find closest value");
        find = sc.nextInt();

        int distance = Math.abs(closest - find);

        for (int i : a)
        {
            int distanceI = Math.abs(i - find);
            if (distance > distanceI)
            {
                closest = i;
                distance = distanceI;
            }
        }

        System.out.println("Closest Value is : " + closest);
    }

}
```

## 53. Magic Matrix.
```java
import java.io.*;

class MagicMatrix
{
    public static void main(String args[]) throws IOException
    {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        System.out.print("Enter the size of the matrix : ");
        int n = Integer.parseInt(br.readLine());

        if (n > 5)
            System.out.println("Enter a number between 1 to 5 ");
        else
        {
            int A[][] = new int[n][n]; // Creating the Magic Matrix
            int i, j, k, t;
         
            /*Initializing every cell of the matrix with 0 */
            for (i = 0; i < n; i++)
            {
                for (j = 0; j < n; j++)
                {
                    A[i][j] = 0;
                }
            }

            /* When the size of the matrix is Odd */
            if (n % 2 != 0)
            {
                i = 0;
                j = n / 2;
                k = 1;
                while (k <= n * n)
                {
                    A[i][j] = k++;
                    i--; // Making one step upward
                    j++; // Moving one step to the right

                    if (i < 0 && j > n - 1) // Condition for the top-right corner element
                    {
                        i = i + 2;
                        j--;
                    }

                    if (i < 0) // Wrapping around the row if it goes out of boundary
                        i = n - 1;

                    if (j > n - 1) // Wrapping around the column if it goes out of boundary
                        j = 0;

                    if (A[i][j] > 0) // Condition when the cell is already filled
                    {
                        i = i + 2;
                        j--;
                    }
                }
            }
            /* When the size of the matrix is even */
            else
            {
                k = 1;
             
                /* Filling the matrix with natural numbers from 1 till n*n */
                for (i = 0; i < n; i++)
                {
                    for (j = 0; j < n; j++)
                    {
                        A[i][j] = k++;
                    }
                }

                j = n - 1;

                for (i = 0; i < n / 2; i++)
                {
                    /* swapping corner elements of primary diagonal */
                    t = A[i][i];
                    A[i][i] = A[j][j];
                    A[j][j] = t;
                 
                    /* swapping corner elements of secondary diagonal */
                    t = A[i][j];
                    A[i][j] = A[j][i];
                    A[j][i] = t;

                    j--;
                }
            }

            /* Printing the Magic matrix */
            System.out.println("The Magic Matrix of size " + n + "x" + n + " is:");
            for (i = 0; i < n; i++)
            {
                for (j = 0; j < n; j++)
                {
                    System.out.print(A[i][j] + "\t");
                }
                System.out.println();
            }
        }
    }
}
```

## 54. Matrix Addition.
```java
import java.util.Scanner; 
  
 class MatrixAddition { 
  
 Scanner scan; 
 int matrix1[][], matrix2[][], sum[][]; 
 int row, column; 
  
 void create() { 
   
  scan = new Scanner(System.in); 
   
  System.out.println("Matrix Addition"); 
   
  // First Matrix Creation.. 
  System.out.println("\nEnter number of rows & columns"); 
  row = Integer.parseInt(scan.nextLine()); 
  column = Integer.parseInt(scan.nextLine()); 
   
  matrix1 = new int[row][column]; 
  matrix2 = new int[row][column]; 
  sum = new int[row][column]; 
  
  System.out.println("Enter the data for first matrix :"); 
  
  for(int i=0; i &lt row; i++) { 
    
   for(int j=0; j &lt column; j++) { 
     
    matrix1[i][j] = scan.nextInt(); 
   } 
  } 
   
  // Second Matrix Creation.. 
  System.out.println("Enter the data for second matrix :"); 
  
  for(int i=0; i &lt row; i++) { 
    
   for(int j=0; j &lt column; j++) { 
     
    matrix2[i][j] = scan.nextInt(); 
   } 
  } 
 } 
  
 void display() { 
   
  System.out.println("\nThe First Matrix is :"); 
   
  for(int i=0; i &lt row; i++) { 
    
   for(int j=0; j &lt column; j++) { 
     
    System.out.print("\t" + matrix1[i][j]); 
   } 
   System.out.println(); 
  } 
   
  System.out.println("\n\nThe Second Matrix is :"); 
   
  for(int i=0; i &lt row; i++) { 
    
   for(int j=0; j &lt column; j++) { 
     
    System.out.print("\t" + matrix2[i][j]); 
   } 
   System.out.println(); 
  } 
 } 
  
 void add() { 
   
  for(int i=0; i &lt row; i++) { 
    
   for(int j=0; j &lt column; j++) { 
     
    sum[i][j] = matrix1[i][j] + matrix2[i][j]; 
   } 
  } 
   
  System.out.println("\n\nThe Sum is :"); 
   
  for(int i=0; i &lt row; i++) { 
    
   for(int j=0; j &lt column; j++) { 
     
    System.out.print("\t" + sum[i][j]); 
   } 
   System.out.println(); 
  } 
 } 
} 
  
class MatrixAdditionExample { 
  
 public static void main(String args[]) { 
   
  MatrixAddition obj = new MatrixAddition(); 
   
  obj.create(); 
  obj.display(); 
  obj.add(); 
 } 
}
```

## 55. Matrix Multiplication. 
```java
import java.util.Scanner;

class MatrixMultiplication
{
    public static void main(String args[])
    {
        int m, n, p, q, sum = 0, c, d, k;

        Scanner in = new Scanner(System.in);
        System.out.println("Enter the number of rows and columns of first matrix");
        m = in.nextInt();
        n = in.nextInt();

        int first[][] = new int[m][n];

        System.out.println("Enter the elements of first matrix");

        for (c = 0; c < m; c++)
        {
            for (d = 0; d < n; d++)
            {
                first[c][d] = in.nextInt();
            }
        }

        System.out.println("Enter the number of rows and columns of second matrix");
        p = in.nextInt();
        q = in.nextInt();

        if (n != p)
            System.out.println("Matrices with entered orders can't be multiplied with each other.");
        else
        {
            int second[][] = new int[p][q];
            int multiply[][] = new int[m][q];

            System.out.println("Enter the elements of second matrix");

            for (c = 0; c < p; c++)
            {
                for (d = 0; d < q; d++)
                {
                    second[c][d] = in.nextInt();
                }
            }

            for (c = 0; c < m; c++)
            {
                for (d = 0; d < q; d++)
                {
                    for (k = 0; k < p; k++)
                    {
                        sum = sum + first[c][k] * second[k][d];
                    }

                    multiply[c][d] = sum;
                    sum = 0;
                }
            }

            System.out.println("Product of entered matrices:-");

            for (c = 0; c < m; c++)
            {
                for (d = 0; d < q; d++)
                {
                    System.out.print(multiply[c][d] + "\t");
                }

                System.out.print("\n");
            }
        }
    }
}

```

## 56. Matrix Operations. 
```java
import java.util.Scanner; 
 
public class Matrices { 
 
   public static void main(String[] args) { 
     
       Scanner scanner = new Scanner(System.in); 
        
       System.out.print("Enter number of rows: "); 
       int rows = scanner.nextInt(); 
        
       System.out.print("Enter number of columns: "); 
       int columns = scanner.nextInt(); 
        
       System.out.println(); 
       System.out.println("Enter first matrix"); 
       int[][] a = readMatrix(rows, columns); 
        
       System.out.println(); 
       System.out.println("Enter second matrix"); 
       int[][] b = readMatrix(rows, columns); 
        
       int[][] sum = add(a, b); 
       int[][] difference1 = subtract(a, b); 
       int[][] difference2 = subtract(b, a); 
        
       System.out.println(); 
       System.out.println("A + B ="); 
       printMatrix(sum); 
        
       System.out.println(); 
       System.out.println("A - B ="); 
       printMatrix(difference1); 
        
       System.out.println(); 
       System.out.println("B - A ="); 
       printMatrix(difference2); 
   } 
 
   public static int[][] readMatrix(int rows, int columns) { 
     
       int[][] result = new int[rows][columns]; 
       Scanner s = new Scanner(System.in); 
        
       for (int i = 0; i < rows; i++) { 
         
           for (int j = 0; j < columns; j++) { 
             
               result[i][j] = s.nextInt(); 
                
           } 
       } 
       return result; 
   } 
 
   public static int[][] add(int[][] a, int[][] b) { 
     
       int rows = a.length; 
       int columns = a[0].length; 
       int[][] result = new int[rows][columns]; 
        
       for (int i = 0; i < rows; i++) { 
         
           for (int j = 0; j < columns; j++) { 
             
               result[i][j] = a[i][j] + b[i][j]; 
                
           } 
       } 
       return result; 
   } 
 
   public static int[][] subtract(int[][] a, int[][] b) { 
     
       int rows = a.length; 
       int columns = a[0].length; 
       int[][] result = new int[rows][columns]; 
        
       for (int i = 0; i < rows; i++) { 
         
           for (int j = 0; j < columns; j++) { 
             
               result[i][j] = a[i][j] - b[i][j]; 
                
           } 
       } 
       return result; 
   } 
 
   public static void printMatrix(int[][] matrix) { 
     
       int rows = matrix.length; 
       int columns = matrix[0].length; 
        
       for (int i = 0; i < rows; i++) { 
         
           for (int j = 0; j < columns; j++) { 
             
               System.out.print(matrix[i][j] + "  "); 
                
           } 
           System.out.println(); 
       } 
   } 
}
```

## 57. Matrix Subtraction.
```java
import java.util.Scanner; 
  
 class Matrix_Subtraction { 
  
 Scanner scan; 
 int matrix1[][], matrix2[][], sub[][]; 
 int row, column; 
  
 void create() { 
   
  scan = new Scanner(System.in); 
   
  System.out.println("Matrix Subtraction"); 
   
  // First Matrix Creation.. 
  System.out.println("\nEnter number of rows & columns"); 
  row = Integer.parseInt(scan.nextLine()); 
  column = Integer.parseInt(scan.nextLine()); 
   
  matrix1 = new int[row][column]; 
  matrix2 = new int[row][column]; 
  sub = new int[row][column]; 
  
  System.out.println("Enter the data for first matrix :"); 
  
  for(int i=0; i &lt row; i++) { 
    
   for(int j=0; j &lt column; j++) { 
     
    matrix1[i][j] = scan.nextInt(); 
   } 
  } 
   
  // Second Matrix Creation.. 
  System.out.println("Enter the data for second matrix :"); 
  
  for(int i=0; i &lt row; i++) { 
    
   for(int j=0; j &lt column; j++) { 
     
    matrix2[i][j] = scan.nextInt(); 
   } 
  } 
 } 
  
 void display() { 
   
  System.out.println("\nThe First Matrix is :"); 
   
  for(int i=0; i &lt row; i++) { 
    
   for(int j=0; j &lt column; j++) { 
     
    System.out.print("\t" + matrix1[i][j]); 
   } 
   System.out.println(); 
  } 
   
  System.out.println("\n\nThe Second Matrix is :"); 
   
  for(int i=0; i &lt row; i++) { 
    
   for(int j=0; j &lt column; j++) { 
     
    System.out.print("\t" + matrix2[i][j]); 
   } 
   System.out.println(); 
  } 
 } 
  
 void sub() { 
   
  for(int i=0; i &lt row; i++) { 
    
   for(int j=0; j &lt column; j++) { 
     
    sub[i][j] = matrix1[i][j] - matrix2[i][j]; 
   } 
  } 
   
  System.out.println("\n\nThe Subtraction is :"); 
   
  for(int i=0; i &lt row; i++) { 
    
   for(int j=0; j &lt column; j++) { 
     
    System.out.print("\t" + sub[i][j]); 
   } 
   System.out.println(); 
  } 
 } 
} 
  
class MatrixSubtractionExample { 
  
 public static void main(String args[]) { 
   
  Matrix_Subtraction obj = new Matrix_Subtraction(); 
   
  obj.create(); 
  obj.display(); 
  obj.sub(); 
 } 
}
```
## 58. Merge two array. 
```java
class MergeArrayDemo
{
 public static void main(String args[])
 {
  Integer a[]={1,2,3,4};
  Integer b[]={5,6,7,0};
  Integer[] both = concat(a, b);
  
  System.out.print("\nFirst  Array : ");
  for(int i=0;i<a.length;i++)
  {
   System.out.print(a[i]+"\t");
  }

  System.out.print("\nSecond Array : ");
  for(int i=0;i<b.length;i++)
  {
   System.out.print(b[i]+"\t");
  }

  System.out.print("\nMerged Array : ");
  for(int i=0;i<both.length;i++)
  {
   System.out.print(both[i]+"\t");
  }
 }

 public static Integer[] concat(Integer[] a, Integer[] b)
 {
  int aLen = a.length;
  int bLen = b.length;
  Integer[] c= new Integer[aLen+bLen];
  System.arraycopy(a, 0, c, 0, aLen);
  System.arraycopy(b, 0, c, aLen, bLen);
  return c;
 }
}
```
## 59. Middle value of an array.

```java
import java.util.*;

class MiddleValue
{
    public static void main(String args[])
    {
        int[] a;
        int i, j, n, sum = 0, swap, size;

        double t;
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter size of array");
        size = sc.nextInt();

        a = new int[size];

        System.out.println("Enter numbers ");
        for (i = 0; i < size; i++)
        {
            a[i] = sc.nextInt();
        }

        System.out.println("Numbers are : ");
        for (i = 0; i < size; i++)
        {
            System.out.print(a[i] + " ");
        }

        //Sorting
        for (i = 0; i < (size - 1); i++)
        {
            for (j = 0; j < (size - i - 1); j++)
            {
                if (a[j] > a[j + 1])
                {
                    swap = a[j];
                    a[j] = a[j + 1];
                    a[j + 1] = swap;
                }
            }
        }

        System.out.println("\nNumbers in sorted order : ");
        for (i = 0; i < size; i++)
        {
            System.out.print(a[i] + " ");
        }

        //Finding the Middle Value
        if (size % 2 == 0)
        {
            n = (size + 1) / 2;
            t = (a[n] + a[n - 1]) / 2.0;
            System.out.println("\nMiddle Value is : " + t);
        }

        else
        {
            System.out.println("\nMiddle Value is : " + a[size / 2]);
        }

    }
}
```


## 60. Mirror Matrix.
```java
import java.util.*;

class MirrorMatrix
{
    public static void main(String[] args)
    {
        int row, column;
        Scanner in = new Scanner(System.in);

        System.out.print("Enter number of rows for matrix :");
        row = in.nextInt();
        System.out.print("Enter number of rows for matrix :");
        column = in.nextInt();

        int matrix[][] = new int[row][column];

        System.out.println("Enter matrix : ");

        for (int i = 0; i < row; i++)
        {
            for (int j = 0; j < column; j++)
            {
                matrix[i][j] = in.nextInt();
            }
        }

        System.out.println("Mirror matrix : ");

        for (int i = 0; i < row; i++)
        {
            for (int j = column - 1; j >= 0; j--)
            {
                System.out.print(matrix[i][j] + "\t");
            }

            System.out.println("");
        }
    }
}
```
## 61. Missing number in an array.

```java
class MissingNumberArray
{
    public static int count = 0;
    public static int position = 0;
    public static boolean flag = false;

    public static void main(String[] args)
    {
        int a[] = {0, 1, 2, 3, 4, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 18, 20, 21, 23};

        findMissingNumbers(a, position);
    }

    private static void findMissingNumbers(int a[], int position)
    {
        if (position == a.length - 1)
            return;

        for (; position < a[a.length - 1]; position++)
        {
            if ((a[position] - count) != position)
            {
                System.out.println("Missing Number: " + (position + count));
                flag = true;
                count++;
                break;
            }
        }

        if (flag)
        {
            flag = false;
            findMissingNumbers(a, position);
        }
    }
}
```




## 62. Multidimensional Array Java.

```java
class MultiDimArrayExample
{
    public static void main(String[] args)
    {
        String[][] names = {{"Mr. ", "Mrs. ", "Ms. "}, {"Smith", "Jones"}};
        // Mr. Smith
        System.out.println(names[0][0] + names[1][0]);
        // Ms. Jones
        System.out.println(names[0][2] + names[1][1]);
    }
}
```
