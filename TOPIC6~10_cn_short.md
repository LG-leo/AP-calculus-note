# AP Calculus AB & BC — 第6~10单元 详尽总结

---

# UNIT 6：积分与累积变化（Integration and Accumulation of Change）

> **考试权重**：AB 17–20% / BC 17–20%（两门考试中权重最高的单元）
> **建议课时**：AB ~18–20 / BC ~15–16
> **主导核心概念**：CHA（变化）、LIM（极限）、FUN（函数分析）
> **对应的持久理解**：LIM-5、LIM-6、FUN-5、FUN-6

---

## 6.1 探索变化的累积（Exploring Accumulations of Change）

**核心思想**：积分的本质是"累积"——将变化率累积起来得到净变化量。本主题建立了"变化率"与"累积量"之间的直觉联系。

**关键知识点**：
- 如果已知某个量的**变化率** $f'(x)$，那么该量在区间 $[a, b]$ 上的**净变化**为 $f(b) - f(a)$，可以用 $f'$ 的定积分表示。
- 引导学生理解"为什么定积分可以表示面积"这一根本问题——因为面积本身就是将无穷多个"高度"（函数值）乘以"宽度"（$dx$）累积的结果。

**示例**：一辆汽车的速度函数为 $v(t)$（英里/小时），那么 $\int_a^b v(t)\,dt$ 表示从时间 $a$ 到 $b$ 行驶的总距离（英里）。这里的物理意义是"将变化率（速度）累积得到净变化量（位移）"。

---

## 6.2 用黎曼和逼近面积（Approximating Areas with Riemann Sums）

**持久理解 LIM-5**：定积分可以用几何和数值方法逼近。

**核心知识点**：
- 定积分可以用**左黎曼和、右黎曼和、中点黎曼和**或**梯形和**来逼近。
- 逼近可以基于**均匀分割**或**非均匀分割**进行计算。
- 根据函数的性态（单调递增/递减、凹凸性），可以判断逼近是**高估**还是**低估**：
  - 如果 $f$ 在区间上**递增**：左黎曼和 $\Rightarrow$ 低估；右黎曼和 $\Rightarrow$ 高估。
  - 如果 $f$ 在区间上**递减**：左黎曼和 $\Rightarrow$ 高估；右黎曼和 $\Rightarrow$ 低估。
  - 中点黎曼和通常比左/右黎曼和更精确。
  - 梯形和：如果 $f$ 是**凹向下**（concave down），梯形和是高估；**凹向上**（concave up），梯形和是低估。

**示例**：给定函数 $f(x) = x^2$ 在 $[0, 2]$ 上，用 $n = 4$ 个子区间的右黎曼和逼近 $\int_0^2 x^2\,dx$：
$$\Delta x = \frac{2-0}{4} = 0.5,\quad \text{右和} = 0.5[f(0.5) + f(1) + f(1.5) + f(2)] = 0.5(0.25 + 1 + 2.25 + 4) = 3.75$$
真实值为 $\frac{8}{3} \approx 2.667$，右黎曼和是高估（因 $f$ 递增）。

---

## 6.3 黎曼和、求和记号与定积分记号（Riemann Sums, Summation Notation, and Definite Integral Notation）

**核心知识点**：
- 黎曼和的定义：将区间 $[a, b]$ 分割为 $n$ 个子区间，每个子区间宽度为 $\Delta x_i$，在第 $i$ 个子区间内取一点 $x_i^*$，则黎曼和为：
  $$\sum_{i=1}^{n} f(x_i^*) \Delta x_i$$
- 当所有子区间的最大宽度趋近于 $0$（即 $n \to \infty$）时，黎曼和的极限就是**定积分**：
  $$\int_a^b f(x)\,dx = \lim_{\max \Delta x_i \to 0} \sum_{i=1}^{n} f(x_i^*) \Delta x_i$$
- 定积分符号 $\int_a^b f(x)\,dx$ 中的 $dx$ 对应于黎曼和中的 $\Delta x$，$f(x)$ 对应于 $f(x_i^*)$。

**示例**：将极限 $\lim_{n \to \infty} \sum_{i=1}^{n} \frac{3}{n}\left(2 + \frac{3i}{n}\right)^2$ 写成定积分形式：
$$\text{令 } \Delta x = \frac{3}{n},\ x_i = 2 + \frac{3i}{n},\ \text{则 } \int_2^5 x^2\,dx$$

---

## 6.4 微积分基本定理与累积函数（The Fundamental Theorem of Calculus and Accumulation Functions）

**持久理解 FUN-5**：微积分基本定理（FTC）将微分和积分连接起来。

**核心知识点**：
- **FTC 第一部分**：如果 $f$ 是连续函数，则函数 $g(x) = \int_a^x f(t)\,dt$ 是 $f$ 的一个反导数，即：
  $$\frac{d}{dx}\int_a^x f(t)\,dt = f(x)$$
- 这一定理说明**积分和微分是互逆运算**——对一个积分函数求导，就回到原被积函数。
- 这一定理可以用来定义新函数，例如：$g(x) = \int_0^x e^{-t^2}\,dt$ 是一个不能用初等函数表示的累积函数。

**示例**：求 $\frac{d}{dx}\int_0^{x^2} \sin(t^2)\,dt$。
$$\text{令 } u = x^2,\ \frac{d}{dx}\int_0^{x^2} \sin(t^2)\,dt = \sin(u^2) \cdot \frac{du}{dx} = \sin(x^4) \cdot 2x$$

---

## 6.5 解释涉及面积的累积函数的行为（Interpreting the Behavior of Accumulation Functions Involving Area）

**核心知识点**：
- 函数 $g(x) = \int_a^x f(t)\,dt$ 的性态可以通过分析 $f$ 的图形来推断：
  - $g$ 递增当且仅当 $f(x) > 0$。
  - $g$ 递减当且仅当 $f(x) < 0$。
  - $g$ 的极值点出现在 $f(x) = 0$ 处（即 $g'(x) = f(x) = 0$）。
  - $g$ 的凹凸性由 $f'(x)$（即 $g''(x)$）决定。
