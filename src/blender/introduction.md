# 关于本文 {#introduction}

本文是Blender源码阅读笔记，主要是为了加深对OpenGL的理解，同时也为了方便以后查阅。

结合blender节点着色器代码和蓝图，在EEVEE渲染器中，可以看到节点的实现方式，这样可以更好的理解节点的实现方式。

将blender的着色器代码在Cocos中实现，可以更好的理解Cocos的渲染管线。

## 本文的目的 {#purpose}
在cocos中实现 吉普力风格材质
![动物毛发&人物皮肤](/public/images/image.png)
![硬表面&透明材质&布料材质](/public/images/image-1.png)
![丝袜材质](/public/images/image-2.png)

## 案例地址 {#casus}
[cocos-blender-shader](https://github.com/s4hyhzi/cocos-blender-shader)