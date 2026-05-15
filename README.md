
#include<stdio.h>
int main()
{
    char operation;
    double n1,n2;

    printf("Enter your operator(+,-,*,/): ");
    scanf("%c", &operation);

    printf("Enter your 1st number to calculate: ");
    scanf("%lf",&n1);

    printf("Enter your 2nd number to calculate: ");
    scanf("%lf",&n2);

    switch(operation)
    {
    case '+':
        printf("%.1lf + %.1lf = %.1lf",n1,n2,n1+n2);
        break;

    case '-':
        printf("%.1lf - %.1lf = %.1lf",n1,n2,n1-n2);
        break;

    case '*':
        printf("%.1lf * %.1lf = %.1lf",n1,n2,n1*n2);
        break;

    case '/':
        if(n2!=0){
        printf("%.1lf / %.1lf = %.1lf",n1,n2,n1/n2);
                 }
        else {
            printf("Its impossible or  error");
            }
        break;

    default :
        printf("ERROR, You need to go to doctor to see the operators");


    }
    return 0;
}
