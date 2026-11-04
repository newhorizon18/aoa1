
# Experiment No. 1 – Insertion Sort

**Created By:** Krish Mhatre

## Aim
To implement Insertion Sort using C.

## Theory
Insertion Sort is a simple sorting algorithm that arranges elements in ascending order.

It works by taking one element at a time and inserting it into its correct position in the sorted part of the array.

## Algorithm
1. Start from the second element.
2. Store the current element in `key`.
3. Compare `key` with previous elements.
4. Shift larger elements one position to the right.
5. Insert `key` at its correct position.
6. Repeat until the array is sorted.

## C Program

```c
#include <stdio.h>

int main() {
    int a[100], n, i, j, key;

    printf("Enter number of elements: ");
    scanf("%d", &n);

    if(n < 1 || n > 100) {
        printf("Invalid number of elements");
        return 1;
    }

    printf("Enter elements: ");
    for(i = 0; i < n; i++)
        scanf("%d", &a[i]);

    for(i = 1; i < n; i++) {
        key = a[i];
        j = i - 1;

        while(j >= 0 && a[j] > key) {
            a[j + 1] = a[j];
            j--;
        }
        a[j + 1] = key;
    }

    printf("Sorted Array: ");
    for(i = 0; i < n; i++)
        printf("%d ", a[i]);

    return 0;
}
```

## How to Run

**Step 1:** Save the file as `insertion.c`.

**Step 2:** Open the terminal and compile:

```bash
gcc insertion.c -o insertion
```

**Step 3:** Run the program in PowerShell:

```powershell
.\insertion
```

## Output

```text
Enter number of elements: 6
Enter elements: 12 5 18 2 9 7
Sorted Array: 2 5 7 9 12 18
```

## Time Complexity

| Case | Complexity |
|------|------------|
| Best Case | O(n) |
| Average Case | O(n²) |
| Worst Case | O(n²) |

**Space Complexity:** O(1)

## Conclusion
Successfully implemented Insertion Sort in C to arrange the given elements in ascending order.
