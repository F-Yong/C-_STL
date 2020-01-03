<font size = 6 color = red>String</font>

---
# 声明
```
string s;   //声明一个string 对象  
string ss[10];  //声明一个string对象的数组
```

# 初始化

使用等号的初始化叫做拷贝初始化，不使用等号的初始化叫做直接初始化。
```
#include <bits/stdc++.h>
using namespace std;

int main()
{
    ios::sync_with_stdio(false);
    string s;//默认初始化，一个空字符串
    string s1("ssss");//s1是字面值“ssss”的副本
    string s2(s1);//s2是s1的副本
    string s3=s2;//s3是s2的副本
    string s4(10,'c');//把s4初始化
    string s5="hiya";//拷贝初始化
    string s6=string(10,'c');//拷贝初始化，生成一个初始化好的对象，拷贝给s6

    //string s(cp,n)
    char cs[]="12345";
    string s7(cs,3);//复制字符串cs的前3个字符到s当中

    //string s(s2,pos2)
    string s8="asac";
    string s9(s8,2);//从s2的第二个字符开始拷贝，不能超过s2的size

    //string s(s2,pos2,len2)
    string s10="qweqweqweq";
    string s11(s10,3,4);//s4是s3从下标3开始4个字符的拷贝，超过s3.size出现未定义
    return 0;
}
```


