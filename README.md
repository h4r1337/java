# java

#### Write a java program to find the sum of digits of a given number. Use command line arguments.

```java
class Sum {
    public static void main(String args[]) {
        int i, n, r, sum=0, n1;
        n = integer.parseInt(args[0]);
        n2 = n;
        while (n > 0) {
            r = n%10;
            sum = sum+r;
            n = n/10;
        }
        System.out.println("Sum of the digits of number " + n1 + " = " + sum);
    }
}
```

#### Write a program to find area and perimeter of a circle using class


```java
import java.util.Scanner;
class CircFind {
    double rad;
    double area() {
        return 3.14 * rad * rad;
    }
    double circum() {
        return 2*3.14*rad;
    }
}
class Circle {
    public static void main(String args[]) {
        CircFind myCirc = new CircFind();
        Scanner inObj = new Scanner(System.in);
        System.out.println("Enter the radius of the circle: ");
        myCirc.rad = inObj.nextDouble();
        System.out.println("The area of the circle is " + myCirc.area());
        System.out.println("The circumference of the circle is " + myCirc.circum());
    }
}
```

#### Prime number

```java
import java.util.Scanner;
class PrimFind {
    int n, flag, i, j;
    void primeOut() {
        for (i = 2; i <= n; i++) {
            flag = 0;
            for (j = 2; j <= i/2; j++) {
                if (i % J == 0) {
                    flag = 1;
                    break;
                }
            }
            if (flag == 0) {
                System.out.println(i);
            }
        }
    }
}

class Prime {
    public static void main(String args[]) {
        PrimFind myPrime = new PrimFind();
        Scanner inObj = new Scanner(System.in);
        System.out.println("Enter the limit: ");
        myPrime.n = inObj.nextInt();
        System.out.println("The prime numbers upto " + myPrime.n + " are:");
        myPrime.primeOut();
    }
}
```

#### Fibonacci series

```java
import java.util.Scanner;
class FiboFind {
    int n1, n2, n3, i, count;
    void fiboOut() {
        n1 = 0;
        n2 = 1;
        System.out.println(n1);
        System.out.println(n2);
        for (i = 3; i <= count; i++) {
            n3 = n1 + n2;
            n1 = n2;
            n2 = n3;
            System.out.println(n3);
        }
    }
}

class Fibonacci {
    public static void main(String args[]) {
        FiboFind myFibo = new FiboFind();
        Scanner inObj = new Scanner(System.in);
        System.out.println("Enter the count: ");
        myFibo.count = inObj.nextInt();
        System.out.println("The first " + myFibo.count + " Fibonacci numbers are:");
        myFibo.fiboOut();
    }
}
```

#### Roots of quadratic equation

```java
import java.util.Scanner;
class QuadEq {
    double a, b, c, d, r1, r2, r, re, im;
    void rootFind() {
        d = b*b-4*a*c;
        if (d > 0) {
            r1 = (-b + Math.sqrt(d))/(2*a);
            r2=(-b-Math.sqrt(d))/(2*a);
        } else if (d == 0) {
            r = -b/(2*a);
        } else {
            re = -b/(2*a);
            im = Math.sqrt(-d)/(2*a);
        }
   }
}

class Quad {
    public static void main(String[] args) {
        QuadEq myQuad = new QuadEq();
        Scanner inObj = new Scanner(System.in);
        System.out.println("Enter the coefficients a, b, c:");
        myQuad.a=inObj.nextDouble();
        myQuad.b=inObj.nextDouble();
        myQuad.c=inObj.nextDouble();
        myQuad.rootFind();
        if(myQuad.d>0) {
            System.out.println("The roots are real and distinct:");
            System.out.println("Root 1: "+myQuad.r1);
            System.out.println("Root 2: "+myQuad.r2);
        }
        else if(myQuad.d==0) {
            System.out.println("The roots are real and equal:");
            System.out.println("Root: "+myQuad.r);
        }
        else {
            System.out.println("The roots are complex:");
            System.out.println("Root 1: "+myQuad.re+" + "+myQuad.im+"i");
            System.out.println("Root 2: "+myQuad.re+" - "+myQuad.im+"i");
        }
    }
}
```

#### Matrix multiplication

