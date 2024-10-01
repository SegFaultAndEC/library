---
tags:
  - cpp
  - 现代cpp
---
```cpp
#include <iostream>
struct Foo{
	int v;
	Foo()=default;
	int func(this Foo& self){
		return 1;
	}
	int func(this Foo&& self){
		return 2;
	}
	int func(this const Foo& self){
		return 3
	}
};
int main(){
	Foo f{};
	const Foo f2{};
	std::cout<<f.func()<<std::endl;
	std::cout<<Foo().func()<<std::endl;
	std::cout<<f2.func()<<std::endl;
	return 0;
}
```