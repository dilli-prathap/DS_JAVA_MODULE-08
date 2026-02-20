# Ex13 Fill the First 10 Elements of an Array with a Constant using Arrays.fill()
## DATE: 20-02-2026
## AIM:
To write a Java program that fills the first 10 elements of an array with a constant value using the Arrays.fill() method.

## Algorithm
1. Start
2. Read the value to fill in the array
3. Create an array of fixed size (10)
4. Use Arrays.fill() to fill the array with the given value
5. Store the filled array
6. Display all elements of the array
7. Stop

## Program:
``` JAVA
/*
Program to FILL the first 10 elements of an array with a constant value using the Arrays.fill() method.
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014 
*/

import java.util.*;

public class FillArrayUsingArraysFill {

    public static int[] fillArray(int size, int value) {
        int[] arr = new int[size];
        Arrays.fill(arr, value);
        return arr;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int value = sc.nextInt();
        int[] arr = fillArray(10, value);
        System.out.println("Array elements:");
        for (int num : arr) {
            System.out.print(num + " ");
        }
        sc.close();
    }
}
```

## Output:

<img width="706" height="176" alt="516794662-aae723c2-ddfa-4dc0-8667-16517f6282b9" src="https://github.com/user-attachments/assets/9f7d35be-7337-48c6-81f5-4bf03cf77b2e" />


## Result:
The program successfully fills the first 10 elements of the array with the constant value 5 using the Arrays.fill() method.
