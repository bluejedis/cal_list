map：
![IMG_20251016_204530](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20251016_204530.54y5ioxra0.jpg)
total: 2+2组

---
## element
### 极值、最值，单调性
- 极值condition：
    - 一阶可导点是极值点的 必要condition
        - $f'(x)=0$
    - 判别极值 3充分condition
        - 第一..
            - f(x) 在$x=x_0$连续;在$x_0$内可导
        - ..二..
        - ..三..
  


#### **单调性**&==极值==
- 单调性
    - 见"单调"
        - → 构造function求 "一阶导" 即$f'(x)$
- 极值
    - 必要condition
        - $f'(x)=0$
    - 充分..
        - 第一
            - >$f(x)$在$x=x_0$处连续;在$x_0$的$\mathring U$可导
        - ..二.. ←即 常用list表法
            - >..二阶可导,$\bf f'(x_0)=0$,$f''(x_0)≠0$
            - $f''(x)＜0$→$f'(x)$↓，左+右-
                - $f(x_0)=0$ 取极大
            - .. ＞ .. →...↑ 左-右+
                - ...极小
        - ..三.. ←？洛必达证明
            - >..n阶可导
                - $f^m(x)$ (m＜n
            - n=2k，对$lim_{x→x_0}\frac{f(x)-f(x_0)}{(x-x_0)^{2k}}$
                - -不断洛必达 →$lim_{x→x_0}\frac{1}{(2k)!}f^{(2k)}(x)$
                    - ↑局部保号
                        - $f^{(2k)}(x)$＜0，原lim中 f(x)＜f(x_0)
                        -  ...＜0，...＞
    
#### 最值/取值range
---
### ==凹凸性==&==拐点==
- >$f''(x)$相关 ←均二阶可导
- concept
    - 凹凸
        - ![Screenshot_2025-09-17-16-33-54-663_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-17-16-33-54-663_com.microsoft.emmx.canary-edit.8vn9yblpkx.jpg)
        - 判别
            - $f''(x)$＞0，凹
            -  ..＜..，凸
    - 拐点
        - >分界点 of 凹弧、凸弧
        - condition
            - >类比极值
            - 必要
                - $f''(x)$=0
            - 充分
                - 第一
                - ..二
                - ..三
---
极值、凹凸性、拐点这几个的常用判别条件如何理解？
为什么二阶导＞0 就是凹的？
二阶导的几何意义是什么？
- 斜率的变化率
    - 凹：斜率变化越来越快
    - 凸：..慢
极值的第二充要条件是怎么来的？
---
---
### 
### 渐近线
- type：
    - 铅垂..
        - y→+/-∞ <span style="color:lightgray">(x→$x_0$</span>
            - ![image](https://bluejedis.github.io/picx-images-hosting/calculus/image.77dy6657f4.webp)
    - --
    - 水平
        - y=b <span style="color:lightgray">(x→$+/- ∞$</span>
            - ![image](https://bluejedis.github.io/picx-images-hosting/calculus/image.8adnh21lj7.webp)
    - 斜
        - y=mx+b<span style="color:lightgray">(x→$+/- ∞$</span>
            - ![image](https://bluejedis.github.io/picx-images-hosting/calculus/image.96a4wic2ma.webp)
- 求
    - step
        - >此类求lim usually代入计算即可
        - 垂
            - >间断点
        - 平
            - >分x趋于+/-∞
                - ↑看哪个lim是常数 (可能有2
        - 斜
            - 求斜率
                - m=$lim_{x→\infty}\frac{f(x)}{x}$
                - b=$lim_{x→\infty}[f(x)-kx]$
                    - <span style="color:lightgray">↑</span>
                        - 原理：
                            - 使曲线与渐近线 高度差趋于一致</span>
                            - $lim_{x→\infty}[f(x)-(mx+b)]$
                                - <span style="color:lightgray"> 同除以x
                                    - $lim_{x→\infty}[\frac{f(x)}{x}-m-\frac{b}{x}]$
                                    - ↑又x→∞，$\frac{b}{x}$可忽略</span>

### 曲率k、曲率半径ρ
- K=$\frac{|y''|}{ (1+y'^2)^{\frac{3}{2}}}$
    - ↑推导：
        - k=|$\frac{d\alpha}{ds}$|
            - $\frac{d\alpha}{ds}$=$\frac{d\alpha}{dx}*\frac{dx}{ds}$
            -  ①求$\frac{d\alpha}{dx}$
                - ==tanα===$\frac{dy}{dx}$ <span style="color:lightgray"> ←α为切线与x轴正方向夹角</span>
                - ↑两边同时求导
                    - $sec^2\alpha \frac{d\alpha}{dx}=y''$
                    - ↑消α ←用tan
                        - $sec^2α=1+tan^2α$
                            - =1+$y'^2$
                - ∴$\frac{d\alpha}{dx}$=$\frac{y''}{1+y'^2}$
            - ②$\frac{dx}{ds}$
                - =$\frac{1}{\frac{ds}{dx}}$
                    - = $\frac{1}{(1+y'^2)^{\frac{1}{2}}}$
            - ③合并
                    
    - 弧微分ds
        - ds=$\sqrt dx^2+dy^2$
            - 直角：ds=$\sqrt {1+y'^2} dx$
- ρ
    - >与k垂直
    - =$\frac{1}{K}$
        - ![](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20251016_083751.lw4ezsjtk.jpg)
- --
## 作图
- base step
    - ① base
        - 定义域
            - 排间断点 (无定义点
        - 交点← x=0,y=0
    - ②求导
        - 一阶
            - 单调性
        - 二阶
            - 拐点
    - ③渐近线
