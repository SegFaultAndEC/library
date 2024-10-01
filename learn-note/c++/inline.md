---
tags:
  - cpp
---
## 内联
inline的功能之一，但通常编译器会自动内联，不适合内联的时候即使有inline编译器也不会内联，因此不需要为了内联而使用inline关键字。
## 防止重复
### 修饰函数
先看示例：
```c++
//foo.h
int foo(int a){
	return a*a;
}

//func1.h
#include "foo.h"
int func1(){
	return foo(1);
}

//func2.h
#include "foo.h"
int func2(){
	return foo(2);
}

//main.cc
#include "func1.h"
#include "func2.h"
int main(){
	return func1()+func2;
}
```
此时程序会报重定义的错误，因为inline只是简单的替换。但当我们在foo前加上inline后编译器就会自动选择一个（若体积相同则随机选不同则选体积大的）函数来运行。
### 修饰变量
通常用于修饰类静态变量
```cpp
//foo.h
struct Foo{
	static int foo=1;
}
```
这种情况下被引用容易报错，同样是因为include的简单粗暴的替换，而加上inline后则可以避免这个问题。
### 修饰命名空间
不做介绍。