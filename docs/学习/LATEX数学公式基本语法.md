### 1. 使用LaTex

有两种方式插入公式:

对于行内公式来说，使用`$你的公式$`:

```latex
$a + b = c$
```

$a + b = c$

独立的公式就是`$$你的公式$$`:

```latex
$$ a + b = c $$
```

$$ a + b = c $$

### 2. 上下标

`^`表示上标，`_`表示下标，正下方的用`\mathop{主体}\limits_下标`，正上方同理.

上下标的内容太多的话，使用`{}`包起来.上下标可以互相嵌套.

```latex
a{b^c}=(1+a^b)^{-2ac^b}
```

$$
a{b^c}=(1+a^b)^{-2ac^b}
$$

```latex
{}^1_2\mathop{0}\limits_3^6{}^5_4
```

$$ {}^1_2\mathop{0}\limits_3^6{}^5_4 $$

### 3. 分数(fraction)

```latex
\frac{2}{7}
```

$$
\frac{2}{7}
$$

```latex
\frac{\rm {d} u}{\rm {d} x}|_{x=0}
```

$$
\frac{\rm {d} u}{\rm {d} x}|_{x=0}
$$

### 4. 括号与分隔符

为了表示整体的时候请用`{}`
`()`，`[]`，`|`.

要表示`{}`需要`\{\}`转义.

显示特大的括号时候需要使用`\left`和`\right`.

```latex
\{c+\left(\frac{(a+b)}}{[a+c]}\right)_{c=0}\}+d
```

$$
\{c+\left(\frac{a+b}{a+c}\right)_{c=0}\}+d
$$

### 5. 乘除

加减直接用就行，乘法用`\times`，除法用`\div`

```latex
(x+y\times x^2)\div3
```

$$
(x+y \times x^2) \div 3
$$

### 6. 开方

```latex
\sqrt{3}，\sqrt[n]{3}
```

$$ \sqrt{3}，\sqrt[n]{3} $$

### 7. 函数

直接用`f()`就好了

```latex
f(x+y^2)=(x^3+y)^{y^2}
```

$$
f(x+y^2)=(x^3+y)^{y^2}
$$

### 8. 矢量

$\cdot$ 使用 `\cdot` 表示，矢量用 `\vec`

```latex
\vec{x}\cdot\vec{y}
```

$$
\vec{x}\cdot\vec{y}
$$

### 9. 微积分

一重积分用 `\int`，二重 `\iint`，依此类推…

曲线积分用 `\oint`，完了曲面积分 `\oiint`

微分用 `\rm {d}`

导数 `'` 就代表自己

``` latex
\int_{\alpha(x)}^{\beta(x)}\frac{\partial{f(x，y)}}{\partial x}\rm dy +\beta'(x)
```

$$
\int_{\alpha(x)}^{\beta(x)}\frac{\partial{f(x，y)}}{\partial x}\rm dy +\beta'(x)
$$

```latex
格林公式
\mathop{\iint}\limits_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y} \right )dxdy=\oint _LPdx+Qdy
```

$$
\mathop{\iint}\limits_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y} \right )dxdy=\oint _LPdx+Qdy
$$

### 10. 极限

极限用 `\lim{}`

箭头用 `\rightarrow`

无限用 `\infty`

```latex
\mathop{\lim}\limits_{n \rightarrow +\infty} \frac{1}{n(n+1)}
```

$$
\mathop{\lim}\limits_{n \rightarrow +\infty} \frac{1}{n(n+1)}
$$

### 11. 累加，累乘

```latex
\mathop{\sum}\limits_{i=0}\limits^n \frac{1}{i^2}

\mathop{\prod}\limits_{i=0}\limits^n \frac{1}{i^2}
```

$$\mathop{\sum} \limits_{i=0}\limits^n \frac{1}{i^2}$$

$$\mathop{\prod}\limits_{i=0}\limits^n \frac{1}{i^2}$$

### 12. 矩阵

矩阵标准形式是

```latex
\begin{matrix}
   1 & 2 & 3 \\\\
   4 & 5 & 6 \\\\
   7 & 8 & 9 \\\\
\end{matrix}
```

