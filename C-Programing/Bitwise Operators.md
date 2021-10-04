#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>
int main()
{
    int i,j,n,k;
    int maAnd=0,maOr=0,maXor=0;
    scanf("%d %d",&n,&k);
    for(i=1;i<=n;i++)
   {
       for(j=i+1;j<=n;j++)
       {
           if(maAnd<(i & j)&&(i & j)<k)
           maAnd=i&j;
           if(maOr<(i |j )&&(i | j)<k)
           maOr=i|j;
           if(maXor<(i ^ j)&&(i ^ j)<k)
           maXor=i^j;
       }
       
   }
       printf("%d\n", maAnd);
       printf("%d\n", maOr);
       printf("%d\n", maXor);
           
       return 0;

}

