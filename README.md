# Array-operations-in-c-
This program performs basic operations on an array such as displaying elements, finding the sum, finding the largest and smallest element, and searching for an element.




CODE:-
#include <stdio.h>

int main() {
    int arr[100], n, i, choice, key;
    int sum = 0, max, min, found = 0;

    printf("Enter number of elements: ");
    scanf("%d", &n);

    printf("Enter array elements:\n");
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    do {
        printf("\n--- Array Operations ---\n");
        printf("1. Display\n");
        printf("2. Sum\n");
        printf("3. Maximum\n");
        printf("4. Minimum\n");
        printf("5. Search\n");
        printf("6. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Array elements: ");
                for (i = 0; i < n; i++)
                    printf("%d ", arr[i]);
                printf("\n");
                break;

            case 2:
                sum = 0;
                for (i = 0; i < n; i++)
                    sum += arr[i];
                printf("Sum = %d\n", sum);
                break;

            case 3:
                max = arr[0];
                for (i = 1; i < n; i++)
                    if (arr[i] > max)
                        max = arr[i];
                printf("Maximum = %d\n", max);
                break;

            case 4:
                min = arr[0];
                for (i = 1; i < n; i++)
                    if (arr[i] < min)
                        min = arr[i];
                printf("Minimum = %d\n", min);
                break;

            case 5:
                printf("Enter element to search: ");
                scanf("%d", &key);

                found = 0;
                for (i = 0; i < n; i++) {
                    if (arr[i] == key) {
                        printf("Element found at position %d\n", i + 1);
                        found = 1;
                        break;
                    }
                }

                if (!found)
                    printf("Element not found\n");
                break;

            case 6:
                printf("Exiting program...\n");
                break;

            default:
                printf("Invalid choice!\n");
        }
    } while (choice != 6);

    return 0;
}


SAMPLE INPUT :-
Enter number of elements: 5
Enter array elements:
10 20 5 40 15
Enter your choice: 3


SAMPLE OUTPUT :-
Maximum = 40



FEATURES :-
*Display array elements.
*Calculate sum.
*Find maximum element.
*Find minimum element.
*Search for an element.