$$
\begin{matrix}
   1   &   2    &   3 \\\\
   4   &   5    &   6 \\\\
   7   &   8    &   9 \\\\
\end{matrix}
$$

`&` 代表空格，`\\` 表示换行，不知道怎么回事要使用 `\\\\` 才行。

我们看到上面的矩阵是不带括号的，要加括号可以使用 `\left{` 或者 `\left[` ，啥样的随你挑，右边同理.

还有一种方法是替换 `martix` 了，`bmartix` 表示带 `[` 的， `Bmartix` 表示 `{` ， `pmartix` 表示 `(`，`vmartix` 表示 `|`...

```latex
\begin{Bmatrix}
3 & 4  \\\\
7 & 5
\end{Bmatrix}+
\begin{vmatrix}
3 & 4  \\\\
7 & 5
\end{vmatrix}=
\left(
\begin{matrix}
6 & 8  \\\\
14 & 10
\end{matrix}
\right)
```

$$
\begin{Bmatrix}
3 & 4  \\\\
7 & 5
\end{Bmatrix}+
\begin{vmatrix}
3 & 4  \\\\
7 & 5
\end{vmatrix}=
\left(
\begin{matrix}
6 & 8  \\\\
14 & 10
\end{matrix}
\right)
$$

麻烦的很，如果只是两行一列的可以用简单的 `\binom{x=1}{y=2}`

$$
\binom{x=1}{y=2}
$$

之前那些矩阵输出自动成行，这儿输出的自动行内样式，怎么变大不用我说了吧.

带省略符号的矩阵 `...` 用 `\cdots`，竖着的用 `\vdots`，斜着的用 `\ddots`

```latex
\left[
\begin{matrix}
 1      & 2      & \cdots & 4      \\\\
 7      & 6      & \cdots & 5      \\\\
 \vdots & \vdots & \ddots & \vdots \\\\
 8      & 9      & \cdots & 0      \\\\
\end{matrix}
\right]
```

$$
\left[
\begin{matrix}
 1      & 2      & \cdots & 4      \\\\
 7      & 6      & \cdots & 5      \\\\
 \vdots & \vdots & \ddots & \vdots \\\\
 8      & 9      & \cdots & 0      \\\\
\end{matrix}
\right]
$$

有特殊需求的可以用 array，然后用 c，l，r控制样式，分别表示居中对齐，左对齐，右对齐.比如增广矩阵:

```latex
 \left[
  \begin{array}{cc|c}
    1 & 2 & 3 \\\\
    4 & 5 & 6
  \end{array}
\right]
```

$$
\left[
  \begin{array}{cc|c}
    1 & 2 & 3 \\\\
    4 & 5 & 6
  \end{array}
\right]
$$

### 13. 方程组

和矩阵差不多的，左边有括号想用啥用啥，右边没括号用 `\right`

```latex
\left\\{
\begin{array}{ccc}
x^2 + y^2 &=& z^2 \\\\
x^3 + y^3 &<& z^3
\end{array}
\right.
```

