

#include<stdio.h>
int main()
{
    char operation;
    double n1,n2;

    jump:

    printf("Enter your operator(+,-,*,/): ");
    scanf(" %c", &operation);
    printf("tomar operator er ASCII value: %d\n\n",operation);
          // ASCII extra add korchi mandatory na

    if(operation != '+' && operation != '-' && operation != '*' && operation != '/')
        {
        printf("ERROR: Onerokom operator disen! thik kora lagbe... TRY AGAIN.\n\n");
        goto jump;
        }

    printf("Enter your 1st number to calculate: ");
     if (scanf("%lf", &n1) != 1)            // songkha er poribrte onno kichu dile abr goto te jabe
     {
        printf("ERROR: Apni number den ni! Shuru theke abar korun.\n\n");
        while(getchar() != '\n');             // otirikto sob soranor jonno
        goto jump;
     }

    printf("Enter your 2nd number to calculate: ");

     if (scanf("%lf", &n2) != 1) {
        printf("ERROR: Apni number den ni! Shuru theke abar korun.\n\n");
        while(getchar() != '\n');
        goto jump; }


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
            printf("Its impossible or  error \n\n");
            goto jump;
            }
        break;

    default :
        printf("ERROR, You need to go to doctor to see the operators ... TRY AGAIN: \n\n");

        goto jump;


    }
    return 0;
}
