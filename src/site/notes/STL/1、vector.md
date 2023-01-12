---
{"dg-publish":true,"permalink":"/STL/1、vector/"}
---

[[CodeGarden\|Go Home]]
[[STL/Standard Template Library\|Back STL]]
## vector 简介
vector 是C++标准模板库中的==类==
这个类提供了很多的端口
使用之前需要添加**头文件** `#include <vector>`
我们可以将 vector 理解为一个[[DataStructure/1、数组（array)\|数组]]，但他是动态扩展的，不同于[[C语言/C\|C语言]]中的静态数组
动态拓展不是在旧空间上接新空间，而是创建一个更大的空间将就旧空间数据拷贝到新空间，然后*释放*旧空间
vector 容器的迭代器是支持随机访问的，就好比数组通过下标随机访问
先了解一下 vector 的构造函数种类
~~~C++
// 默认构造函数
vector<T> v;

vector(n, elem); // 构造函数将 n 个 elem 拷贝给本身

vector(v.begin(), v.end()); // 将v[begin(), end()) 拷贝给自身
 
vector(const vector& vec); // 拷贝构造函数
~~~
使用方法比较简单
~~~C++
#include <iostream>
#include <vector>

void PrintVector(const std::vector<int>& v) {
    for (std::vector<int>::const_iterator it = v.begin(); it != v.end(); it++) {
        std::cout << *it;
    }
    std::cout << std::endl;
}

int main() {
    std::vector<int> iv1(10, 1);
    std::vector<int> iv2(iv1.begin(), iv1.end());
    std::vector<int> iv3(iv2);
    PrintVector(iv1); // 10 个 1
    PrintVector(iv2); // 10 个 1
    PrintVector(iv3); // 10 个 1
    system("pause");
    return 0;
}
~~~

运行结果：
~~~text
1111111111
1111111111
1111111111
请按任意键继续. . .
~~~

上面的代码中 PrintVector 函数中的*迭代器*现在还没有提到
## vector 赋值操作


