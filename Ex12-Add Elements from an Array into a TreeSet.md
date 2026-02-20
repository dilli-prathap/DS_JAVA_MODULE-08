# Ex12 Add Elements from an Array into a TreeSet
## DATE: 20-02-2026
## AIM:
To write a Java program that adds elements from an array into a TreeSet and displays the elements in sorted order.

## Algorithm
1. Start
2. Read number of elements (n)
3. Input array elements
4. Create an empty ArrayList
5. Add all array elements into the ArrayList
6. Create a TreeSet using the ArrayList
7. Store elements in the TreeSet (duplicates removed and sorted automatically)
8. Display the elements of the TreeSet
9. Stop

## Program:
``` JAVA
/*
Program that adds elements from an array into a TreeSet and displays the elements in sorted order.
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
import java.util.*;

public class ArrayToTreeSet {

    public static TreeSet<Integer> convertArrayToTreeSet(int[] arr) {
        List<Integer> list = new ArrayList<>();
        for(int x : arr){
            list.add(x);
        }
        
        TreeSet<Integer> treeSet = new TreeSet<>(list);
        return treeSet;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        TreeSet<Integer> treeSet = convertArrayToTreeSet(arr);
        System.out.println("Elements in TreeSet:");
        for (int num : treeSet) {
            System.out.println(num);
        }

        sc.close();
    }
}
```

## Output:

<img width="624" height="436" alt="516793884-b60e3c0f-761e-4118-af05-eb4781b2939f" src="https://github.com/user-attachments/assets/a051d468-45d2-4a90-a585-2e73c870f265" />


## Result:
The program successfully adds elements from an array into a TreeSet.
