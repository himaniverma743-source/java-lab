[Prgram-1 wap for arthmatic logic](#assi-1)

[Prgram-2 wap for Hello World](#assi-2)

[Program-3 wap for the addition of two distances where each distance is given in meter, cm](#assi-3)

[program-4 wap for the addition of two times where each time is given in hours, minutes](#assi-4)

[program-5 wap for the addition of two times where each time is given in hours, minutes and seconds](#assi-5)

[program-6 wap for the addition of two distance where each distance is given in meter, centi-meter and millimeter](#assi-6)

[Program-7 WAP using objects and classes to do reverse of 1-D Array](#assi-7)

[Program-8 Write a class for implementation operation of matrix(3X3): 1.Transpose, 2.Sum,3.Multiply, 4.Sum of Rows,
5.Sum of Column, 6.Sum of diagonal](#assi-8)

[Program-9 Collect the code of C language for any 5 operation convert the logic to java in object orented fashion](#assi-9)

[Program-10 Demonstrate all 3 types of inheritance 1. Single, 2, Multilevel 3. Hierarchial](#assi-10)

[Program-11 Write a program using three classes to print 1-100 ,1-100,1-100 with and without thread and analyse the output and repeat the same program using runnable interface](#assi-11)

[Program=12  Using the concept of multithreading the output of all three threads must be synchronised (use join method](#assi-12)

[Program-13 Addition of 2 numbers using swing](#assi-13)

[Program-14  Make a registration form with 10 elements and send the data into database (use jdbc connectivity](#assi-14)

[Program-15  Make one calculator in swing](#assi-15)

[Program-16  Matrix Addition using swing class](#assi-16)

[Program-17 Create one jframe apply 10 buttons on that after clicking on each button a new
structure is created.(Circle, oval rectangle, etc ....](#assi-17)

[Program-18  Just using mouse Event create a frame like paint brush with selection of colour and width](#assi-18)

[Program-19 Create a package of any 5 classes of your choice and import it](#assi-19)

[Program-20 Create one package and sub package  import and test it](#assi-20)

[Program-21   Create one small array of size 5 apply array out of bounds exception using try catch give a proper message in catch and demonstrate the exception exactly in the same fashion demonstrate arithmetic exception](#assi-21)

[Program-22 To test the range of age of one student.write a program using user defined exception](#assi-22)

[Program-23  File Handling Programs](#assi-23)

[Program-24   Inheritance Programs, using interface and abstract classes](#assi-24)


## assi-1
```

public class Cla{
static int add(int a, int b){
return a+b;
}
static int sub(int a, int b){
return a-b;
}
static int mul(int a, int b){
return a*b;
}
static int div(int a,int b){
return a/b;
}
public static void main(String[]args){
int n1=Integer.parseInt(args[0]);
int n2=Integer.parseInt(args[1]); 
System.out.println(add(n1,n2));  
System.out.println(sub(n1,n2));
System.out.println(mul(n1,n2)); 
System.out.println(div(n1,n2));             
}
}
```

<img width="349" height="73" alt="image" src="https://github.com/user-attachments/assets/dc45e89b-53e3-40ce-b14c-91e5bd25b2b7" />

## assi-2

```
public class Add{
public static void main(String[]args)
{
System.out.println("Hi");
}
}
```

<img width="349" height="73" alt="image" src="https://github.com/user-attachments/assets/dd84586d-f80d-49c9-a114-d68bb2b52fe4" />

## assi-3

```
import java.util.Scanner;

public class DistanceAddition {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int m1, cm1, m2, cm2;
        int meter, cm;

        System.out.println("Enter first distance (meter and centimeter): ");
        m1 = sc.nextInt();
        cm1 = sc.nextInt();

        System.out.println("Enter second distance (meter and centimeter): ");
        m2 = sc.nextInt();
        cm2 = sc.nextInt();

        meter = m1 + m2;
        cm = cm1 + cm2;

        if (cm >= 100) {
            meter = meter + (cm / 100);
            cm = cm % 100;
        }

        System.out.println("Sum of distances = " + meter + " meter " + cm + " centimeter");
    }
}

```
<img width="579" height="169" alt="Screenshot 2026-03-18 184535" src="https://github.com/user-attachments/assets/0203355f-fdfa-4baa-b4f0-35f9680fcf04" />

##assi-4

```

import java.util.Scanner;

class Time {
    int hours, minutes;

    void addTime(int h1, int m1, int h2, int m2) {
        hours = h1 + h2;
        minutes = m1 + m2;

        if (minutes >= 60) {
            hours = hours + minutes / 60;
            minutes = minutes % 60;
        }
    }

    void display() {
        System.out.println("Total Time = " + hours + " hours " + minutes + " minutes");
    }

    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        int h1, m1, h2, m2;

        System.out.print("Enter first time (hours minutes): ");
        h1 = sc.nextInt();
        m1 = sc.nextInt();

        System.out.print("Enter second time (hours minutes): ");
        h2 = sc.nextInt();
        m2 = sc.nextInt();

        Time t = new Time();   // object creation
        t.addTime(h1, m1, h2, m2);
        t.display();
    }
}

```
<img width="523" height="97" alt="Screenshot 2026-03-18 184224" src="https://github.com/user-attachments/assets/c82c8e25-3793-46d5-94ba-e67a56e2ce5d" />

##assi-5

```
import java.util.Scanner;

class Time {
    int hours, minutes, seconds;

    void addTime(int h1, int m1, int s1, int h2, int m2, int s2) {
        hours = h1 + h2;
        minutes = m1 + m2;
        seconds = s1 + s2;

        if (seconds >= 60) {
            minutes = minutes + seconds / 60;
            seconds = seconds % 60;
        }

        if (minutes >= 60) {
            hours = hours + minutes / 60;
            minutes = minutes % 60;
        }
    }

    void display() {
        System.out.println("Total Time = " + hours + " hours " + minutes + " minutes " + seconds + " seconds");
    }

    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        int h1, m1, s1, h2, m2, s2;

        System.out.print("Enter first time (hours minutes seconds): ");
        h1 = sc.nextInt();
        m1 = sc.nextInt();
        s1 = sc.nextInt();

        System.out.print("Enter second time (hours minutes seconds): ");
        h2 = sc.nextInt();
        m2 = sc.nextInt();
        s2 = sc.nextInt();

        Time t = new Time();   // object creation
        t.addTime(h1, m1, s1, h2, m2, s2);
        t.display();
    }
}

```
<img width="652" height="95" alt="Screenshot 2026-03-18 185225" src="https://github.com/user-attachments/assets/71080d14-92f1-4c66-a730-79a4acb6d4a8" />

##assi-6

```
import java.util.Scanner;

class Distance {
    int meter, centimeter, millimeter;

    void addDistance(int m1, int c1, int mm1, int m2, int c2, int mm2) {
        meter = m1 + m2;
        centimeter = c1 + c2;
        millimeter = mm1 + mm2;

        if (millimeter >= 10) {
            centimeter = centimeter + millimeter / 10;
            millimeter = millimeter % 10;
        }

        if (centimeter >= 100) {
            meter = meter + centimeter / 100;
            centimeter = centimeter % 100;
        }
    }

    void display() {
        System.out.println("Total Distance = " + meter + " meter " + centimeter + " centimeter " + millimeter + " millimeter");
    }

    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        int m1, c1, mm1, m2, c2, mm2;

        System.out.print("Enter first distance (meter centimeter millimeter): ");
        m1 = sc.nextInt();
        c1 = sc.nextInt();
        mm1 = sc.nextInt();

        System.out.print("Enter second distance (meter centimeter millimeter): ");
        m2 = sc.nextInt();
        c2 = sc.nextInt();
        mm2 = sc.nextInt();

        Distance d = new Distance();   // object creation
        d.addDistance(m1, c1, mm1, m2, c2, mm2);
        d.display();
    }
}

```
<img width="778" height="98" alt="Screenshot 2026-03-18 185524" src="https://github.com/user-attachments/assets/6fdc1515-1c6d-4f30-923e-d556b09e45c3" />

##assi-7

```

// Main class
public class MainClass {
    public static void main(String[] args) {

        ArrayOperations obj = new ArrayOperations();

        System.out.println("Original Array:");
        obj.displayArray();

        obj.reverseArray();

        System.out.println("Reversed Array:");
        obj.displayArray();
    }
}

// Class containing all functions
class ArrayOperations {

    int[] arr = {10, 20, 30, 40, 50};  // predefined array

    // Method to reverse array
    void reverseArray() {
        int start = 0, end = arr.length - 1;

        while (start < end) {
            int temp = arr[start];
            arr[start] = arr[end];
            arr[end] = temp;

            start++;
            end--;
        }
    }

    // Method to display array
    void displayArray() {
        for(int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }
}

```

<img width="208" height="127" alt="Screenshot 2026-03-20 194325" src="https://github.com/user-attachments/assets/7b3b744b-c282-4d09-bcc4-9e520c873e88" />

##assi-8

```
public class MatrixOperations {

    int[][] A = {
        {1,2,3},
        {4,5,6},
        {7,8,9}
    };

    int[][] B = {
        {9,8,7},
        {6,5,4},
        {3,2,1}
    };

    void display(int[][] M){
        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                System.out.print(M[i][j]+" ");
            }
            System.out.println();
        }
    }

    void transpose(){
        int[][] T = new int[3][3];

        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                T[j][i] = A[i][j];
            }
        }

        System.out.println("Transpose of Matrix A:");
        display(T);
    }

    void sum(){
        int[][] S = new int[3][3];

        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                S[i][j] = A[i][j] + B[i][j];
            }
        }

        System.out.println("Sum of A and B:");
        display(S);
    }

    void multiply(){
        int[][] M = new int[3][3];

        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                for(int k=0;k<3;k++){
                    M[i][j] += A[i][k]*B[k][j];
                }
            }
        }

        System.out.println("Multiplication of A and B:");
        display(M);
    }

    void rowSum(){
        for(int i=0;i<3;i++){
            int sum=0;
            for(int j=0;j<3;j++){
                sum += A[i][j];
            }
            System.out.println("Row "+(i+1)+" Sum = "+sum);
        }
    }

    void columnSum(){
        for(int j=0;j<3;j++){
            int sum=0;
            for(int i=0;i<3;i++){
                sum += A[i][j];
            }
            System.out.println("Column "+(j+1)+" Sum = "+sum);
        }
    }

    void diagonalSum(){
        int p=0,s=0;

        for(int i=0;i<3;i++){
            p += A[i][i];
            s += A[i][2-i];
        }

        System.out.println("Primary Diagonal Sum = "+p);
        System.out.println("Secondary Diagonal Sum = "+s);
    }

    public static void main(String[] args){

        MatrixOperations obj = new MatrixOperations();

        System.out.println("Matrix A:");
        obj.display(obj.A);

        System.out.println("Matrix B:");
        obj.display(obj.B);

        obj.transpose();
        obj.sum();
        obj.multiply();
        obj.rowSum();
        obj.columnSum();
        obj.diagonalSum();
    }
}

```

<img width="302" height="742" alt="Screenshot 2026-03-20 195216" src="https://github.com/user-attachments/assets/5317538a-3903-48f8-a7a0-d75f3dbcc836" />

##assi-9

```

public class NumberOperations {

    int num = 5;     // for factorial & fibonacci
    int pal = 121;   // for palindrome
    int arm = 153;   // for armstrong

    // 1. Factorial
    void factorial() {
        int fact = 1;

        for (int i = 1; i <= num; i++) {
            fact *= i;
        }

        System.out.println("Factorial of " + num + " = " + fact);
    }

    // 2. Fibonacci Series
    void fibonacci() {
        int a = 0, b = 1;

        System.out.println("Fibonacci series:");

        for (int i = 1; i <= num; i++) {
            System.out.print(a + " ");
            int c = a + b;
            a = b;
            b = c;
        }

        System.out.println();
    }

    // 3. Palindrome Number
    void palindrome() {
        int temp = pal;
        int rev = 0;

        while (temp > 0) {
            int digit = temp % 10;
            rev = rev * 10 + digit;
            temp /= 10;
        }

        if (pal == rev)
            System.out.println(pal + " is Palindrome");
        else
            System.out.println(pal + " is Not Palindrome");
    }

    // 4. Armstrong Number
    void armstrong() {
        int temp = arm;
        int sum = 0;

        while (temp > 0) {
            int digit = temp % 10;
            sum += digit * digit * digit;
            temp /= 10;
        }

        if (sum == arm)
            System.out.println(arm + " is Armstrong");
        else
            System.out.println(arm + " is Not Armstrong");
    }

    // 5. Pattern
    void pattern() {
        System.out.println("Pattern:");

        for (int i = 1; i <= 5; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }

    // Main method
    public static void main(String[] args) {

        NumberOperations obj = new NumberOperations();

        obj.factorial();
        obj.fibonacci();
        obj.palindrome();
        obj.armstrong();
        obj.pattern();
    }
}

```

<img width="214" height="281" alt="Screenshot 2026-03-20 195911" src="https://github.com/user-attachments/assets/e6a5c3e9-bf2a-4475-9b37-ce540eaf47a2" />

##assi-10

```

// Base class
public class A {

    void showA() {
        System.out.println("Class A (Parent)");
    }

    public static void main(String[] args) {

        // Single Inheritance
        System.out.println("Single Inheritance:");
        B obj1 = new B();
        obj1.showA();
        obj1.showB();

        // Multilevel Inheritance
        System.out.println("\nMultilevel Inheritance:");
        C obj2 = new C();
        obj2.showA();
        obj2.showB();
        obj2.showC();

        // Hierarchical Inheritance
        System.out.println("\nHierarchical Inheritance:");
        D obj3 = new D();
        E obj4 = new E();

        obj3.showA();
        obj3.showD();

        obj4.showA();
        obj4.showE();
    }
}

// Single Inheritance
class B extends A {
    void showB() {
        System.out.println("Class B (Child of A)");
    }
}

// Multilevel Inheritance
class C extends B {
    void showC() {
        System.out.println("Class C (Child of B)");
    }
}

// Hierarchical Inheritance
class D extends A {
    void showD() {
        System.out.println("Class D (Another Child of A)");
    }
}

class E extends A {
    void showE() {
        System.out.println("Class E (Another Child of A)");
    }
}

```

<img width="297" height="373" alt="Screenshot 2026-03-20 200413" src="https://github.com/user-attachments/assets/22ca8314-1232-4743-a0af-3fce7bed8bb4" /> 

##assi-11

```

class A extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("A (Thread): " + i);
        }
    }

    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("A (Normal): " + i);
        }
    }
}

class B extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("B (Thread): " + i);
        }
    }

    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("B (Normal): " + i);
        }
    }
}

class C extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("C (Thread): " + i);
        }
    }

    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("C (Normal): " + i);
        }
    }
}

public class Main {
    public static void main(String[] args) {

        A a = new A();
        B b = new B();
        C c = new C();

        // 🔹 Without Thread (Sequential)
        System.out.println("----- WITHOUT THREAD -----");
        a.print();
        b.print();
        c.print();

        // 🔹 With Thread (Concurrent)
        System.out.println("----- WITH THREAD -----");
        a.start();
        b.start();
        c.start();
    }
}

```

<img width="190" height="879" alt="image" src="https://github.com/user-attachments/assets/b1c26b8a-0f15-4df4-9037-1ae81ee8f02e" />
<img width="119" height="811" alt="image" src="https://github.com/user-attachments/assets/639baa6a-965a-44de-b941-1e052d0ecc83" />
<img width="142" height="834" alt="image" src="https://github.com/user-attachments/assets/48aed606-7cd7-4024-8afa-26c331f58ee5" />
<img width="121" height="850" alt="image" src="https://github.com/user-attachments/assets/e71cf2df-2dce-4c2b-814f-cf5a1fcc2c35" />

#assi-12

```

class A extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("A: " + i);
        }
    }
}

class B extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("B: " + i);
        }
    }
}

class C extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("C: " + i);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        A a = new A();
        B b = new B();
        C c = new C();

        try {
            a.start();
            a.join();   // wait until A finishes

            b.start();
            b.join();   // wait until B finishes

            c.start();
            c.join();   // wait until C finishes

        } catch (InterruptedException e) {
            System.out.println(e);
        }
    }
}

```

<img width="79" height="881" alt="image" src="https://github.com/user-attachments/assets/4f3c0465-28b4-4580-a6f6-bf527b01cdbf" />
<img width="100" height="880" alt="image" src="https://github.com/user-attachments/assets/70ad4364-d6a3-4302-b2ba-1799401a5681" />
<img width="71" height="895" alt="image" src="https://github.com/user-attachments/assets/fcf608f0-f418-4b2f-9ea1-932aa576c3a1" />
<img width="47" height="886" alt="image" src="https://github.com/user-attachments/assets/93aecbe0-8e05-4290-9f1b-8b1c1803e9e1" />
<img width="49" height="881" alt="image" src="https://github.com/user-attachments/assets/53afca08-a9df-474b-b6c5-7a8d27aa5235" />
<img width="64" height="557" alt="image" src="https://github.com/user-attachments/assets/79e0774c-4ec6-48f2-9694-37abef39e217" />

#assi-13

```

import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int a = sc.nextInt();

        System.out.print("Enter second number: ");
        int b = sc.nextInt();

        int sum = a + b;

        System.out.println("Result: " + sum);
    }
}

```

<img width="239" height="83" alt="image" src="https://github.com/user-attachments/assets/5228854d-4cb0-4643-9a2c-f0c182fd6c4f" />

##assi-14

```

import java.util.*;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // 🔹 Taking 10 inputs (Registration Form)
        System.out.print("Enter Name: ");
        String name = sc.nextLine();

        System.out.print("Enter Email: ");
        String email = sc.nextLine();

        System.out.print("Enter Password: ");
        String password = sc.nextLine();

        System.out.print("Enter Gender: ");
        String gender = sc.nextLine();

        System.out.print("Enter Course: ");
        String course = sc.nextLine();

        System.out.print("Enter Address: ");
        String address = sc.nextLine();

        System.out.print("Enter Phone: ");
        String phone = sc.nextLine();

        System.out.print("Enter Age: ");
        String age = sc.nextLine();

        System.out.print("Enter City: ");
        String city = sc.nextLine();

        System.out.print("Enter State: ");
        String state = sc.nextLine();

        // 🔹 Display Data (Simulating Database Storage)
        System.out.println("\n--- Registration Data ---");
        System.out.println("Name: " + name);
        System.out.println("Email: " + email);
        System.out.println("Password: " + password);
        System.out.println("Gender: " + gender);
        System.out.println("Course: " + course);
        System.out.println("Address: " + address);
        System.out.println("Phone: " + phone);
        System.out.println("Age: " + age);
        System.out.println("City: " + city);
        System.out.println("State: " + state);

        System.out.println("\nData Stored Successfully (Simulated)");
    }
}

```

<img width="377" height="696" alt="image" src="https://github.com/user-attachments/assets/356e7b9d-cec1-43c9-b781-44e2a13a0352" />

##assi-15

```

import javax.swing.*;
import java.awt.event.*;

public class Main {
    public static void main(String[] args) {

        JFrame f = new JFrame("Calculator");

        // Text fields
        JTextField t1 = new JTextField();
        JTextField t2 = new JTextField();
        JTextField result = new JTextField();

        // Buttons
        JButton add = new JButton("+");
        JButton sub = new JButton("-");
        JButton mul = new JButton("*");
        JButton div = new JButton("/");

        // Set positions
        t1.setBounds(50, 50, 150, 30);
        t2.setBounds(50, 100, 150, 30);
        result.setBounds(50, 150, 150, 30);

        add.setBounds(220, 50, 50, 30);
        sub.setBounds(280, 50, 50, 30);
        mul.setBounds(220, 100, 50, 30);
        div.setBounds(280, 100, 50, 30);

        // Action logic
        ActionListener al = new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                try {
                    int a = Integer.parseInt(t1.getText());
                    int b = Integer.parseInt(t2.getText());
                    int res = 0;

                    if (e.getSource() == add) res = a + b;
                    if (e.getSource() == sub) res = a - b;
                    if (e.getSource() == mul) res = a * b;
                    if (e.getSource() == div) res = a / b;

                    result.setText(String.valueOf(res));

                } catch (Exception ex) {
                    JOptionPane.showMessageDialog(f, "Invalid Input");
                }
            }
        };

        // Add listeners
        add.addActionListener(al);
        sub.addActionListener(al);
        mul.addActionListener(al);
        div.addActionListener(al);

        // Add components
        f.add(t1); f.add(t2); f.add(result);
        f.add(add); f.add(sub); f.add(mul); f.add(div);

        // Frame settings
        f.setSize(400, 300);
        f.setLayout(null);
        f.setVisible(true);
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }
}

```

<img width="724" height="562" alt="image" src="https://github.com/user-attachments/assets/2ffa3921-7985-4af4-88d8-19933d3ce32a" />

##assi-16

```
import java.util.*;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int[][] A = new int[2][2];
        int[][] B = new int[2][2];
        int[][] C = new int[2][2];

        System.out.println("Enter Matrix A:");
        for(int i=0;i<2;i++){
            for(int j=0;j<2;j++){
                A[i][j] = sc.nextInt();
            }
        }

        System.out.println("Enter Matrix B:");
        for(int i=0;i<2;i++){
            for(int j=0;j<2;j++){
                B[i][j] = sc.nextInt();
            }
        }

        // Addition
        for(int i=0;i<2;i++){
            for(int j=0;j<2;j++){
                C[i][j] = A[i][j] + B[i][j];
            }
        }

        System.out.println("Result Matrix:");
        for(int i=0;i<2;i++){
            for(int j=0;j<2;j++){
                System.out.print(C[i][j] + " ");
            }
            System.out.println();
        }
    }
}

```

<img width="177" height="240" alt="image" src="https://github.com/user-attachments/assets/abe425cb-b1ac-4da6-a93f-26bff1bc3d35" />

##assi-17

```

import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

class DrawPanel extends JPanel {
    String shape = "";

    public void setShape(String s) {
        shape = s;
        repaint();
    }

    public void paintComponent(Graphics g) {
        super.paintComponent(g);

        if (shape.equals("Circle"))
            g.drawOval(150, 100, 100, 100);

        if (shape.equals("Oval"))
            g.drawOval(120, 100, 150, 80);

        if (shape.equals("Rectangle"))
            g.drawRect(120, 100, 150, 80);

        if (shape.equals("Square"))
            g.drawRect(150, 100, 100, 100);

        if (shape.equals("Line"))
            g.drawLine(100, 100, 250, 200);

        if (shape.equals("Triangle")) {
            int x[] = {150, 200, 250};
            int y[] = {200, 100, 200};
            g.drawPolygon(x, y, 3);
        }

        if (shape.equals("Arc"))
            g.drawArc(120, 100, 150, 100, 0, 180);

        if (shape.equals("RoundRect"))
            g.drawRoundRect(120, 100, 150, 80, 30, 30);

        if (shape.equals("Filled Circle"))
            g.fillOval(150, 100, 100, 100);

        if (shape.equals("Filled Rect"))
            g.fillRect(120, 100, 150, 80);
    }
}

public class Main {
    public static void main(String[] args) {

        JFrame f = new JFrame("Shapes using Buttons");
        f.setSize(500, 400);
        f.setLayout(null);

        DrawPanel panel = new DrawPanel();
        panel.setBounds(0, 100, 500, 300);

        String names[] = {
            "Circle", "Oval", "Rectangle", "Square", "Line",
            "Triangle", "Arc", "RoundRect", "Filled Circle", "Filled Rect"
        };

        int x = 10;

        for (int i = 0; i < 10; i++) {
            JButton btn = new JButton(names[i]);
            btn.setBounds(x, 10, 120, 30);
            x += 125;

            btn.addActionListener(new ActionListener() {
                public void actionPerformed(ActionEvent e) {
                    panel.setShape(((JButton)e.getSource()).getText());
                }
            });

            f.add(btn);
        }

        f.add(panel);

        f.setVisible(true);
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }
}

```

<img width="625" height="614" alt="image" src="https://github.com/user-attachments/assets/0ea85cb3-0514-463a-aa43-483120b9fa6d" />

##assi-18

```

import java.awt.*;
import java.awt.event.*;

public class PaintBrush extends Frame implements MouseListener, MouseMotionListener, ItemListener
{
    Choice colorChoice;
    Choice widthChoice;

    int x, y;
    Color currentColor = Color.BLACK;
    int brushSize = 5;

    public PaintBrush()
    {
        setTitle("Simple Paint Brush");
        setSize(600,500);
        setLayout(new FlowLayout());

        // Color Selection
        add(new Label("Select Color:"));
        colorChoice = new Choice();
        colorChoice.add("Black");
        colorChoice.add("Red");
        colorChoice.add("Blue");
        colorChoice.add("Green");
        add(colorChoice);

        // Width Selection
        add(new Label("Brush Width:"));
        widthChoice = new Choice();
        widthChoice.add("5");
        widthChoice.add("10");
        widthChoice.add("15");
        widthChoice.add("20");
        add(widthChoice);

        colorChoice.addItemListener(this);
        widthChoice.addItemListener(this);

        addMouseListener(this);
        addMouseMotionListener(this);

        // Closing Window
        addWindowListener(new WindowAdapter(){
            public void windowClosing(WindowEvent we){
                System.exit(0);
            }
        });

        setVisible(true);
    }

    public void itemStateChanged(ItemEvent e)
    {
        if(colorChoice.getSelectedItem().equals("Black"))
            currentColor = Color.BLACK;
        if(colorChoice.getSelectedItem().equals("Red"))
            currentColor = Color.RED;
        if(colorChoice.getSelectedItem().equals("Blue"))
            currentColor = Color.BLUE;
        if(colorChoice.getSelectedItem().equals("Green"))
            currentColor = Color.GREEN;

        brushSize = Integer.parseInt(widthChoice.getSelectedItem());
    }

    public void mousePressed(MouseEvent e)
    {
        x = e.getX();
        y = e.getY();
    }

    public void mouseDragged(MouseEvent e)
    {
        Graphics g = getGraphics();
        g.setColor(currentColor);
        g.fillOval(e.getX(), e.getY(), brushSize, brushSize);

        x = e.getX();
        y = e.getY();
    }

    // Required empty methods
    public void mouseClicked(MouseEvent e){}
    public void mouseReleased(MouseEvent e){}
    public void mouseEntered(MouseEvent e){}
    public void mouseExited(MouseEvent e){}
    public void mouseMoved(MouseEvent e){}

    public static void main(String args[])
    {
        new PaintBrush();
    }
}

```

<img width="685" height="366" alt="image" src="https://github.com/user-attachments/assets/7dc765eb-6539-4731-bd36-c67a898c7c1a" />

##assi-19

```

class Add {
    void sum(int a, int b) {
        System.out.println("Sum = " + (a+b));
    }
}

class Subtract {
    void sub(int a, int b) {
        System.out.println("Difference = " + (a-b));
    }
}

class Multiply {
    void mul(int a, int b) {
        System.out.println("Product = " + (a*b));
    }
}

class Divide {
    void div(int a, int b) {
        System.out.println("Quotient = " + (a/b));
    }
}

class Modulus {
    void mod(int a, int b) {
        System.out.println("Remainder = " + (a%b));
    }
}

public class Main {
    public static void main(String args[]) {

        Add a = new Add();
        Subtract s = new Subtract();
        Multiply m = new Multiply();
        Divide d = new Divide();
        Modulus mo = new Modulus();

        a.sum(20,10);
        s.sub(20,10);
        m.mul(20,10);
        d.div(20,10);
        mo.mod(20,10);
    }
}

```

<img width="168" height="142" alt="image" src="https://github.com/user-attachments/assets/d88561b3-d8bf-46b0-8220-f0a2c950a4bf" />

##assi-20

```

public class PackageDemo
{
    // Simulating package mypack
    static class Addition
    {
        void add(int a, int b)
        {
            System.out.println("Sum = " + (a+b));
        }
    }

    // Simulating subpackage mypack.subpack
    static class Multiply
    {
        void mul(int a, int b)
        {
            System.out.println("Product = " + (a*b));
        }
    }

    public static void main(String args[])
    {
        Addition obj1 = new Addition();
        Multiply obj2 = new Multiply();

        obj1.add(10,5);
        obj2.mul(10,5);
    }
}

```

<img width="144" height="61" alt="image" src="https://github.com/user-attachments/assets/a3ca9cef-aa3c-4ff5-a52b-f0b03802563d" />

##assi-21

```

public class ExceptionDemo
{
    public static void main(String args[])
    {
        // Array Out of Bounds Exception
        try
        {
            int arr[] = {10,20,30,40,50};

            System.out.println("Array Elements:");
            for(int i=0;i<=5;i++) // causes exception
            {
                System.out.println(arr[i]);
            }
        }

        catch(ArrayIndexOutOfBoundsException e)
        {
            System.out.println("Error: Array index is out of bounds!");
        }


        // Arithmetic Exception
        try
        {
            int a=10, b=0;
            int c=a/b; // causes exception

            System.out.println("Result = " + c);
        }

        catch(ArithmeticException e)
        {
            System.out.println("Error: Division by zero is not allowed!");
        }
    }
}

```

<img width="402" height="240" alt="image" src="https://github.com/user-attachments/assets/5f46278c-be3d-4f41-b0a4-47bcd271e5c4" />

 ##assi-22

 ```

import java.util.Scanner;

class InvalidAgeException extends Exception
{
    InvalidAgeException(String msg)
    {
        super(msg);
    }
}

public class StudentAgeTest
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);

        try
        {
            System.out.print("Enter student age: ");
            int age = sc.nextInt();

            if(age < 18 || age > 25)
            {
                throw new InvalidAgeException("Age must be between 18 and 25");
            }

            System.out.println("Valid Student Age");
        }

        catch(InvalidAgeException e)
        {
            System.out.println("Exception: " + e.getMessage());
        }
    }
}

```

<img width="491" height="66" alt="image" src="https://github.com/user-attachments/assets/4810f4c0-9c17-4924-9af7-04b0ae7ffbd2" />

##assi-23

```

import java.io.*;

public class FileHandlingDemo
{
    public static void main(String args[]) throws Exception
    {
        // Writing into file
        FileWriter fw = new FileWriter("data.txt");
        fw.write("Hello Java");
        fw.close();

        // Character by Character Reading
        System.out.println("Character by Character:");
        FileReader fr = new FileReader("data.txt");

        int ch;
        while((ch = fr.read()) != -1)
        {
            System.out.print((char)ch);
        }
        fr.close();

        System.out.println();

        // Byte by Byte Reading
        System.out.println("Byte by Byte:");
        FileInputStream fin = new FileInputStream("data.txt");

        int b;
        while((b = fin.read()) != -1)
        {
            System.out.print((char)b);
        }
        fin.close();
    }
}

```

<img width="275" height="162" alt="image" src="https://github.com/user-attachments/assets/5e6d109c-27c3-4e0e-b312-35fbaa81d65b" />

##assi-24

```

class Animal
{
    void sound()
    {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal
{
    void bark()
    {
        System.out.println("Dog barks");
    }
}

public class Main
{
    public static void main(String args[])
    {
        Dog d = new Dog();

        d.sound();
        d.bark();
    }
}

```

<img width="256" height="92" alt="image" src="https://github.com/user-attachments/assets/b9fb38e6-fbb9-45e2-8d7b-2473e8f89177" />


