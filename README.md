# Code-12
Exp 12

#include <stdio.h>

void selectionSort(int a[], int n) {
    for (int i = 0; i < n - 1; i++) {
        int minIdx = i;

        for (int j = i + 1; j < n; j++) {
            if (a[j] < a[minIdx])
                minIdx = j;
        }

        int temp = a[i];
        a[i] = a[minIdx];
        a[minIdx] = temp;
    }
}

void display(int a[], int n) {
    for (int i = 0; i < n; i++)
        printf("%d ", a[i]);

    printf("\n");
}

int main() {
    int a[100], n;

    printf("Enter number of elements: ");
    if (scanf("%d", &n) != 1) return 0;

    printf("Enter %d elements:\n", n);

    for (int i = 0; i < n; i++) {
        scanf("%d", &a[i]);
    }

    selectionSort(a, n);

    printf("Sorted array using Selection Sort: ");
    display(a, n);

    return 0;
}
