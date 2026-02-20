# Ex15 Value Existence Check in a TreeMap
## DATE: 20-02-2026
## AIM:
To write a Java program that checks whether a given value exists in a TreeMap.

## Algorithm

1. Start
2. Read number of key-value pairs (n)
3. Create an empty TreeMap
4. For each pair:
5. Read key
6. Read value
7. Insert key and value into the TreeMap
8. Read the value to search
9. If TreeMap contains the search value, print "Value exists"
10. Else print "Value does not exist"
11. Stop   

## Program:
```
/*
Program to checks whether a given value exists in a TreeMap.
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014 
*/

import java.util.*;

public class TreeMapValueExistenceCheck {

    public static void checkValue(TreeMap<Integer, String> map, String searchValue) {
        if(map.containsValue(searchValue)){
            System.out.println("Value \""+searchValue+"\" exists in the TreeMap.");
        }else{
            System.out.println("Value \""+searchValue+"\" does not exist in the TreeMap.");
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        TreeMap<Integer, String> map = new TreeMap<>();

        int n = sc.nextInt();

        for (int i = 0; i < n; i++) {
            int key = sc.nextInt();
            sc.nextLine();  
            String value = sc.nextLine();
            map.put(key, value);
        }
        String searchValue = sc.nextLine();

        checkValue(map, searchValue);
        sc.close();
    }
}
```

## Output:

<img width="972" height="668" alt="516798421-7b5e2020-dba4-407f-89da-2b589d20945d" src="https://github.com/user-attachments/assets/91288659-4efb-406c-a335-dc457c8ea03a" />


## Result:
Thus, the program successfully checks whether a specified value exists in a TreeMap using the containsValue() method.
