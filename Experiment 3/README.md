## Experiment 3

## Experiment 3A

## TITLE: Implementing constructor overloading

---

## SOURCE CODE: student

```

class student{
String name;
int age;
double marks;
student(){
}
student(String name,int age,double marks){
this.name=name;
this.age=age;
this.marks=marks;
}
void display(){
System.out.println("Name:"+name);
System.out.println("Age:"+age);
System.out.println("marks:"+marks);
}
}

```

## MAIN.JAVA

```
class Main {
public static void main(String args[]){
student std = new student();
std.display();
student std1 =new student("Hari",40,67.8);
std1.display();
}
}

```

## OUTPUT:
<img width="1920" height="1080" alt="EXP3A" src="https://github.com/user-attachments/assets/113ac400-e805-4b86-9049-cc7ea3ac9347" />




## Experiment 3B
## TITLE:Implementing BinarySearch.

---

## SOURCE CODE:Binary Search

```

import java.util.Scanner;

class BinarySearch {

    int list[];
    int size;

    BinarySearch(int size) {
        list = new int[size];
        this.size = size;
    }

    void setList() {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the list items in Ascending Order.");

        for (int i = 0; i < size; i++) {
            System.out.print("Enter the value of " + (i + 1) + " item: ");
            list[i] = sc.nextInt();
        }
    }

    void getList() {
        System.out.print("Sorted Array: ");
        for (int i = 0; i < size; i++) {
            System.out.print(list[i] + " ");
        }
        System.out.println();
    }

    int binarySearch(int key) {

        int low = 0;
        int high = size - 1;

        while (low <= high) {
            int mid = (low + high) / 2;

            if (list[mid] == key)
                return mid;
            else if (list[mid] < key)
                low = mid + 1;
            else
                high = mid - 1;
        }
        return -1;
    }
}

```

## MAIN.JAVA:

```

import java.util.Scanner;

class Main {

    public static void main(String args[]) {

        Scanner sc = new Scanner(System.in);

        BinarySearch bs = new BinarySearch(10);
        bs.setList();
        bs.getList();

        System.out.print("Enter the key to search: ");
        int key = sc.nextInt();

        int index = bs.binarySearch(key);

        if (index == -1)
            System.out.println("Key item does not exist");
        else
            System.out.println("Key item exists at index: " + index);
    }
}

```

## OUTPUT:

<img width="1920" height="1080" alt="EXP 3B" src="https://github.com/user-attachments/assets/5ece6d1d-c612-4543-af02-6374bfdfeb87" />



## EXPERIMENT 3C
## TITLE:Implementing Bubble Sort.

---

## SOURCE CODE:Bubble Sort

```

class BubbleSort {

	void bubbleSort(int arr[]) {

		int n = arr.length;
		int temp = 0;

		for(int i=0 ; i < n-1 ; i++) {

			for(int j=0; j<n-i-1; j++) {

				if(arr[j] > arr[j+1]) {

					temp = arr[j+1];
					arr[j+1] = arr[j];
					arr[j] = temp;

				}
			}
		}

	}

}

```

## MAIN.JAVA:

```

import java.util.Scanner;

class Main {

    public static void main(String args[]) {

        Scanner sc = new Scanner(System.in);

        BinarySearch bs = new BinarySearch(10);
        bs.setList();

        System.out.print("Enter the key to search: ");
        int key = sc.nextInt();

        int index = bs.binarySearch(key);

        if (index == -1)
            System.out.println("Key item does not exist");
        else
            System.out.println("Key item exists at index: " + index);
    }
}

```

## OUTPUT:


<img width="1920" height="1080" alt="EXP 3C" src="https://github.com/user-attachments/assets/00fbdb3e-d0d0-47a2-bbc7-af612563d896" />




