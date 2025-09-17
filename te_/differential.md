# d概念 计算
## concept
### 导数
- 导数
    - >$△→0$ ← 不再 只研究 起点&终点
    - $f'(x_0)=lim_{\Delta x→0}\frac{\Delta y}{\Delta x}$
        - $\frac{f(x_0+△x)-f(x_0)}{△x}$
        - $\frac{f(x)-f(x_0)}{x-x_0}$
    - 几何angle
        - 有垂直于x轴'切线
            - $f'(x)=±\infty$
        - 切线方程
            - ![IMG_20250916_201600](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20250916_201600.175qv4dc7m.jpg)
        - 法线..
            - ![Screenshot_2025-09-16-20-11-48-274_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-16-20-11-48-274_com.microsoft.emmx.canary-edit.8vn9x18cot.jpg)
- 单侧导数(左右
    - >九点前瞬时，还是..后的
    - $△x→0^-$ ← 左导数
    - $△x→0^+$ ← 右..
- 高阶..
    - $f^{(n)}(x_0)=lim_{\Delta x→0}\frac{f^{(n-1)}(x_0+△x)-f^{(n-1)}(x_0)}{△x}$

---
### 微分
- $dy=Adx$
    - ↑ $△y=A△x+\omicron (△x)$
        - $\omicron (△x)$是比$△x→0$更小的高阶无穷小
- 可微
    -  >可微 ←→ 可导
---
---
## count

- base 1 4
    - 四则
    - 分段
        - count左右导
    - 复合
        - >微分形式不变性: 
            - $dy=f'(u)du$ 总成立
        - ![Screenshot_2025-09-16-20-54-42-639_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-16-20-54-42-639_com.microsoft.emmx.canary-edit.7eh4vbo2kd.jpg)
            - ↑ 以dx为基准
            - 对比
                - ![Screenshot_2025-09-16-20-55-34-409_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-16-20-55-34-409_com.microsoft.emmx.canary-edit.4n82n923k4.jpg)
                - 以d[g(x)]
    - 反
        - $\phi'(x)=\frac{1}{f'(x)}$
    - 参数
        
- base-隐、对、幂指
    - 隐
        - 两边同时对x求导
            - 解y'
    - **对**
        - >for 多项 乘、除，乘方、开方 ←两边同时取对
            - $lny=lnf(x)$
        - 再同时对x求导
    - **幂指**
        - >for $u(x)^{v(x)}$ ← 化为指对
            - $e^{v(x)lnu(x)}$
            - 对x求导
            - ![Screenshot_2025-09-16-21-37-54-828_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-16-21-37-54-828_com.microsoft.emmx.canary-edit.7w76jy9lje.jpg)
                - <span style="color:lightgray">$e^x$求导不变, 括号外化为原型</span>
