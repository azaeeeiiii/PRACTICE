# ForEachIn2D

This Java program demonstrates the use of **2D arrays** and **for-each loops**. It creates a 2D array, assigns values, prints the array, and calculates the sum of its elements.

---

## Features

- Creates a 2D array of size 3x2 (3 rows and 2 columns).
- Prints the **number of rows** and **number of columns**.
- Assigns values to the array using nested `for` loops.
- Displays array elements using a **for-each loop**.
- Calculates and prints the **sum of all elements** in the array.

---

## How it Works

1. Initialize a 2D array of integers:

```java
int[][] nums = new int[3][2];


class ForEachIn2D {
    public static void main(String[] args) {
        int sum = 0; //Store the value of the sum to zero.
        int[][] nums = new int[3][2]; //This creates a 2D array; Row = 3, Column = 2

        // print the number of rows
        System.out.println("Length of rows: " + nums.length); //This will print how many rows the array has. 
                                                                //nums.length count how many rows in the array.
        /*
             *  Row Columns
                0 → [ 0, 0 ]   
                1 → [ 0, 0 ]   
                2 → [ 0, 0 ] 
            */ 

        // ensure there is at least one row before accessing length of columns
        if (nums.length > 0) {
            System.out.println("Length of columns: " + nums[0].length); //This will access the length of the first row (columns). 
                                                                        //nums[0].length counts how mant columns in the first row. 
        } else {
            System.out.println("Array is empty, no columns.");
        }

        // assigning values to the array
        for(int row = 0; row < nums.length; row++) { //This checks each row one by one. 
            for(int col = 0; col < nums[row].length; col++) { //This checks each column, starting from zero and looping until the last column.
                nums[row][col] = (row + 1) * (col + 1);
            }
        }

        // using for-each loop to display the elements and calculate the sum
        for(int[] rvals : nums) {
            for(int cvals : rvals) {
                System.out.print(cvals + " ");
                sum += cvals;
            }
            System.out.println();
        }

        // print the total sum
        System.out.println("Summation: " + sum);
    }
}
