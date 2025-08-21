



**第二部分：高等数学章节精讲**

# Base

## **Limit & continuity**

### **第1讲 函数极限与连续**

#### **一、函数极限的<span style="border-bottom: 2px solid black;">定义</span>及使用**

* **重要的公式与概念定义**
    * $\epsilon-\delta$ 定义: $\lim_{x \to x_0} f(x) = A \iff \forall \epsilon > 0, \exists \delta > 0$, 当 $0 < |x - x_0| < \delta$ 时, 有 $|f(x) - A| < \epsilon$.
    * 左右极限: $\lim_{x \to x_0} f(x) = A \iff \lim_{x \to x_0^-} f(x) = \lim_{x \to x_0^+} f(x) = A$.

* **涉及的重要题型**
    * **题型**: 用定义证明极限。
    * **通式通法**: 核心是找到 $\delta$ 与 $\epsilon$ 的关系。
    * **做题步骤**:
        1.  **化简**: 从不等式 $|f(x) - A| < \epsilon$ 出发, 进行化简变形, 使其能够出现 $|x - x_0|$ 因子。
        2.  **寻找**: 通过<span style="border-bottom: 2px solid black;">放缩</span>法, 建立 $|x-x_0|$ 与 $\epsilon$ 的关系, 从而找到一个合适的 $\delta$ (通常是 $\epsilon$ 的表达式)。
        3.  **书写**: 按定义格式, 清晰地写出证明过程。

#### **二、函数极限的<span style="border: 1px solid black; padding: 5px; display: inline-block;">计算</span>**

* **重要的公式与概念定义**
    * 两个重要极限:<span style="border: 1px solid black; padding: 5px; display: inline-block;">
        * $\lim_{x \to 0} \frac{\sin x}{x} = 1$
        * $\lim_{x \to \infty} (1 + \frac{1}{x})^x = e$ 或 $\lim_{x \to 0} (1 + x)^{\frac{1}{x}} = e$</span>
    * 等价无穷小替换 (当 $x \to 0$ 时):
        * $\sin x \sim x$, $\tan x \sim x$, $\arcsin x \sim x$, $\arctan x \sim \boxed{x}$
        * $1 - \cos x \sim \frac{1}{2}x^2$
        * $e^x - 1 \sim \boxed{x}$, $a^x - 1 \sim x \ln a$
        * $\ln(1+x) \sim \boxed{x}$, $\log_a(1+x) \sim \frac{x}{\ln a}$
        * $(1+x)^\alpha - 1 \sim \alpha x$
    * 洛必达法则: 若 <span style="border: 1px solid black; padding: 5px; display: inline-block;">$\lim \frac{f(x)}{g(x)}$ 是 $\frac{0}{0}$ 或 $\frac{\infty}{\infty}$ 型, 且 $\lim \frac{f'(x)}{g'(x)}$ 存在(或为$\infty$)</span>, $\Rightarrow$ $\lim \frac{f(x)}{g(x)} = \lim \frac{f'(x)}{g'(x)}$.
    * 泰勒公式 (麦克劳林公式):
        $f(x) = f(0) + f'(0)x + \frac{f''(0)}{2!}x^2 + \dots + \boxed{\frac{f^{(n)}(0)}{n!}x^n} + o(x^n)$

* **涉及的重要题型**
    * **题型1: <span style="border: 1px solid black; padding: 5px; display: inline-block;">$\frac{0}{0}$ 或 $\frac{\infty}{\infty}$ </span>型**
        * **通式通法**: 方法优先级：等价<span style="border-bottom: 3px dotted black;">无穷小</span> $\rightarrow$ <span style="border-bottom: 2px solid black;">洛必达</span>法则 $\rightarrow$ 泰勒展开。
        * **做题步骤**:
            1.  **先替换**: 观察式子中是否有可用的等价无穷小, 尤其是乘除部分, 优先替换简化。
            2.  **再洛必达**: 替换后若仍为不定式, 使用洛必达法则。对于复杂乘积的求导要细心。
            3.  **终极泰勒**: 若洛必达法则使用复杂或失效(如导数不存在或循环), 或出现加减法抵消的情况, 优先考虑泰勒展开, 特别是展开到非零的最低次项。
    * **题型2: $0 \cdot \infty$, $\infty - \infty$, <span style="border-bottom: 2px solid black;">$1^\infty$, $0^0$, $\infty^0$</span> 型**
        * **通式通法**: 核心思想是转化为 $\frac{0}{0}$ 或 $\frac{\infty}{\infty}$ 型。
        * **做题步骤**:
            1.  <span style="border-bottom: 2px solid black;">**变形**</span>: 将 $0 \cdot \infty$ 化为 $\frac{0}{1/\infty}$ 或 $\frac{\infty}{1/0}$; 将 $\infty - \infty$ 通过通分、有理化或变量替换等方法合并。
            2.  **取指对**: 对 $1^\infty, 0^0, \infty^0$ 型, 设原极限为 $A$, 取对数 $\lim \ln A$ 转化为 $0 \cdot \infty$ 型, 再按步骤1处理。
                1.  **还原**: 求出 $\lim \ln A = B$ 后, 务必记得原极限 $A = e^B$。

#### **三、函数极限的<span style="border-bottom: 2px solid black;">存在性</span>**

* **重要的公式与概念定义**
    * <span style="border-bottom: 2px solid black;">夹逼</span>定理 (Squeeze Theorem): 若在 $x_0$ 某去心邻域内, $g(x) \le f(x) \le h(x)$, 且 <span style="border: 1px solid black; padding: 5px; display: inline-block;">$\lim_{x \to x_0} g(x) = \lim_{x \to x_0} h(x) = A$</span>, $\Rightarrow$ <span style="border: 1px solid black; padding: 5px; display: inline-block;">$\lim_{x \to x_0} f(x) = A$</span>.
    * <span style="border-bottom: 2px solid black;">单调有界</span>准则: 单调有界数列必有极限。

* **涉及的重要题型**
    * **题型**: 证明极限存在并求极限。
    * **通式通法**: 常用夹逼定理和单调有界准则。
    * **做题步骤**:
        1.  **观察函数/数列结构**: 如果是复杂函数或含n项和/积的数列, 优先考虑夹逼。如果是递推关系式定义的数列, 优先考虑单调有界。
        2.  **构造夹逼/证明单调有界**:
            * 夹逼: 通过放缩法找到两个极限相同的更简单的函数/数列来“夹住”目标。
            * 单调有界: 用作差/作商法或数学归纳法证明单调性, 用放缩法证明有界性。
        3.  **求极限**: 利用夹逼定理直接得出极限, 或对递推式两边同时取极限解出 $A = f(A)$。

#### **四、函数极限的应用——<span style="border: 1px solid black; padding: 5px; display: inline-block;">连续 间断</span>**

