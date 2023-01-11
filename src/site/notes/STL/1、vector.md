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
~~~C++
// 采用模板实现类实现，默认构造函数
vector<T> v;
 
// 将 v[begin(), end()) 区间中的元素拷贝给本身
vector(<v.begin(), v.end()>);
 
//构造函数将 n 个 elem 拷贝给本身
vector(n, elem);
 
// 拷贝构造函数
vector(const vector& vec);
~~~





