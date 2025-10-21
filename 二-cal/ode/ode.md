求解微分方程，就是求解 y=f(x)的表达式（y关于x的表达式

- concept
    - 微分方程
    - ..阶、解(通解、initial condition、特解
        - 阶
            - 导数'最高阶数
        - **通解**
            - 解 include 独立常数'个数=阶数
                - ensure常数C'**condition** ← 初始condition
                    - 常数**确定** ← 特解
# 拿到 先看**阶**
map:
![IMG_20251021_233703](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20251021_233703.eswrli05d.jpg)
## 一阶 (3+1
- 求解
    - variate可分离
        - directly
            - >$\int \frac{dy}{y}$=$\int f(x)(dx) + C$
            - ？题里面tanx的原函数怎么会有ln？
        - 可化为..
            - >含有x、y不可分的整体，换元
                - 最终 三角函数内部拆不出来，也可
                    - eg.![IMG_20251021_230030](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20251021_230030.3rbmlxogoj.jpg)
        - 齐次微分equation
            - >令$u=\frac{y}{x}$
            - 应用型，最后再带具体值← 求C的表达式即可，不用去根号<span style="color:lightgray">←最终求 L表达式才移项</span>
                - ![IMG_20251021_225634](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20251021_225634.5mo7ejuyrk.jpg)
            - ln中的符号"-"很重要，影响合并后形式
                - ![IMG_20251021_230102](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20251021_230102.39lkxcmwuw.jpg)
          
        - --
    - **一阶线性**//再算一遍
        - >公式求通解
        - 求解u(x)部分，积分怎么没带常数c←u(x)取最简，带了c 构造式可约


## 二阶可降
>注意lnx与lnC0收束
    - 除法运算 分母不为0← 分母为0为"奇解"，求通解时可忽略
- $y''=f(x)$
- $F(x,y',y'')=0$
    -  >y'=p(x) →y''=p'
    - eg.![IMG_20251021_232843](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20251021_232843.54y5pzyupi.jpg)
- $F(y,y',y'')=0$
    - >y'=p(y) →y''=$\frac{dp}{dy}$*y'=$\frac{dp}{dy}$*p
        - 注意每一步常数项均可收束
            - 积分时
                - 将symbol/明显不相关常数提出

## 线性：二阶&n阶
- 二阶常系数
    - 齐次equation 通解
        - y''+py'+q=0 --特征equation-->$\lambda^2+p\lambda+q=0$
            - $p^2-4q ＞ 0$ 两不等实根
                - $y=C_1e^{\lambda_1x}+C_2e^{\lambda_2x}$
            - ..=.. 相等实根
                - $..=({C_1+C_2x})e^{\lambda x}$
            - ..＜.. 共轭复根$\alpha±\beta i $
                - $..=({C_1\cos \beta x+C_2\sin \beta x})e^{\alpha x}$
    - ==非.. 特..==
        - 由f(x)设特解，回代
            - f(x)可能形式情况
                - base1
                    - 题中$Q_m(x)$设为ax+b
                        - ↑$Q_m(x)$与$P_m(x)$**同次**
                - base2
                - base1+base2
- n阶常系数
    - 齐..通..
---
方程的形式＜-- >解的形式
- 线性通解
    - 线性： 二次&高阶：
        - 取等式左边part=0
    - 公式中的结论，只用替换r1,r2
---
---
# 抽象
## 已知解，反求系数λ,u
- >将已知解代入
    - 若是长表达式，设为$y_3$等
        - 将系数常数提出← 求谁，分离谁
        - eg.![IMG_20251021_212852](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20251021_212852.8hgvk96bzo.jpg)
- --
##  △不解，与性质相结合
- 与 **二阶常系数线性**e结合
    - ↑不解方程←解不出特解，通解不能做,系数不确定，结论might正好相反
    - 将方程中y''、y'、y转换为$f''(x_0)$ $f'(x_0)$ $f(x_0)$
        - 构造欲求
        - eg. $f''(x_0)-2f'(x_0)+4f(x_0)=0$
            - 又$f'(x_0)=0$ $f(x_0)＞0$
            - ∴ $f''(x_0)=-4f'(x_0)＜0$
            - 故![IMG_20251021_214531](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20251021_214531.3ns0o563z0.jpg)
            