- 这种分析可以通过图形、数值、解析和语言四种表征进行。

---

## 6.6 应用定积分的性质（Applying Properties of Definite Integrals）

**持久理解 FUN-6**：认识应用几何和数学规则的机会可以简化积分。

**核心知识点**（定积分的基本性质）：
1. 常数倍：$\int_a^b c f(x)\,dx = c\int_a^b f(x)\,dx$
2. 和差：$\int_a^b [f(x) \pm g(x)]\,dx = \int_a^b f(x)\,dx \pm \int_a^b g(x)\,dx$
3. 交换上下限：$\int_a^b f(x)\,dx = -\int_b^a f(x)\,dx$
4. 零区间：$\int_a^a f(x)\,dx = 0$
5. 区间可加性：$\int_a^b f(x)\,dx + \int_b^c f(x)\,dx = \int_a^c f(x)\,dx$
6. 可以用几何图形（三角形、矩形、半圆等）的面积来计算某些定积分。
7. 定积分的定义可以扩展到具有**可去间断**或**跳跃间断**的函数。

**示例**：已知 $\int_1^3 f(x)\,dx = 5$，$\int_3^5 f(x)\,dx = 2$，求 $\int_1^5 3f(x)\,dx$。
$$\int_1^5 3f(x)\,dx = 3\int_1^5 f(x)\,dx = 3\left(\int_1^3 f(x)\,dx + \int_3^5 f(x)\,dx\right) = 3(5 + 2) = 21$$

---

## 6.7 微积分基本定理与定积分（The Fundamental Theorem of Calculus and Definite Integrals）

**核心知识点**：
- **FTC 第二部分**：如果 $f$ 在 $[a, b]$ 上连续，$F$ 是 $f$ 的任意一个反导数（即 $F' = f$），则：
  $$\int_a^b f(x)\,dx = F(b) - F(a)$$
- 反导数的定义：函数 $f$ 的反导数是函数 $g$，满足 $g'(x) = f(x)$。
- 如果 $f$ 在包含 $a$ 的区间上连续，则 $F(x) = \int_a^x f(t)\,dt$ 是 $f$ 在该区间上的一个反导数。

**示例**：求 $\int_0^{\pi} \sin x\,dx$。
$$\int_0^{\pi} \sin x\,dx = [-\cos x]_0^{\pi} = (-\cos\pi) - (-\cos 0) = (-(-1)) - (-1) = 1 + 1 = 2$$

---

## 6.8 求反导数和不定积分：基本规则和记号（Finding Antiderivatives and Indefinite Integrals: Basic Rules and Notation）

**核心知识点**：
- 不定积分记号：$\int f(x)\,dx = F(x) + C$，其中 $F'(x) = f(x)$，$C$ 是任意常数。
- 基本反导数公式（由微分法则反推）：
  - $\int x^n\,dx = \frac{x^{n+1}}{n+1} + C\ (n \neq -1)$
  - $\int \frac{1}{x}\,dx = \ln|x| + C$
  - $\int e^x\,dx = e^x + C$
  - $\int \sin x\,dx = -\cos x + C$
  - $\int \cos x\,dx = \sin x + C$
  - $\int \sec^2 x\,dx = \tan x + C$
  - $\int \csc^2 x\,dx = -\cot x + C$
  - $\int \sec x \tan x\,dx = \sec x + C$
  - $\int \csc x \cot x\,dx = -\csc x + C$
  - $\int \frac{1}{\sqrt{1-x^2}}\,dx = \arcsin x + C$
  - $\int \frac{1}{1+x^2}\,dx = \arctan x + C$
- 许多函数**没有封闭形式的反导数**（如 $e^{-x^2}$、$\frac{\sin x}{x}$ 等）。

---

## 6.9 用代换法积分（Integrating Using Substitution）

**核心知识点**：
- 变量代换（$u$-substitution）是寻找反导数的关键技术，本质是**链式法则的逆运算**。
- 对于不定积分：$\int f(g(x)) \cdot g'(x)\,dx = \int f(u)\,du$，其中 $u = g(x)$，$du = g'(x)\,dx$。
- 对于定积分：代换后**必须相应地改变积分上下限**：
  $$\int_a^b f(g(x)) \cdot g'(x)\,dx = \int_{g(a)}^{g(b)} f(u)\,du$$

**示例**：求 $\int_0^1 2x e^{x^2}\,dx$。
$$\text{令 } u = x^2,\ du = 2x\,dx,\ \text{当 } x=0 \Rightarrow u=0,\ x=1 \Rightarrow u=1$$
$$\int_0^1 2x e^{x^2}\,dx = \int_0^1 e^u\,du = [e^u]_0^1 = e - 1$$

---

## 6.10 用长除法和配方法积分函数（Integrating Functions Using Long Division and Completing the Square）

**核心知识点**：
- 对于形如 $\int \frac{P(x)}{Q(x)}\,dx$（$P$ 和 $Q$ 是多项式）的积分，如果分子次数 $\geq$ 分母次数，先做**多项式长除法**化为"多项式 $+$ 真分式"的形式。
- 对于分母为二次式的积分，通过**配方法**将分母化为 $(x + a)^2 + b^2$ 或 $(x + a)^2 - b^2$ 的形式，然后使用 $\arctan$ 或 $\ln$ 等公式。

**示例**：求 $\int \frac{x^2}{x+1}\,dx$。
$$\frac{x^2}{x+1} = x - 1 + \frac{1}{x+1}\ (\text{长除法})$$
$$\int \frac{x^2}{x+1}\,dx = \int \left(x - 1 + \frac{1}{x+1}\right)dx = \frac{x^2}{2} - x + \ln|x+1| + C$$

