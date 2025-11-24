# recursive-functions
c program for recursive functions for number to check if given number is recursive or not
#include <stdio.h>

int Prime(int n, int i)
{
   
    if (i == 1)
        return 1;

    if (n % i == 0)
        return 0;

    return Prime(n, i - 1);
}

int main()
{
    int n;

    printf("Enter a number: ");
    scanf("%d", &n);


    if (Prime(n, n / 2))
{
        printf("%d is a PRIME number.\n", n);
}
    else
{
        printf("%d is NOT a prime number.\n", n);
}
    return 0;
}
