## Practice Assessment 2: For-Each in 2D Array

## Goal
The goal of this code is to create a 2D array, assign values to its elements based on their row and column positions, and display the array. It also calculates and prints the total sum of all elements using a for-each loop.

---

## How It Works
1. This part will store the value of the sum to zero, create a 2D array having a row of 3 and a column of 2. This will also print how many rows the array has. 
```java
int sum = 0; //Store the value of the sum to zero.
        int[][] nums = new int[3][2]; //This creates a 2D array; Row = 3, Column = 2

        System.out.println("Length of rows: " + nums.length);
```
For example..
| ROW | COLUMN | VALUE |
|-----|--------|-------|
| 0   | 0      | 0     |
| 0   | 1      | 0     |
| 1   | 0      | 0     |
| 1   | 1      | 0     |
| 2   | 0      | 0     |
| 2   | 1      | 0     |


2. This code checks if the 2D array has at least one row. If there is at least one row, it prints the number of columns in the first row; otherwise, it prints that the array is empty.

```java
if (nums.length > 0) {
    System.out.println("Length of columns: " + nums[0].length);  // nums[0].length counts how many columns are in the first row
} else {
    System.out.println("Array is empty, no columns."); //This will print how many rows the array has. 
                                                                //nums.length count how many rows in the array.
}
        }
```

3. This loop goes through each row and column of the array. It fills each element with the value of (row + 1) * (col + 1).
```java
  for(int row = 0; row < nums.length; row++) { //This checks each row one by one.
     for(int col = 0; col < nums[row].length; col++) { //This checks each column, starting from zero and looping until the last column.
       nums[row][col] = (row + 1) * (col + 1);
            }
        }
   ```
### Computation 
| ROWS | COLUMNS |(row + 1) * (col + 1)| VALUE |
|------|---------|--------------------|-------|
| 0    | 0       | (0 + 1) * (0 + 1)  | 1     |
| 0    | 1       | (0 + 1) * (1 + 1)  | 2     |
| 1    | 0       | (1 + 1) * (0 + 1)  | 2     |
| 1    | 1       | (1 + 1) * (1 + 1)  | 4     |
| 2    | 0       | (2 + 1) * (0 + 1)  | 3     |
| 2    | 1       | (2 + 1) * (1 + 1)  | 6     |

4. This part uses a for-each loop to loop through each row and each element in the 2D array. This will print all the numbers in a grid format. At the same time, it adds every element to sum and finally prints the total sum of all numbers.
  ```java
for (int[] rvals : nums) {          // This will loop through each row
    for (int cvals : rvals) {       // This will loop through each column in the row
        System.out.print(cvals + " "); // This will print the current element
        sum += cvals;               // This will add the current element to sum
    }
    System.out.println();            // This will move to the next line after each row
}

System.out.println("Summation: " + sum); // This will print the total sum
```

## Output
```text
Length of rows: 3
Length of columns: 2
1 2 
2 4 
3 6 
Summation: 18
```
## Learnings
This code helped me understand how a 2D array works in Java and how each element is calculated. I was able to think through the computations and also learned how to sum all the elements using loops and conditions.




