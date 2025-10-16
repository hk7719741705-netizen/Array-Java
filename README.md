# Array-Java
// ======= 1. Find the Largest Element in an Array =======
class LargestElement {
    public static void main(String[] args) {
        int[] arr = {10, 25, 30, 5, 60, 15};
        int max = arr[0];

        for (int i = 1; i < arr.length; i++) {
            if (arr[i] > max)
                max = arr[i];
        }
        System.out.println("Largest element: " + max);
    }
}

// ======= 2. Find the Smallest Element in an Array =======
class SmallestElement {
    public static void main(String[] args) {
        int[] arr = {45, 12, 78, 3, 90, 24};
        int min = arr[0];

        for (int i = 1; i < arr.length; i++) {
            if (arr[i] < min)
                min = arr[i];
        }
        System.out.println("Smallest element: " + min);
    }
}

// ======= 3. Sum and Average of Array Elements =======
class SumAndAverage {
    public static void main(String[] args) {
        int[] arr = {5, 10, 15, 20, 25};
        int sum = 0;

        for (int num : arr)
            sum += num;

        double avg = (double) sum / arr.length;
        System.out.println("Sum = " + sum);
        System.out.println("Average = " + avg);
    }
}

// ======= 4. Reverse an Array =======
class ReverseArray {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};

        System.out.print("Reversed array: ");
        for (int i = arr.length - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
    }
}

// ======= 5. Sort an Array =======
import java.util.Arrays;
class SortArray {
    public static void main(String[] args) {
        int[] arr = {10, 3, 7, 2, 15, 5};
        Arrays.sort(arr);

        System.out.println("Sorted array: " + Arrays.toString(arr));
    }
}

// ======= 6. Copy One Array to Another =======
class CopyArray {
    public static void main(String[] args) {
        int[] arr1 = {1, 2, 3, 4, 5};
        int[] arr2 = new int[arr1.length];

        for (int i = 0; i < arr1.length; i++) {
            arr2[i] = arr1[i];
        }

        System.out.println("Copied array:");
        for (int num : arr2)
            System.out.print(num + " ");
    }
}

// ======= 7. Find Duplicate Elements =======
class DuplicateElements {
    public static void main(String[] args) {
        int[] arr = {4, 2, 7, 4, 8, 2, 9};

        System.out.print("Duplicate elements: ");
        for (int i = 0; i < arr.length; i++) {
            for (int j = i + 1; j < arr.length; j++) {
                if (arr[i] == arr[j]) {
                    System.out.print(arr[i] + " ");
                    break;
                }
            }
        }
    }
}

// ======= 8. Count Even and Odd Numbers =======
class EvenOddCount {
    public static void main(String[] args) {
        int[] arr = {10, 21, 32, 43, 54, 65};
        int even = 0, odd = 0;

        for (int num : arr) {
            if (num % 2 == 0)
                even++;
            else
                odd++;
        }

        System.out.println("Even numbers: " + even);
        System.out.println("Odd numbers: " + odd);
    }
}

// ======= 9. Merge Two Arrays =======
class MergeArrays {
    public static void main(String[] args) {
        int[] arr1 = {1, 3, 5};
        int[] arr2 = {2, 4, 6};
        int[] merged = new int[arr1.length + arr2.length];

        int k = 0;
        for (int num : arr1)
            merged[k++] = num;
        for (int num : arr2)
            merged[k++] = num;

        System.out.print("Merged array: ");
        for (int num : merged)
            System.out.print(num + " ");
    }
}

// ======= 10. Frequency of Each Element =======
class FrequencyArray {
    public static void main(String[] args) {
        int[] arr = {1, 2, 2, 3, 3, 3, 4};
        boolean[] visited = new boolean[arr.length];

        System.out.println("Element | Frequency");
        for (int i = 0; i < arr.length; i++) {
            if (visited[i])
                continue;
            int count = 1;
            for (int j = i + 1; j < arr.length; j++) {
                if (arr[i] == arr[j]) {
                    visited[j] = true;
                    count++;
                }
            }
            System.out.println("   " + arr[i] + "     |     " + count);
        }
    }
}