* **重要的公式与概念定义**
    * 函数连续性: 
      * <span style="border: 1px solid black; padding: 5px; display: inline-block;">存在&&相等</span>
        * $\lim_{x \to x_0} f(x) = \boxed{f(x_0)} \iff \lim_{x \to x_0^-} f(x) = \lim_{x \to x_0^+} f(x) = f(x_0)$.
    * 间断点分类:
        * 第一类: <span style="border-bottom: 3px dotted black;">左右</span>极限<span style="border-bottom: 3px dotted black;">都</span>存在。(可去间断点: $L=R \ne f(x_0)$; 跳跃间断点: $L \ne R$)
        * 第二类: <span style="border-bottom: 2px solid black;">至少一个</span>左右极限<span style="border-bottom: 2px solid black;">不存在</span>。(无穷间断点, 震荡间断点)

* **涉及的重要题型**
    * **题型**: 讨论函数的连续性, 判断间断点类型。
    * **通式通法**: 紧扣定义, 计算分段点或无定义点的左极限、右极限和函数值。
    * **做题步骤**:
        1.  **找可疑点**: 找出函数定义域的分段点、无定义点、或以任何形式导致函数表达式发生改变的点。
        2.  **三项计算**: 计算在这些可疑点 $x_0$ 处的左极限 $\lim_{x \to x_0^-} f(x)$、右极限 $\lim_{x \to x_0^+} f(x)$ 和函数值 $f(x_0)$。
        3.  **下结论**: 根据三者的关系, 依据定义判断该点是连续点还是何种类型的间断点。
    ---
### **第2讲 数列极限**

#### **一、数列极限的定义及使用**

* **重要的公式与概念定义**
    * $\epsilon-N$ 定义: $\lim_{n \to \infty} x_n = A \iff \forall \epsilon > 0, \exists N \in \mathbb{N}^+$, 当 $n > N$ 时, 有 $|x_n - A| < \epsilon$.

* **涉及的重要题型**: 与函数极限类似, 定义主要用于理论证明, 计算题中较少直接使用。

#### **二、数列极限的存在性与<span style="border: 1px solid black; padding: 5px; display: inline-block;">计算</span>**

* **重要的公式与概念定义**
    * 单调有界准则: 单调有界数列必有极限。
    * <span style="border: 1px solid black; padding: 5px; display: inline-block;">夹逼</span>定理: 若 $y_n \le x_n \le z_n$, 且 $\lim_{n \to \infty} y_n = \lim_{n \to \infty} z_n = A$, 则 $\lim_{n \to \infty} x_n = A$.
    * 函数极限与数列极限关系 (<span style="border: 1px solid black; padding: 5px; display: inline-block;">海涅</span>定理): 若 $\lim_{x \to x_0} f(x) = A$, 则对任何<span style="border-bottom: 2px solid black;">以 $x_0$ 为极限</span>的数列 $\{x_n\}$ ($x_n \ne x_0$), 都有 $\lim_{n \to \infty} f(x_n) = A$. (常用于将数列极限转化为函数极限)。

* **涉及的重要题型**
    * **题型1: 递推数列 $x_{n+1}=f(x_n)$**
        * **通式通法**: 单调有界准则。
        * **做题步骤**:
            1.  **证明有界**: 用数学归纳法或放缩法证明数列 $\{x_n\}$ 有上界或下界。
            2.  **证明单调**: 用 $x_{n+1} - x_n$ 的符号或 $\frac{x_{n+1}}{x_n}$ 与1的大小关系判断单调性。
            3.  **求解极限**: 设 $\lim_{n \to \infty} x_n = A$, 对递推式两边取极限, 解方程 $A=f(A)$。
    * **题型2: n项和或n项积的极限**
        * **通式通法**: 夹逼定理或定积分定义法。
        * **做题步骤**:
            1.  **识别类型**: 观察式子结构。如果是和式且每项分母为 $n$, 分子是关于 $i$ 的函数, 形如 $\lim_{n \to \infty} \sum_{i=1}^n \frac{1}{n} f(\frac{i}{n})$, 考虑定积分定义。否则考虑夹逼。
            2.  **实施方法**:
                * 定积分法: 将和式凑成 $\int_0^1 f(x)dx$ 的形式并计算。
                * 夹逼法: 将和或积的每一项进行适当的放缩(通常是放大分母/缩小分子得到下界, 缩小分母/放大分子得到上界), 使得上下界易于求极限且极限值相等。
            3.  **得出结论**: 根据定理得出最终极限值。

---

## **differential**

### **第3讲 概念**

#### **一、导数定义（导数在一点的问题）**

* **重要的公式与概念定义**
    * 导数定义: $f'(x_0) = \lim_{\Delta x \to 0} \boxed{\frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x}} = \lim_{x \to x_0} \boxed{\frac{f(x) - f(x_0)}{x - x_0}}$.
    * 导数与连续关系: 可导<span style="border-bottom: 2px solid black;">必连续</span>, 连续不一定可导。
    * 左右导数: $f'(x_0)$ 存在 $\iff f'_-(x_0) = f'_+(x_0)$.

* **涉及的重要题型**
    * **题型**: 利用导数定义求<span style="border-bottom: 2px solid black;">某一点</span>的导数, 或判断<span style="border-bottom: 2px solid black;">可导性</span>。
    * **通式通法**: 严格套用导数定义式, 转化为求一个极限问题。
    * **做题步骤**:
        1.  **写定义**: 准确写出 $f'(x_0)$ 的定义式。对于分段函数在分段点的可导性, 需要分别写出左导数和右导数的定义式。
        2.  **代入计算**: 将函数表达式代入, 计算极限。此时可能会用到前面求极限的各种方法。
        3.  **比较判断**: 如果是判断可导性, 比较计算出的左右导数是否相等。若相等则可导, 否则不可导。

#### **二、微分**

* **重要的公式与概念定义**
    * 微分定义: 若 $\Delta y = f(x_0 + \Delta x) - f(x_0) = A \Delta x + o(\Delta x)$, 则称函数 $f(x)$ 在 $x_0$ 点可微, 且 <span style="border: 1px solid black; padding: 5px; display: inline-block;">$dy = A \Delta x$</span>.
    * 可微与可导关系: 函数在某点可微的 $\iff$ 该函数在该点可导, 且 <span style="border: 1px solid black; padding: 5px; display: inline-block;">$dy = f'(x) dx$</span>.

* **涉及的重要题型**
    * **题型**: 求函数的微分。
    * **通式通法**: 微分就是导数乘以 $dx$。
    * **做题步骤**:
        1.  **求导数**: 计算出函数 $f(x)$ 的导数 $f'(x)$。
        2.  **乘dx**: 将求得的导数乘以 $dx$, 即得微分 $dy = f'(x) dx$.

### **第4讲 计算**

#### **一、基本求导<span style="border-bottom: 3px dotted black;">公式</span>**

* **重要的公式与概念定义**:
    * $(C)'=0$, $(x^\alpha)'=\alpha x^{\alpha-1}$, $(\sin x)'=\cos x$, $(\cos x)'=-\sin x$,<span style="border: 1px solid black; padding: 5px; display: inline-block;">$(\tan x)'=\sec^2 x$, $(\cot x)'=-\csc^2 x$, $(\sec x)'=\sec x \tan x$, $(\csc x)'=-\csc x \cot x$</span>.
    * $(e^x)'=e^x$, $(a^x)'=a^x \ln a$.
    * $(\ln |x|)'=\frac{1}{x}$, <span style="border: 1px solid black; padding: 5px; display: inline-block;">$(\log_a |x|)'=\frac{1}{x \ln a}$</span>.
    * $(\arcsin x)'=\frac{1}{\sqrt{1-x^2}}$, $(\arccos x)'=-\frac{1}{\sqrt{1-x^2}}$, $(\arctan x)'=\frac{1}{1+x^2}$, $(\text{arccot } x)'=-\frac{1}{1+x^2}$.
    * 四则运算法则: $(u \pm v)' = u' \pm v'$, $(uv)' = u'v + uv'$, $(\frac{u}{v})' = \frac{u'v - uv'}{v^2}$.
    ---