```java
import java.util.Scanner;
class MatrixEq
{
    int i,j,k,s,m1,m2,n1,n2;
    int[][] a;
    int[][] b;
    int[][] mul;
    MatrixEq(int m1, int n1, int m2, int n2)
{
        this.m1 = m1;
        this.n1 = n1;
        this.m2 = m2;
        this.n2 = n2;
        a = new int[m1][n1];
        b = new int[m2][n2];
        mul = new int[m1][n2];
    }
    void matMul()
{
        for(i=0;i<m1;i++)
    {
            for(j=0;j<n2;j++)
        {
                mul[i][j]=0;
                for(k=0;k<n1;k++)
            {
                    mul[i][j]+=a[i][k]*b[k][j];
                }
            }
        }
    }
}
class Matrix
{
    public static void main(String args[])
{
        Scanner inObj=new Scanner(System.in);
        System.out.println("Enter the order of the matrix 1: ");
        System.out.println("\nEnter the number of rows: ");
        int m1=inObj.nextInt();
        System.out.println("\nEnter the number of columns: ");
        int n1=inObj.nextInt();
        System.out.println("Enter the order of the matrix 2: ");
        System.out.println("\nEnter the number of rows: ");
        int m2=inObj.nextInt();
        System.out.println("\nEnter the number of columns: ");
        int n2=inObj.nextInt();
        if(n1!=m2){
            System.out.println("\nMatrix multiplication not possible");
        }
        else
    {
            MatrixEq myMat=new MatrixEq(m1, n1, m2, n2);
            System.out.println("\nEnter the elements of Matrix 1: ");
            for(int i=0;i<m1;i++){
                for(int j=0;j<n1;j++)
            {
                    myMat.a[i][j]=inObj.nextInt();
                }
            }
            System.out.println("\nEnter the elements of Matrix 2: ");
            for(int i=0;i<m2;i++)
        {
                for(int j=0;j<n2;j++)
            {
                    myMat.b[i][j]=inObj.nextInt();
                }
            }
            myMat.matMul();
            System.out.println("\nMatrix 1:");
            for(int i=0;i<m1;i++)
        {
                for(int j=0;j<n1;j++)
            {
                    System.out.print(myMat.a[i][j] + "\t");
                }
                System.out.println();
            }
            System.out.println("\nMatrix 2:");
            for(int i=0;i<m2;i++)
        {
                for(int j=0;j<n2;j++)
            {
                    System.out.print(myMat.b[i][j] + "\t");
                }
                System.out.println();
            }
            System.out.println("\nResultant Matrix: ");
            for(int i=0;i<m1;i++)
        {
                for(int j=0;j<n2;j++)
            {
                    System.out.print(myMat.mul[i][j]+"\t");
                }
                System.out.println();
            }
        }
    }
}
```

#### Sort numeric array

```java
import java.util.Scanner;
class NumArr
{
    int[] arr;
    int n,i,j,index,temp;
    NumArr(int n)
{
        this.n =n;
        arr=new int[n];
    }void sort()
{
        for (i=0;i<n-1;i++)
    {
            index=i;
            for (j=i+1;j<n;j++)
        {
                if (arr[j]<arr[index])
            {
                    index=j;
                }
            }
            temp=arr[i];
            arr[i]=arr[index];
            arr[index]=temp;
        }
    }
}class Linear
{
    public static void main(String args[])
{
        int i,n;
        Scanner inObj=new Scanner(System.in);
        System.out.println("Enter the number of elements in the array: ");
        n=inObj.nextInt();
        NumArr myArr=new NumArr(n);
        System.out.println("\nEnter the elements of the array: ");
        for(i=0;i<n;i++)
    {
            myArr.arr[i]=inObj.nextInt();
        }
        myArr.sort();
        System.out.println("\nSorted Array:");
        for(i=0;i<n;i++)
    {0
            System.out.print(myArr.arr[i]+"\t");
        }
    }
}
```

#### Student details

```java
import java.util.Scanner;
class Student
{
    String name;
    int rollno;
    int[] marks=new int[5];
    int total;
    double per;
    int i;
    void markCal()
{
        total=0;
        for (i=0;i<5;i++)
    {total=total+marks[i];
        }
        per=(double)total/500*100;
    }
}
public class StudDet
{
    public static void main(String args[])
{
        int i;
        Scanner inObj=new Scanner(System.in);
        Student myStud=new Student();
        System.out.println("Enter the student details: ");
        System.out.println("Enter student name:");
        myStud.name=inObj.nextLine();
        System.out.println("Enter roll number:");
        myStud.rollno=inObj.nextInt();
        System.out.println("Enter marks of 5 subjects:");
        for (i=0;i<5;i++)
    {
            myStud.marks[i] = inObj.nextInt();
        }
        myStud.markCal();
        System.out.println("\nStudent Details:");
        System.out.println("Name: "+myStud.name);
        System.out.println("Roll Number: "+myStud.rollno);
        System.out.println("Total Marks: "+myStud.total);
        System.out.println("Percentage: "+myStud.per+"%");
    }
}
```

