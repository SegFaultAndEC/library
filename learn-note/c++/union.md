---
tags:
  - cpp
---
如下：
```cpp
struct vector2 {
  int x, y;
  vector2(int x,int y):x(x),y(y){}
};

struct vector4 {
  union {
    struct {
      int x, y, z, w;
    };
    struct {
      vector2 a, b;
    };
  };
};
int main(){
    vector4 v1;
    vector4 v2;
    v1.x=1;
    v1.y=2;
    v1.z=3;
    v1.w=4;
    v2.a=vector2(1,2);
    v2.b=vector2(3,4);
}
```
到最后v1与v2是相同的