
# multi integral

## **第16讲 多元函数积分学**

### **Triple积分 (三重积分)**

* **1. 概念与对称性**
    * **概念**: $\iiint_\Omega f(x,y,z)dV$ 表示空间物体 $\Omega$ 的某种<span style="border-bottom: 2px solid black;">物理量</span>（如质量）。
    * **对称性 (<span style="border: 1px solid black; padding: 5px; display: inline-block;">轮换对称性</span>)**: 若积分区域 $\Omega$ 关于变量 $x, y$ 轮换对称 (即 $(\underline{x},\boxed{y},z) \in \Omega \iff (\boxed{y},\underline{x},z) \in \Omega$), 且被积函数满足 $f(x,y,z) = f(y,x,z)$, 则 $\iiint_\Omega f(x,y,z)dV = \iiint_\Omega f(x,y,z)dV$ 可以通过变量轮换来简化。例如 $\iiint_\Omega x^2 dV = \iiint_\Omega y^2 dV$。

* **2. 计算**
    * **(1) 直角坐标系 (投影穿线法)**
        * **适用场合**: 积分区域是长方体、棱柱、或由几个平面/柱面围成的简单区域。
        * **通式通法**: “先一后二”，将三重积分化为一次定积分和一次二重积分。
        * **做题步骤**:
            1.  **投影**: 将空间体 $\Omega$ 投影到一个坐标面 (如 xoy面) 上，得到投影区域 $D_{xy}$。
            2.  **定限**: 确定 $D_{xy}$ 的范围。然后，在 $D_{xy}$ 内任取一点 $(x,y)$，沿 z 轴方向作直线穿过空间体 $\Omega$，穿入的曲面为 z 的下限 $z_1(x,y)$，穿出的曲面为 z 的上限 $z_2(x,y)$。
            3.  **计算**: 将三重积分写成累次积分形式 $\iint_{D_{xy}} \left[ \int_{z_1(x,y)}^{z_2(x,y)} f(x,y,z)dz \right] dxdy$，然后计算。
    * **(2) 柱..**
        * **适用场合**: 积分区域 $\Omega$ 的形状是柱体、锥体，或其在 xoy 面上的投影 $D_{xy}$ 是圆形或扇形。被积函数含 $x^2+y^2$。
        * **通式通法**: 坐标变换 $x=r\cos\theta, y=r\sin\theta, z=z$。体积微元 $dV = \boxed{r}dzdrd\theta$。
        * **做题步骤**:
            1.  **画图定限**: 画出 $\Omega$ 及 $D_{xy}$ 的图。用极坐标的方式确定 $D_{xy}$ 中 $r$ 和 $\theta$ 的范围。
            2.  **穿线定限**: 确定 z 的上下限 $z_1(r,\theta), z_2(r,\theta)$。
            3.  **代入计算**: 写出累次积分 $\int_{\theta_1}^{\theta_2} d\theta \int_{r_1(\theta)}^{r_2(\theta)} dr \int_{z_1(r,\theta)}^{z_2(r,\theta)} f(r\cos\theta, r\sin\theta, z) \cdot \boxed{r} dz$ 并计算。
    * **(3) 球..**
        * **适用场合**: 积分区域 $\Omega$ 是球体、锥体或其一部分。被积函数含 $x^2+y^2+z^2$。
        * **通式通法**: 坐标变换 $x=\rho\sin\phi\cos\theta, y=\rho\sin\phi\sin\theta, z=\rho\cos\phi$。体积微元 $dV = {\boxed{\rho^2\sin\phi}} d\rho d\phi d\theta$。
        * **做题步骤**:
            1.  **画图定限**: 画出区域 $\Omega$ 的草图。
            2.  **定各变量范围**:
                * $\rho$ (到原点的距离): 从原点引射线，穿入界的 $\rho$ 为下限，穿出界的 $\rho$ 为上限。
                * $\phi$ (与 z 轴正向的夹角): 范围是 $[0, \pi]$。
                * $\theta$ (投影到 xoy 面的极角): 范围是 $[0, 2\pi]$。
            3.  **代入计算**: 写出累次积分 $\int_{\theta_1}^{\theta_2} d\theta \int_{\phi_1}^{\phi_2} d\phi \int_{\rho_1(\phi,\theta)}^{\rho_2(\phi,\theta)} f(\dots) \cdot \rho^2\sin\phi d\rho$ 并计算。
    ---