**示例**：求 $\int \frac{1}{x^2 + 4x + 13}\,dx$。
$$x^2 + 4x + 13 = (x^2 + 4x + 4) + 9 = (x+2)^2 + 3^2$$
$$\int \frac{1}{(x+2)^2 + 3^2}\,dx = \frac{1}{3}\arctan\left(\frac{x+2}{3}\right) + C$$

---

## 🔸 6.11 用分部积分法积分（Integrating Using Integration by Parts）— BC ONLY

**核心知识点**：
- 分部积分是**积法则的逆运算**，公式为：
  $$\int u\,dv = uv - \int v\,du$$
- 关键在于选择合适的 $u$ 和 $dv$。通常按照 **LIATE** 优先顺序选择 $u$：对数函数（Logarithms）、反三角函数（Inverse trig）、代数函数（Algebraic）、三角函数（Trig）、指数函数（Exponentials）。
- 有时需要多次应用分部积分，或在过程中出现循环。

**示例**：求 $\int x e^x\,dx$。
$$\text{令 } u = x,\ dv = e^x\,dx \Rightarrow du = dx,\ v = e^x$$
$$\int x e^x\,dx = x e^x - \int e^x\,dx = x e^x - e^x + C$$

---

## 🔸 6.12 用线性部分分式积分（Integrating Using Linear Partial Fractions）— BC ONLY

**核心知识点**：
- 某些有理函数可以分解为**线性非重复因式的分式和**，从而应用基本的积分技巧。
- 分解形式：若分母可分解为 $(x - r_1)(x - r_2)\cdots$，则：
  $$\frac{P(x)}{(x-r_1)(x-r_2)} = \frac{A}{x-r_1} + \frac{B}{x-r_2}$$

**示例**：求 $\int \frac{1}{x^2 - 1}\,dx$。
$$\frac{1}{x^2-1} = \frac{1}{(x-1)(x+1)} = \frac{1/2}{x-1} - \frac{1/2}{x+1}$$
$$\int \frac{1}{x^2-1}\,dx = \frac{1}{2}\ln|x-1| - \frac{1}{2}\ln|x+1| + C = \frac{1}{2}\ln\left|\frac{x-1}{x+1}\right| + C$$

---

## 🔸 6.13 计算反常积分（Evaluating Improper Integrals）— BC ONLY

**持久理解 LIM-6**：极限的使用使我们能够证明无界区域的面积极限可能是有限的。

**核心知识点**：
- 反常积分是指满足以下条件之一的积分：
  - **无穷限**：一个或两个积分限为无穷大（如 $\int_a^\infty$、$\int_{-\infty}^b$、$\int_{-\infty}^\infty$）。
  - **无界被积函数**：被积函数在积分区间内趋于无穷（如 $\int_a^b$ 中 $f$ 在 $a$ 或 $b$ 附近无界）。
- 反常积分通过**极限**来定义：
  - $\int_a^\infty f(x)\,dx = \lim_{t \to \infty} \int_a^t f(x)\,dx$
  - $\int_a^b f(x)\,dx$（$f$ 在 $b$ 处无界）$= \lim_{t \to b^-} \int_a^t f(x)\,dx$
- 如果极限存在且为有限值，则积分**收敛**；否则**发散**。

**示例**：判断 $\int_1^\infty \frac{1}{x^2}\,dx$ 是否收敛。
$$\int_1^\infty \frac{1}{x^2}\,dx = \lim_{t \to \infty} \int_1^t x^{-2}\,dx = \lim_{t \to \infty} \left[-x^{-1}\right]_1^t = \lim_{t \to \infty} \left(-\frac{1}{t} + 1\right) = 1$$
因此该反常积分收敛于 $1$。

---

## 6.14 选择反微分技巧（Selecting Techniques for Antidifferentiation）

本主题的重点是**选择合适的方法**。学生需要练习判断何时以及如何应用所有与反微分相关的学习目标。需要综合考虑的被积函数形式包括：
- 基本公式直接应用
- $u$-代换
- 分部积分（BC）
- 部分分式（BC）
- 长除法与配方法
- 三角恒等式化简

---

# UNIT 7：微分方程（Differential Equations）

> **考试权重**：AB 6–12% / BC 6–9%
> **建议课时**：AB ~8–9 / BC ~9–10
> **主导核心概念**：FUN（函数分析）
> **对应的持久理解**：FUN-7

**单元概述**：学生将学习建立和求解可分离的微分方程。斜率场可用于表示微分方程的解曲线，建立"存在无穷多个通解（仅差一个积分常数）"的理解。通过初始条件可以确定唯一特解。通过建立和求解指数增长/衰减和逻辑斯谛增长（BC）的微分方程，学生加深对相关模型的理解。

---

## 7.1 用微分方程建模情境（Modeling Situations with Differential Equations）

**核心知识点**：
- 微分方程建立了一个函数与其导数之间的关系。例如："某量的变化率与该量的大小成正比"可以写作 $\frac{dy}{dt} = ky$。
- 将语言描述转化为微分方程是实际应用的核心技能。

**示例**："一个容器中盐的质量 $S$ 的变化率与流入速率和流出速率之差成正比" $\Rightarrow \frac{dS}{dt} = \text{流入率} - \text{流出率}$。

---

## 7.2 验证微分方程的解（Verifying Solutions for Differential Equations）

**核心知识点**：
- 可以通过**求导**来验证一个函数是否是给定微分方程的解。
- 一个微分方程通常有**无穷多个通解**，它们之间只差一个常数。

**示例**：验证 $y = Ce^{2x}$ 是 $\frac{dy}{dx} = 2y$ 的解。
$$\frac{dy}{dx} = 2Ce^{2x} = 2(Ce^{2x}) = 2y \quad \checkmark$$

---

## 7.3 绘制斜率场（Sketching Slope Fields）

