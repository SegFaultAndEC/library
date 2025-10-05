## 概念
着色器是一个脚本，它应用材质中包含的属性，以将 3D 对象的网格渲染到屏幕上的 2D 图像。
## 分类
### 顶点着色器
对网格的顶点进行作，通常会更改其位置以使表面移动或变换。
### 片元着色器
也称为像素着色，是表示网格表面以产生 2D 图像中每个像素的颜色的着色。
## Physically based shaders and rendering(PBR)
使用 PBR 时，光源和表面的属性保持独立。光源根据其亮度、颜色和范围进行定义。使用材质根据颜色、反射率和其他影响光线在其上行为方式的真实属性来定义表面。
使用非基于物理的渲染 ， 渲染的颜色、阴影和反射要么在没有 PBR 的情况下近似，要么只是不渲染。使用非 PBR 着色器时，红色材质可能会渲染为纯红色或具有简单的反射和阴影。非 PBR 通常看起来不像 PBR 那样逼真，但它可能更适合风格化效果。卡通着色器使 3D 场景中的表面看起来像 2D 卡通，是一种非 PBR 着色器。
## Lit and Unlit
Lit shaders respond to the light in the scene, and unlit shaders don’t. Unlit shaders are useful for certain artistic effects or for optimised projects that run more efficiently by not using lighting.