### **ⅠLine积分 & ⅡLine积分 (第一类与第二类曲线积分)**

#### **第一类曲线积分 (对弧长的积分)**: $\int_L f(x,y)ds$
* **概念**: 几何意义是<span style="border-bottom: 3px dotted black;">变密度</span><span style="border-bottom: 2px solid black;">曲线</span>的<span style="border-bottom: 2px solid black;">质量</span>，或以 L 为准线、母线平行于 z 轴、高为 $f(x,y)$ 的柱面侧面积。
* **通式通法**: 化为定积分。
* **做题步骤**:
    1.  **参数化**: 将曲线 L 写成参数方程 $x=x(t), y=y(t)$ ($t \in [\alpha, \beta]$)。
    2.  **计算弧长微元**: $ds = {\boxed{\sqrt{[x'(t)]^2 + [y'(t)]^2}}} dt$。
    3.  **代入计算**: $\int_\alpha^\beta f(x(t), y(t)) \sqrt{[x'(t)]^2 + [y'(t)]^2} dt$。
    ---
#### **第二类曲线积分 (对坐标的积分)**: $\int_L P(x,y)dx + Q(x,y)dy$
* **概念**: 物理意义是变力 $\vec{F}=(P,Q)$ 沿路径 L 所做的功。
* **通式通法**: 方法一：化为定积分。方法二：格林公式。
* **做题步骤 (方法一：化为定积分)**:
    1.  **参数化**: 将曲线 L 写成参数方程 $x=x(t), y=y(t)$ ($t \in [\alpha, \beta]$)。**注意积分方向**，参数 $t$ 的起始点要与 L 的方向一致。
    2.  **计算坐标微元**: $dx = x'(t)dt$, $dy = y'(t)dt$。
    3.  **代入计算**: $\int_\alpha^\beta [P(x(t), y(t))x'(t) + Q(x(t), y(t))y'(t)] dt$。
* **做题步骤 (方法二：<span style="border: 1px solid black; padding: 5px; display: inline-block;">格林</span>公式)**:
    1.  **判断条件**: 检查曲线 L 是否为**封闭**的，且方向为**正向**(逆时针)。P, Q 在 L 所围区域 D 内是否具有一阶连续偏导数。
    2.  **应用公式**: $\oint_L Pdx + Qdy = \iint_D (\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}) dxdy$。如果 L 是顺时针，则公式右边加负号。
    3.  **计算二重积分**: 用直角坐标或极坐标计算右侧的二重积分。如果 $\frac{\partial Q}{\partial x} = \frac{\partial P}{\partial y}$，则积分与路径无关，可以直接找一个方便的路径。
    ---
### **ⅠSurface积分 & ⅡSurface积分 (第一类与第二类曲面积分)**

#### **第一类曲面积分 (对面积的积分)**: $\iint_\Sigma f(x,y,z)dS$
* **概念**: 几何意义是变密度<span style="border-bottom: 2px solid black;">曲面</span>的<span style="border-bottom: 2px solid black;">质量</span>。
* **通式通法**: "一投二代三计算"，化为二重积分。
* **做题步骤**:
    1.  **投影**: 将空间曲面 $\Sigma$ (方程为 $z=z(x,y)$) 投影到 xoy 面上，得到投影区域 $D_{xy}$。
    2.  **计算面积微元**: $dS = {\boxed{\sqrt{1 + (\frac{\partial z}{\partial x})^2 + (\frac{\partial z}{\partial y})^2}}} dxdy$。
    3.  **代入计算**: $\iint_{D_{xy}} f(x, y, z(x,y)) \sqrt{1 + z_x^2 + z_y^2} dxdy$。
    ---