**核心知识点**：
- 斜率场（Slope Field）是微分方程在平面上**有限个点**处的图形化表示。
- 在点 $(x, y)$ 处，画一条斜率为 $\frac{dy}{dx} = f(x, y)$ 的小线段。
- 斜率场提供了一阶微分方程的解曲线行为的信息。

**示例**：$\frac{dy}{dx} = x$ 的斜率场——在 $(x, y)$ 处斜率为 $x$，因此所有点 $(1, y)$ 处的斜率都是 $1$，所有点 $(-2, y)$ 处的斜率都是 $-2$。

---

## 7.4 使用斜率场推理（Reasoning Using Slope Fields）

**核心知识点**：
- 微分方程的解是函数或函数族。
- 从斜率场可以推断解的性态：解曲线沿着斜率场的方向延伸。
- 通过给定一点（初始条件），可以在斜率场中画出特定的解曲线。

---

## 🔸 7.5 用欧拉方法逼近解（Approximating Solutions Using Euler's Method）— BC ONLY

**核心知识点**：
- 欧拉方法是一种使用**切线逼近**逐点逼近微分方程解的过程。
- 给定微分方程 $\frac{dy}{dx} = f(x, y)$ 和初始条件 $(x_0, y_0)$，步长为 $h$：
  $$x_{n+1} = x_n + h$$
  $$y_{n+1} = y_n + h \cdot f(x_n, y_n)$$
- 欧拉方法本质上是用一系列切线线段（线性逼近）来近似解曲线。

**示例**：用欧拉方法（步长 $h = 0.5$）在 $\frac{dy}{dx} = x + y$，$y(0) = 1$ 下逼近 $y(1)$。

| $n$ | $x_n$ | $y_n$ | $f(x_n, y_n)$ | $y_{n+1}$ |
|-----|-------|-------|---------------|-----------|
| 0 | 0 | 1 | 1 | $1 + 0.5(1) = 1.5$ |
| 1 | 0.5 | 1.5 | 2.0 | $1.5 + 0.5(2) = 2.5$ |
| 2 | 1.0 | 2.5 | — | — |

所以 $y(1) \approx 2.5$。

---

## 7.6 用分离变量法求解通解（Finding General Solutions Using Separation of Variables）

**核心知识点**：
- 某些微分方程可以通过**分离变量法**求解：将所有含 $y$ 的项移到一边，所有含 $x$ 的项移到另一边。
  $$\frac{dy}{dx} = g(x)h(y) \Rightarrow \frac{dy}{h(y)} = g(x)\,dx$$
- 然后两边分别求反导数（积分），得到通解（含一个任意常数 $C$）。

**示例**：求 $\frac{dy}{dx} = 2xy$ 的通解。
$$\frac{dy}{y} = 2x\,dx \Rightarrow \int \frac{dy}{y} = \int 2x\,dx \Rightarrow \ln|y| = x^2 + C \Rightarrow y = \pm e^{x^2 + C} = Ae^{x^2}$$

---

## 7.7 用初始条件和分离变量法求解特解（Finding Particular Solutions Using Initial Conditions and Separation of Variables）

**核心知识点**：
- 通解描述了无穷多个解。通过给定一点（初始条件），可以确定唯一的**特解**（particular solution）。
- 函数 $F$ 定义为 $F(x) = y_0 + \int_{x_0}^x f(t)\,dt$ 是微分方程 $\frac{dy}{dx} = f(x)$ 满足 $F(x_0) = y_0$ 的一个特解。
- 微分方程的解可能受到**定义域限制**（例如对数函数的自变量必须为正）。

**示例**：求 $\frac{dy}{dx} = 2xy$ 满足 $y(0) = 3$ 的特解。
$$\text{由通解 } y = Ae^{x^2},\ \text{代入 } x = 0,\ y = 3 \Rightarrow 3 = A \cdot e^0 = A \Rightarrow y = 3e^{x^2}$$

---

## 7.8 带微分方程的指数模型（Exponential Models with Differential Equations）

**核心知识点**：
- "某量的变化率与该量的大小成正比"的数学模型是：
  $$\frac{dy}{dt} = ky$$
- 该方程的通解为 $y = y_0 e^{kt}$，其中 $y_0$ 是 $t = 0$ 时的初始值。
- 当 $k > 0$ 时为**指数增长**；当 $k < 0$ 时为**指数衰减**。
- 应用场景包括：人口增长、放射性衰变、牛顿冷却定律、连续复利等。

---

## 🔸 7.9 带微分方程的逻辑斯谛模型（Logistic Models with Differential Equations）— BC ONLY

**核心知识点**：
- "某量的变化率与该量的大小及该量与承载容量之差的乘积成正比"的数学模型是：
  $$\frac{dy}{dt} = ky(a - y)$$
  其中 $a$ 是**承载容量**（carrying capacity，即 $t \to \infty$ 时的极限值）。
- 逻辑斯谛微分方程和初始条件可以在**不解微分方程**的情况下进行解释：
  - 当 $y$ 接近 $0$ 时，增长率近似为指数增长。
  - 当 $y$ 接近 $a$ 时，增长率趋近于 $0$。
- 承载容量是当自变量趋于无穷时逻辑斯谛微分方程的**极限值**。
- 因变量变化最快的时刻发生在 $y = \frac{a}{2}$ 处（即承载容量的一半），此时增长速率最大。

---

# UNIT 8：积分的应用（Applications of Integration）

> **考试权重**：AB 10–15% / BC 6–9%
> **建议课时**：AB ~19–20 / BC ~13–14
> **主导核心概念**：CHA（变化）
> **对应的持久理解**：CHA-4、CHA-5、CHA-6

**单元概述**：学生将学习如何求函数的平均值、用积分建模粒子运动与净变化、以及确定由函数图形定义的面积、体积和弧长（BC）。贯穿本单元的核心思想是：面积、体积和长度问题都是**黎曼和的极限情形**——这可以避免学生记忆大量看似无关的公式。

