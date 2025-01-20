
// 1) Using a single loop

 import java.util.Scanner
 public class Main{
    public static void main(String[] args) {
        int rows = 4; 
        int columns = 12;

        for (int i = 0; i < rows; i++) {
            StringBuilder row = new StringBuilder(); 
            for (int j = 0; j < columns; j++) {
                if (j < 4) {
                   row.append("*"); // Green stripe
                } else if (j < 8) {
                    row.append("="); // White stripe
                } else {
                     row.append("*"); // Green stripe
                }
            }
            System.out.println(row); 
        }
    }
}
 
//1b Using a nested loop

import java.util.Scanner
public class Main {
    public static void main(String[] args) {
        int rows = 4; // Number of rows in the flag
        int columns = 12; // Number of columns in the flag

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                if (j < 4) {
                    System.out.print("*"); // Green section
                } else if (j < 8) {
                    System.out.print("="); // White section
                } else {
                    System.out.print("*"); // Green section
                }
            }
            System.out.println(); // Move to the next row
        }
    }
}

//2a) Using a single loop
 
import java.util.Scanner
public class Main {
    public static void main(String[] args) {
        int rows = 6;
        int columns = 11; // Total characters per row (including spaces)

        for (int i = 0; i < rows; i++) {
            StringBuilder row = new StringBuilder();

            for (int j = 0; j < columns; j++) {
                if (i < 3 && j < 3) {
                    row.append("*"); // Top three rows, first three stars
                } else {
                    row.append("="); // All equals in other parts
                }
            }
            System.out.println(row);
        }
    }
}

//2b)Using a nested loop
import java.util.Scanner 
public class Main {
    public static void main(String[] args) {
        int rows = 6;
        int columns = 11; // Total characters per row (including spaces)

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                if (i < 3 && j < 3) {
                    System.out.print("*"); // Top three rows, first three stars
                } else {
                    System.out.print("="); // All equals in other parts
                }
            }
            System.out.println(); // Move to the next row
        }
    }
}

// 3) 
import java.util.Arrays;

public class Statistics {
    public static void main(String[] args) {
        // Given array
        int[] array = {2, 5, 5, 9, 4, 7, 0, 9, 6, 11, 12};

        // Calculate mean
        double mean = calculateMean(array);
        System.out.println("Mean: " + mean);

        // Calculate median
        double median = calculateMedian(array);
        System.out.println("Median: " + median);

        // Calculate standard deviation
        double stdDev = calculateStandardDeviation(array, mean);
        System.out.println("Standard Deviation: " + stdDev);
    }

    // Method to calculate mean
    public static double calculateMean(int[] array) {
        int sum = 0;
        for (int num : array) {
            sum += num;
        }
        return (double) sum / array.length;
    }

    // Method to calculate median
    public static double calculateMedian(int[] array) {
        Arrays.sort(array);
        int n = array.length;
        if (n % 2 == 0) {
            return (array[n / 2 - 1] + array[n / 2]) / 2.0;
        } else {
            return array[n / 2];
        }
    }

    // Method to calculate standard deviation
    public static double calculateStandardDeviation(int[] array, double mean) {
        double sumSquaredDifferences = 0;
        for (int num : array) {
            sumSquaredDifferences += Math.pow(num - mean, 2);
        }
        return Math.sqrt(sumSquaredDifferences / array.length);
    }
}





// 4) 
 
import java.util.Scanner;

public class Array {
    public static void main(String[] args) {
        // Declare an array of length 10
        int[] numbers = new int[10];
        
        // Create a Scanner object for user input
        Scanner scanner = new Scanner(System.in);

        // Part (a): Populate the array with user input
        System.out.println("Please enter 10 numbers:");
        for (int i = 0; i < numbers.length; i++) {
            System.out.print("Enter value for index " + i + ": ");
            numbers[i] = scanner.nextInt();
        }

        // Part (b): Print the elements of the array using a for-each loop
        System.out.println("\nThe values you entered are:");
        for (int number : numbers) {
            System.out.println(number);
        }

        // Close the scanner
        scanner.close();
    }
}

//5) 
import java.util.Scanner;

public class TwoDArray {
    public static void main(String[] args) {
        // Declare a 2D array of size 10x10
        int[][] array = new int[10][10];

        // Create a Scanner object for user input
        Scanner scanner = new Scanner(System.in);

        // Part (a): Assign elements to the array with user input
        System.out.println("Enter elements for a 10x10 array:");
        for (int i = 0; i < 10; i++) {
            for (int j = 0; j < 10; j++) {
                System.out.print("Enter element for index [" + i + "][" + j + "]: ");
                array[i][j] = scanner.nextInt();
            }
        }

        // Part (b): Print out the array elements using a for-each loop
        System.out.println("\nElements of the array:");
        for (int[] row : array) {
            for (int element : row) {
                System.out.print(element + " ");
            }
            System.out.println();
        }

        scanner.close();
    }
}