$$
\left\\{
\begin{array}{ccc}
x^2 + y^2 &=& z^2 \\\\
x^3 + y^3 &<& z^3
\end{array}
\right.
$$

当然还有些更简单的方案

```latex
\begin{cases}
x^2+y^2=z^2，x=1\\\\
z^2+y^2=x^3，y=2
\end{cases}
```

$$
\begin{cases}
x^2+y^2=z^2，x=1\\\\
z^2+y^2=x^3，y=2
\end{cases}
$$

### 14. 希腊字母

数学公式里一堆堆的希腊字母，来一个个说吧.

|  符号  |  表示方法 |    符号     |  表示方法 |
| --------- | -------- | --------- | ----------- |
|  $\alpha$   | \alpha      |  $\beta$       | \beta       |
| $\gamma$      | \gamma      |$\Gamma$      | \Gamma      |
| $\delta$      | \delta      | $\Delta$      | \Delta      |
| $\epsilon$    | \epsilon    | $\varepsilon$ | \varepsilon |
| $\zeta$       | \zeta       | $\eta$        | \eta        |
| $\theta$      | \theta      | $\Theta$      | \Theta      |
| $\vartheta$   | \vartheta   |  $\iota$       | \iota       |
| $\kappa$      | \kappa      | $\lambda$     | \lambda     |
| $\mu$         | \mu         |  $\nu$         | \nu         |
| $\xi$         | \xi         |  $\Xi$         | \Xi         |
| $\pi$         | \pi         | $\Pi$         | \Pi         |
| $\varpi$      | \varpi      |  $\rho$        | \rho        |
| $\varrho$     | \varrho     | $\varsigma$   | \varsigma   |
| $\Sigma$      | \Sigma      | $\sigma$      | \sigma      |
| $\tau$        | \tau        | $\phi$        | \Phi        |
| $\upsilon$    | \upsilon    | $\Upsilon$    | \Upsilon    |
| $\varphi$     | \varphi     | $\chi$        | \chi        |
| $\psi$        | \psi        | $\Psi$        | \Psi        |
| $\omega$      | \omega      | $\Omega$      | \Omega      |

### 15. 其他数学符号

#### 关系运算符

| 符号         | 表示方法   | 符号         | 表示方法   |
|:-------------|:-----------| :-------------|:-----------|
| $\pm$        | \pm        | $\times$     | \times     |
| $\div$       | \div       | $\mid$       | \mid       |
| $\circ$      | \circ      | $\ast$       | \ast       |
| $\bigodot$   | \bigodot   | $\bigotimes$ | \bigotimes |
| $\bigoplus$  | \bigoplus  |
| $\leq$       | \leq       | $\geq$       | \geq       |
| $\neq$       | \neq       | $\approx$    | \approx    |
| $\equiv$     | \equiv     |
| $\sum$       | \sum       | $\prod$      | \prod      |
| $\coprod$    | \coprod    |

#### 集合运算符

| 符号       | 表示方法 | 符号       | 表示方法 |
|:-----------|:---------|:-----------|:---------|
| $\bot$     | \bot     | $\angle$   | \angle   |
| $30^\circ$ | 30^\circ |
| $\sin$     | \sin     | $\cos$     | \cos     |
| $\tan$     | \tan     |
| $\cot$     | \cot     | $\sec$     | \sec     |
| $\csc$     | \csc     |

#### 微积分运算符

| 符号      | 表示方法 | 符号      | 表示方法 |
|:----------|:---------| :----------|:---------|
| $\prime$  | \prime   | $\int$    | \int     |
| $\iint$   | \iint    | $\iiint$  | \iiint   |
| $\iiiint$ | \iiiint  | $\rm {d}$ | \rm {d}  |
| $\oint$   | \oint    | $\lim$    | \lim     |
| $\infty$  | \infty   |

#### 逻辑运算符

| 符号          | 表示方法    | 符号          | 表示方法    |
|:--------------|:------------|:--------------|:------------|
| $\because$    | \because    | $\therefore$  | \therefore  |
| $\forall$     | \forall     | $\exists$     | \exists     |
| $\not=$       | \not=       | $\not>$       | \not>       |
| $\not\subset$ | \not\subset |

#### 戴帽符号

| 符号        | 表示方法  |
|:------------|:----------|
| $\hat{y}$   | \hat{y}   |
| $\check{y}$ | \check{y} |
| $\breve{y}$ | \breve{y} |

#### 连线符号

| 符号                                                | 表示方法                                     |
|:----------------------------------------------------|:---------------------------------------------|
| $\overline{a+b+c+d}$                                | \overline{a+b+c+d}                           |
| $\underline{a+b+c+d}$                               | \underline{a+b+c+d}                          |
| $\overbrace{a + \underbrace{b + c}_{1.0}+ d}^{2.0}$ | \overbrace{a+\underbrace{b+c}_{1.0}+d}^{2.0} |

### 16. 转义等问题

在markdown中`_word_`表示斜体，于是在LaTex中，要使用`\_`

输入矩阵时候`\\`用写成`\\\`

输出字符:{，}，_时候要用`\\{`，`\\}`，`\_`

要输出字符`空格`，`#`，`$`，`%`，`&`用命令:`\空格`， `\#`， `\$`，`\%`，`\&`.

### 17. 标注

转载自：http://fredalxin.github.io/2016/02/24/MathJax/
