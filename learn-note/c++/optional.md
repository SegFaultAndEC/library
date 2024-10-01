---
tags:
  - cpp
  - 标准库
---
如下：
```cpp
#include <iostream>
#include <optional>
void print(std::optional<int> a){
	if(a)
		std::cout<<*a;
}

int main(){
	std::optional<int> a;
	a=20;
	print(a);
	a=nullopt;
	print(a);
}
```