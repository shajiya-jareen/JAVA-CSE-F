## Experiment-6
## TITLE : 6A)Write a JAVA program that describes exception handling mechanism.

## SOURCE CODE :

```

import java.util.Scanner;

public class Solution {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter size of array: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter " + n + " elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        System.out.print("Enter index to access: ");
        int index = sc.nextInt();

        try {
            System.out.println("Element at index " + index + " is: " + arr[index]);
        } 
        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Invalid index! Please enter index between 0 and " + (n - 1));
        }

        sc.close();
    }
}

```

## OUTPUT :

<img width="1920" height="1080" alt="Exp6a" src="https://github.com/user-attachments/assets/0c0d1093-5590-4118-b64a-871ccb56ba43" />


## TITLE : 6B) Write a JAVA program Illustrating Multiple Catch Clauses.

## SOURCE CODE :

```

import java.util.Scanner;
import java.util.InputMismatchException;

public class MultipleCatchExample {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int arr[] = {10, 20, 30, 40, 50};

        try {
            System.out.print("Enter first number: ");
            int a = sc.nextInt();

            System.out.print("Enter second number: ");
            int b = sc.nextInt();

            int result = a / b;
            System.out.println("Result of division: " + result);

            System.out.print("Enter index to access array element: ");
            int index = sc.nextInt();

            System.out.println("Element at index " + index + " = " + arr[index]);
        }

        catch (ArithmeticException e) {
            System.out.println("Error: Division by zero is not allowed.");
        }

        catch (InputMismatchException e) {
            System.out.println("Error: Please enter numeric values only.");
        }

        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Error: Invalid array index.");
        }

        catch (Exception e) {
            System.out.println("Some other error occurred.");
        }

        finally {
            System.out.println("Program continues...");
            sc.close();
        }
    }
}

```

## OUTPUT :


<img width="1920" height="1080" alt="Exp6b" src="https://github.com/user-attachments/assets/dbf3e01a-c93a-41ad-9f4e-0999ecf630f0" />



## TITLE : 6C) Write a JAVA program for creation of JAVA Built-in Exception Scenario.

## SOURCE CODE :

```

import java.util.Scanner;

public class Solution {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        try {
            System.out.print("Enter an integer to divide 100: ");
            int n = sc.nextInt();
            int result = 100 / n;
            System.out.println("Result: " + result);

            int[] arr = new int[3];
            System.out.println("Accessing element at index 5:");
            System.out.println(arr[5]);

            System.out.print("Enter a number as text: ");
            String s = sc.next();
            int num = Integer.parseInt(s);
            System.out.println("Converted number: " + num);
        }

        catch (ArithmeticException e) {
            System.out.println("ArithmeticException: Division by zero.");
        }

        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("ArrayIndexOutOfBoundsException: Invalid index.");
        }

        catch (NumberFormatException e) {
            System.out.println("NumberFormatException: Invalid numeric format.");
        }

        catch (Exception e) {   
            System.out.println("Some other exception occurred.");
        }

        System.out.println("Program continues...");
        sc.close();
    }
}

```

## OUTPUT :


<img width="1920" height="1080" alt="Exp6c" src="https://github.com/user-attachments/assets/7b167ca6-46e5-4bad-93a0-7860ab5f6377" />
