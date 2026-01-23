# Experiment 1:
## TITLE: 1a) Display the primitive datatypes
## SOURCE CODE:

```

class datatypes{
static byte b;
static short s;
static int i;
static double d;
static float f;
static char c;
static boolean bool;
public static void main(String args[]){
System.out.println("default primitive datatypes:");
System.out.println("byte:"+b);
System.out.println("short:"+s);
System.out.println("int:"+i);
System.out.println("double:"+d);
System.out.println("float:"+f);
System.out.println("char:"+c);
System.out.println("boolean:"+bool);
}
}

```
## OUTPUT:

<img width="1920" height="1080" alt="Exp1a" src="https://github.com/user-attachments/assets/504e44d4-1f52-4254-8663-4c18e4878d1f" />


## TITLE: 1b.) Display the quadratic equation.
## SOURCE CODE:

```

import java.util.Scanner;
public class task2{
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
double a,b,c;
System.out.println("Enter a,b,c values:");
a = sc.nextDouble();
b = sc.nextDouble();
c = sc.nextDouble();
double D = b*b - 4*a*c;
if (D > 0){
double x1 = (-b + Math.sqrt(D)) / (2*a);
double x2 = (-b - Math.sqrt(D)) / (2*a);
System.out.println("Roots are Real and Distinct");
System.out.println("x1 = " + x1 + ",x2= " + x2);
}else if (D == 0) {
double x =-b / (2*a);
System.out.println("Roots are Real and Equal");
System.out.println("x = "+ x);
} else {
double real = -b / (2*a);
double img = Math.sqrt(-D) / (2*a);
System.out.println("Roots are complex");
System.out.println("x1 = " +real + " + i" + img);
System.out.println("x2 = " +real + " + i" + img);
}
sc.close();
}
}

```

## OUTPUT:

<img width="1920" height="1080" alt="Exp1b" src="https://github.com/user-attachments/assets/ca6813ce-3f21-4f13-86c4-b43bdc817b99" />