---

## 8.1 求函数在区间上的平均值（Finding the Average Value of a Function on an Interval）

**核心知识点**：
- 连续函数 $f$ 在区间 $[a, b]$ 上的**平均值**为：
  $$\text{平均值} = \frac{1}{b-a}\int_a^b f(x)\,dx$$
- 注意与"平均变化率" $\frac{f(b)-f(a)}{b-a}$ 的区别——平均值是函数值本身的平均，而平均变化率是斜率。

**示例**：求 $f(x) = \sin x$ 在 $[0, \pi]$ 上的平均值。
$$\frac{1}{\pi - 0}\int_0^{\pi} \sin x\,dx = \frac{1}{\pi}[-\cos x]_0^{\pi} = \frac{1}{\pi}(1 + 1) = \frac{2}{\pi}$$

---

## 8.2 用积分连接位置、速度和加速度（Connecting Position, Velocity, and Acceleration of Functions Using Integrals）

**核心知识点**：
- 对于沿直线运动（rectilinear motion）的质点，在时间区间 $[a, b]$ 上：
  - **位移** = $\int_a^b v(t)\,dt$（速度的定积分）
  - **总路程** = $\int_a^b |v(t)|\,dt$（速率的定积分）
- 这里体现了积分作为累积函数的应用：速度的累积 = 位移，速率的累积 = 总路程。

---

## 8.3 在应用情境中使用累积函数和定积分（Using Accumulation Functions and Definite Integrals in Applied Contexts）

**核心知识点**：
- 定义为积分的函数表示**变化率的累积**。
- 一个量在区间上的变化率的定积分给出该量的**净变化**。
- 定积分可以在许多应用情境中表示累积和净变化信息，例如：
  - 水的流入/流出量
  - 人口变化
  - 能量消耗
  - 收入等

---

## 8.4 求表示为 $x$ 函数的曲线间面积（Finding the Area Between Curves Expressed as Functions of $x$）

**核心知识点**：
- 平面上区域的面积可以用定积分计算。
- 若 $f(x) \geq g(x)$ 在 $[a, b]$ 上，则 $y = f(x)$ 和 $y = g(x)$ 之间的面积为：
  $$\text{面积} = \int_a^b [f(x) - g(x)]\,dx$$

**示例**：求 $y = x$ 和 $y = x^2$ 所围区域的面积。
$$\text{交点：} x = x^2 \Rightarrow x = 0, 1$$
$$\text{面积} = \int_0^1 (x - x^2)\,dx = \left[\frac{x^2}{2} - \frac{x^3}{3}\right]_0^1 = \frac{1}{2} - \frac{1}{3} = \frac{1}{6}$$

---

## 8.5 求表示为 $y$ 函数的曲线间面积（Finding the Area Between Curves Expressed as Functions of $y$）

**核心知识点**：
- 平面区域的面积也可以用 $y$ 的函数来计算。
- 若 $x = f(y) \geq x = g(y)$ 在 $[c, d]$ 上，则面积为：
  $$\text{面积} = \int_c^d [f(y) - g(y)]\,dy$$
- 当区域更容易用 $y$ 描述（如边界是 $x = \text{函数形式}$）时，这种方法更简便。

---

## 8.6 求相交于多于两点的曲线间面积（Finding the Area Between Curves That Intersect at More Than Two Points）

**核心知识点**：
- 当面由多个交点界定时，可能需要用两个或多个定积分的**和**，或者通过计算**两个函数差的绝对值的定积分**来求面积。
- 关键在于正确识别各子区间上哪个函数在上方。
  $$\text{面积} = \int_a^b |f(x) - g(x)|\,dx$$

---

## 8.7 横截面体积：正方形和矩形（Volumes with Cross Sections: Squares and Rectangles）

**核心知识点**：
- 已知横截面形状的立体的体积可以用定积分和这些形状的面积公式来求得。
- 如果垂直于 $x$ 轴的横截面积（已知形状）为 $A(x)$，则体积为：
  $$V = \int_a^b A(x)\,dx$$
- 正方形横截面：$A(x) = [s(x)]^2$，其中 $s(x)$ 是正方形的边长（通常是上下函数之差）。

---

## 8.8 横截面体积：三角形和半圆（Volumes with Cross Sections: Triangles and Semicircles）

**核心知识点**：
- 三角形横截面（等腰直角三角形常见）：$A(x) = \frac{1}{2}[s(x)]^2$（两腰相等时）。
- 半圆横截面：$A(x) = \frac{\pi}{2}[r(x)]^2$，其中 $r(x)$ 是半圆的半径。
- 其他几何定义的横截面同样适用此方法：**积分的横截面积**。

---

## 8.9 圆盘法体积：绕 $x$ 轴或 $y$ 轴旋转（Volume with Disc Method: Revolving Around the $x$- or $y$-Axis）

**核心知识点**：
- **圆盘法**（Disc Method）：将平面区域绕坐标轴旋转形成的旋转体的体积。
- 绕 $x$ 轴旋转：$V = \pi \int_a^b [R(x)]^2\,dx$，其中 $R(x)$ 是旋转半径（曲线到 $x$ 轴的距离）。
- 绕 $y$ 轴旋转：$V = \pi \int_c^d [R(y)]^2\,dy$，其中 $R(y)$ 是旋转半径。

**示例**：求 $y = \sqrt{x}$ 在 $[0, 4]$ 上绕 $x$ 轴旋转的体积。
$$V = \pi \int_0^4 (\sqrt{x})^2\,dx = \pi \int_0^4 x\,dx = \pi \left[\frac{x^2}{2}\right]_0^4 = 8\pi$$

---

## 8.10 圆盘法体积：绕其他轴旋转（Volume with Disc Method: Revolving Around Other Axes）

