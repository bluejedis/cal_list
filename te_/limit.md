# <span style="color:lightgray">before

# F

## concept
- 海涅定理
    - >f(x)在$\mathring U(x_0,\delta)$内有定义
        - $lim_{x→x_0}f(x)=A$存在$\Leftrightarrow$
        - 在$∀$ $\mathring U$内 以$\bf x_0$为极限的数列$\{\bf{x_n}\}$
            - $lim_{\bf n→\infty}f(x_n)=A$存在
    - --
    - eg.证 $lim_{x \to 0}\frac{1}{x}sin\frac{1}{x}$不存在
        - >key:取$n → ∞$，$x→0$，x取不同的n的表达式
            - $x_n=\frac{1}{n\pi}$
                - $lim_{n→∞}f(x_n)=0*0=0$
            - $x_n=\frac{1}{(2n+\frac{1}{2})\pi}$
                - $lim_{n→∞}f(x_n)=lim_{n→∞}(2n+\frac{1}{2})\pi=∞$
- 无穷小
    - >函数值为0 ($x→x_0$or$x→∞$时
        - 无穷大同理
- 连续
    - 极限值=函数值
        
## count

### 性质
- 存在←→ 左右极限相等
    - ？$e^\frac{1}{x}$分式部分的值是怎么求出来的

- 有界$\Leftrightarrow$
    - 在[a,b]上连续，则在[a,b]上有界
### 7未定式

#### $\frac{0}{0}$ $\frac{\infty}{\infty}$ $0 \cdot \infty$

#### $\infty - \infty$

#### $\infty^0$ $0^0$ $1^\infty$

#### 已知一个lim 求另一个式子

## 无穷小比阶
>本质还是算lim

## 连续&间断

---
---
# S
## concept
- 定义
    - >∀$\epsilon＞0$，∃$N\in N_+$, 当$n＞N$时，恒有$x_n-a＜\epsilon$← a是 数列$\{x_n\}$的极限or $\{x_n\}$收敛于a
        - 记为：$\{x_n→a\}$($n→\infty$ or $lim_{n→∞}x_n=a$
- 性质
- 单调有界
## te
### use定义证lim
- 与1作差 ＜$\epsilon$
    - ？为什么这里要取整数部分，再+1
    - ![Screenshot_2025-09-17-21-13-42-261_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-17-21-13-42-261_com.microsoft.emmx.canary-edit.6bhflvvegf.jpg)