#### Number of objects

```java
class ObjectCounter
{
    static int count = 0;
    ObjectCounter()
{
        count++;
    }
    public static void main(String args[])
{
        ObjectCounter obj1 = new ObjectCounter();
        ObjectCounter obj2 = new ObjectCounter();
        ObjectCounter obj3 = new ObjectCounter();
        System.out.println("Number of objects created: "+count);
    }
}
```

#### Complex number

```java
class CompNum
{
    double real,imag;
    CompNum(double real, double imag){
        this.real=real;
        this.imag=imag;
    }
    CompNum()
{
        this.real=0;
        this.imag=0;
    }
    CompNum add(CompNum other)
{
        return new CompNum(this.real+other.real,this.imag+other.imag);
    }
    CompNum sub(CompNum other)
{
        return new CompNum(this.real-other.real,this.imag-other.imag);
    }
    void print()
{
        System.out.println(this.real+" + "+this.imag+"i");
    }
}
class Complex
{
    public static void main(String args[])
{
        CompNum num1=new CompNum(2, 3);
        CompNum num2=new CompNum(1, 2);
        CompNum sum=num1.add(num2);
        CompNum diff=num1.sub(num2);
        System.out.print("Number 1: ");
        num1.print();
        System.out.print("Number 2: ");
        num2.print();
        System.out.print("Sum: ");
        sum.print();
        System.out.print("Difference: ");
        diff.print();
    }
}
```

#### Method overloading

```java
class Complex
{
    public static void main(String args[])
{
        CompNum num1=new CompNum(2, 3);
        CompNum num2=new CompNum(1, 2);
        CompNum sum=num1.add(num2);
        CompNum diff=num1.sub(num2);
        System.out.print("Number 1: ");
        num1.print();
        System.out.print("Number 2: ");
        num2.print();
        System.out.print("Sum: ");
        sum.print();
        System.out.print("Difference: ");
        diff.print();
    }
}
class Area
{
    public static void main(String args[])
{
        AreaFind myArea=new AreaFind();
        Scanner inObj=new Scanner(System.in);
        System.out.println("Enter the side of the square: ");
        int sq=inObj.nextInt();
        System.out.println("Enter the radius of the circle: ");
        double rad=inObj.nextDouble();
        System.out.println("Enter the length and breadth of rectangle: ");
        int len=inObj.nextInt();
        int bre=inObj.nextInt();
        System.out.println("Enter the sides of the triangle: ");
        double a=inObj.nextDouble();
        double b=inObj.nextDouble();
        double c=inObj.nextDouble();
        System.out.println("Area of the square is "+myArea.area(sq));
        System.out.println("Area of the circle is "+myArea.area(rad));
        System.out.println("Area of the rectangle is "+myArea.area(len,bre));
        System.out.println("Area of the triangle is "+myArea.area(a,b,c));
    }
}
```

#### Sort from command line

```java
import java.util.Arrays;
class AlphaSort
{
    public static void main(String args[])
{
        Arrays.sort(args);
        System.out.println("Sorted List: ");
        for(String st:args)
    {
            System.out.println(st);
        }
    }
}
```

#### Matching rectangle

```java
import java.util.Scanner;
class Rectangle
{
    double width, length, area;
    String color;
    void setWidth(double width){
        this.width=width;
    }
    void setLength(double length)
{
        this.length=length;
    }
    void setColor(String color)
{
        this.color=color;
    }
    void findArea()
{
        this.area=this.width*this.length;
    }
    double getArea()
{
        return this.area;
    }
    String getColor()
{
        return this.color;
    }
}
class Rect
{
    public static void main(String args[])
{
        Rectangle rect1=new Rectangle();
        Rectangle rect2=new Rectangle();
        Scanner inObj=new Scanner(System.in);
        System.out.println("Enter the width, length and color of rectangle 1: ");
        rect1.setWidth(inObj.nextDouble());
        rect1.setLength(inObj.nextDouble());
        rect1.setColor(inObj.nextLine());
        rect1.findArea();
        System.out.println("Enter the width, length and color of rectangle 2: ");
        rect2.setWidth(inObj.nextDouble());
        rect2.setLength(inObj.nextDouble());
        rect2.setColor(inObj.nextLine());
        rect2.findArea();
        if(rect1.getArea()==rect2.getArea() && rect1.getColor().equals(rect2.getColor()))
        System.out.println("Matching Rectangles");
        else
        System.out.println("Non-matching rectangles");
    }
}
```