**核心知识点**：
- 旋转体可以绕平面上的**任意水平线或竖直线**旋转。
- 关键是通过**半径调整**来适应轴的偏移：
  - 绕水平线 $y = c$ 旋转：$R(x) = |f(x) - c|$
  - 绕竖直线 $x = d$ 旋转：$R(y) = |g(y) - d|$

---

## 8.11 垫圈法体积：绕 $x$ 轴或 $y$ 轴旋转（Volume with Washer Method: Revolving Around the $x$- or $y$-Axis）

**核心知识点**：
- **垫圈法**（Washer Method）：当旋转区域有空心（即旋转体横截面呈环形）时使用。
- 绕 $x$ 轴旋转：$V = \pi \int_a^b \left([R_{\text{外}}(x)]^2 - [R_{\text{内}}(x)]^2\right)dx$
- 绕 $y$ 轴旋转：$V = \pi \int_c^d \left([R_{\text{外}}(y)]^2 - [R_{\text{内}}(y)]^2\right)dy$

---

## 8.12 垫圈法体积：绕其他轴旋转（Volume with Washer Method: Revolving Around Other Axes）

**核心知识点**：
- 垫圈法同样可以推广到绕任意水平线或竖直线旋转的情形，关键是正确确定内外半径（考虑轴的位置）。

---

## 🔸 8.13 光滑平面曲线的弧长与行进距离（The Arc Length of a Smooth, Planar Curve and Distance Traveled）— BC ONLY

**持久理解 CHA-6**：定积分使我们能够解决区间上长度累积变化的问题。

**核心知识点**：
- 由函数 $y = f(x)$ 定义的平面曲线的弧长公式：
  $$L = \int_a^b \sqrt{1 + [f'(x)]^2}\,dx$$
- 由参数方程 $x = x(t)$，$y = y(t)$ 定义的曲线的弧长公式：
  $$L = \int_a^b \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}\,dt$$
- 这也等于质点在时间区间 $[a, b]$ 内沿曲线运动的总距离。

---

# UNIT 9：参数方程、极坐标与向量值函数（Parametric Equations, Polar Coordinates, and Vector-Valued Functions）— BC ONLY

> **考试权重**：BC 11–12%
> **建议课时**：BC ~10–11
> **主导核心概念**：CHA（变化）、FUN（函数分析）

**单元概述**：学生将在直线运动的基础上，解决**质点在平面曲线上运动**的问题。学生将定义参数方程和向量值函数来描述平面运动，并应用微积分解决运动问题。极坐标方程是参数方程的特殊情形。本单元应作为**巩固已学知识并将技能转移到新情境**的机会，而非记忆新的事实。

---

## 9.1 定义和微分参数方程（Defining and Differentiating Parametric Equations）

**核心知识点**：
- 参数方程用参数 $t$ 表示曲线：$x = f(t)$，$y = g(t)$。
- 链式法则用于求 $\frac{dy}{dx}$：
  $$\frac{dy}{dx} = \frac{dy/dt}{dx/dt},\quad \text{前提是 } \frac{dx}{dt} \neq 0$$
- 这一公式的直观理解：$y$ 相对于 $x$ 的变化率等于 $y$ 相对于 $t$ 的变化率除以 $x$ 相对于 $t$ 的变化率。

---

## 9.2 参数方程的二阶导数（Second Derivatives of Parametric Equations）

**核心知识点**：
- 参数曲线的二阶导数 $\frac{d^2y}{dx^2}$ 不能用简单的方法得到，而是需要：
  $$\frac{d^2y}{dx^2} = \frac{d}{dx}\left(\frac{dy}{dx}\right) = \frac{\frac{d}{dt}\left(\frac{dy}{dx}\right)}{\frac{dx}{dt}}$$
- 即先对 $\frac{dy}{dx}$（它是 $t$ 的函数）关于 $t$ 求导，再除以 $\frac{dx}{dt}$。

---

## 9.3 求参数方程给出曲线的弧长（Finding Arc Lengths of Curves Given by Parametric Equations）

**核心知识点**：
- 参数曲线的弧长公式：
  $$L = \int_a^b \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}\,dt$$
- 这本质上是将曲线分割为无穷多小段，每段的长度由勾股定理给出。

---

## 9.4 定义和微分向量值函数（Defining and Differentiating Vector-Valued Functions）

**核心知识点**：
- 向量值函数：$\mathbf{r}(t) = \langle f(t), g(t) \rangle$ 或 $\mathbf{r}(t) = f(t)\mathbf{i} + g(t)\mathbf{j}$。
- 导数：$\mathbf{r}'(t) = \langle f'(t), g'(t) \rangle$，表示**速度向量**。
- 速度向量的方向是曲线的切线方向。

---

## 9.5 向量值函数的积分（Integrating Vector-Valued Functions）

**核心知识点**：
- 向量值函数的积分是分量分别积分：
  $$\int_a^b \mathbf{r}(t)\,dt = \left\langle \int_a^b f(t)\,dt, \int_a^b g(t)\,dt \right\rangle$$
- 定积分给出**位移向量**。

---

## 9.6 用参数方程和向量值函数解决运动问题（Solving Motion Problems Using Parametric and Vector-Valued Functions）

**核心知识点**：
- 位置：$\mathbf{r}(t) = \langle x(t), y(t) \rangle$
- 速度：$\mathbf{v}(t) = \mathbf{r}'(t) = \langle x'(t), y'(t) \rangle$
- 速率：$\text{speed} = |\mathbf{v}(t)| = \sqrt{[x'(t)]^2 + [y'(t)]^2}$
- 加速度：$\mathbf{a}(t) = \mathbf{v}'(t) = \langle x''(t), y''(t) \rangle$
- 总路程：$\int_a^b |\mathbf{v}(t)|\,dt = \int_a^b \sqrt{[x'(t)]^2 + [y'(t)]^2}\,dt$