#### **二、复合函数求导**

* **通式通法**: 链式法则 (Chain Rule): 若 $y=f(u)$, $u=g(x)$, 则 $\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx} $= <span style="border: 1px solid black; padding: 5px; display: inline-block;">$f'(g(x))g'(x)$</span>.
* **做题步骤**:
    1.  **分层**: 将复杂函数从外到内分解成基本函数的复合。
    2.  **逐层求导**: 从最外层函数开始, 对每一层函数求导。
    3.  **相乘**: 将各层求导的结果连乘起来。

#### **三、隐..**

* **通式通法**: 方程 $F(x, y) = 0$ <span style="border-bottom: 3px dotted black;">两边</span>对 $x$ 求导, 视 <span style="border-bottom: 2px solid black;">$y$ 为 $x$ 的函数</span>。
* **做题步骤**:
    1.  **两边求导**: 将方程 $F(x,y)=0$ 两边同时对自变量 $x$ 进行求导。
    2.  **注意链式法则**: 遇到含有 $y$ 的项时, 要使用链式法则, 即 $(f(y))' = \boxed{f'(y) \cdot y'}$.
    3.  **解出$y'$**: 求导后得到一个关于 $y'$ 的代数方程, 从中解出 $y'$ 的表达式。

#### **四、反..**