#### Office database using inheritance

```java
import java.util.Scanner;
class Employee
{
    String emp_code, emp_name, address, ph_no;
    double da=10, hra=20, bp=0;
    double salFind(){
        return bp+bp*da/100+bp*hra/100;
    }
    void emPrint()
{
        System.out.println();
        System.out.println("Employee name: "+emp_name);
        System.out.println("Employee code: "+emp_code);
        System.out.println("Address: "+address);
        System.out.println("Phone number: "+ph_no);
        System.out.println("Basic Pay: $"+bp);
        System.out.println("DA: $"+(bp*da/100));
        System.out.println("HRA: $"+(bp*hra/100));
        System.out.println("Salary: $"+salFind());
    }
}
class Manager extends Employee
{
    Manager(String emp_code, String emp_name, String address, String ph_no)
{
        this.emp_code=emp_code;
        this.emp_name=emp_name;
        this.address=address;
        this.ph_no=ph_no;
        this.bp=5000;
    }
}
class Typist extends Employee
{
    Typist(String emp_code, String emp_name, String address, String ph_no)
{
        this.emp_code=emp_code;
        this.emp_name=emp_name;
        this.address=address;
        this.ph_no=ph_no;
        this.bp=3000;
    }
}
class Officer extends Employee
{
    Officer(String emp_code, String emp_name, String address, String ph_no)
{
        this.emp_code=emp_code;
        this.emp_name=emp_name;
        this.address=address;
        this.ph_no=ph_no;
        this.bp=4000;
    }
}
class EmpDet
{
    public static void main(String args[])
{
        String emp_code, emp_name, address, ph_no;
        Scanner inObj=new Scanner(System.in);
        System.out.println("Office Management");
        System.out.println("Manager[1]\tTypist[2]\tOfficer[3]: ");int choice=inObj.nextInt();
        inObj.nextLine();
        System.out.println("Enter the Name: ");
        emp_name=inObj.nextLine();
        System.out.println("Enter the Code: ");
        emp_code=inObj.nextLine();
        System.out.println("Enter the Address: ");
        address=inObj.nextLine();
        System.out.println("Enter the Phone Number: ");
        ph_no=inObj.nextLine();
        switch(choice)
    {
            case 1:
        {
                Manager myMan=new Manager(emp_code, emp_name, address, ph_no);
                myMan.emPrint();
            } break;
            case 2:
        {
                Typist myTyp=new Typist(emp_code, emp_name, address, ph_no);
                myTyp.emPrint();
            } break;
            case 3:
        {
                Officer myOff=new Officer(emp_code, emp_name, address, ph_no);
                myOff.emPrint();
            } break;
            default:System.out.println("Invalid Choice");
        }
    }
}
```

#### Drug info - abstract class

```java
import java.util.Scanner;
abstract class Drug
{
    String name, purpose;
    int dos;
    Drug(String name,String purpose, int dos)
{
        this.name=name;
        this.purpose=purpose;
        this.dos=dos;
    }
    void getName()
{
        System.out.println("Name: "+name);
    }
    void getPurpose()
{
        System.out.println("Purpose: "+purpose);
    }
    void getDos()
{
        System.out.println("No of Times/Day: "+dos);}
    abstract void getDrugInfo();
}
class Aspirin extends Drug
{
    void setDos()
{
        this.dos=2;
    }
    public Aspirin(String name, String purpose, int dos)
{
        super(name, purpose, dos);
    }
    void getDrugInfo()
{
        getName();
        getPurpose();
        getDos();
    }
}
class Ibuprofen extends Drug
{
    void setDos()
{
        this.dos=3;
    }
    public Ibuprofen(String name, String purpose, int dos)
{
        super(name, purpose, dos);
    }
    void getDrugInfo()
{
        getName();
        getPurpose();
        getDos();
    }
}
class DrugDet
{
    public static void main(String args[])
{
        Scanner inObj=new Scanner(System.in);
        System.out.println("Enter the choice: [(1) Aspirin/(2) Ibuprofen]");
        int choice=inObj.nextInt();
        if(choice==1)
    {
            Aspirin myAspirin=new Aspirin("Aspirin", "Pain relief", 0);
            myAspirin.setDos();
            myAspirin.getDrugInfo();
        }
        else if(choice==2)
    {
            Ibuprofen myIbuprofen=new Ibuprofen("Ibuprofen", "Pain and Inflammation relief", 0);
            myIbuprofen.setDos();
            myIbuprofen.getDrugInfo();
        }
        elseSystem.out.println("Invalid Choice");
    }
}
```

