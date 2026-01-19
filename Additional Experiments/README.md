#Additional Experiment 2
##TITLE: 2)Display the Fibonacci series.
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
#output
<img width="1920" height="1080" alt="add exp2" src="https://github.com/user-attachments/assets/642d89dd-6f1e-4299-9abf-4b36eb60f0b4" />

}

