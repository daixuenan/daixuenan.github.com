### OpenGL

[GLSL中文手册](https://blog.csdn.net/xhm01291212/article/details/79270836)
注：该文档部分api在有些版本不兼容

1、[简介](https://daixuenan.github.io/opengl/introduce)
2、[3D](https://daixuenan.github.io/opengl/3d)

### 未整理的笔记

tips:颜色混合算法
```markdown
gl_FragColor.xyz = color.rgb * color.a + colorBg.rgb * colorBg.a * (1.0 - color.a);
gl_FragColor.a = color.a;
```

tips:顶点着色器 片元着色器 int类型精度不匹配

tips:ortho只做正视投影，无法做相机视角，需要perspective透视投影矩阵

tips:振幅运动
A是振幅 w是角频率 &是初相位 t是时间
参考 https://wenku.baidu.com/view/b58f328f6e1aff00bed5b9f3f90f76c661374ca0.html
```markdown
w=PI/2
x=Asin(wt+&)
```

tips:电击效果
```markdown
gl_FragColor = vec4(1.0-color.rgb, color.w);
```

tips:纹理A外接纹理B旋转缩放保持外接方案
先计算纹理A外接四边形宽高，再计算宽高比，取较大值做缩放

tips:深度检测触发后，纹理将被视为物体，而非颜色。因此即使被透明部分覆盖的内容，也展示不出来，而是显示的黑色。
这个场景可以利用discard方法 放弃当前透明部分纹理绘制，而是让给后面的纹理绘制。(而对于半透明的颜色不太好处理)
[参考](https://learnopengl.com/Advanced-OpenGL/Blending)

### [HOME](https://daixuenan.github.io/)