#### Interface Playing

```java
interface Playing
{
    abstract void play(); //Public by default
}
class Child implements Playing
{
    @Override //Explicit overriding essential
    public void play()
{
        System.out.println("The child is playing with toys");
    }
}
class Musician implements Playing
{
    @Override
    public void play()
{
        System.out.println("The Musician is playing Instruments");
    }
}
class Actor implements Playing
{
    @Override
    public void play()
{
        System.out.println("The Actor is playing a role in film");
    }
}
class PlayDet
{
    public static void main(String args[])
{
        Child myChild = new Child();
        Musician myMusician = new Musician();
        Actor myActor = new Actor();
        myChild.play();
        myMusician.play();
        myActor.play();
    }
}
```

#### Package Shape

```java
//File 1
import Shape.Figure;
class ShapeCal
{
    public static void main(String args[])
{
        Figure myFig = new Figure();double cubeSide = 3.0;
        double cubeVolume = myFig.volume(cubeSide);
        System.out.println("Volume of the cube: " + cubeVolume);
        double cylinderRadius = 3.0;
        double cylinderHeight = 5.0;
        double cylinderVolume = myFig.volume(cylinderRadius, cylinderHeight);
        System.out.println("Volume of the cylinder: " + cylinderVolume);
        double boxLength = 4.0;
        double boxWidth = 3.0;
        double boxHeight = 5.0;
        double boxVolume = myFig.volume(boxLength, boxWidth, boxHeight);
        System.out.println("Volume of the rectangular box: " + boxVolume);
    }
}
//File 2
package Shape;
public class Figure
{
    public double volume(double side)
{
        return side * side * side;
    }
    public double volume(double radius, double height)
{
        return 3.14* radius * radius * height;
    }
    public double volume(double length, double width, double height)
{
        return length * width * height;
    }
}
```

#### Package Math

```java
//File 1
import math.Calculator;
class Calc
{
    public static void main(String args[])
{
        Calculator myCalc = new Calculator();
        double addResult = myCalc.add(10, 5);
        System.out.println("Addition: 10 + 5 = " + addResult);
        double subtractResult = myCalc.subtract(10, 5);
        System.out.println("Subtraction: 10 - 5 = " + subtractResult);
        double multiplyResult = myCalc.multiply(10, 5);
        System.out.println("Multiplication: 10 * 5 = " + multiplyResult);
        double divideResult = myCalc.divide(10, 5);
        System.out.println("Division: 10 / 5 = " + divideResult);
    }
}
//File 2
package math;
public class Calculator
{public double add(double a, double b)
{
        return a + b;
    }
    public double subtract(double a, double b)
{
        return a - b;
    }
    public double multiply(double a, double b)
{
        return a * b;
    }
    public double divide(double a, double b)
{
        return a / b;
    }
}
```

#### Handle Exception

```java
class AriException
{
    public static void main(String args[])
{
        int numerator = 10;
        int denominator = 0;
        try
    {
            int result = numerator/denominator;
            System.out.println("Result: " + result);
        }
        catch (ArithmeticException e)
    {
            System.out.println("Error: Division by zero is not allowed.");
        }
    }
}
```

#### Custom Exception

```java
class MyCustomException extends Exception
{
    public MyCustomException(String message)
{
        super(message);
    }
}
class CustException
{
    public static void main(String args[])
{
        try
    {
            validateAge(15);
        }
        catch (MyCustomException e)
    {
            System.out.println("Caught exception: "+e.getMessage());
        }}
    public static void validateAge(int age) throws MyCustomException
{
        if (age<18)
    {
            throw new MyCustomException("Age must be 18 or older.");
        }
        else
    {
            System.out.println("Age is valid.");
        }
    }
}
```

#### Threading

```java
class OddPrinter extends Thread
{
    public void run()
{
        for(int i=1;i<=10;i+=2)
    {
            System.out.println("Odd: "+i);
        }
    }
}
class EvenPrinter extends Thread
{
    public void run()
{
        for(int i=2;i<=10;i+=2)
    {
            System.out.println("Even: "+i);
        }
    }
}
class OddEvenThreads
{
    public static void main(String args[])
{
        OddPrinter myOdd=new OddPrinter();
        EvenPrinter myEven=new EvenPrinter();
        myOdd.start();
        myEven.start();
    }
}
```
