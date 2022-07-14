//pattern
#include <stdio.h>

int main()
{

    int n;
    printf("Enter the number : ");
    scanf("%d", &n);
    int len = (2 * n) - 1;
    // Complete the code to print the pattern.
    for (int i = 1; i <= len; i++)
    {
        for (int j = 1; j <= len; j++)
        {
            int min = (i < j) ? i - 1 : j - 1;
            min = (min < len - i) ? min : len - i;
            min = (min < len - j) ? min : len - j;
            printf("%d ", n - min);
        }
        printf("\n");
    }
    return 0;
}
