# Cyuanshuo.github.io
## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/Cyuanshuo/Cyuanshuo.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

### 回形阵
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
- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Cyuanshuo/Cyuanshuo.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
