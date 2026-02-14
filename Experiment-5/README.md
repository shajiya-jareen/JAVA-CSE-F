## Experiment-5

## TITLE: 5A) Write a JAVA program to implement Interface. What kind of Inheritance can be achieved?

## SOURCE CODE:

```

interface Sortable {
    void sort(int[] arr);
}
class BubbleSort implements Sortable {

    public void sort(int[] arr) {
        int n = arr.length;

        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {

                if (arr[j] > arr[j + 1]) {
                    // swap
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }
}
class SelectionSort implements Sortable {

    public void sort(int[] arr) {
        int n = arr.length;

        for (int i = 0; i < n - 1; i++) {

            int minIndex = i;

            for (int j = i + 1; j < n; j++) {
                if (arr[j] < arr[minIndex]) {
                    minIndex = j;
                }
            }

            int temp = arr[minIndex];
            arr[minIndex] = arr[i];
            arr[i] = temp;
        }
    }
}
public class TestSort {

    public static void main(String[] args) {

        int[] arr1 = {5, 2, 9, 1, 3};

        Sortable ref;

        ref = new BubbleSort();
        ref.sort(arr1);

        System.out.println("Array sorted using BubbleSort:");
        display(arr1);

        int[] arr2 = {8, 4, 7, 6, 2};

        ref = new SelectionSort();
        ref.sort(arr2);

        System.out.println("Array sorted using SelectionSort:");
        display(arr2);
    }

    static void display(int[] arr) {
        for (int num : arr) {
            System.out.print(num + " ");
        }
        System.out.println();
    }
}

```

## OUTPUT:

<img width="1920" height="1080" alt="Exp5A" src="https://github.com/user-attachments/assets/ca7c8815-843b-4fd8-bc06-d99c0aebf9c7" />


## TITLE: 5B) Write a JAVA program that implements Runtime polymorphism.

## SOURCE CODE:

```

class Vehicle{
void run(){
System.out.println("A Vehicle is running.");
}
}
class Car extends Vehicle{
void run(){
System.out.println("A Car is running on four wheels.");
}
}
class Bike extends Vehicle{
void run(){
System.out.println("A Bike is running on two wheels.");
}
}
public class TestVehicle{
public static void main(String[] args){
Vehicle v;
v=new Car();
v.run();
v=new Bike();
v.run();
v=new Vehicle();
v.run();
}
}

```


## OUTPUT:

<img width="1920" height="1080" alt="Exp5B" src="https://github.com/user-attachments/assets/aa865ca4-6c36-4e6a-a150-a06bea7f020d" />



## TITLE: 5C) Write a JAVA program using StringBuffer to delete, remove character.

## SOURCE CODE:

```

public class StringBufferDeleteDemo{
public static void main(String[] args){
StringBuffer sb = new StringBuffer("Java Programming");
System.out.println("Original String:"+sb);
sb.deleteCharAt(4);
System.out.println("After deleting the character at index 4:"+sb);
sb.delete(0,4);
System.out.println("After deleting the characters from index 0 to 4:"+sb);
}
}

```

## OUTPUT:

<img width="1920" height="1080" alt="Exp5C" src="https://github.com/user-attachments/assets/8ed03e51-7cf8-4376-8568-b6b6cd7605f2" />

