
https://vwg48dhsr5g.feishu.cn/docx/WsekdASuVoRzpMxwgt9cKtjlnEb?from=from_copylink ←detail
### 考研数学二：常微分方程求解核心方法汇总

| **方程大类** | **方程类型** | **方程通式** | **求解核心步骤** |
| :--- | :--- | :--- | :--- |
| **一阶<br>常微分方程** | **1. 可分离变量方程** | $\frac{dy}{dx} = f(x)g(y)$ | 1.  **分离变量**：将方程变形为 $\frac{dy}{g(y)} = f(x)dx$ (确保 $g(y) \neq 0$ )。<br>2.  **两边积分**：$ \int \frac{dy}{g(y)} = \int f(x)dx + C $。<br>3.  **求解**：计算积分，得到含有任意常数 C 的隐式或显式通解。 |
| | **2. 齐次方程** | $\frac{dy}{dx} = \varphi(\frac{y}{x})$ | 1.  **变量代换**：令 $ u = \frac{y}{x} $，则 $ y = ux $，$ \frac{dy}{dx} = u + x\frac{du}{dx} $。<br>2.  **代入化简**：原方程变为 $ u + x\frac{du}{dx} = \varphi(u) $。<br>3.  **分离变量**：整理为 $ \frac{du}{\varphi(u) - u} = \frac{dx}{x} $，这变成了可分离变量方程。<br>4.  **求解积分**：积分后得到关于 $u$ 和 $ x $的解。<br>5.  **回代**：将$ u = \frac{y}{x} $ 代回，得到原方程的通解。 |
| | **3. 一阶线性方程** | $\frac{dy}{dx} + P(x)y = Q(x)$ | 1.  **套用通解公式**：直接使用公式求解。<br>    $ y = e^{-\int P(x)dx} \left( \int Q(x)e^{\int P(x)dx} dx + C \right) $。<br>2.  **分步计算**：<br>    a. 计算积分因子 $ \mu(x) = e^{\int P(x)dx} $。<br>    b. 通解为 $ y = \frac{1}{\mu(x)} \left( \int \mu(x)Q(x)dx + C \right) $。 |
| | | | |
| **二阶<br>常微分方程** | **可降阶** |  $y'' = f(x)$ |   **直接积分**：对 $ f(x) $ 连续积分两次。<br>    $ y' = \int f(x)dx + C_1 $。<br>    $ y = \int (\int f(x)dx + C_1)dx + C_2 $。 |
| | |   $y'' = f(x, y')$ <br> (不显含y) | 1.  **降阶**：令 $ p = y' $，则 $ y'' = p' $。<br>2.  **化为一阶方程**：原方程变为 $ p' = f(x, p) $。<br>3.  **求解**：解此关于 $p$ 的一阶方程，得到 $ p = \varphi(x, C_1) $。<br>4.  **还原积分**：由 $ y' = p = \varphi(x, C_1) $，积分得到 $ y = \int \varphi(x, C_1)dx + C_2 $。 |
| | |   $y'' = f(y, y')$ <br> (不显含x) | 1.  **降阶**：令 $ p = y' $，则 $ y'' = \frac{dp}{dx} = \frac{dp}{dy} \cdot \frac{dy}{dx} = p\frac{dp}{dy} $。<br>2.  **化为一阶方程**：原方程变为 $ p\frac{dp}{dy} = f(y, p) $。<br>3.  **求解**：解此关于 $p$ 和 $y$ 的一阶方程，得到 $ p = \psi(y, C_1) $。<br>4.  **还原积分**：由 $ \frac{dy}{dx} = p = \psi(y, C_1) $，分离变量得 $ \frac{dy}{\psi(y, C_1)} = dx $，积分求解。 |
|
| 二阶及<br>n阶**常系数**<br>线性方程 | **齐次**linear e | $y'' + py' + qy = 0$ <br>($p, q$ 为常数) | 1.  **写出特征方程**：$ r^2 + pr + q = 0 $。<br>2.  **求解特征根** $ r_1, r_2 $。<br>3.  **根据特征根写出通解**：<br>    a. **两个不等实根** $ r_1 \neq r_2 $：$ y = C_1e^{r_1x} + C_2e^{r_2x} $。<br>    b. **两个相等实根** $ r_1 = r_2 = r $：$ y = (C_1 + C_2x)e^{rx} $。<br>    c. **一对共轭复根** $ r = \alpha \pm i\beta $：$ y = e^{\alpha x}(C_1\cos(\beta x) + C_2\sin(\beta x)) $。 |
| | **非齐次**.. | $y'' + py' + qy = f(x)$ | **通解 = 齐次通解 + 非齐次特解 ($y = y_c + y_p$)**<br>1.  **求齐次通解** $ y_c $：求解对应齐次方程 $y'' + py' + qy = 0$ (见类型6)。<br>2.  **求非齐次特解** $y_p$ (使用待定系数法):<br>    **情况一: $ f(x) = P_m(x)e^{\lambda x} $**<br>    设特解 $ y_p = x^k Q_m(x)e^{\lambda x} $，其中 $Q_m(x)$ 是与 $P_m(x)$ 同次的一般多项式。<br>    $k$ 的取值取决于 $\lambda$ 是否为特征根：<br>    - $\lambda$ **不是**特征根，则 $ k=0 $。<br>    - $\lambda$ **是单**特征根，则 $ k=1 $。<br>    - $\lambda$ **是重**特征根，则 $ k=2 $。<br>    **情况二: $ f(x) = e^{\alpha x}[P_l(x)\cos(\beta x) + P_n(x)\sin(\beta x)] $**<br>    设特解 $ y_p = x^k e^{\alpha x}[R_m(x)\cos(\beta x) + S_m(x)\sin(\beta x)] $，其中 $ m = \max{l, n} $，$ R_m(x), S_m(x) $是$ m $ 次一般多项式。<br>    $k$ 的取值取决于 $\alpha \pm i\beta$ 是否为特征根：<br>    - $\alpha \pm i\beta$ **不是**特征根，则 $ k=0 $。<br>    - $\alpha \pm i\beta$ **是**特征根，则 $ k=1 $。<br>3.  **写出总通解**：将求得的 $y_c$ 和 $y_p$ 相加。 |
| | | | |
| | **n阶常系数齐次线性方程** | $y^{(n)} + a_1y^{(n-1)} + \dots + a_{n-1}y' + a_ny = 0$ | 1.  **写出特征方程**：$ r^n + a_1r^{n-1} + \dots + a_n = 0 $。<br>2.  **求解所有特征根**。<br>3.  **叠加通解**：<br>    - 每个 **k重实根** $ r $，对应解的部分为 $ (C_1+C_2x+\dots+C_kx^{k-1})e^{rx} $。<br>    - 每对 **k重共轭复根** $ \alpha \pm i\beta $，对应解的部分为 $ e^{\alpha x}[(A_1+\dots+A_kx^{k-1})\cos(\beta x) + (B_1+\dots+B_kx^{k-1})\sin(\beta x)] $。<br>4.  将所有根对应的解相加得到总通解。 |

**核心备考建议**：

  * **第一步永远是判别类型**：拿到题目后，首先要准确判断它属于以上哪种类型。
  * **计算要准确**：积分计算、解代数方程（尤其是特征方程）是基础，务必保证准确性。
  * **待定系数法是重点**：对于二阶常系数非齐次方程，$k$ 值的判断是核心和难点，一定要熟练掌握。
  * **公式要记牢**：一阶线性方程的通解公式必须烂熟于心，可以节约大量时间。
---

- 常系数:
  - 系数为 常数
  - ↑常规 常微分方程
    - 系数可以含x等变量 ←exactly is 变系数 de