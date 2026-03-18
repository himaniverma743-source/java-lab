[Prgram-1 wap for arthmatic logic](#assi-1)

[Prgram-2 wap for Hello World](#assi-2)

[Program-3 wap for the addition of two distances where each distance is given in meter, cm](#assi-3)

[program-4 wap for the addition of two times where each time is given in hours, minutes](#assi-4)

[program-5 wap for the addition of two times where each time is given in hours, minutes and seconds](#assi-5)

[program-6 wap for the addition of two distance where each distance is given in meter, centi-meter and millimeter](#assi-6)

[program-7 wap using object and classes to do the reverse of 1d array](#assi-7)

[program-8 wap for transpose of matrix 3*3](#assi-8)

[program-9 wap for sum of matrix](#assi-9)

[program-10 wap for multiply of matrix](#assi-10)

[program-11 wap for sum of rows of matrix](#assi-11)

[program-12 wap for sum of columns of matrix](#assi-12)

[program-13 wap for sum of diagonals of matrix](#assi-13)

[program-14 wap for factorial of numbers](#assi-14)

[program-15 wap for fabannoic series](#assi-15)

[program-16 wap for palendrome numbers](#assi-16)

[program-17 wap for armstrong numbers](#assi-17)

[program-18 wap for
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

<img width="579" height="169" alt="Screenshot 2026-03-18 184535" src="https://github.com/user-attachments/assets/03d4c7e1-ed6e-4c9f-9423-6b569d493039" />

```
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


