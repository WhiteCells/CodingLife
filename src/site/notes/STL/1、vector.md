---
{"dg-publish":true,"permalink":"/stl/1-vector/"}
---

[[CodeGarden\|Go Home]]
[[STL/Standard Template Library\|Back STL]]

vector 是C++标准模板库中的==类==
这个类提供了很多的端口
使用之前需要添加**头文件** `#include <vector>`
我们可以理解 vector 为一个数组，但他是动态扩展的，不同于[[C语言/C\|C语言]]中的静态数组
他这个动态拓展不是在旧空间上接新空间，而是在创建一个更大的空间将就旧空间拷贝到新空间，然后*释放*旧空间。





