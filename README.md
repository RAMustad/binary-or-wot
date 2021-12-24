#include <stdio.h>

void binarytodecimal(int n);


int main() {

    int num;
    printf("Input a binary number: ");
    scanf("%d", &num);

    int copy = num, temp = 0;

    while(copy != 0) {
        temp = copy%10;

        if((temp==0) || (temp==1)) {
            copy = copy/10;
            if(copy == 0) {
                printf("valid binary number.\n");
                break;
            }
        }
        else {
            printf("Not a valid binary number. Try again\n");
            main();
        }

    }

    return 0;
}
