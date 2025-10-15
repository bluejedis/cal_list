---
# S
## concept
- 定义
    - >∀$\epsilon＞0$，∃$N\in N_+$, 当$n＞N$时，恒有$|x_n-a|＜\epsilon$← a是 数列$\{x_n\}$的极限or $\{x_n\}$收敛于a
        - 记为：$\{x_n→a\}$($n→\infty$ or $lim_{n→∞}x_n=a$
- 性质
- 单调有界
## te
---
### 证lim存在/x_n收敛
#### 具体型
>use"是常数"，即求极限值a 
- 用定义
    - >与A作差 ＜$\epsilon$
        - ？为什么这里要取整数部分，再+1
        - ![Screenshot_2025-09-17-21-13-42-261_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-17-21-13-42-261_com.microsoft.emmx.canary-edit.6bhflvvegf.jpg)
- --
#### 抽象型
- 单
    - 只给新的lim，**证存在**
        -  用定义
            - >构造 $x_n-a＜\epsilon$
            - 证明：lim|a_n|=lA|
                - ↑即证|a_n|-|A| $＜\epsilon$
                    - ↑不等式
                        - | |a_n|-|A| | ≤ |a_n-A| ＜$\epsilon$
    - 给出a_n等表达式，证存在&求值
        - 普通数列
            - **证存在**
                - >单调有界
                    - 1) 有界
                        - $a_{n+1}$≥ or≤ ←可用基本不等式
                    - 2) 单调
                        - $a_{n+1}-a_n$
                - 保号性
                    - A≥ or ≤ 1)中$a_{n+1}$边界
            - 求具体值
                - >skill: 左n+1，右n← 等式两端取lim，均A
                    - ↑解关于A的方程
                - --
                - eg.$a_{n+1}=\frac{1}{2}(a_n+\frac{2}{a_n})$
            ---
        - 表达式与三角函数有关
            - **证存在**
                - >still 单调有界
                - 1)有界(不等式) 2)单调($x_n+1$)
                    - >数学归纳
                    - 根据给出的第一项不等式情况
                        - 推出第n项
                            - eg.
                                - 1项：0＜x＜π
                                    - 0＜sinx＜x ←是个结论？
                                - n项：0＜sinx_n＜x_n ＜π
                                    - ∴ 代入题中条件
                                        - 0＜$x_{n+1}$=sinx_n＜x_n单减
                                        - ↑？单调性怎么看出来的？
            - 求值
                - >左n+1，右n← 两边取lim
                    - 解A
    - --
    - 给$x_n$的具体序列
        - 多n求和
            - ①找$\Sigma$通式 放缩
            - ②夹逼准则，左右lim值，即原式lim值
                - eg.![IMG_20251015_080206](https://bluejedis.github.io/picx-images-hosting/Math/IMG_20251015_080206.45i23c5fh1.webp)
- 双
    - 要证明lim存在的情况下，不能直接用lim表示
        - ↑存在性未知
        - 设新变量，再表示
            - $u_n=a_n+b_n$ $v_n=a_n-b_n$
                - $a_n=1/2(u_n+v_n)$
                - $b_n=1/2(u_n-v_n)$
- --
### 证lim不存在/x_n发散
>"单调有界"←选取子列 证发散
- eg. "收敛数列的 ∀子列 也收敛"逆否
    -  ![IMG_20251015_073805](https://bluejedis.github.io/picx-images-hosting/Math/IMG_20251015_073805.2vf4wztwii.webp)
    - 子列
        - {2n}发散
        - {$\frac{1}{2n+1}$}∈(0,1] 单调有界
