## Welcome to GitHub Pages



### Markdown



```markdown

###杨辉三角
#include <stdio.h>
int main()
{
    int a[6][11];           //定义数组，注意要有输出空格的地方
    int i,j;
    for(i=0;i<6;i++)
    {
        for(j=0;j<11;j++)
        {
            a[i][j]=0;       //将所有数组值赋值为零（待会先赋值，值为零的地方说明没赋值，就输出空格）
        }
    }
    for(i=0;i<6;i++)
    {
                j=5-i;         //先将两侧的赋值1
            a[i][j]=1;
            a[i][10-j]=1;
    }
    a[0][5]=1;
    for(i=2;i<6;i++)
    {
        for(j=7-i;j<=i+3;j+=2)     //每一项为上面两项之和
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
                printf(" ");      //输出，因为值为零的地方没有赋值，这里不能输出东西，所以输出空格
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

[Link](url) and ![Image](url=https://ss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=3855262064,1896479038&fm=26&gp=0.jpg)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Theme

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Cyuanshuo/Cyuanshuo.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
