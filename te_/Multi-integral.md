# triple

## concept&性质

- concept
    - 几何意义：四维图形'体积
- 性质
    - base
        - **空间**区域'体积
            - $\iiint_{\Omega}1dv=V$
                - ↑和二重 求v可以互化吧？
    - 对称
        - 普通
            - (关于 平面 ← ？非坐标平面也可？
                - 不然这里是怎么变为4倍的？
                    - ![Screenshot_2025-09-15-15-14-02-861_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-15-15-14-02-861_com.microsoft.emmx.canary-edit.41yez6klbx.jpg)
        - 轮换
            - 求$\iiint_z^2dv$ ($\Omega$为球
                - $\frac{1}{3}x^2+y^2+z^2$
                    - use球坐标 计算
    - 形心
        - $\bar x= \frac{\iiint_\Omega xdv}{\iiint_\Omega dv}$
            - 逆用
                - eg.I Line
 
## 计算
- 直角
    - 先z后xy
        - >上下曲面or ..+侧is柱面
            - z为关于(x,y)表达式
        - $\iint_{D}d{\sigma}\int_{z_1(x,y)}^{z_2{(x,y)}}f(x,y,z)dz$
    - ..xy..z
        - >..平..(旋转体
            - z可直接定a,b
                - or有一面为 横截z的平面 即可
        - $\int_a^b dz \iint_{D}f(x,y,z)d{\sigma}$
            - ？这一步D_{xy}区域上的积分又是怎么一下子算出来等于$\pi(1-z^2)$的？
                - ![Screenshot_2025-09-15-13-15-47-441_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-15-13-15-47-441_com.microsoft.emmx.canary-edit.3rbl5wxgog.jpg)
                    - ↑确实是结论
                        - ![Screenshot_2025-09-15-13-15-47-441_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-15-13-15-47-441_com.microsoft.emmx.canary-edit.3rbl5wxgog.jpg)
- 柱(z+极
    - >$\Omega$usually为旋转体
    - >先z后xy中，$D$适合极($x^2+y^2$等
        - 先xy后z中，有适用的不行吗?因为后续含z?
    - $\iint_{D}d{\sigma}\int_{z_1(r,\theta)}^{z_2{(r,\theta)}}f(r,\theta,z)dz$
- 球
    - >$\Omega$为球
    - >$\theta \in [0,2\pi]$,$\phi \in [0,\pi] $,$r \in [0,.. ] $
        - 直接写范围，均 常
    - 三边长的另外2边why $rd\phi$ $rsin\phi d\theta$

    ---
    - attention
        - ①定义域
            - 画图+写变量范围
                - function中if have 绝对值 等, domain范围might need 分段
                    - <span style="color:lightgray">函数不会influence 变量</span>

    ---
## <span style="color:green">应用</span>
- 求 空间物体 形心竖坐标
    - $\bar z$
- 求转动惯量
---
---
# Line&Surface..

## Ⅰ型（数量函数
### L
>$ds$ 对曲线段L
    - 定:直先段

#### 平面
- base equation
    - 普通式
        - >$ds=\sqrt {1+y'^2}dx$
    - 参数式
        ->$..=\sqrt {{x'(t)}^2+{y'(t)}^2} dt$
    - 极
        ->$..=\sqrt {r(\theta)^2+ {r'}(\theta)^2 }d\theta$
- count
    - 表达式complex的，反复utilize性质化简
        ->给周长a等,就是在hint
        1. 对称性
            - 消去为0部分
        2. observe已知等式 与 表达式
            - 表达式无法陪凑，拆已知式
        3. 形心公式
            - $\iint y ds$
                - $=\bar y * a$
                - ↑这里的$\bar y=1$怎么来的？
                    - ![Screenshot_2025-09-15-15-41-48-179_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-15-15-41-48-179_com.microsoft.emmx.canary-edit.6bhfip4xnz.jpg)
    ---
    - 怎么推出来的？
        - ↑弧长
####  space
    - 参数式
        - >$..=\sqrt {{x'(t)}^2+{y'(t)}^2}+{z'(t)}^2} dt$
        - though题中未给
            - space中 need化为参方算
            - >曲线 直角坐标方程→only t'参/用几何性质
                - 球面与平面的交线
                - ？怎么化的 ← 配凑？
                - ![Screenshot_2025-09-15-15-14-02-861_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-15-15-14-02-861_com.microsoft.emmx.canary-edit.41yez6klbx.jpg)
            - ？为什么视频里的这道题可以避免用,书上的这个又要画出来
                - ![Screenshot_2025-09-15-15-29-00-762_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-15-15-29-00-762_com.microsoft.emmx.canary-edit.2rvhsvm7v8.jpg)
 

### S
>$dS$  空间曲面
    - 二重: 二维平面
#### count
- 首先考虑use性质化简
- base step：
    - ①..
        - 曲面投影到某一平面
    - ②..
        - 表达式转为 二重积分(z=f(x,y)
            - $dS=\sqrt {1+{z'}_x^2+{z'}_y^2 } d\sigma$
        - $\iint_{D_{xy}} f(x,y,z(x,y)) \sqrt {1+{z'}_x^2+{z'}_y^2 } d\sigma$
    - ③..
#### <span style="color:green">应用
- 求截面面积
    - 被积函数=1 即求面积
        - $\iint_{D_{xy}} f(x,y,z(x,y)) \sqrt {1+{z'}_x^2+{z'}_y^2 } d\sigma$
            - <span style="color:lightgray">将所给方程</span>改写为 $z=$
            - ？这个后面计算直接得出最后结果是怎么来的
                - ![Screenshot_2025-09-15-16-33-45-445_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-15-16-33-45-445_com.microsoft.emmx.canary-edit.23288x9iqf.jpg)
    - 截面方程：
        - 联立2方程，求得xoy平面投影 

## II型（向量..
### L
>Pdx+Qdy(平面
- 平面
    - green
- 空间
    - stokes
### S
>Pdx+Qdy+Rdz
- count
    - 直接
        - 拆为3个integral, space曲面 向各面投影
    - gauss
        - >封闭,连续
        - method
            - 补为封闭
            - 挖去奇点
---
对以上积分test中总假设存在
- 形心
    - ![Screenshot_2025-09-15-11-24-06-988_com](https://bluejedis.github.io/picx-images-hosting/calculus/Screenshot_2025-09-15-11-24-06-988_com.microsoft.emmx.canary-edit.9ddbjnyqyp.jpg)
- --
注意区分
L的space情况 & S (I II型都need)
- --
应用题type
什么情况use,use什么积分
---
总思路：

反复use**对称性**
>all based on 定义域 对称
- 普通
    - 偶函数性:
        - 化$\Sigma$为求2k$\Sigma_1$
    - 奇函数性：消去part

- 轮换
    - 将求single 化为求$\frac{1}{n}$整体
---
//left第II型