---

## 9.7 定义极坐标和极坐标微分（Defining Polar Coordinates and Differentiating in Polar Form）

**核心知识点**：
- 极坐标 $(r, \theta)$ 与直角坐标的转换：$x = r\cos\theta$，$y = r\sin\theta$。
- 极曲线 $r = f(\theta)$ 可以看作参数方程：$x = f(\theta)\cos\theta$，$y = f(\theta)\sin\theta$，参数为 $\theta$。
- 求 $\frac{dy}{dx}$ 在极坐标下：
  $$\frac{dy}{dx} = \frac{dy/d\theta}{dx/d\theta} = \frac{f'(\theta)\sin\theta + f(\theta)\cos\theta}{f'(\theta)\cos\theta - f(\theta)\sin\theta}$$

---

## 9.8 求极坐标区域或单条极曲线所围面积（Find the Area of a Polar Region or the Area Bounded by a Single Polar Curve）

**核心知识点**：
- 极曲线 $r = f(\theta)$ 从 $\theta = \alpha$ 到 $\theta = \beta$ 所围区域的面积：
  $$\text{面积} = \frac{1}{2}\int_\alpha^\beta [f(\theta)]^2\,d\theta$$
- 注意面积公式来源于将区域分割为无穷多个**扇形**（而非矩形），扇形面积为 $\frac{1}{2}r^2\Delta\theta$。

---

## 9.9 求两条极曲线所围区域的面积（Finding the Area of the Region Bounded by Two Polar Curves）

**核心知识点**：
- 两条极曲线 $r = f(\theta)$（外部）和 $r = g(\theta)$（内部）之间的面积：
  $$\text{面积} = \frac{1}{2}\int_\alpha^\beta \left([f(\theta)]^2 - [g(\theta)]^2\right)d\theta$$
- 关键是找到两条曲线的交点（确定积分上下限）。

---

# UNIT 10：无穷序列与级数（Infinite Sequences and Series）— BC ONLY

> **考试权重**：BC 17–18%（BC中权重最高）
> **建议课时**：BC ~17–18
> **主导核心概念**：LIM（极限）
> **对应的持久理解**：LIM-7、LIM-8

**单元概述**：无穷级数是微积分中最为抽象和深入的内容之一。学生将学习如何判定级数的收敛性（7种检验法）、理解幂级数及其收敛区间、以及用泰勒级数和麦克劳林级数逼近函数。本单元的核心思想是"用无穷多项的和来代表一个有限值"。

---

## 10.1 定义收敛和发散无穷级数（Defining Convergent and Divergent Infinite Series）

**核心知识点**：
- 无穷级数 $\sum_{n=1}^\infty a_n$ 的**部分和** $S_N = \sum_{n=1}^N a_n$。
- 如果 $\lim_{N \to \infty} S_N$ 存在且为有限值，则级数**收敛**于该值；否则**发散**。

---

## 10.2 处理几何级数（Working with Geometric Series）

**核心知识点**：
- 几何级数：$\sum_{n=0}^\infty ar^n = a + ar + ar^2 + \cdots$
- 当 $|r| < 1$ 时收敛，和为：
  $$\sum_{n=0}^\infty ar^n = \frac{a}{1 - r}$$
- 当 $|r| \geq 1$ 时发散。

**示例**：求 $\sum_{n=0}^\infty \left(\frac{1}{2}\right)^n$。
$$a = 1,\ r = \frac{1}{2},\ |r| < 1 \Rightarrow \text{和为 } \frac{1}{1 - 1/2} = 2$$

---

## 10.3 第 $n$ 项发散检验（The $n$th Term Test for Divergence）

**核心知识点**：
- 如果 $\lim_{n \to \infty} a_n \neq 0$，则级数 $\sum a_n$ **发散**。
- ⚠️ 反之不成立：如果 $\lim_{n \to \infty} a_n = 0$，**不能**推出级数收敛（调和级数就是反例）。

---

## 10.4 积分检验法（Integral Test for Convergence）

**核心知识点**：
- 如果 $f$ 是 $[1, \infty)$ 上的连续、正、递减函数，且 $a_n = f(n)$，则：
  - $\sum_{n=1}^\infty a_n$ 收敛当且仅当 $\int_1^\infty f(x)\,dx$ 收敛。
- 常用于判断 $p$-级数等。

---

## 10.5 调和级数和 $p$-级数（Harmonic Series and $p$-Series）

**核心知识点**：
- $p$-级数：$\sum_{n=1}^\infty \frac{1}{n^p}$
  - 当 $p > 1$ 时收敛
  - 当 $p \leq 1$ 时发散
- 调和级数（$p = 1$）：$\sum_{n=1}^\infty \frac{1}{n}$ 发散（尽管 $\frac{1}{n} \to 0$）。

---

## 10.6 比较检验法（Comparison Tests for Convergence）

**核心知识点**：
- **直接比较检验**：若 $0 \leq a_n \leq b_n$ 对所有 $n$ 成立，则：
  - $\sum b_n$ 收敛 $\Rightarrow$ $\sum a_n$ 收敛
  - $\sum a_n$ 发散 $\Rightarrow$ $\sum b_n$ 发散
- **极限比较检验**：若 $\lim_{n \to \infty} \frac{a_n}{b_n} = c > 0$（有限非零），则 $\sum a_n$ 和 $\sum b_n$ 同敛散。

**示例**：判断 $\sum_{n=1}^\infty \frac{1}{n^2 + 1}$ 的收敛性。
$$\frac{1}{n^2 + 1} < \frac{1}{n^2},\ \sum \frac{1}{n^2}\ \text{收敛（$p=2>1$）} \Rightarrow \sum \frac{1}{n^2+1}\ \text{收敛}$$

---

## 10.7 交错级数检验法（Alternating Series Test for Convergence）

