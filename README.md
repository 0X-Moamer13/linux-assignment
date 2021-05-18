# linux-assignment
#include <stdio.h>

int main()
{
    int m, n, p, q, c, d, k, sum = 0;
    int first[10][10], second[10][10], multiply[10][10];

    printf("\nEnter the type of matrix 1:\n");
    scanf("%d%d", &m, &n);



    printf("\nEnter the type of matrix 2:\n");
    scanf("%d%d", &p, &q);


    if ( n != p )
    {
        printf("\nMatrices with entered orders can't be multiplied with each other.\n");
        printf("\nThe column of first matrix should be equal to row of second.\n");
    }
    else
    {

        printf("\nEnter the elements of first matrix:\n");
        for (  c = 0 ; c < m ; c++ )
            for ( d = 0 ; d < n ; d++ )
                scanf("%d", &first[c][d]);


        printf("\nEnter the elements of second matrix:\n");
        for ( c = 0 ; c < p ; c++ )
            for ( d = 0 ; d < q ; d++ )
                scanf("%d", &second[c][d]);


        for ( c = 0 ; c < m ; c++ )
        {
            for ( d = 0 ; d < q ; d++ )
            {
                for ( k = 0 ; k < p ; k++ )
                {
                    sum = sum + first[c][k]*second[k][d];
                }

                multiply[c][d] = sum;
                sum = 0;
            }
        }


        printf("\nThe product of entered matrices is:\n");
        for ( c = 0 ; c < m ; c++ )
        {
            for ( d = 0 ; d < q ; d++ )
                printf("%d\t", multiply[c][d]);

            printf("\n");
        }
    }

    return 0;
![Screenshot 05-18-2021 23 12 35](https://user-images.githubusercontent.com/77538165/118725357-b5798a80-b7e4-11eb-8d58-f3645f89b1b9.png)


