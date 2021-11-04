### OpenGL

[GLSL中文手册](https://blog.csdn.net/xhm01291212/article/details/79270836)
注：该文档部分api在有些版本不兼容

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

### [HOME](https://daixuenan.github.io/)