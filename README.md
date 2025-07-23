# Weighted-Grade-Calculator
A simple weighted grade calculator in C.
[Up#include <stdio.h>

int main() {
    int count, i;
    float grades[100], weights[100];
    float total_weight = 0.0f, average = 0.0f;

    printf("How many grades will you enter? ");
    scanf("%d", &count);

    for (i = 0; i < count; i++) {
        printf("%d.enter your grades: ", i + 1);
        scanf("%f", &grades[i]);

        printf("Enter the weight of the %d.grades(example, 0.2): ", i + 1);
        scanf("%f", &weights[i]);

        total_weight += weights[i];
    }

    if (total_weight != 1.0f) {
        printf("\nERROR: The total weights sum to %.2f, but should be 1.0 (100%%)!\n", total_weight);
        return 1;
    }

    for (i = 0; i < count; i++) {
        average += grades[i] * weights[i];
    }

    printf("\nAverage: %.2f\n", average);


    if (average >= 90)
        printf("Letter Grade: AA - Status: Passed\n");
    else if (average >= 80)
        printf("Letter Grade: BA - Status: Passed\n");
    else if (average >= 70)
        printf("Letter Grade: BB - Status: Passed\n");
    else if (average >= 60)
        printf("Letter Grade: CB - Status: Passed\n");
    else if (average >= 50)
        printf("Letter Grade: CC - Status: Passed\n");
    else if (average >= 40)
        printf("Letter Grade: DC - Status: Conditionally Passed\n");
    else
        printf("Letter Grade: FF - Status: Failed\n");

    return 0;
}
loading Weighted_Grade_Calculator.c…]()