#### **第二类曲面积分 (对坐标的积分)**: $\iint_\Sigma P dy dz + Q dz dx + R dx dy$
* **概念**: 物理意义是向量场 $\vec{F}=(P,Q,R)$ 穿过曲面 $\Sigma$ 的**通量**。
* **通式通法**: 方法一：化为二重积分。方法二：<span style="border-bottom: 3px dotted black;">高斯</span>公式。方法三：<span style="border: 1px solid black; padding: 5px; display: inline-block;">斯托克斯</span>公式。
* **做题步骤 (方法一：化为二重积分)**:
    1.  **定侧与投影**: 确定曲面 $\Sigma$ 的指定侧（法向量方向）。将积分拆为三部分，例如计算 $\iint_\Sigma R(x,y,z) dxdy$。
    2.  **代入换元**: 将曲面方程 $z=z(x,y)$ 代入 $R(x,y,z)$。
    3.  **加负号判断**: 投影到 xoy 面。判断曲面法向量的 z 分量符号。若为正（指向z轴正向，称为“上侧”），则 $\iint_\Sigma R dxdy = +\iint_{D_{xy}} R(x,y,z(x,y)) dxdy$；若为负（称为“下侧”），则加负号。
* **做题步骤 (方法二：高斯公式)**:
    1.  **判断条件**: 检查曲面 $\Sigma$ 是否为<span style="border-bottom: 3px dotted black;">**封闭**</span>的，且方向为**外侧**。P, Q, R 在 $\Sigma$ 所围空间体 $\Omega$ 内是否具有一阶连续偏导数。
    2.  **应用公式**: $\oiint_\Sigma P dydz + Q dzdx + R dxdy = \iiint_\Omega (\frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z}) dV$。如果 $\Sigma$ 是内侧，则公式右边加负号。
    3.  **计算三重积分**: 用直角、柱面或球面坐标计算右侧的三重积分。
* **做题步骤 (方法三：斯托克斯公式)**:
    1.  **判断条件**: 检查曲面 $\Sigma$ 是否为<span style="border: 1px solid black; padding: 5px; display: inline-block;">**不封闭**</span>的。
    2.  **应用公式**: 将对**不封闭曲面**的第二类曲面积分，转化为沿其**边界曲线 L** 的第二类曲线积分。$\iint_\Sigma (\frac{\partial R}{\partial y} - \frac{\partial Q}{\partial z})dydz + \dots = \oint_L Pdx+Qdy+Rdz$。**注意 L 的方向与 $\Sigma$ 的法向量方向要符合右手定则**。
    3.  **计算曲线积分**: 用参数法计算右侧的第二类曲线积分。

---
# differential equation&series

## **第17讲 微分方程**

### **一、一阶微分方程的求解**

#### **题型1: 可分离变量的方程**: $y' = f(x)g(y)$
* **通式通法**: 分离变量，两边积分。
* **做题步骤**:
    1.  **分离**: 将方程写成 $\frac{\boxed{dy}}{g(y)} = f(x){\boxed{dx}}$ 的形式。
    2.  **积分**: 两边同时积分 $\int \frac{dy}{g(y)} = \int f(x)dx + C$。
    3.  **求解**: 化简得到 $y$ 与 $x$ 的关系。
####  **题型2: 一阶线性微分方程**: $y' + {\underline{p(x)}}y = {\boxed{q(x)}}$
* **通式通法**: 公式法。
* **做题步骤**:
    1.  **套公式**: 通解为 $y = e^{-\int {\underline{p(x)}}dx} \left[ \int {\boxed{q(x)}}e^{\int {\underline{p(x)}}dx} dx + C \right]$。
    2.  **计算积分**: 依次计算公式中的两个积分。
    3.  **整理**: 化简得到最终通解。

### **二、二阶可降阶..**

