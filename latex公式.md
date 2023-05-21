### 规范
- latex公式中，关键字内如果有超过一个字符时应用“{}”括起。
- 数学公式中只有变量和函数单字符的名称（例如$f(x)$）需要使用斜体，其余情况字符均应使用罗马体（直立体）。
	- 将字符转为罗马体的方式：
		1. \rm+字符：$x_{\rm i}$
		2. \text+字符：$x_{\text i}$
	- 两种方式的区别
		1. \rm后的内容不支持显示空格，且若不加“{}”其会将后面所跟的所有字符全部转为罗马体。
		 $$
		 x_{\rm i j} \\
		 x_{\rm {i j}}
	$$
		3. \text后“{}”内的所有内容支持显示一个空格，且若不加“{}”其只将后面所跟的第一个字符转为罗马体。
		$$
		x_{\text i j} \\
		x_{\text {i   j}}
		$$
- 在公式内部如果需要换红使用“\\”，案例参考上述公式。
- 在一些数学符号中如果限制条件显示在右下角，可以使用\limits_来强制显示在符号下方。
$$
\lim\limits_{x\to0}
$$
### 希腊字母
反斜杠加字母名称。
$$
\alpha,\beta,\lambda,\cdots
$$
完整字母表如下：
![希腊字母表](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9waWMxLnpoaW1nLmNvbS92Mi1kYTNlNzE3Y2Y2NzA1ODJmYmZiZGRkZWUzMzA3MzUyNF9yLmpwZw?x-oss-process=image/format,png)
### 上下标
- 上标：$x^2$
- 下标：$x_1$
### 分式和根式
- 分式
	$$\frac ab \quad \frac{\frac{1}{a+b}+1}{y+1}$$
	如果嵌套分式中的子分式过小可以使用\dfrac变大。
	$$\frac{\dfrac{1}{a+b}+1}{y+1}$$
- 根式
	$$\sqrt{x+y}$$
	如果有次数限定则添加[]。
	$$\sqrt[3] x$$
### 数学符号
#### 普通运算符
- 一般运算符直接输入。
$$+-*/$$
- 特殊运算符使用反斜杠加符号名称。
 $$
 \times\,
 \div\,
 \cdot\,
 $$
#### 数集
- \mathbb加字符：$\mathbb R$
- 反斜杠加字符：$\Z_+$
注意：只有有意义的数集字符才能被显示。
#### 花体字符
- $\mathcal F$
- $\mathscr F$
#### 省略号
- 横向：$\cdots$
- 纵向：$\vdots$
- 斜向：$\ddots$
#### 大型运算符
- 二重积分：$\iint$
- 三重积分：$\iiint$

注：大型运算符号的限定条件遵从上下标的表示方式。
#### 标注符号
- $\bar x$
- $\vec x$
- $\overrightarrow{AB}$ 
#### 其他符号
- 无穷：$\infty$
- 微分：$\partial$
- 三角函数：
	- $\sin x$
	- $\cos x$
	- $\sec x$
	- $\csc x$
	...
- 极限：$\lim\limits_{x\to0}$
#### [详细符号](https://blog.csdn.net/Changxing_J/article/details/115265901?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167585164316800211521602%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=167585164316800211521602&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v31_ecpm-2-115265901-null-null.142^v73^insert_down3,201^v4^add_ask,239^v1^control&utm_term=latex%E6%A0%87%E6%B3%A8%E7%AC%A6%E5%8F%B7&spm=1018.2226.3001.4187)
### 行间公式
#### 多行公式
- 公式环境
$$
\begin{align}
f(x)=a+b+c \\
g(x)=x+y
 \end{align}
 $$
- 对齐控制
使用“&”进行控制对齐位置。
$$
\begin{align}
 f(x)&=a+b+c\\
	 &=d+f
 \end{align}
$$
#### 多行大括号
$$
f(x)=
\begin{cases}
\sin x\ &-\pi\le x\le \pi\\
0&其他
\end{cases}
$$
#### 矩阵
- 省略矩阵
$$
\begin{matrix}
a & b & \cdots & c \\
\vdots & \vdots & \ddots & \vdots \\
e & f & \cdots & g
\end{matrix}
$$
- 方括号矩阵
$$
\begin{bmatrix}
a & b & \cdots & c \\
\vdots & \vdots & \ddots & \vdots \\
e & f & \cdots & g
\end{bmatrix}
$$
- 圆括号矩阵
$$
\begin{pmatrix}
a & b & \cdots & c \\
\vdots & \vdots & \ddots & \vdots \\
e & f & \cdots & g
\end{pmatrix}
$$
- 行列式
$$
\begin{vmatrix}
a & b & \cdots & c \\
\vdots & \vdots & \ddots & \vdots \\
e & f & \cdots & g
\end{vmatrix}
$$
- 矩阵表示
矩阵字母一般用加粗罗马体表示：
$$
\bf A=
\begin{bmatrix}
a & b & \cdots & c \\
\vdots & \vdots & \ddots & \vdots \\
e & f & \cdots & g
\end{bmatrix}
$$
转置符号应用罗马体表示：$\bf B^{\rm T}$

### 空格
latex公式中不显示空格，空格应用特定语法表示，不同的表示方法产生的空格不同：
$$
a b\\
a\,b\\
a\ b\\
a\quad b
$$ 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1OTg0NDE5NDJdfQ==
-->