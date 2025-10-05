# sorting.algorithms-cpp


***

### **Experiment 1: Bubble Sort**

**Aim:** To implement and demonstrate the **Bubble Sort** algorithm, which repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order.

**Theory:** **Bubble Sort** is a simple comparison-based sorting algorithm. It works by moving the largest (or smallest) unsorted element to its correct position at the end of the unsorted portion of the list in each pass.
* It makes multiple passes through the list.
* In each pass, adjacent elements are compared, and if they are out of order, they are swapped.
* After the first pass, the largest element "bubbles up" to the end of the array. The time complexity is $\mathcal{O}(n^2)$.

**Algorithm:**
1.  **Input:** The program prompts the user to enter the number of elements and the array values.
2.  **Define `swap` function:** A helper function `swap` is defined to exchange the values of two integers using pointers.
3.  **Sorting Loop:** An outer `while` loop iterates `n` times (where `n` is the number of elements), representing the passes.
4.  **Comparison and Swap:** An inner `for` loop iterates through the unsorted part of the array, comparing `array[i]` with `array[i+1]`.
5.  If `array[i] > array[i+1]`, the `swap` function is called to exchange their values.
6.  The outer loop counter `n` is incremented after each pass, reducing the size of the unsorted portion.
7.  **Output:** The sorted array is printed.

***

### **Experiment 2: Insertion Sort**

**Aim:** To implement and demonstrate the **Insertion Sort** algorithm, which builds the final sorted array one item at a time.

**Theory:** **Insertion Sort** works by treating the array as two parts: a sorted subarray and an unsorted subarray.
* It iterates through the unsorted elements, taking one element at a time.
* This element (**`key`**) is compared with the elements in the sorted subarray.
* Elements larger than the `key` in the sorted subarray are shifted one position to the right to make space.
* The `key` is then inserted into its correct sorted position. The average and worst-case time complexity is $\mathcal{O}(n^2)$, but it is efficient for small datasets or nearly sorted data.

**Algorithm:**
1.  **Define `insertionSort` function:** The function takes the array `arr` and its size `n`.
2.  **Outer Loop:** A `for` loop iterates from the second element (`i=1`) to the end of the array. The element at index `i` is the `key` to be inserted.
3.  **Inner Loop (Shifting):** A `while` loop compares `key` with elements in the sorted subarray (`arr[j]`).
4.  If an element `arr[j]` is greater than `key`, it is shifted one position to the right (`arr[j+1] = arr[j]`).
5.  The `j` index is decremented (`j--`) to continue shifting to the left.
6.  **Insertion:** The `key` is finally placed into its correct spot at `arr[j+1]`.
7.  **In `main`:** The array is initialized, sorted using `insertionSort`, and both the original and sorted arrays are printed.

***

### **Experiment 3: Selection Sort (Pointer-Based Implementation)**

**Aim:** To implement and demonstrate the **Selection Sort** algorithm using pointer arithmetic for finding the smallest element and placing it at the correct position.

**Theory:** **Selection Sort** divides the array into two parts: a sorted part at the beginning and an unsorted part remaining at the end.
* It repeatedly finds the **minimum element** from the unsorted part.
* It then **swaps** the minimum element with the element at the beginning of the unsorted part, thereby extending the sorted part.
* The algorithm performs $n$ passes, and its time complexity is $\mathcal{O}(n^2)$.

**Algorithm:**
1.  **Input:** The program prompts the user for the array elements.
2.  **Define `s_sort` function:** The function takes a pointer to the array (`int* a`) and the number of elements.
3.  **Outer Loop (Passes):** A `while` loop iterates `elements` times. In each iteration, the starting position of the unsorted segment is advanced by one (by incrementing pointer `a`).
4.  **Inner Loop (Comparison):** A `for` loop iterates through the rest of the unsorted array using pointer `b`.
5.  **Comparison and Swap:** Inside the inner loop, it compares the value pointed to by `a` (the current minimum candidate) with the value pointed to by `b`. If the current minimum candidate (`*a`) is greater than the element being checked (`*b`), the `swap` function is called to exchange them. *Note: In a standard selection sort, the swap is usually performed only once per pass, outside the inner loop, after finding the true minimum.*
6.  **Output:** The sorted array is printed.

***

### **Conclusion**

These experiments successfully implemented and demonstrated three foundational comparison-based sorting algorithms: **Bubble Sort**, **Insertion Sort**, and **Selection Sort**. All three algorithms have a time complexity of $\mathcal{O}(n^2)$, making them inefficient for large datasets. However, they clearly illustrate different sorting mechanics: Bubble Sort compares and swaps adjacent elements; Insertion Sort builds a sorted subarray by shifting elements; and Selection Sort repeatedly finds and places the minimum element.
