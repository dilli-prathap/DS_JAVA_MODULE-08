# Ex11 Convert HashSet to ArrayList in Java
## DATE: 20-02-2026
## AIM:
To convert a collection of distinct integers stored in a HashSet into an ArrayList and display its contents.

## Algorithm
1. Start
2. Read number of elements (n)
3. Create an empty HashSet
4. Insert n elements into the HashSet
5. Convert the HashSet into an ArrayList
6. Store the converted elements in a list
7. Display the elements of the ArrayList
8. Stop

## Program:
``` JAVA
/*
Program to To convert a collection of distinct integers stored in a HashSet into an ArrayList and display its contents.
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
import java.util.*;

public class HashSetToArrayList {

    public static ArrayList<Integer> convertToArrayList(HashSet<Integer> set) {
        ArrayList<Integer> list = new ArrayList<>(set);
        return list;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        HashSet<Integer> set = new HashSet<>();
        for (int i = 0; i < n; i++) {
            int num = sc.nextInt();
            set.add(num);
        }

        ArrayList<Integer> list = convertToArrayList(set);
        System.out.println("ArrayList contents:");
        for (int num : list) {
            System.out.print(num + " ");
        }
        sc.close();
    }
}
```

## Output:

<img width="524" height="550" alt="516792341-4c2d3837-0a87-41dd-826e-6475bc62bfe8" src="https://github.com/user-attachments/assets/d38fc7ec-f7d2-4828-bb2f-071e6cc345ec" />


## Result:
The program successfully converts a collection of distinct integers stored in a HashSet into an ArrayList
