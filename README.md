## Hello World!

### Markdown

```markdown
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

