# concept

##  不定&定 
- 性质(related 证明
    - >奇偶 有界 单调 周期
    - 奇偶
        - 
    - T
    - 有界

## 变限
- >存在,则必连续
- 求导
    - $\frac{d}{dx}[\int_{\psi_1{x}}^{\psi_2{x}}f(t)dt]$
        - $f({\psi_2(x)})({\psi_2(x)})'-f({\psi_1(x)})({\psi_1(x)})'$
            - eg求导那步怎么得出来的？ 和移出的积分没有关系啊？
                - ![Screenshot_2025-09-16-09-22-28-242_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-16-09-22-28-242_com.microsoft.emmx.canary-edit.3uv74tu3f8.jpg)
                - f(t)部分含有变量x，need移出，才能用公式


- 证明：
    - 
## 反常
- >由S=h*l(l→∞)存在(0*∞时)
    - 推出收敛条件：
        - $lim_{x→\infty}f(x)=0$
        - h(即f(x))越小，越易收敛
- 收敛性
    - >均$lim_{△→∞}$ ← 无穷区间上的反常积分
        - ↑上下限自身
    - >$lim_{\varepsilon→0^{+/-}}$ ← 无界函数
        - ↑$b/a - \varepsilon$
        -?<span style="color:lightgray"> 这两个概念有什么区别</span>
            - 无穷区间上的..，是区间内有点取∞
            - 无界函数.., f(x)值在有限domain上，有瑕点
                - 瑕点
                    - >令函数极限值=∞的点
    - ？如何理解"反常积分是变限积分的极限"这句话
         - 无界函数的情况 不是 不符合吗
         - ![Screenshot_2025-09-16-17-32-39-277_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-16-17-32-39-277_com.microsoft.emmx.canary-edit.wix1t42xw.jpg)


---
# count
## 不定 //回来再sum一下,形如xx 的通式通法
- base公式(10g
- 3method
    - 凑微分
        - >从原式中拆一部分,构造$g'(x)dx=d(g(x))$
        - usually 一个$\frac{1}{\sqrt ..}$ 拆为2个乘积, 再构造
    ---
    - 换元
        - >原式含$\sqrt a^2 ± x^2$
            - different 情况, choose different表达式
        - 三角代换
            - x=asint/atant/asect
                - $\sqrt a^2-x^2$ ← 令$x=asint$
                - $\frac{1}{\sqrt a^2+x^2}$ ←..$x=atant$
                    - >$tant'=\boxed sec^2t$
                        - $tant=\frac{x}{a}$ 
                            - 平方,再utilize $sin^2=1-cos^2$
                    - > $\int sect dt=ln |sect+tant| +C$
                        - $-lna+C$ ==均常==→C
                - $\frac{1}{\sqrt x^2-a^2}$←..$x=asect$
                    - >$(sect)'=sect tant$
                    -?为什么这里分了x的正负讨论
                        - 之前的却没有；为什么x的正负会影响表达式？
                        - ![Screenshot_2025-09-16-11-15-58-492_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-16-11-15-58-492_com.microsoft.emmx.canary-edit.4n82mocrnf.jpg)
    ---
    - 分部积分
        - >含$ln$ $e^x$的乘法形式等
        - $\int udv=uv - \int vdu$
            - <span style="color:lightgray">↑推导：对乘法求导 取积分</span>
            - >求$\int udv$难，但交换后的$\int vdu$易
        - type:
            - 对于$P_n{x}*e^{kx}/sinax/cosbx$ ($P_n(x)$为关于x的多项式
                - 推广式：$v^{(n+1)}$←(n+1阶导
                - ![Screenshot_2025-09-16-08-43-08-059_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-16-08-43-08-059_com.microsoft.emmx.canary-edit.86u0cc07qp.jpg)
                - eg.![Screenshot_2025-09-16-09-00-32-727_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-16-09-00-32-727_com.microsoft.emmx.canary-edit.23289winb7.jpg)
                - step：
                    - 列
                        -  >按$P_n(x)$的最高次确定为n
                            - u升阶到$u^{(n+1)}$,$v^{(n+1)}$降阶到v
                        -  ![IMG_20250916_090403](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20250916_090403.9kgjge0gyc.jpg)
                    - 写
                        - ![Screenshot_2025-09-16-09-10-36-877_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-16-09-10-36-877_com.microsoft.emmx.canary-edit.8hgu5idcxa.jpg)
- 有理函数
    - 因式分解
        - ![IMG_20250916_162421](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20250916_162421.6wr36gz1xl.jpg)
    - 求解A B C
        - 系数对应相等
            - ![IMG_20250916_162457](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20250916_162457.1ovsjh61xf.jpg)
        - 特值法
            - observe特殊值，代入，消去其他系数
                - 以此重复

## 定 //same
- 牛-莱
    - base
    - 推广：广义
        - 区间上 有限个 间断点，只要exist 原函数
            - 牛-莱 仍能使用
    - **count**:
        - 求数列极限
            - >提$\frac{1}{n}$，凑$\frac{i}{n}$视为$x$
            - 夹逼准则失效时, use
            - 
- base method
    - 性质
        - 奇偶、T
        - 区间再现; 华里士(点火)
    - 换元
    - 分部

## 变限
- f(x)是周期为T的可积函数
    - $\int_{x}^{x+2\pi}$=$\int_0^\pi$
        - 即$\int_0^T$=$\int_a^a+T$
- 求导公式
    - >f(t)含x需分离
    - 令$x^2-t^2=u$
        - u的新区间; du
- combine with隐函数
    - 由目标 找向 已知
- S(t) as 分段函数
    - 由题设条件，写其表达式
    - <span style="color:lightgray">？这个$t\in [1,2]$上是怎么写出面积表达式的？</span>
        - ![Screenshot_2025-09-16-17-04-19-593_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-16-17-04-19-593_com.microsoft.emmx.canary-edit.2a5g5teqh6.jpg)
 
---
## 反常
- 无穷区间类
    - 正常按积分的步骤做
        - 凑微/换元
            - >最后代入区间值(might换元后 不含∞
            - skill：令$x-1=sec$
        - 分部
            -?<span style="color:lightgray">最后求极限的值是怎么求出来的</span>![Screenshot_2025-09-16-17-53-14-032_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-16-17-53-14-032_com.microsoft.emmx.canary-edit.7p3yoakr6h.jpg)
- 无界函数类
    - 无穷间断点
        - 两段区间 相加
- --
- 判敛 //left
    - >2conclusion & 无穷小/无穷大 比阶
        - 主体： $\frac{1}{x^p}dx$
            - 无穷区间类
                - $\int_1^{+\infty}$
                    - $p ＞ 1$ **收敛**
                    - $p \le 0$divergence
            - 无界函数类
                - $\int_0^1$   
                - > ($p ＞0$,奇点$x=0$
                    - $p \ge 1$ d
                    - $0 ＜ .. ＜1$**收敛**
---
证明题
- 存在性related
- 性质
---
不定count思路
- 单一类：
    - $\frac{1}{\sqrt △ ( ) }$ ← 凑微
    - $\frac{1}{\sqrt...±...}$ ← 换元
- 单含sin 的处理(恒等变换+换元
    - 

？凑微不就是换元的特殊情况吗
分部里也含凑dv的情况
---
---
# geometry application
- s
    - 直角坐标下，平面图形
    - 极.., 扇形
- v-旋转体
    - 绕x轴
        - $\int_a^b \pi y(x)^2$
        - 2条
            - $\int_a^b \pi |y_2(x)^2-y_1(x)^2|$
    - ..y..
        - >圆柱体 展开为 长方体
            - ![Screenshot_2025-09-16-19-43-23-290_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-16-19-43-23-290_com.microsoft.emmx.canary-edit.7p3yoeih2e.jpg)
        - $dV= 2\pi x |y(x)| dx$
            - $V= 2\pi \int_a^b x |y(x)| dx$
            - 2条y
                - $V= 2\pi \int_a^b x |y_2(x)-y_1(x)| dx$
                

- $\bar y$
    - $\frac{1}{b-a}\int_a^b y(x) dx$

# integral=式&..不等..
- =
    - 中值
    - 夹逼
    - integral法
- 不等
    - 单调
    - 拉格朗日中值
    - Taylor
    - integral
