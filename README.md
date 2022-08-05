#include <stdio.h>
#include <stdlib.h>

int main()
{
    int cmonth[13] = {0, 31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};

    int i;

    int fday;
    scanf( "%i %i", &i, &fday);
    int r = 7 - fday;
        int sum = 0;
    for(int j = 1; j < i; j++){
        printf("%d\n", cmonth[j]);
        sum = sum + cmonth[j];
    }
    sum = sum - r;
    int br = sum%7;
     printf("%i\n", br);

       int c = br;
       int b =0;
       while(c < 1){
               c++;
               b++;
       }
                   printf("%i\n", b);
    printf("%s\t%s\t%s\t%s\t%s\t%s\t%s\t\n", "M", "T", "W", "T", "F", "S", "S");

    for(int j = br; j < cmonth[i]; j++){
       b++;

        if(b == 7){
               b = 0;
               printf("\n");
        }
        if(br < 1){
               printf("%s", "\t");


        }else{

                    printf("%d\t", j);
        }

       br++;


    }

    return 0;
}