#### **题型1: $y''=f(x)$ 型**
* **通式通法**: 逐次积分。
* **做题步骤**: 对方程两边连续积分两次即可。
####  **题型2: $y''=f(x, \boxed{y'})$ 型 (不显含y)**
* **通式通法**: <span style="border-bottom: 2px solid black;">换元</span>法。
* **做题步骤**:
    1.  **换元**: 令 $\boxed{p=y'}$, 则 $y''=p'$。方程化为一阶方程 $p' = f(x,p)$。
        1.  **解一阶方程**: 解出 $p = \phi(x, C_1)$。
    2.  **还原**: 代回 $y'=\phi(x, C_1)$, 再积分一次得到 $y$。
####  **题型3: $y''=f({\underline{y}}, y')$ 型 (不显含x)**
* **通式通法**: 换元法。
* **做题步骤**:
    1.  **换元**: 令 $p=y'$, 则 $y'' = \frac{dp}{dx} = \frac{dp}{dy}\frac{dy}{dx} = p\frac{dp}{dy}$。方程化为 $p\frac{dp}{dy} = f(y,p)$。
    2.  **解一阶方程**: 解出 $p$ 与 $y$ 的关系 $p=\psi(y, C_1)$。
    3.  **还原**: 代回 $y'=\psi(y, C_1)$, 分离变量 $\frac{dy}{\psi(y, C_1)} = dx$, 再积分一次。

### **三、高阶常系数线性..**

####  **方程形式**: $y'' + py' + qy = f(x)$
* **通式通法**: 通解 = 齐次方程<span style="border-bottom: 2px solid black;">通</span>解 + 非齐次方程<span style="border-bottom: 2px solid black;">特</span>解 ($y = y_c + y_p$)。
* **做题步骤**:
    1.  **求齐次通解 $y_c$**:
        * 写出特征方程 ${\boxed{\lambda}}^2 + p{\boxed{\lambda}} + q = 0$。
        * 根据特征根的情况写出 $y_c$：
            * 两不等实根 $\lambda_1, \lambda_2$: $y_c = C_1e^{\lambda_1 x} + C_2e^{\lambda_2 x}$。
            * 两相等实根 $\lambda_1 = \lambda_2$: $y_c = (C_1 + C_2{\underline{x}})e^{\lambda_1 x}$。
            * 共轭复根 $\alpha \pm i\beta$: $y_c = e^{\alpha x}(C_1\cos\beta x + C_2\sin\beta x)$。
    2.  **求非齐次特解 $y_p$ (<span style="border-bottom: 2px solid black;">待定系数</span>法)**:
        * 观察右侧 $f(x)$ 的形式。
          * $f(x) = {\boxed{P_m(x)}}e^{ax}$ 型: 设 $y_p = x^k Q_m(x)e^{ax}$，其中 $Q_m(x)$ 是与 $P_m(x)$ 同次的多项式，$k$ 是 $a$ 作为特征根的重数（0, 1, 或 2）。
          * $f(x) = e^{ax}[{\boxed{P_l(x)\cos\omega x + P_n(x)\sin\omega x}}]$ 型: 设 $y_p = x^k e^{ax}[R_N(x)\cos\omega x + S_N(x)\sin\omega x]$，其中 $N=\max\{l,n\}$, $k$ 是 $a+i\omega$ 作为特征根的重数（0 或 1）。
    3.  **组合**: 将 $y_c$ 和 $y_p$ 相加得到最终通解。

---

## **第18讲 无穷级数**

### **一、<span style="border-bottom: 2px solid black;">数项</span>级数的判敛**

* **通式通法**: <span style="border-bottom: 2px solid black;">正项</span>级数判敛法为主, 任意项级数看绝对收敛。
* **做题步骤**:
    1.  **首步：检查必要条件**: 计算通项 $\lim_{n \to \infty} {\boxed{u_n}}$ 是否等于 0。若不等于 0, 则级数必发散。
    2.  **次步：选择判别法 (正项级数)**:
        * **比值法/根值法**: 若通项含 $n!$, $a^n$ 等, 优先用比值法 ($\lim_{n \to \infty} {\boxed{\frac{u_{n+1}}{u_n}}}$) 或根值法 ($\lim_{n \to \infty} {\boxed{\sqrt[n]{u_n}}}$)。若极限 $<1$ 收敛, $>1$ 发散, $=1$ 失效。
        * **比较判别法**: 若通项是多项式分式, 用极限形式的比较判别法, 与 <span style="border-bottom: 2px solid black;">p-级数</span> $\sum\frac{1}{\boxed{{n^p}}}$ 比较。
        * **积分判别法**: 若通项 $u_n=f(n)$ 对应的函数 $f(x)$ 易于积分, 可用 ${\boxed{\int_1^\infty}} f(x)dx$ 的敛散性判断。
    3.  **最终：处理交错/任意项级数**:
        * 对<span style="border-bottom: 3px dotted black;">交错</span>级数, 用<span style="border-bottom: 2px solid black;">莱布尼茨</span>判别法。
        * 对任意项级数, 先判断其绝对值构成的正项级数 <span style="border-bottom: 3px dotted black;">$\sum|u_n|$</span> 是否收敛。若收敛, 则原级数绝对收敛(从而也收敛)。若不收敛, 再判断原级数是否条件收敛。
        ---
### **二、<span style="border: 1px solid black; padding: 5px; display: inline-block;">幂</span>级数$\sum_{n=0}^\infty {\underline{a_n x^n}}$的收敛域**

* **通式通法**: 先求收敛半径, 再单独判断端点。
* **做题步骤**:
    1.  **求收敛半径 R**: 对幂级数 $\sum_{n=0}^\infty {\underline{a_n x^n}}$, 计算极限 $\rho = \lim_{n \to \infty} {\boxed{|\frac{a_{n+1}}{a_n}|}}$ (或 $\lim_{n \to \infty} {\boxed{\sqrt[n]{|a_n|}}}$)。收敛半径 $R = \frac{1}{\boxed{\rho}}$。
    2.  **写出开区间**: 得到开的收敛区间 $(-R, R)$。
    3.  **判断端点**: 将 $x=R$ 和 $x=-R$ 分别代入原级数, 得到两个数项级数, 用<span style="border-bottom: 2px solid black;">数项</span>级数的判别法单独判断其敛散性, 最终确定完整的收敛域。

        ---
### **三、函数<span style="border-bottom: 3px dotted black;">展开</span>为幂级数**

* **通式通法**: 间接展开法：利用已知的基本展开式, 通过代换、四则运算、逐项求导、逐项积分得到。
* **重要公式**:
    * $e^x = \sum_{n=0}^\infty \frac{x^{\boxed{n}}}{{\boxed{n}}!}, x \in (-\infty, +\infty)$
    * $\sin x = \sum_{n=0}^\infty (-1)^n \frac{x^{\boxed{2n+1}}}{{\boxed{(2n+1)}}!}, x \in (-\infty, +\infty)$
    * $\cos x = \sum_{n=0}^\infty (-1)^n \frac{x^{{\boxed{2n}}}}{{\boxed{(2n)}}!}, x \in (-\infty, +\infty)$
    * $\frac{1}{1-x} = \sum_{n=0}^\infty x^n, x \in (-1, 1)$
    * $\ln(1+x) = \sum_{n=0}^\infty (-1)^n \frac{x^{n+1}}{n+1}, x \in (-1, 1]$
* **做题步骤**:
    1.  **变形**: 将目标函数通过代数变形, <span style="border-bottom: 2px solid black;">凑成</span>某个<span style="border-bottom: 2px solid black;">基本</span>展开式的形式。
    2.  **代换/运算**:
        * 例如, 求 $e^{-x^2}$ 的展开, 就在 $e^u$ 的展开式中<span style="border-bottom: 2px solid black;">令 $u=-x^2$</span>。
        * 例如, 求 $\frac{x}{1+x^2}$, 就在 $\frac{1}{1-u}$ 中令 $u=-x^2$ 再整体乘以 $x$。
    3.  **求导/积分**: 例如, 求 $\arctan x$ 的展开式, 可以先<span style="border-bottom: 3px dotted black;">求</span>其<span style="border-bottom: 3px dotted black;">导数</span> $(\arctan x)' = \frac{1}{1+x^2}$ 的展开式, 然后再<span style="border-bottom: 2px solid black;">逐项积分</span>回来。

### **四、幂级数<span style="border-bottom: 2px solid black;">求和</span>函数**

* **通式通法**: 逐项求导or逐项积分, 将未知的数项级数或幂级数凑成已知和函数的幂级数形式。
* **做题步骤**:
    1.  **观察结构**: 观察级数通项, 看它像哪个基本展开式的通项求导或积分后的结果。例如, 看到分母有 $n+1$, 想到可能是积分得到的; 看到分子有系数 $n$, 想到可能是求导得到的。
    2.  **构造辅助函数**: 写出该幂级数的和函数 $S(x)$。对 $S(x)$ 进行逐项求导或积分, 得到一个新的、更容易求和的幂级数 $S_1(x)$。
    3.  **求和并还原**: 求出 $S_1(x)$ 的和函数 (通常是某个初等函数), 然后再通过积分或求导的逆运算, 还原出 $S(x)$ (注意处理积分常数)。