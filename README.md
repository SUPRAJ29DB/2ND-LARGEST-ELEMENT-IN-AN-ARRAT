# 2ND-LARGEST-ELEMENT-IN-AN-ARRAY
LET ARR[]={1, 2, 3, 4, 5} THEN OUTPUT WILL BE 4.....

```
#include <stdio.h>
#include <limits.h>

int secondlargest(int arr[], int n) {
    int firstlargest = INT_MIN, secondlargest = INT_MIN;

    for (int i = 0; i < n; i++) {
        if (arr[i] > firstlargest) {
            firstlargest = arr[i];
        }
    }

    for (int i = 0; i < n; i++) {
        if (arr[i] > secondlargest && arr[i] < firstlargest) {
            secondlargest = arr[i];
        }
    }

    if (secondlargest == INT_MIN) {
        return INT_MIN;  // No second largest found
    }

    return secondlargest;
}

int main() {
    int n, i;
    printf("Enter size of array: ");
    scanf("%d", &n);

    if (n < 2) {
        printf("Array must have at least 2 elements to find second largest.\n");
        return 0;
    }

    int arr[n];
    for (i = 0; i < n; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%d", &arr[i]);
    }

    int _2ndlargest = secondlargest(arr, n);

    if (_2ndlargest == INT_MIN) {
        printf("Second largest element not found (all elements may be equal).\n");
    } else {
        printf("The second largest element is: %d\n", _2ndlargest);
    }

    return 0;
}
```
    //
// Created by Suprakash Ghosh on 25-07-2025.
//
*** SAME CODE WILL BE APPLICABE FOR FINDING LARGEST ELEMENT .... IN THAT CODE YOU NEED TO CHANGE SOMETHING........
......IN THAT FUNCTION AND OTHER LOGIC IS SAME....****
