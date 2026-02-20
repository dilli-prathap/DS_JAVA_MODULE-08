# Ex14 Tracking the First Unique Number in a Stream using LinkedHashMap
## DATE:  20-02-2026
## AIM:
To implement a program that tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.

## Algorithm
1. Start
2. Read number of elements (n)
3. Create an empty LinkedHashMap to store element frequency
4. For each element in the stream:
5. Read the current number
6. Update its frequency in the map
7. Traverse the map in insertion order
8. Find the first element with frequency equal to 1
9. If found, print the first unique number
10. Else print "No unique number"
11. Repeat until all elements are processed
12. Stop   

## Program:
``` JAVA
/*
Program to tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.
Developed by: 
RegisterNumber:  
*/

import java.util.*;

public class FirstUniqueNumberStream {

    public static void processStream(int n, Scanner sc) {
        LinkedHashMap<Integer, Integer> freqMap = new LinkedHashMap<>();
        for(int i=0; i<n; i++){
            int current = sc.nextInt();
            
            freqMap.put(current, freqMap.getOrDefault(current, 0)+1);
            
            int fUniq = -1;
            
            for(Map.Entry<Integer, Integer> entry : freqMap.entrySet()){
                if(entry.getValue() == 1){
                    fUniq = entry.getKey();
                    break;
                }
            }
            
            if(fUniq != -1){
                System.out.println("First unique number: "+fUniq);
            }else{
                System.out.println("No unique number");
            }
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        processStream(n, sc);
        sc.close();
    }
}
```

## Output:

<img width="686" height="507" alt="516797242-9cb53408-1cbe-4bef-aa1e-de010ab47226" src="https://github.com/user-attachments/assets/3cc28c1e-de19-442b-86fa-6ee115b8976f" />


## Result:
The program successfully tracks and returns the first unique number at any point in the integer stream using a LinkedHashMap.
