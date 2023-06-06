# DinoFEM2D


# 0、安装与库说明

```plain
库说明
在终端安装 numpy\pyvista\rich三个库，即可。
可以使用如下命令整体安装。
pip install -r .\requirements.txt -i  https://pypi.tuna.tsinghua.edu.cn/simple

也可以如下单独安装：
pip install numpy --trusted-host  https://pypi.tuna.tsinghua.edu.cn/simple
pip install pyvista -i  https://pypi.tuna.tsinghua.edu.cn/simple
pip install rich -i  https://pypi.tuna.tsinghua.edu.cn/simple
```

# 一、边界类型及定义规则

```plain
边界名称，对应 边界类型
对所有边界形成的字典.
在边界处理的时候，根据BN边界的index，通过boundaries_name找到边界名称，
再通过边界名称在这个字典中查找边界类型
```
DinoFem 的边界设定，以字典形式来完成。
边界名称 对应的边界的类型及函数信息。

这个信息存储在Mesh2D类的boundary_type_dict,和boundary_value_dict两个字典中。

边界类型以BoundaryType定义

```plain
class BoundaryType(Enum):
    Dirichlet = -1
    ZeroGradient = -2
    NonZeroGradient = -3
```
字典设定规则如下
|边界类型|数学表达|标记|值|
|:----|:----|:----|:----|
|Dirichlet|T=g|Dirichlet|g函数类型|
|齐次Neumann|Grad T = 0|ZeroGradient|None|
|非齐次Neumann|Grad T = phi|NonZeroGradient|phi函数类型|

# 二、求解器使用案例

## 1、泊松方程求解
## 2、抛物方程求解
## 3、线弹性方程求解
## 4、Stokes方程求解
## 5、稳态NS方程求解
## 6、瞬态NS方程求解

详细说明见文件文档