**核心知识点**：
- 交错级数：$\sum_{n=1}^\infty (-1)^{n-1} b_n$（$b_n > 0$）。
- 如果满足以下两个条件，则交错级数收敛：
  1. $b_{n+1} \leq b_n$（项递减）
  2. $\lim_{n \to \infty} b_n = 0$

---

## 10.8 比值检验法（Ratio Test for Convergence）

**核心知识点**：
- 令 $L = \lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right|$，则：
  - 若 $L < 1$：级数**绝对收敛**
  - 若 $L > 1$：级数**发散**
  - 若 $L = 1$：检验**无效**（需用其他方法）
- 比值检验对含阶乘或指数函数的级数尤为有效。

---

## 10.9 确定绝对收敛或条件收敛（Determining Absolute or Conditional Convergence）

**核心知识点**：
- 如果 $\sum |a_n|$ 收敛，则 $\sum a_n$ **绝对收敛**。
- 如果 $\sum a_n$ 收敛但 $\sum |a_n|$ 发散，则 $\sum a_n$ **条件收敛**。
- 绝对收敛的级数可以重排项而不改变和；条件收敛的级数则不能。

---

## 10.10 交错级数误差界（Alternating Series Error Bound）

**核心知识点**：
- 对于满足交错级数检验条件的交错级数，用前 $N$ 项逼近级数和时的**误差不超过被舍去的第一项**的绝对值：
  $$|S - S_N| \leq b_{N+1}$$
  其中 $S$ 是真和，$S_N$ 是前 $N$ 项部分和。

---

## 10.11 函数的泰勒多项式逼近（Finding Taylor Polynomial Approximations of Functions）

**核心知识点**：
- 函数 $f$ 在 $x = a$ 处的 $n$ 阶泰勒多项式：
  $$P_n(x) = f(a) + f'(a)(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \cdots + \frac{f^{(n)}(a)}{n!}(x-a)^n$$
- 当 $a = 0$ 时称为**麦克劳林多项式**。

**示例**：$f(x) = e^x$ 在 $x = 0$ 处的 3 阶麦克劳林多项式：
$$P_3(x) = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!}$$

---

## 10.12 拉格朗日误差界（Lagrange Error Bound）

**核心知识点**：
- 对于泰勒多项式 $P_n(x)$ 对 $f(x)$ 的逼近，误差满足：
  $$|f(x) - P_n(x)| \leq \frac{M}{(n+1)!}|x-a|^{n+1}$$
  其中 $M$ 是 $|f^{(n+1)}(z)|$ 在 $x$ 和 $a$ 之间的最大值。
- 这一公式给出了误差的**上界估计**。

---

## 10.13 幂级数的收敛半径和收敛区间（Radius and Interval of Convergence of Power Series）

**核心知识点**：
- 幂级数：$\sum_{n=0}^\infty c_n (x - a)^n$
- 存在收敛半径 $R$（$0 \leq R \leq \infty$），使得：
  - 当 $|x - a| < R$ 时，级数**绝对收敛**
  - 当 $|x - a| > R$ 时，级数**发散**
  - 当 $|x - a| = R$ 时，需要**分别检验端点**
- 通常用**比值检验**求 $R$。

---

## 10.14 求函数的泰勒级数或麦克劳林级数（Finding Taylor or Maclaurin Series for a Function）

**核心知识点**：
- $f$ 在 $x = a$ 处的泰勒级数：
  $$\sum_{n=0}^\infty \frac{f^{(n)}(a)}{n!}(x - a)^n$$
- 常用麦克劳林级数（需熟记）：
  - $e^x = \sum_{n=0}^\infty \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots$
  - $\sin x = \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \cdots$
  - $\cos x = \sum_{n=0}^\infty \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \cdots$
  - $\frac{1}{1-x} = \sum_{n=0}^\infty x^n = 1 + x + x^2 + x^3 + \cdots$（$|x| < 1$）
  - $\ln(1+x) = \sum_{n=1}^\infty \frac{(-1)^{n-1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \cdots$（$-1 < x \leq 1$）

---

## 10.15 将函数表示为幂级数（Representing Functions as Power Series）

**核心知识点**：
- 可以通过对已知级数进行**代数操作**（代换、微分、积分）来得到新函数的幂级数表示。
- 这些操作在收敛区间的内部保持收敛性（端点可能改变）。

**示例**：求 $\frac{1}{1 + x^2}$ 的幂级数。
$$\frac{1}{1 + x^2} = \frac{1}{1 - (-x^2)} = \sum_{n=0}^\infty (-x^2)^n = \sum_{n=0}^\infty (-1)^n x^{2n}$$
收敛区间：$|x| < 1$。

进一步，从 $x = 0$ 到 $x$ 积分可得 $\arctan x$ 的级数：
$$\arctan x = \int_0^x \frac{1}{1+t^2}\,dt = \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{2n+1}$$

---

# 📊 AB 与 BC 在第 6–10 单元的对比总结

| 维度 | AB（第6-8单元） | BC（第6-10单元） |
|------|----------------|-----------------|
| **单元6（积分）** | 基本积分技巧：代换法、长除法、配方法 | 同上 + 分部积分、部分分式、反常积分 |
| **单元7（微分方程）** | 斜率场、分离变量、指数模型 | 同上 + 欧拉方法、逻辑斯谛模型 |
| **单元8（积分应用）** | 平均值、运动、面积、体积（圆盘/垫圈/横截面） | 同上 + 弧长 |
| **单元9（参数/极坐标/向量）** | ❌ 不考 | ✅ 全部内容 |
| **单元10（无穷级数）** | ❌ 不考 | ✅ 全部内容（7种检验法+泰勒级数） |
| **积分单元权重** | 17–20%（最高） | 17–20%（并列最高） |
| **核心思想** | 将积分作为累积工具解决几何和物理问题 | 在 AB 基础上扩展积分技巧+平面曲线+级数理论 |
