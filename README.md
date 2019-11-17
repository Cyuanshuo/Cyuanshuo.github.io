## Hello World!
********************************************************************************************

### Markdown

********************************************************************************************

```markdown

###杨辉三角
#include <stdio.h>
int main()
{
    int a[6][11];           
    int i,j;
    for(i=0;i<6;i++)
    {
        for(j=0;j<11;j++)
        {
            a[i][j]=0;       
        }
    }
    for(i=0;i<6;i++)
    {
                j=5-i;         
            a[i][j]=1;
            a[i][10-j]=1;
    }
    a[0][5]=1;
    for(i=2;i<6;i++)
    {
        for(j=7-i;j<=i+3;j+=2)     
        {
            a[i][j]=a[i-1][j-1]+a[i-1][j+1];
        }
    }
    for(i=0;i<6;i++)
    {
        for(j=0;j<11;j++)
        {
            if(a[i][j]==0)
            {
                printf(" ");     
            }
            else
            {
            printf("%d",a[i][j]);
            }
        }
        printf("\n");
    }

  return 0;
}

###回形阵
#include <iostream>

using namespace std;

int main()
{
    int n,i,j,k,t;
    cin>>n;
    int a[n][n]={};
    if(n%2==0)
    {
        t=n/2;
    }
    else
    {
        t=n/2+1;
    }
    for(k=1;k<=t;k++)
    {

        for(i=0;i<n;i++)
        {
            for(j=0;j<n;j++)
            {
                if(i==k-1||i==n-k||j==k-1||j==n-k)
                {
                     if(a[i][j]==0)
                     {
                         a[i][j]=k;
                     }
                }

            }
        }
     }

    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)
        {
            cout<<a[i][j];
        }
        cout<<endl;
    }
    return 0;
}
###
**********************************************************************************************
