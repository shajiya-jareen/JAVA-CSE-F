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
