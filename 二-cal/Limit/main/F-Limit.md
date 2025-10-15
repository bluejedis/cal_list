
# <span style="color:lightgray"> base</span>

## <span style="color:lightgray"> concept</span>
- 海涅定理←link F与S
    - >f(x)在$\mathring U(x_0,\delta)$内有定义
        - $lim_{x→x_0}f(x)=A$存在$\Leftrightarrow$
        - 在$∀$ $\mathring U$内 以$\bf x_0$为极限的数列$\{\bf{x_n}\}$
            - $lim_{\bf n→\infty}f(x_n)=A$存在
                - <span style="color:lightgray">↑actually 等量代换</span>
    - --
    - eg.证 $lim_{x \to 0}\frac{1}{x}sin\frac{1}{x}$不存在
        - >key:取$n → ∞$，$x→0$，x取不同的n的表达式<span style="color:lightgray">← 证此时lim值不同，非常数</span>
            - $x_n=\frac{1}{n\pi}$
                - $lim_{n→∞}f(x_n)=0*0=0$
            - $x_n=\frac{1}{(2n+\frac{1}{2})\pi}$
                - $lim_{n→∞}f(x_n)=lim_{n→∞}(2n+\frac{1}{2})\pi=∞$
- 无穷小
    - >函数值为0 ($x→x_0$or$x→∞$时
        - 无穷大同理
- 连续
    - 极限值=函数值
---
---

## ⭐count
- **base** step
    - >判类，看趋近，化简
        - **等价无穷小**itself ← 低阶近似，泰勒展开
            - if无穷小为0-0等，泰勒 展开到第二阶
    - 再
        - **洛**
            - ↑慎用← 判断条件
            - ↑处理后，形式较简单的可洛
                - 如 只有一个项为e^x、sinx等
                    - ↑分式中，**展开不了上下同阶**(展开后阶次不一致
                        - 洛
    - --
    - 近似数列←如 取整symbol等
        - 夹逼
            - eg.![Screenshot_2025-10-15-13-47-59-039_com](https://bluejedis.github.io/picx-images-hosting/Math/Screenshot_2025-10-15-13-47-59-039_com.microsoft.emmx.canary-edit.8z6wzt4c4f.webp)
            - 利用不等式，构造题中函数表达式
                - 分正负discuss
                    - ![Screenshot_2025-10-15-13-49-25-536_com](https://bluejedis.github.io/picx-images-hosting/Math/Screenshot_2025-10-15-13-49-25-536_com.microsoft.emmx.canary-edit.9kgkm3zcx8.webp)
   
### 性质
- 存在←→ 左右极限相等
    - ？$e^\frac{1}{x}$分式部分的值是怎么求出来的

- 有界$\Leftrightarrow$
    - 在[a,b]上连续，则在[a,b]上有界
- --
- --
### △3类未定
- 思路map
    -  ![](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20251015_234435.77dy5huu2k.jpg)

#### $\frac{0}{0}$ $\frac{\infty}{\infty}$ ← $0 \cdot \infty$
- $\frac{0}{0}$
    - ①无 多根号、多三角函数
        - 洛
            - 含有$\bf \frac{1}{x^2}$元素
                - 令其=t
                - ↑避免无法求导
    - ②含$\sqrt a - \sqrt b$or$\sqrt a - b$
        - 有理化← 2平方项 勿少
            - eg. ![IMG_20251015_131312](https://bluejedis.github.io/picx-images-hosting/Math/IMG_20251015_131312.6m4aiks7h4.webp)
                - ![IMG_20251015_131423](https://bluejedis.github.io/picx-images-hosting/Math/IMG_20251015_131423.7lkdvqkp4w.webp)
                - 同除以x的次方←要保证x→+，否则t=-x
            - tips:
                - 三角函数
                    - tanx-sinx=tanx(1-cosx)
                - 见tanx与ln(1+x)同时appear ←Taylor 上下展开到同阶/"幂次最低"(x系数不相等项)
                    - ![](https://bluejedis.github.io/picx-images-hosting/calculus/IMG_20251015_162200.96a4ve7a71.jpg)
                        - eg.![屏幕截图-2025-10-15-125659](https://github.com/bluejedis/picx-images-hosting/raw/master/Math/屏幕截图-2025-10-15-125659.5c1dc8hvj6.webp)
                        - ![image](https://github.com/bluejedis/picx-images-hosting/raw/master/Math/image.491o1clj0e.webp)
                        - ![image](https://github.com/bluejedis/picx-images-hosting/raw/master/Math/image.8s3p4buytv.webp)
                - 

- $\frac{\infty}{\infty}$
    - ①观察format
        - 洛
    - ②"抓大头"
        - >分子分母中，增长最快(高阶)项
            - eg.$\lim_{x \to \infty} \frac{3x^2 + 5x}{2x^2 - x}$
                - $ \lim_{x \to \infty} \frac{3 + 5/x}{2 - 1/x} = \frac{3}{2}$
    - ③有理化
---
- $0 \cdot \infty$
    - 含多项式较多时
        - →分式
    - 较简单
        - 等价o→  0*0
            - ↑除∞外，0*∀均0
---
#### $\infty - \infty$↑
- >想尽办法通分，化为情况1)
    - 无分母
        - **倒代换**
            - $u=\frac{1}{x}$


---
####
####  $\infty^0$ $0^0$; $1^\infty$ <span style="color:lightgray"> ←阶</span>

- $\infty^0$ $0^0$
    - > lim$u^v$ =exp{$\lim vlnu$}
- $1^\infty$
    - >exp{$\lim v(u-1)$}
        - ↑=exp{$\lim vln[1+(u-1)]$} <span style="color:lightgray">(← rem性推导
        - exp{$\lim vlnu$}</span>

#### 已知一个lim 求另一个式子
- 由未知找向已知
    - $\lim \frac{x^3}{f(x)}$
        - $\Leftrightarrow$ 求$\lim \frac{f(x)}{x^3}$
        - ↑构造已知式等式求值
            - $\lim \frac{x-sinx+f(x)}{x^4}$ *++x++ =0
#### 反求参
- 正常解求lim即可
## 无穷小比阶
- >本质还是算lim
    - 构造比值式即可
        - skill：
            - $e^{tanx}$-$e^x$泰勒展开到1阶的依据？
            - 书上是默认等价无穷小推导的
    - --
    - o&T应用
        - 含根式
            - 视为$\frac{1}{k}$ 次方
                -  eg. $\sqrt[3] {x+1}$
                    -  ${(x+1)}^{\frac{1}{3}}$
                    - ~ $\frac{1}{3}$x
## 连续&间断
- 连续
    - 左lim=右lim
        - 在$x_0=0$处
            - usually 式子有意义可直接代入值计算
- 间断点
    - type(2 2<span style="color:lightgray">"跳去乌镇"</span>
        - 1类
            - >左右存在
                - 跳
                - **去**
                    - >唯一lim存在'情况
        - 2类
            - >not
                - 无
                    - ↑左右lim之一/全部 → +/- ∞
                - 振
    - --
    - judge类型
        - step
            - ①写间断点
                - 无定义点
                - + 分段<span style="color:lightgray">← for 分段function</span>
            - ②对每个$x_0$求 左右极限<span style="color:lightgray">←优先带值计算</span>
                - 绝对值在分母，该点又为0
                    - ↑分类讨论去绝对值符号
                - ==x→1==
                    - 想到lnx=ln[1+(x-1)] ~ (x-1)
---
---
# 与∫ 结合