* **通式通法**: 若 $y=f(x)$ 的反函数为 $x=g(y)$, 则 $g'(y) = \boxed{\frac{1}{f'(x)}}$ 或 $\frac{dx}{dy} = \frac{1}{dy/dx}$.
* **做题步骤**:
    1.  **求原函数导数**: 计算出 $y=f(x)$ 的导数 $f'(x)$。
    2.  **取倒数**: 直接取导数的倒数, $\frac{1}{f'(x)}$。
    3.  **变量替换**: 将表达式中的 $x$ 用反函数 <span style="border-bottom: 2px solid black;">$g(y)$ 替换</span>, 得到完全以 $y$ 为变量的结果。

#### **五、分段..（含绝对值）**

* **通式通法**: 分段点处用<span style="border-bottom: 2px solid black;">定义</span>求, 非分段点处直接用公式求。
* **做题步骤**:
    1.  **处理非分段点**: 在每个分段区间内部, 函数有明确的表达式, 直接套用求导公式。
    2.  **处理分段点**: 在分段点 $x_0$, 必须用左右导数的定义分别求 $f'_-(x_0)$ 和 $f'_+(x_0)$。
    3.  **比较下结论**: 比较左右导数是否相等, 以判断在分段点是否可导。绝对值函数先化为分段函数再处理。

#### **六、<span style="border: 1px solid black; padding: 5px; display: inline-block;">对数</span>..**

* **适用场合**: 多个函数<span style="border-bottom: 3px dotted black;">连乘、连除或开方</span>, 形式复杂。
* **做题步骤**:
    1.  **两边取对数**: 在方程 $y=f(x)$ 两边同时取自然对数 <span style="border: 1px solid black; padding: 5px; display: inline-block;">$\ln y = \ln f(x)$</span>。
    2.  **化简并求导**: 利用对数的性质将乘除化为加减, 幂指化为乘法, 然后两边对 $x$ <span style="border-bottom: 2px solid black;">隐函数求导</span>, 得 $\frac{1}{y} y' = (\ln f(x))'$.
    3.  **解出$y'$**: 将右侧求导结果乘以 $y$, 并将 $y$ 用 $f(x)$ 代回, 即 $y' = y \cdot (\ln f(x))' = f(x) \cdot (\ln f(x))'$.

#### **七、幂指..**

* **适用场合**: $y = [f(x)]^{g(x)}$ 型函数。
* **通式通法**: 方法一: 改写为<span style="border: 1px solid black; padding: 5px; display: inline-block;"> $y = e^{g(x)\ln f(x)}$</span> 再求导。方法二: 对数求导法。
* **做题步骤 (方法一)**:
    1.  **指数化**: 将 $y = [f(x)]^{g(x)}$ 改写为 $y=e^{g(x)\ln f(x)}$。
    2.  **复合求导**: 对 $e$ 的指数函数进行<span style="border-bottom: 2px solid black;">复合函数求导</span>。
    3.  **整理**: $y' = e^{g(x)\ln f(x)} \cdot [g'(x)\ln f(x) + g(x)\frac{f'(x)}{f(x)}] = [f(x)]^{g(x)} [g'(x)\ln f(x) + \frac{g(x)f'(x)}{f(x)}]$。

#### **八、Parametric equation..**

* **通式通法**:
    * 一阶导数: $\frac{dy}{dx} = \frac{dy/dt}{dx/dt} = \boxed{\frac{\psi'(t)}{\phi'(t)}}$.
    * 二阶导数: $\frac{d^2y}{dx^2} = \frac{d}{dx}(\frac{dy}{dx}) = \frac{d(\frac{\psi'(t)}{\phi'(t)})/dt}{dx/dt}$.
* **做题步骤**:
    1.  **求一阶导**: 分别求 $y$ 和 $x$ 对参数 $t$ 的导数, 然后相除。
    2.  **求二阶导预备**: 将一阶导数结果看作一个关于 $t$ 的新函数, 对 $t$ 求导。
    3.  **再除$x$对$t$的导**: 将上一步的结果再除以 $dx/dt$, 得到二阶导数。

#### **九、高阶导数**

* **通式通法**: 归纳法或利用莱布尼茨公式。
* **莱布尼茨公式**: $(uv)^{(n)} = \sum_{k=0}^n C_n^k u^{(n-k)}v^{(k)}$.
* **做题步骤**:
    1.  **直接计算**: 先求一、二、三阶导数, 观察规律, 用数学归纳法写出 $n$ 阶导数表达式。
    2.  **公式法**: 对两个函数乘积求高阶导数, 直接使用莱布尼茨公式。
    3.  **分解**: 将复杂函数分解为基本函数的和, 再分别求高阶导数。

    ---
好的，我们继续上一部分未完成的内容，从第五讲开始。

    ---
### **第5讲 一元函数微分学的应用（一）——几何应用**

#### **一、研究对象**

* **重要的公式与概念定义**
    * **切线与法线**:
        * 切线方程: $y - y_0 = f'(x_0)(x - x_0)$
        * 法线方程: $y - y_0 = \boxed{-\frac{1}{f'(x_0)}}(x - x_0)$ (当 $f'(x_0) \ne 0$)
    * **曲率K**: $K = \boxed{\frac{|y''|}{(1 + y'^2)^{3/2}}}$
    * **曲率半径R**: $R = \frac{1}{K}$

#### **二、研究内容 (函数图像的性态)**

* **重要的公式与概念定义**
    * **单调性**:
        * $f'(x) > 0 \implies f(x)$ 单调递增
        * $f'(x) < 0 \implies f(x)$ 单调递减
    * **极值**:
        * 必要条件: $f'(x_0)=0$ 或 $f'(x_0)$ 不存在, 则 $x_0$ 为驻点或尖点，可能是极值点。
        * 第一充分条件: $f'(x)$ 在 $x_0$ 两侧异号。
        * 第二充分条件: <span style="border-bottom: 2px solid black;">$f'(x_0)=0$ 且 $f''(x_0) \ne 0$</span>。($f''(x_0)<0$ 为极大值, $f''(x_0)>0$ 为极小值)。
    * **凹凸性**:
        * $f''(x) > 0 \implies$ 曲线是凹的 (concave up)
        * $f''(x) < 0 \implies$ ..凸.. (concave down)
    * **拐点**:
        * 必要条件: $f''(x_0)=0$ 或 $f''(x_0)$ 不存在。
        * 充分条件: $f''(x)$ 在 $x_0$ 两侧<span style="border-bottom: 2px solid black;">异号</span>。
    * **<span style="border-bottom: 3px dotted black;">渐近线</span>**:
        * 水平渐近线: $\lim_{x \to \infty} f(x) = A \implies y=A$
        * 垂直渐近线: $\lim_{x \to x_0} f(x) = \infty \implies x=x_0$
        * 斜渐近线: $y=ax+b$, 其中 $a = \lim_{x \to \infty} \boxed{\frac{f(x)}{x}}$, $b = \lim_{x \to \infty} \boxed{[f(x) - ax]}$

* **涉及的重要题型**
    * **题型**: 全面研究函数性态并绘制草图, 或求单调区间、极值、凹凸区间、拐点、渐近线。
    * **通式通法**: 系统化流程：定义域 $\rightarrow$ <span style="border-bottom: 3px dotted black;">一</span>阶导数 $\rightarrow$ <span style="border-bottom: 3px dotted black;">二</span>阶导数 $\rightarrow$ 渐近线。
    * **做题步骤**:
        1.  **一阶信息**: 求 $f'(x)$, 令其等于0或不存在, 找出驻点和不可导点。用这些点划分定义域, 判断各区间 $f'(x)$ 的符号, 确定单调区间和极值点。
        2.  **二阶信息**: 求 $f''(x)$, 令其等于0或不存在, 找出可能的拐点。用这些点划分定义域, 判断各区间 $f''(x)$ 的符号, 确定凹凸区间和拐点。
        3.  **综合分析**: 结合极限思想求出所有渐近线, 并将上述所有信息(单调性、极值、凹凸性、拐点、渐近线)整合, 绘制函数大致图像。

---
### **第6讲 一元函数微分学的应用（二）——中值定理、微分等式与微分不等式**

#### **一、中值定理**

* **重要的公式与概念定义**
    * **费马引理 (Fermat's Theorem)**: 若 $f(x)$ 在 $x_0$ 处<span style="border-bottom: 2px solid black;">可导且取极值</span>, 则 $f'(x_0)=0$。
    * **罗尔定理 (Rolle's Theorem)**: 若 $f(x)$ 在 $[a,b]$ 连续, $(a,b)$ 可导, 且 $f(a)=f(b)$, 则 $\exists \xi \in (a,b)$ 使得 <span style="border-bottom: 3px dotted black;">$f'(\xi)=0$</span>。
    * **<span style="border: 1px solid black; padding: 5px; display: inline-block;">拉格朗日</span>中值定理 (Lagrange's Mean Value Theorem)**: 若 $f(x)$ 在 $[a,b]$ 连续, $(a,b)$ 可导, 则 $\exists \xi \in (a,b)$ 使得 $f'(\xi) = \boxed{ \frac{f(b)-f(a)}{b-a}}$。
    * **柯西中值定理 (Cauchy's Mean Value Theorem)**: 若 $f(x), g(x)$ 在 $[a,b]$ 连续, $(a,b)$ 可导, 且 $g'(x) \ne 0$, 则 $\exists \xi \in (a,b)$ 使得 $\frac{f'(\xi)}{g'(\xi)} = \boxed{\frac{f(b)-f(a)}{g(b)-g(a)}}$。
    * **泰勒中值定理 (Taylor's Theorem with Lagrange Remainder)**: ...则 $f(x) = \sum_{k=0}^{n-1} \frac{f^{(k)}(x_0)}{k!}(x-x_0)^k + \boxed{\frac{f^{(n)}(\xi)}{n!}(x-x_0)^n}$。

* **涉及的重要题型**
    * **题型**: 证明存在点 $\xi$ 使其导数/函数值满足某个等式。
    * **通式通法**: 核心是构造<span style="border-bottom: 2px solid black;">辅助函数</span>, 将问题转化为罗尔定理的应用。
    * **做题步骤**:
        1.  **变形**: 将要证明的结论 $\dots = 0$ 变形, 使得左侧的结构能看出某个函数的导数形式。例如, 看到 <span style="border: 1px solid black; padding: 5px; display: inline-block;">$f'(\xi) + g(\xi)f(\xi) = 0$</span>, 就要联想到 $[e^{G(x)}f(x)]'$ (其中$G'(x)=g(x)$)。
        2.  **构造**: 构造辅助函数 $F(x)$, 其形式通常是将变形后的等式“积分”回去。常用形式有 $F(x)=f(x)$, $F(x)=f(x)g(x)$, $F(x)=\frac{f(x)}{g(x)}$, $F(x) = f(x)e^{\phi(x)}$等。
        3.  **验证**: 验证构造的 $F(x)$ 在某个区间 $[a,b]$ 上满足罗尔定理的条件 ($F(a)=F(b)$), 从而证明结论。若涉及二阶导数 $f''(\xi)$, 则需对 $f'(x)$ 和另一个函数应用罗尔定理, 或者对 $F(x)$ 使用两次罗尔定理。

#### **二、微分等式问题（方程的<span style="border-bottom: 3px dotted black;">根</span>、函数的<span style="border-bottom: 2px solid black;">零点</span>）**

* **通式通法**: 结合函数的单调性与零点存在定理/介值定理。
* **做题步骤**:
    1.  **存在性**: 利用零点存在定理（若 $f(x)$ 在 <span style="border: 1px solid black; padding: 5px; display: inline-block;">$[a,b]$ 连续& $f(a)f(b)<0$</span>, 则 $\exists \xi \in (a,b)$ 使 $f(\xi)=0$）证明根至少存在一个。
    2.  **唯一性**: 求导 $f'(x)$, 分析其在区间内的符号。若 $f'(x)$ 恒大于零或恒小于零, 则函数单调, 根最多只有一个。
    3.  **下结论**: 结合以上两步, 得出根唯一存在。

#### **三、微分不等式问题**

* **通式通法**: 将不等式移项, 构造<span style="border-bottom: 2px solid black;">辅助函数</span>, 利用函数的单调性证明。
* **做题步骤**:
    1.  **构造函数**: 将要证的不等式, 如 $f(x) > g(x)$ (对 $x>a$), 移项构造成 <span style="border: 1px solid black; padding: 5px; display: inline-block;">$F(x) = f(x) - g(x) > 0$</span>。
    2.  **求导判断单调性**: 计算 $F'(x)$, 并判断其在 $x>a$ 区间内的符号, 从而确定 $F(x)$ 的单调性。
    3.  **利用端点值**: 计算 $F(a)$ 的值 (通常 $F(a)=0$)。结合单调性（如 $F(x)$ 递增）和端点值, 得出 $F(x) > F(a) = 0$, 从而原不等式得证。

### **第7讲 一元函数微分学的应用（三）——物理应用与经济应用**

* **物理应用**: 主要考察<span style="border-bottom: 2px solid black;">变化率</span>问题。如速度是位移对时间的导数 $v(t) = s'(t)$, 加速度是速度对时间的导数 $a(t) = v'(t)$。相关变化率问题核心是找出变量间的关系式, 然后两边对时间 $t$ 求导。
* **经济应用**: 主要涉及边际与弹性的概念。（数一不作要求）

---
## **integral**

### **第8讲 概念与性质**

#### **一、祖孙三代**

* **重要的公式与概念定义**
    * **原函数**: 若 $F'(x)=f(x)$, 则 $F(x)$ 是 $f(x)$ 的一个原函数。
    * **不定积分**: $f(x)$ 的全体原函数称为 $f(x)$ 的不定积分, 记作 $\int f(x)dx = \boxed{F(x)} + C$ 。
    * **定积分**: $\int_a^b f(x)dx$ 是一个数值, 代表函数图像在 $[a,b]$ 区间上与x轴围成的面积的代数和。
    * **变上限积分函数**: $\Phi(x) = \int_a^x f(t)dt$ 是一个函数, 且 $(\int_a^x f(t)dt)' = f(x)$。

#### **二、积分比大小**

* **通式通法**: 利用定积分性质。若在 <span style="border-bottom: 3px dotted black;">$[a,b]$ 上 $f(x) \ge g(x)$</span>, 则 $\int_a^b f(x)dx \ge \int_a^b g(x)dx$ ($a<b$)。
* **做题步骤**:
    1.  <span style="border-bottom: 2px solid black;">**作差**</span>: 将要比较的两个积分相减, 合并成一个积分 $\int_a^b [f(x)-g(x)]dx$。
        1.  **判断符号**: 判断被积函数 $f(x)-g(x)$ 在积分区间上的符号。
        2.  **得出结论**: 若被积函数恒为正, 则积分为正, 反之亦然。

#### **三、定义**

* **重要的公式与概念定义**: $\int_a^b f(x)dx = \lim_{\lambda \to 0} \boxed{\sum_{i=1}^n f(\xi_i) \Delta x_i}$ (其中 $\lambda = \max\{\Delta x_i\}$)。
* **涉及的重要题型**: 将<span style="border-bottom: 2px solid black;">极限形式</span>的<span style="border-bottom: 2px solid black;">和</span>式转化为定积分求解。
* **通式通法**: 核心是凑出定积分定义的形式 $\lim_{n \to \infty} \sum_{i=1}^n \boxed{\frac{b-a}{n} f(a + \frac{b-a}{n}i)}$
* **做题步骤**:
    1.  **提取因子**: 从和式中提出因子 $\frac{1}{n}$。
    2.  **变量替换**: 将和式中的 $\boxed{\frac{i}{n}}$ 视作变量 $x$, $\boxed{\frac{1}{n}}$ 视作 $dx$
    3.  **确定积分限**: 观察 $i$ 的变化范围, 如从1到n, 则 $x=\frac{i}{n}$ 的范围近似从0到1, 从而确定积分上下限, 写出定积分并计算。

#### **四、<span style="border: 1px solid black; padding: 5px; display: inline-block;">反常</span>积分的判敛**

* **重要的公式与概念定义**
    * 无穷区间上的反常积分: $\int_a^{+\infty} f(x)dx$
    * 无界函数的反常积分: 在瑕点 $c$ 处, $\int_a^b f(x)dx$
    * p-积分判敛:<span style="border: 1px solid black; padding: 5px; display: inline-block;">
        * $\int_1^{+\infty} \frac{1}{x^p} dx$: 当 $p>1$ 时收敛, $p \le 1$ 时发散。
        * $\int_0^1 \frac{1}{x^p} dx$: 当 $p<1$ 时收敛, $p \ge 1$ 时发散。</span>
* **涉及的重要题型**: 判断反常积分的收敛性。
* **通式通法**: 比较判别法和极限形式的比较判别法。
* **做题步骤**:
    1.  **找到标准**: 观察被积函数 $f(x)$, 在积分的“问题点”(无穷远或瑕点)附近, 找一个行为相似且敛散性已知的简单函数 $g(x)$ (通常是p-积分形式)。
    2.  **求极限**: 计算 $\lim_{x \to \infty (\text{or } x_0)} \frac{f(x)}{g(x)} = L$。
    3.  **下结论**: 若 $0 < L < +\infty$, 则 $\int f(x)dx$ 与 $\int g(x)dx$ 同敛散。若 $L=0$ 或 $L=\infty$, 需结合比较判别法分析。
    ---
### **第9讲 计算**

#### **一、基本积分公式**

* 与基本求导公式<span style="border-bottom: 2px solid black;">互逆</span>, 务必熟记。特别注意: $\int \frac{1}{1+x^2}dx = \arctan x + C$, $\int \frac{1}{\sqrt{1-x^2}}dx = \arcsin x + C$。

#### **二、<span style="border-bottom: 2px solid black;">不定</span>积分的计算**

* **通式通法**: 凑微分法(第一类换元), 变量代换法(第二类换元), 分部积分法。
* **题型1: 凑微分法**
    * **做题步骤**:
        1. **观察**: 观察被积函数, 看是否能写成 $f(g(x))g'(x)$ 的形式。
        2. **凑**: 将 $g'(x)dx$ 凑成 $d(g(x))$。
        3. **积分**: 对变量 $g(x)$ 进行积分。
* **题型2: <span style="border: 1px solid black; padding: 5px; display: inline-block;">分部积分</span>法**
    * **公式**: <span style="border: 1px solid black; padding: 5px; display: inline-block;">$\int u dv = uv - \int v du$</span>.
    * **做题步骤**:
        1. **选u,dv**: 选择谁作 <span style="border-bottom: 3px dotted black;">$u$ 的原则</span>是“反对幂指三”。(反三角函数, 对数函数, 幂函数, 指数函数, 三角函数)。排在前面的优先选作 $u$。
        2. **套公式**: 计算出 $du$ 和 $v = \int dv$, 然后代入分部积分公式。
        3. **再积分**: 计算 $\int v du$, 有时需要再次使用分部积分法。

#### **三、<span style="border-bottom: 3px dotted black;">定</span>积分..**

* **通式通法**: 牛顿-莱布尼茨公式, 换元法, 分部积分法, 利用奇偶性和周期性。
* **牛顿-莱布尼茨公式**: $\int_a^b f(x)dx = F(b) - F(a)$。
* **利用<span style="border: 1px solid black; padding: 5px; display: inline-block;">对称性</span>**:
    * 若 $f(x)$ 为奇函数, 则 $\int_{-a}^a f(x)dx = 0$。
    * 若 $f(x)$ 为偶函数, 则 $\int_{-a}^a f(x)dx = 2\int_0^a f(x)dx$。
* **做题步骤**:
    1. **观察**: 观察被积函数和积分区间。区间是否<span style="border-bottom: 2px solid black;">对称</span> $[-a, a]$？函数有无奇偶性？
    2. **化简**: 利用奇偶性、周期性或一些定积分性质(如 $\int_0^{\pi} xf(\sin x)dx = \frac{\pi}{2}\int_0^{\pi} f(\sin x)dx$)简化计算。
       1. **计算**: 用牛顿-莱布尼茨公式, 或配合换元、分部积分法求解。

#### **四、变限积分..**

* **通式通法**: 核心是变限积分求导。
* **公式**: $\boxed{\frac{d}{dx}} \int_{\phi(x)}^{\psi(x)} f(t)dt = \boxed{f[\psi(x)]\psi'(x)} - f[\phi(x)]\phi'(x)$。
* **涉及的重要题型**: 求含变限积分的函数的导数或极限。
* **做题步骤**:
    1. **识别**: 辨认出题目中的变限积分结构。
    2. **求导**: 若是求导问题, 直接套用上述公式。
    3. **<span style="border-bottom: 2px solid black;">处理极限</span>**: 若是求极限问题, 且为 $\frac{0}{0}$ 型 (当 $x \to a$ 时, $\int_a^x f(t)dt \to 0$), 则常与洛必达法则结合使用, 对分子或分母的变限积分求导。

#### **五、反常积分..**

* **通式通法**: 将反常积分转化为正常定积分的极限。
* **做题步骤**:
    1. **写成极限**:
        * $\int_a^{+\infty} f(x)dx = \boxed{\lim_{b \to +\infty}} \int_a^b f(x)dx$。
        * 若 $c$ 为瑕点, $\int_a^b f(x)dx = \lim_{\epsilon \to 0^+} \int_a^{c-\epsilon} f(x)dx + \lim_{\delta \to 0^+} \int_{c+\delta}^b f(x)dx$。
    2. **计算定积分**: 先把极限符号外的定积分算出来, 结果是关于极限变量(如$b, \epsilon$)的表达式。
    3. **<span style="border-bottom: 2px solid black;">求极限</span>**: 最后计算上一步得到的表达式的极限。若极限存在, 则反常积分收敛于此极限值。

---
### **第10讲 一元函数积分学的应用（一）——几何应用**

* **重要的公式与概念定义**
    * **平面图形面积**:
        * 直角坐标: $S = \int_a^b [f_{上}(x) - f_{下}(x)]dx$ 或 $S = \int_c^d [g_{右}(y) - g_{左}(y)]dy$.
        * 极坐标: $S = \frac{1}{2} \int_\alpha^\beta r^2(\theta)d\theta$.
    * **旋转体体积**:
        * 绕x轴: $V_x = \pi \int_a^b y^2(x) dx$.
        * 绕y轴: $V_y = \pi \int_c^d x^2(y) dy$. (或用壳法: $V_y = 2\pi \int_a^b x f(x) dx$)
    * **<span style="border: 1px solid black; padding: 5px; display: inline-block;">曲线弧长</span>**:
        * 直角坐标: $L = \int_a^b \sqrt{1 + [y'(x)]^2} dx$.
        * 参数方程: $L = \int_\alpha^\beta \sqrt{[x'(t)]^2 + [y'(t)]^2} dt$.
        * 极坐标: $L = \int_\alpha^\beta \sqrt{[r(\theta)]^2 + [r'(\theta)]^2} d\theta$.
    * **旋转曲面面积**: (绕x轴) $S = 2\pi \int_a^b |y(x)| \sqrt{1 + [y'(x)]^2} dx$.

* **涉及的重要题型**: 求面积, 体积, 弧长, 旋转曲面面积。
* **通式通法**: 画图, 选元, 定限, 积分。
* **做题步骤**:
    1. **画草图**: 根据题目描述画出相关曲线和区域的草图, 明确积分区域或旋转体形状。
    2. **选坐标和积分元**: 根据图形特点选择最方便的坐标系(直角/极坐标)。确定积分元(是 $dx$, $dy$ 还是 $d\theta$?), 并写出微元(面积微元 $dA$, 体积微元 $dV$ 等)的表达式。
    3. **定限并积分**: 根据草图确定积分变量的上下限, 列出积分式并计算。

---
### **第11讲 一元函数积分学的应用（二）——积分等式与积分不等式**

* **通式通法**: 与微分中值定理类似, 核心是构造<span style="border-bottom: 2px solid black;">辅助函数</span>, 但这次是利用积分的性质或对变限积分函数求导。
* **做题步骤**:
    1. **构造辅助函数**:
        * **等式证明**: 证明 $\int_a^b f(x)dx = C$ 这类, 常常需要构造一个变限积分函数 $F(x) = \int_a^x f(t)dt$, 然后证明 $F'(x)$ 满足某个性质, 或者证明 $F(b)=C$。
        * **不等式证明**: 类似微分不等式, 构造 $F(x) = \int_a^x f(t)dt - \int_a^x g(t)dt$, 通过证明 $F'(x) = f(x) - g(x)$ 的符号来确定 $F(x)$ 的单调性, 进而证明不等式。
    2. **求导分析**: 对构造的辅助函数求导, 分析其导数的性质 (如符号、零点)。
    3. **积分/代入**: 利用导数的性质推断原函数的性质(如单调性、最值), 或利用<span style="border: 1px solid black; padding: 5px; display: inline-block;">积分中值</span>定理 $\int_a^b f(x)dx = f(\xi)(b-a)$ 进行变换, 从而得证。

### **第12讲 一元函数积分学的应用（三）——物理应用**

* **重要的公式与概念定义**
    * **变力做功**: $W = \int_a^b F(x)dx$ (力 $F(x)$ 沿直线从 $a$ 移动到 $b$)
    * **水压力**: 压力 = 压强 $\times$ 面积。对水平窄条带取微元, $dF = \boxed{p \cdot dA} = \rho g h \cdot w(h)dh$, 然后积分 $F = \int_c^d \rho g h w(h)dh$。
    * <span style="border: 1px solid black; padding: 5px; display: inline-block;">**质心**</span>: $\bar{x} = \frac{\int_a^b \boxed{x} \rho(x) f(x) dx}{\int_a^b \rho(x) f(x) dx}$, $\bar{y} = \frac{\frac{1}{2}\int_a^b \rho(x) f^{\boxed2}(x) dx}{\int_a^b \rho(x) f(x) dx}$ (密度为 $\rho(x)$ 的平面薄片)。

* **通式通法**: 微元法。
* **做题步骤**:
    1. **建立坐标系**: 选择合适的坐标系来描述物理情景。
    2. **取微元**: 在积分变量方向上(如位移、深度)取一个微小量, 计算这个微元对应的物理量 (功微元 $dW$, 压力微元 $dF$ 等)。
    3. **积分求和**: 在指定范围内对微元进行积分, 得到总量。

---
# Multi (多元函数)

## **第13讲 多元函数微积分**

### **概念**
* **偏导数**: $f_x(x_0, y_0) = \frac{\partial z}{\partial x}|_{(x_0,y_0)} = \lim_{\Delta x \to 0} \frac{f(x_0+\Delta x, y_0) - f(x_0, y_0)}{\Delta x}$.
* **全微分**: 若 $\Delta z = A\Delta x + B\Delta y + o(\rho)$, 则称 $f$ 在该点可微, $dz = A\Delta x + B\Delta y = \boxed{\frac{\partial z}{\partial x}}dx + \frac{\partial z}{\partial y}dy$。
* **关系**: 偏导数存在且连续 $\implies$ 可微 $\implies$ 连续 $\implies$ 偏导数存在。

### **复合函数求导法（<span style="border-bottom: 3px dotted black;">链式</span>求导规则）**
* **通式通法**: 画出变量间的依赖关系图, 然后沿着所有能到达目标自变量的路径, 将路径上的偏导数相乘, 最后将所有路径的结果相加。
    * 例如 $z = f(u,v)$, $u = u(x,y)$, $v = v(x,y)$, 则 $\frac{\partial z}{\partial x} = \frac{\partial z}{\partial u}\frac{\partial u}{\partial x} + \frac{\partial z}{\partial v}\frac{\partial v}{\partial x}$。
* **做题步骤**:
    1. **画依赖图**: 清晰画出变量间的复合/依赖关系。
    2. **应用法则**: 根据图, 沿着路径应用链式法则, 写出求导表达式。
    3. **计算代入**: 分别计算路径上的各个偏导数并代入, 注意变量要统一。

### **<span style="border-bottom: 2px solid black;">隐</span>函数求导法**
* **通式通法**:
    * 方程 $F(x,y,z)=0$ 确定 $z=z(x,y)$: $\frac{\partial z}{\partial x} = \boxed{-\frac{F_x}{F_{\boxed{z}}}}$, $\frac{\partial z}{\partial y} = -\frac{F_y}{F_z}$。
    * 方程组 $\begin{cases} F(x,y,u,v)=0 \\ G(x,y,u,v)=0 \end{cases}$ 确定 $u=u(x,y), v=v(x,y)$: 求 $\frac{\partial u}{\partial x}$ 时, 将方程组两边对 $x$ 求偏导, 得到关于 $\frac{\partial u}{\partial x}, \frac{\partial v}{\partial x}$ 的线性方程组, 然后用<span style="border-bottom: 2px solid black;">克拉默法则</span>求解。
* **做题步骤**:
    1. **移项构造**: 将所有项移到一边, 构造 $F(x,y,z)=0$ 的形式。
    2. **套公式/求偏导**:
        * 对于单个方程, 直接套用公式。
        * 对于方程组, 两边对<span style="border-bottom: 2px solid black;">自变量求导</span>, 将要求的因变量看作函数, 其他因变量看作常数。
    3. **求解**: 解代数方程或线性方程组, 得出所求的偏导数。

### **四、多元函数的<span style="border: 1px solid black; padding: 5px; display: inline-block;">极、最值</span>**
* **通式通法**:
    * 无条件极值: 先找驻点, 再用二阶偏导数判别。
    * 条件极值(最值): <span style="border: 1px solid black; padding: 5px; display: inline-block;">拉格朗日乘数</span>法。
    * 闭区域最值: 比较内部驻点和边界上的最值。
* **做题步骤 (无条件极值)**:
    1. **求驻点**: 联立方程组 $\begin{cases} f_x(x,y)=0 \\ f_y(x,y)=0 \end{cases}$ 解出所有驻点 $(x_0, y_0)$。
    2. **计算判别式**: 计算 $A=f_{\boxed{xx}}(x_0,y_0)$, $B=f_{\boxed{xy}}(x_0,y_0)$, $C=f_{\boxed{yy}}(x_0,y_0)$, 并计算 $\Delta = AC-B^2$。
    3. **判断**: 若 $\Delta > 0$, $A<0$ 则为极大值; $\Delta > 0$, $A>0$ 则为极小值。若 $\Delta < 0$ 则非极值点。若 $\Delta = 0$ 则方法失效。
* **做题步骤 (条件极值-拉格朗日乘数法)**:
    1. **构造拉格朗日函数**: 对目标函数 $f(x,y)$ 和约束条件 $\phi(x,y)=0$, 构造 $L(x,y,\lambda) = f(x,y) + \boxed{\lambda} \phi(x,y)$。
    2. **联立方程**: 求解方程组 $\begin{cases} L_x = f_x + \lambda \phi_x = 0 \\ L_y = f_y + \lambda \phi_y = 0 \\ L_{\boxed{\lambda}} = \phi(x,y) = 0 \end{cases}$ 得到可能的极值点。
    3. **判断**: 根据问题是求最值还是极值, 结合实际意义或比较各点函数值来确定。

### **五、偏微分方程（含偏导数的等式）**
* **通式通法**: 通过变量代换将复杂的偏微分方程化为简单的常微分方程。
* **做题步骤**:
    1. **变量代换**: 根据题目给出的新变量 (如 $u=x+y, v=x-y$), 将原函数 $z=f(x,y)$ 看作 $z=f(u(x,y), v(x,y))$。
    2. **求偏导**: 利用链式法则, 用<span style="border-bottom: 2px solid black;">新变量</span> $u,v$ 来表示旧的偏导数 $\frac{\partial z}{\partial x}$ 和 $\frac{\partial z}{\partial y}$。
    3. **代入化简**: 将这些表达式代入原偏微分方程, 得到一个关于 $u,v$ 的新方程, 通常这个方程会更简单, 可以当作常微分方程来求解。
    ---
## **第14讲 二重积分**

### **一、概念**

* **定义**: $\iint_D f(x,y)d\sigma = \lim_{\lambda \to 0} \sum_{i=1}^n f(\xi_i, \eta_i) \Delta \sigma_i$。
* **性质**: 线性性, 区域可加性, 比较定理, 估值定理, 中值定理。
* **对称性**:
    * 若积分区域 $D$ 关于 $y$ 轴对称,
        * $f(x,y)$ 是关于 $x$ 的奇函数, 则 $\iint_D f(x,y)d\sigma = 0$。
        * $f(x,y)$ 是关于 $x$ 的偶函数, 则 $\iint_D f(x,y)d\sigma = 2\iint_{D_1} f(x,y)d\sigma$, 其中 $D_1$ 是 $D$ 在 $y$ 轴右侧的部分。
    * 关于 $x$ 轴对称及关于原点对称有类似结论。

### **二、计算**

* **题型1: 直角坐标系计算**
    * **通式通法**: "先一后二", 将二重积分化为两次定积分。
    * **做题步骤**:
        1. **画区域**: 画出积分区域 $D$ 的草图。
        2. **定序定限**:
            * 选择积分顺序: $dx dy$ 或 $dy dx$。原则是让积分限尽可能简单(常数)。
            * 定限:
                * $dydx$ (X-型): $x$ 的范围是常数 $[a,b]$, $y$ 的范围是函数 $[y_1(x), y_2(x)]$。所谓"后积先定限, 限为常数; 先积后定限, 限为函数"。
                * $dxdy$ (Y-型): $y$ 的范围是常数 $[c,d]$, $x$ 的范围是函数 $[x_1(y), x_2(y)]$。
        3. **计算**: 先对内层积分, 再对外层积分。
* **题型2: 极坐标系计算**
    * **适用场合**: 被积函数含 $x^2+y^2$ 或 $\frac{y}{x}$, 积分区域是圆形、扇形、环形。
    * **通式通法**:
        * 坐标变换: $x=r\cos\theta, y=r\sin\theta$。
        * 面积微元: $d\sigma = dx dy =\boxed{ r }dr d\theta$。
    * **做题步骤**:
        1. **画区域**: 画出积分区域 $D$ 的草图。
        2. **定限**:
            * 定 $r$ 的范围: 从原点出发, 做射线穿过区域, "穿入点"的 $r$ 为下限, "穿出点"的 $r$ 为上限。$r$ 的范围可以是 $[\phi_1(\theta), \phi_2(\theta)]$。
            * 定 $\theta$ 的范围: 射线扫过整个区域, 其起始角度为下限 $\alpha$, 终止角度为上限 $\beta$。
        3. **计算**: 将被积函数和面积微元都换成极坐标形式, 写出积分 $\int_\alpha^\beta d\theta \int_{\phi_1(\theta)}^{\phi_2(\theta)} f(r\cos\theta, r\sin\theta) r dr$ 并计算。

---
## **Multi integral (多元函数积分学)**

### **第15讲 预备知识 (空间解析几何&场论)**

#### **一、向量的运算及其运用**

* **重要的公式与概念定义**
    * **数量积 (点乘)**: $\vec{a} \cdot \vec{b} = |\vec{a}||\vec{b}|\cos\theta$。几何意义：向量 $\vec{a}$ 在向量 $\vec{b}$ 上的投影与 $|\vec{b}|$ 的乘积。
    * **向量积 (叉乘)**: $\vec{a} \times \vec{b}$ 是一个向量，其模为 $|\vec{a}||\vec{b}|\boxed{\sin\theta}$，方向符合<span style="border-bottom: 2px solid black;">右手</span>定则。几何意义：以 $\vec{a}, \vec{b}$ 为邻边的平行四边形的面积。
    * **混合积**: $[\vec{a}\ \vec{b}\ \vec{c}] = (\vec{a} \times \vec{b}) \cdot \vec{c}$。几何意义：以 $\vec{a}, \vec{b}, \vec{c}$ 为棱的平行六面体的体积。

#### **二、平面、直线及位置关系**

* **重要的公式与概念定义**
    * **平面方程**:
        * 点法式: $A(x-x_0) + B(y-y_0) + C(z-z_0) = 0$，法向量 $\vec{n}=(A,B,C)$。
        * 一般式: $Ax+By+Cz+D=0$。
    * **直线方程**:
        * 点向式/对称式: $\frac{x-x_0}{m} = \frac{y-y_0}{n} = \frac{z-z_0}{p}$，方向向量 $\vec{s}=(m,n,p)$。
        * 参数式: $\begin{cases} x = x_0 + mt \\ y = y_0 + nt \\ z = z_0 + pt \end{cases}$。
        ---
#### **三、空间<span style="border-bottom: 3px dotted black;">曲线</span>的切线与法平面**

* **重要的公式与概念定义**
    * **曲线方程**: 参数式 $\vec{r}(t) = (x(t), y(t), z(t))$。
    * **切向量**: $\vec{r}'(t) = (x'(t), y'(t), z'(t))$。
    * **<span style="border-bottom: 2px solid black;">切线</span>方程**: 在点 $P_0(x_0, y_0, z_0)$ (对应参数$t_0$)，$\frac{x-x_0}{x'(t_0)} = \frac{y-y_0}{y'(t_0)} = \frac{z-z_0}{z'(t_0)}$。
    * **<span style="border: 1px solid black; padding: 5px; display: inline-block;">法平面</span>方程**: $\boxed{x'(t_0)}(x-x_0) + \boxed{y'(t_0)}(y-y_0) + z'(t_0)(z-z_0) = 0$。

#### **四、空间<span style="border: 1px solid black; padding: 5px; display: inline-block;">曲面</span>的切平面与法线**

* **重要的公式与概念定义**
    * **曲面方程**: $F(x,y,z) = 0$。
    * **法向量**: $\vec{n} = (\frac{\partial F}{\partial x}, \frac{\partial F}{\partial y}, \frac{\partial F}{\partial z})|_{P_0}$。
    * **切平面方程**: 在点 $P_0(x_0, y_0, z_0)$， $F_x(P_0)(x-x_0) + F_y(P_0)(y-y_0) + F_z(P_0)(z-z_0) = 0$。
    * **法线方程**: $\frac{x-x_0}{F_x(P_0)} = \frac{y-y_0}{F_y(P_0)} = \frac{z-z_0}{F_z(P_0)}$。
       
        ---
#### **五、<span style="border-bottom: 2px solid black;">旋转</span>曲面**

* **通式通法**: 空间曲线绕坐标轴旋转。
* **做题步骤**:
    1.  **确定曲线和轴**: 明确是哪条曲线 C 绕哪个轴旋转（例如 xoz 平面上的曲线 $f(x,z)=0$ 绕 z 轴旋转）。
    2.  **应用“旋转体公式”**: 核心思想是，旋转面上任意一点 $P(x,y,z)$ 到旋转轴的距离，= <span style="border-bottom: 2px solid black;">生成曲线上</span>与它“同高”的点 $P'(x_0, 0, z_0)$ 到旋转轴的距离。
    3.  **建立方程**: 例如，上述曲线<span style="border-bottom: 2px solid black;">绕 z 轴</span>旋转，则有 $\sqrt{x^2+y^2} = |x_0|$ 且 $z=z_0$。将 $x_0 = \pm\sqrt{x^2+y^2}$ 和 $z_0=z$ 代入曲线方程 $f(x_0,z_0)=0$, 得到 $f(\boxed{\pm\sqrt{x^2+y^2}}, z)=0$。
        
        ---
#### **六、<span style="border: 1px solid black; padding: 5px; display: inline-block;">场论</span>初步**

* **重要的公式与概念定义**
    * **梯度 (Gradient)**: 数量场 $u=u(x,y,z)$ 的梯度是一个向量场, $\text{grad } u = \nabla u = (\frac{\partial u}{\partial x}, \frac{\partial u}{\partial y}, \frac{\partial u}{\partial z})$。其方向是函数 $u$ 增长最快的方向，其模为最大变化率。
    * **散度 (Divergence)**: 向量场 $\vec{F}=(P,Q,R)$ 的散度是一个数量场, $\text{div } \vec{F} = \nabla \cdot \vec{F} = \frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z}$。表示源的强度。
    * **旋度 (Curl)**: 向量场 $\vec{F}=(P,Q,R)$ 的旋度是一个向量场, $\text{curl } \vec{F} = \nabla \times \vec{F} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ P & Q & R \end{vmatrix}$。表示场的旋转程度。

