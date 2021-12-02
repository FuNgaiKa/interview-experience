2021.12.2 16：00 50min



题目：

- 字符串的压缩

- 利用字符重复出现的次数，编写一种方法，实现基本的字符串压缩功能。比如，字符串aabcccccaaa会变为a2b1c5a3。

  若“压缩”后的字符串没有变短，则返回原先的字符串。你可以假设字符串中只包含大小写英文字母（a至z）。

  ```cpp
  class Solution {
  public:
      string compressString(string S) {
  
      }
  };
  ```

- 

```c++
\#include <iostream>

\#include<cstring>

\#include<algorithm>

using namespace std;

int main() {

    string a;

    cin>>a;

    string ans;

    int i=0,j=0;

    int len=a.size();

    while(j<len){

            while(a[i]==a[j]){

                  j++;

                }

            ans+=a[i];

            int cnt=j-i;

            if(cnt<10)

            ans+=j-i+'0';



            else{

                  string num;

                  while(cnt){

                        int tmp=cnt%10;

                        num+=tmp+'0';

                        cnt/=10;

                      }

                  reverse(num.begin(),num.end());

                  ans+=num;

                }

            i=j;

    }

    if(ans.size()<a.size()){

            cout<<ans<<endl;

    }

    else{

            cout<<a<<endl;

    }

    //int a;

    //cin >> a;

    // cout << << endl;

}
```



说大于10的时候有bug。

改了一下，面试官：有api可以用。atoi()。



有了解什么开源组件吗？

有了解什么框架吗？



你的线程池项目讲讲？

你的锁是怎么实现的呢？

我：我忘了那个api了。



项目是等于模拟打开网页的过程？不会涉及到html、css这些吗？

针对打开网页的过程，我说了http等。

面试官：这是底层的知识。



问项目：实习项目，线程池。

有用到trpc吗？有学到什么呢？



面试官介绍了他的部门：财付通，做点公司炒股的业务。

技术栈：c++。准备转go。



协程的理解。



反问：

掏心窝子说，现在不是秋招密集期，基础下降了。请问面试官看重哪一个点？

面试官：不同部门不一样，大家业务和侧重点都不一样blabla。

很大程度上也是运气吧。看岗位是否和候选人匹配。



贵部门更看重候选人哪一点？

做业务的，没那么底层。看重基础和知识的拓展面。

算法，基础，项目吃透。