- more-高阶、变限积分;basic求导公式
    - 高阶
        - 归纳法
        - 高阶求导公式(+;×
            - +：
                - 各自高阶导 相加
            - ×：
                - $\Sigma_{k=0}^{n} C_n^k u^{n-k}v^{k}$
                    - ![IMG_20250917_082505](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20250917_082505.7eh4w0apdr.jpg)
        - 泰勒展开
            - ？怎么求极限章节和导数章节，给的展开不一样
                - ![Screenshot_2025-09-17-08-34-41-921_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-17-08-34-41-921_com.microsoft.emmx.canary-edit.6pnvc023wy.jpg)
                - ![IMG_20250917_083348](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20250917_083348.58hqa8xz86.jpg)

---
## te
### concept
#### 证明
- base
    - $f'(x)$为奇/偶函数
        - >要证什么，list什么的表达式←表达式$f'(-x)$
            - $lim_{△x→0}\frac{f(-x+△x)-f(-x)}{△x}$
            - 原f(x)为偶
                - =$lim_{△x→0}\frac{f(x-△x)-f(x)}{- △x}$
                - ∴f'(-x)=-f'(x)
            -..奇
                - =$lim_{△x→0}\frac{- f(x-△x)-f(x)}{-△x}$
                - ∴f'(-x)=f'(x)
    - ...周期函数
        - >所有x都要换为x+T
        - $f'(x+T)=\frac{f(x+T+△x)-f(x\bf{+T})=f(x+△x)-f(x)}{△x}$
### 抽象
- 比大小
    -  >由未知找向已知，use已知性质化为已知式
        - >无穷阶可导，求导一次，奇偶性互换一次
        - 二阶可导→二阶导存在→f''(0)=0
- 证可导
    - >在点$x=x_0$处可导←→$f'(0)$存在
    - >构造表达式
        - 题中已知f(0)=1，则将非f部分化为1，等价于f(0)
        - ![IMG_20250917_112045](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20250917_112045.39ljk2nipb.jpg)
        - 可直接 泰勒展开替换(上下同阶
            - ![IMG_20250917_112810](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20250917_112810.3uv76dr81r.jpg)
        - 约去x 提2
- 命题: 连续, 怎样的表达式 使f(x_0) f'(x_0)存在
    -?为什么$lim\frac{f(x)}{x}=A$存在
        - 则有 $f(0)=lim_{x→0}f(x)=0$
        - ![Screenshot_2025-09-17-11-39-13-490_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-17-11-39-13-490_com.microsoft.emmx.canary-edit.5mo61ap069.jpg)

- 微分
    - 比阶
        - >注意比较的是$\omicron (x)$ 还是$△x$
        - $△x$直写
            - $dy=Adx$
            - =$f'(x)dx$
    - 求$f'(x_0)$
        - 复合函数dy
            - $dy=f'(x^2)dx^2$
                - =$\underline{2xf'(x^2)}dx$
### count

#### 一阶导
- 三角函数
    - $\prod_{n=1}^100$形式，注意第一项
    - utilize反函数
        - $\arcsin x$
        - $\arctan x$
    - --
- 含| |
    - >分类讨论 去| |
    - $ln |x| $
        - x≠0，
        - 故去绝对值 分x＞0, x＜0讨论
    - $2^{|x-a|}$
        - 分 ＞, =,＜ 讨论
        - ？为什么这里x=a时 也是用的定义求导数，什么时候用定义求导数，什么时候不用定义求？
            - ![Screenshot_2025-09-17-14-11-30-864_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-17-14-11-30-864_com.microsoft.emmx.canary-edit.2yypr3dadr.jpg)
        - --
- 分段，**可导**
    - >连续 + 左导=右导
        - 连续
            - $lim_{x→0^-}f(x)=f(0)$
        - 左右导
            - ?为什么这里 左右导 是用定义求的，求导公式不能直接用吗
                - ![Screenshot_2025-09-17-14-11-17-124_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-17-14-11-17-124_com.microsoft.emmx.canary-edit.5c1c8ar3mn.jpg)
       
- 复合
    - 复合+分段：y=f[f(x)]
        - 复合函数求导
            - y'=$\underline{f'[f(x)]}*\underline{f'(x)}$
                - ①$u=f(x)$, $f'[u]$
                - ②直算$f'(x)$
        - 在对应分段 计算 所需element
---
- 反
    - >二阶导：
        - >tip: 反函数二阶导 表达式中的y和x还是对于 ，原式，而言
        - $\frac{d[\frac{dx}{dy}]}{dy}$
            - =$\frac{d[\frac{1}{f'(x)}]}{dy}$
            - =$\frac{d[\frac{1}{f'(x)}]}{dx} * \frac{dx}{dy}$
        - $\underline{\frac{-f''(x)}{f'(x)^2}} * \underline{\frac{1}{f'(x)}}$
    - +变限积分求导
- 参
    - >二阶导$\frac{d^2y}{dx^2}$
        - $\frac{d[\frac{dy}{dx}]}{dx}$
        - =$\underline{\frac{d[\frac{dy}{dx}]}{dt}} * \underline{\frac{dt}{dx}}$
            - 再分别算两个部分
- 隐
    - y的导 要写作y'
---
- $x^x$ $x^{\frac{1}{x}}$ (x＞0
    - 两边取对
    - 再两边对x求导
- $y=\sqrt[3]{\frac{(x+1)(2x-1)^2}{(4-3x)^5}}$
    - 两边取对，并将次数提在ln前 ← 未给＞0，则加| |
    - 再两边求导 (拿掉绝对值
        - y'的解 中含y部分，用原表达式的x替换
- --

#### n阶     
---
todo:
连续 可导 可微
---
---
# geometry application
## element
### 极值、最值
- 一阶可导点是极值点的 必要condition
    - $f'(x)=0$
- 判别极值 3充分condition
    - 第一..
        - f(x) 在$x=x_0$连续;在$x_0$内可导
    - ..二..
    - ..三..
#### concept
#### 单调性&极值
- 一阶导数取极值 的 必要condition
- 判别极值 的 充分..
    - 第一
        - >$f(x)$在$x=x_0$处连续;在$x_0$的$\mathring U$可导
    - ..二..
        - >..二阶可导,$\bf f'(x_0)=0$,$f''(x_0)≠0$
        - $f''(x)＜0$→$f'(x)$↓，左+右-
            - $f(x_0)=0$ 取极大
        - .. ＞ .. →...↑ 左-右+
            - ...极小
    - ..三.. ←？洛必达证明
        - >..n阶可导
    
#### 最值/取值range
---
### 凹凸性&拐点
- concept
    - 凹凸
        - ![Screenshot_2025-09-17-16-33-54-663_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-17-16-33-54-663_com.microsoft.emmx.canary-edit.8vn9yblpkx.jpg)
    - 拐点
### 渐近线
- 铅垂..
- 水平
- 斜
## 作图
# 中值定理、零点、不等式

## 中值
4 4 1 (1)

## 零点
- concept
    - 证 存在/唯一
    - 实系数齐次方程at least 一个实根
- count - 方程根（零点）
## 不等式
- 函数性态
- 常数变量化
- 中值