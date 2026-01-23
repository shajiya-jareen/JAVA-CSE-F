# Additional Experiments:

## TITLE: 2)Display the Fibonacci series.
## SOURCE CODE:

```
import java.util.Scanner;
class Fibonacciseries{
int sum;
int n;
int FirstNumber;
int SecondNumber;
int ThirdNumber;
Fibonacciseries(int number){
n=number;
FirstNumber = 0;
SecondNumber = 1;
}
void generate(){
if(n>0)
System.out.print("Fibonacci Series :");
while(n>0){
if(n == 1){
System.out.println(FirstNumber+".");
sum=sum+FirstNumber;
}else{
System.out.print(FirstNumber+",");
sum=sum+FirstNumber;
}
ThirdNumber=FirstNumber + SecondNumber;
FirstNumber=SecondNumber;
SecondNumber=ThirdNumber;
n--;
}
System.out.println("Sum of Fibonacci Series="+sum);
}
public static void main(String[] args){
Scanner sc = new Scanner(System.in);
System.out.print("Enter the value of n:");
int number = sc.nextInt();
Fibonacciseries f = new Fibonacciseries(number);
f.generate();
}

```
## OUTPUT:


<img width="1920" height="1080" alt="add exp2" src="https://github.com/user-attachments/assets/642d89dd-6f1e-4299-9abf-4b36eb60f0b4" />





# ADDITIONAL EXPERIMENT 1:
## TITLE: 1) Insert a sub string into a given main string.
## SOURCE CODE:

```

import java.util.Scanner;

class Substring {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the main string: ");
        String mainString = sc.nextLine();

        System.out.print("Enter the substring to insert: ");
        String subString = sc.nextLine();

        System.out.print("Enter the position: ");
        int position = sc.nextInt();

        if (position >= 0 && position <= mainString.length()) {
            String firstPart = mainString.substring(0, position);
            String secondPart = mainString.substring(position);

            String resultString = firstPart + subString + secondPart;
            System.out.println("Resulting string: " + resultString);
        } else {
            System.out.println("Invalid position");
        }
    }
}


```

## OUTPUT:

<img width="1920" height="1080" alt="add exp1" src="https://github.com/user-attachments/assets/fc4ba73d-0c5e-490e-91df-c79d04eb35a7" />




# ADDITIONAL EXPERIMENT 3:
## TITLE: 3) Determine if a given string is palindrome or not.
## SOURCE CODE:

```

import java.util.Scanner;

class Palindrome {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a String:");
        String str= sc.nextLine();
        int start = 0;
        int end = str.length() - 1;
        while (start < end) {
            if (str.charAt(start) != str.charAt(end)) {
                System.out.println(str+" is not a palindrome");
                return;
            }

            start++;
            end--;
        }
        System.out.println(str+" is a palindrome");
    }
}

```

## OUTPUT:

<img width="1920" height="1080" alt="add exp3" src="https://github.com/user-attachments/assets/20564cc4-4b9f-4962-b998-510b5d05f68e" />


# ADDITIONAL EXPERIMENT 4:
## TITLE: 4) Check if a number is a perfect number.
## SOURCE CODE:

```

import java.util.Scanner;

class PerfectNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int num = sc.nextInt();

        int sum = 0;

        for (int i = 1; i < num; i++) {
            if (num % i == 0) {
                sum += i;
            }
        }

        if (sum == num)
            System.out.println(num + " is a perfect number.");
        else
            System.out.println(num + " is not a perfect number.");
    }
}

```

## OUTPUT:

<img width="1920" height="1080" alt="add exp4" src="https://github.com/user-attachments/assets/27b53eef-4da1-4176-b25c-89966578ad26" />




