








以下是对 **AP Calculus AB/BC** 课程 **第 1–5 单元** 的完整详细阐述，严格按照考纲（Course and Exam Description）的结构和内容编写。

---

# 📘 Unit 1：极限与连续性（Limits and Continuity）

| 项目 | AB | BC |
|------|-----|-----|
| **考试权重** | 10–12% | 4–7% |
| **建议课时** | ~22–23 课时 | ~13–14 课时 |
| **涉及核心概念** | CHA, LIM, FUN |

---

## 1.1 微积分导论：变化能否在瞬间发生？（Introducing Calculus: Can Change Occur at an Instant?）

**持久理解（Enduring Understanding）**：微积分使我们能够将对运动的知识推广到涉及变化的多样问题中。

**学习目标 CHA-1.A**：根据包含该瞬间的区间上的平均变化率来解释该瞬间的变化率。

**核心知识**：
- 微积分使用**极限**来理解和建模动态变化。
- 由于平均变化率将一个变量的变化除以另一个变量的变化，因此当自变量的变化为零时，平均变化率**无定义**。
- **极限概念**允许我们以平均变化率来定义瞬时变化率。

> **例**：考虑函数 $f(t)$ 表示汽车在 $t$ 秒时行驶的距离（米）。在 $t=2$ 秒到 $t=2.1$ 秒之间的平均速度为 $\frac{f(2.1)-f(2)}{0.1}$ 米/秒。当时间间隔趋近于零时，这个平均速度的极限就是 $t=2$ 时的**瞬时速度**。

---

## 1.2 定义极限与使用极限记号（Defining Limits and Using Limit Notation）

**持久理解 LIM-1**：使用定义、定理和性质进行推理可用于证明关于极限的论断。

**学习目标 LIM-1.A**：使用正确的记号解析地表示极限。

> **定义**：给定函数 $f$，当 $x$ 趋近于 $c$ 时 $f(x)$ 的极限是实数 $R$，如果 $f(x)$ 可以通过使 $x$ 足够接近 $c$（但不等于 $c$）而任意接近 $R$。如果极限存在且为实数，则标准记号为：
>
> $$\lim_{x \to c} f(x) = R$$

**学习目标 LIM-1.B**：解释用解析记号表达的极限。极限可以通过多种方式表达，包括图形、数值和解析方式。

> ⚠️ **排除声明**：$\varepsilon$-$\delta$ 定义**不在 AP 考试范围内**。

**正确的记号**：
- $\lim_{x \to c} f(x) = L$ — 双侧极限
- $\lim_{x \to c^-} f(x)$ — 左极限
- $\lim_{x \to c^+} f(x)$ — 右极限

---

## 1.3 从图形估计极限值（Estimating Limit Values from Graphs）

**学习目标 LIM-1.C**：估计函数的极限。

- 极限的概念包括**单侧极限**。
- 关于函数的图形信息可用于估计极限。
- 由于尺度问题，函数的图形表示**可能遗漏重要的函数行为**。
- 对于某些函数在特定 $x$ 值处，**极限可能不存在**。极限不存在的几种情况：
  1. 函数**无界**（趋于无穷）
  2. 函数在该值附近**振荡**
  3. **左极限不等于右极限**

> **示例**（文档列举）：
> - $\displaystyle \lim_{x \to 0} \frac{1}{x^2}$ 不存在（无界）
> - $\displaystyle \lim_{x \to 0} \frac{|x|}{x}$ 不存在（左右极限不等）
> - $\displaystyle \lim_{x \to 0} \sin\left(\frac{1}{x}\right)$ 不存在（振荡）
> - $\displaystyle \lim_{x \to 0} \frac{1}{x}$ 不存在（左右极限不等）

---

## 1.4 从表格估计极限值（Estimating Limit Values from Tables）

**学习目标 LIM-1.C**（续）：数值信息可用于估计极限。

从表格估计极限时，观察当 $x$ 越来越接近 $c$ 时 $f(x)$ 趋近于的值。

> **例**：给定表格数据：
> | $x$ | 1.9 | 1.99 | 1.999 | 2.001 | 2.01 | 2.1 |
> |-----|------|-------|-------|-------|------|------|
> | $f(x)$ | 3.71 | 3.9701 | 3.997 | 4.003 | 4.0301 | 4.31 |
>
> 可估计 $\displaystyle \lim_{x \to 2} f(x) \approx 4$。

---

## 1.5 用极限的代数性质确定极限（Determining Limits Using Algebraic Properties of Limits）

**学习目标 LIM-1.D**：使用极限定理确定函数的极限。

**极限的代数性质**：设 $\lim_{x \to c} f(x) = L$，$\lim_{x \to c} g(x) = M$，则：

| 性质 | 公式 |
|------|------|
| 和的极限 | $\displaystyle \lim_{x \to c} [f(x) + g(x)] = L + M$ |
| 差的极限 | $\displaystyle \lim_{x \to c} [f(x) - g(x)] = L - M$ |
| 积的极限 | $\displaystyle \lim_{x \to c} [f(x) \cdot g(x)] = L \cdot M$ |
| 商的极限 | $\displaystyle \lim_{x \to c} \frac{f(x)}{g(x)} = \frac{L}{M}$（$M \neq 0$） |
| 常数倍 | $\displaystyle \lim_{x \to c} [k \cdot f(x)] = k \cdot L$ |
| 复合函数 | 若 $g$ 在 $L$ 处连续，则 $\displaystyle \lim_{x \to c} f(g(x)) = f(\lim_{x \to c} g(x))$ |

---

## 1.6 用代数操作确定极限（Determining Limits Using Algebraic Manipulation）

**学习目标 LIM-1.E**：使用函数的等价表达式或夹逼定理确定函数的极限。

在求极限之前，可能有必要或有帮助将表达式重新排列为等价形式。

**常用技巧**：
1. **因式分解并约去公因式**（有理函数）
2. **乘以共轭表达式**（含根式的函数）
3. **使用三角函数的等价形式**

---

## 1.7 选择确定极限的方法（Selecting Procedures for Determining Limits）

本主题专注于**选择**确定极限的适当方法的技能。学生应练习何时以及如何应用所有与确定极限相关的学习目标。

**策略选择流程图**：
- 直接代入是否有效？$\Rightarrow$ 是 $\Rightarrow$ 完成
- $\frac{0}{0}$ 型 $\Rightarrow$ 因式分解/约分、乘以共轭、三角恒等式
- $\frac{k}{0}$ 型（$k\neq 0$）$\Rightarrow$ 无穷极限，检查垂直渐近线
- 含 $\sin x / x$ 形式 $\Rightarrow$ 夹逼定理

---

## 1.8 用夹逼定理确定极限（Determining Limits Using the Squeeze Theorem）

**学习目标 LIM-1.E**（续）：夹逼定理可用于求函数的极限。

**夹逼定理**：如果在一个包含 $c$ 的区间内（除 $c$ 自身外）有 $g(x) \leq f(x) \leq h(x)$，且 $\displaystyle \lim_{x \to c} g(x) = \lim_{x \to c} h(x) = L$，则 $\displaystyle \lim_{x \to c} f(x) = L$。

> **例**：夹逼定理可用于证明两个重要极限：
>
> $$\lim_{x \to 0} \frac{\sin x}{x} = 1 \quad \text{和} \quad \lim_{x \to 0} \frac{1 - \cos x}{x} = 0$$

---

## 1.9 连接极限的多重表征（Connecting Multiple Representations of Limits）

本主题专注于**连接表征**。学生应练习在单一表征内或跨多种表征转换数学信息。

---

## 1.10 探索间断的类型（Exploring Types of Discontinuities）

**持久理解 LIM-2**：使用定义、定理和性质进行推理可用于证明关于连续性的论断。

**学习目标 LIM-2.A**：使用定义证明关于一点处连续性的结论。

**间断的三种类型**：
1. **可去间断（Removable）**：极限存在但 $f(c)$ 与该极限不相等或 $f(c)$ 无定义
2. **跳跃间断（Jump）**：左右极限存在但不相等
3. **无穷间断（Discontinuity due to vertical asymptote）**：极限趋于 $\pm\infty$

---

## 1.11 定义一点的连续性（Defining Continuity at a Point）

**学习目标 LIM-2.A**（续）：函数 $f$ 在 $x=c$ 处连续，当且仅当：

1. $f(c)$ **存在**（$c$ 在定义域内）
2. $\displaystyle \lim_{x \to c} f(x)$ **存在**
3. $\displaystyle \lim_{x \to c} f(x) = f(c)$

**⚠️ 必须同时满足全部三个条件！**

---

## 1.12 确认区间上的连续性（Confirming Continuity over an Interval）

**学习目标 LIM-2.B**：确定函数连续的区间。

- 函数在区间上连续当且仅当它在区间内的**每一点**都连续。
- **多项式、有理函数、幂函数、指数函数、对数函数和三角函数**在其定义域内的所有点都连续。

---

## 1.13 移除间断（Removing Discontinuities）

**学习目标 LIM-2.C**：确定 $x$ 的值或求解参数，使不连续函数连续（如可能）。

- 如果函数的极限在图形中的一个间断点处存在，则可以通过在该点定义或重新定义函数值等于极限值来**移除**该间断。
- 对于一个分段函数在其定义域分界处连续，分界两侧的表达式在该点的值必须相等，且等于函数在该点的值。

> **例**：设 $f(x) = \begin{cases} \frac{x^2-1}{x-1}, & x \neq 1 \\ k, & x = 1 \end{cases}$
>
> 要使 $f$ 在 $x=1$ 处连续，需要 $\displaystyle \lim_{x \to 1} \frac{x^2-1}{x-1} = \lim_{x \to 1} (x+1) = 2$，所以 $k=2$。

---

## 1.14 连接无穷极限与垂直渐近线（Connecting Infinite Limits and Vertical Asymptotes）

**学习目标 LIM-2.D**：使用涉及无穷的极限解释函数的行为。

- 极限的概念可以扩展到**无穷极限**。
- 函数的**渐近性和无界行为**可以用极限描述和解释。

若 $\displaystyle \lim_{x \to c} f(x) = \pm\infty$，则直线 $x=c$ 是 $f$ 的**垂直渐近线**。

---

## 1.15 连接无穷远处的极限与水平渐近线（Connecting Limits at Infinity and Horizontal Asymptotes）

**学习目标 LIM-2.D**（续）：
- 极限的概念可以扩展到**无穷远处的极限**。
- **无穷远处的极限描述端行为**。
- 函数及其变化率的相对大小可以使用极限进行比较。

若 $\displaystyle \lim_{x \to \infty} f(x) = L$ 或 $\displaystyle \lim_{x \to -\infty} f(x) = L$，则直线 $y=L$ 是 $f$ 的**水平渐近线**。

> **例**：$\displaystyle \lim_{x \to \infty} \frac{3x^2+2x}{x^2-1} = 3$，所以 $y=3$ 是水平渐近线。

---

## 1.16 运用介值定理（Working with the Intermediate Value Theorem — IVT）

**持久理解 FUN-1**：存在定理使我们能够在不精确定位的情况下得出关于函数在区间上行为的结论。

**学习目标 FUN-1.A**：使用介值定理解释函数在区间上的行为。

> **介值定理（IVT）**：如果 $f$ 是闭区间 $[a, b]$ 上的连续函数，且 $d$ 是介于 $f(a)$ 和 $f(b)$ 之间的某个数，则 IVT 保证在 $a$ 和 $b$ 之间至少存在一个数 $c$，使得 $f(c) = d$。

---

# 📘 Unit 2：微分：定义与基本性质（Differentiation: Definition and Fundamental Properties）

| 项目 | AB | BC |
|------|-----|-----|
| **考试权重** | 10–12% | 4–7% |
| **建议课时** | ~13–14 课时 | ~9–10 课时 |
| **涉及核心概念** | CHA, FUN, LIM |

---

## 2.1 定义一点的平均变化率和瞬时变化率（Defining Average and Instantaneous Rates of Change at a Point）

**持久理解 CHA-2**：导数通过将极限应用于区间变化率的知识，使我们能够确定瞬间的变化率。

**学习目标 CHA-2.A**：使用差商确定平均变化率。

**平均变化率**的两种等价形式：

$$\frac{f(a+h) - f(a)}{h} \quad \text{或} \quad \frac{f(x) - f(a)}{x - a}$$

**学习目标 CHA-2.B**：将函数的导数表示为差商的极限。

**瞬时变化率**（即导数）的定义：

$$f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h} = \lim_{x \to a} \frac{f(x) - f(a)}{x - a}$$

前提是该极限存在。

---

## 2.2 定义函数的导数和导数记号（Defining the Derivative of a Function and Using Derivative Notation）

**学习目标 CHA-2.B**（续）：

$f$ 的**导数函数**定义为：

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

前提是该极限存在。

**导数记号**（若 $y = f(x)$）：
- $f'(x)$
- $y'$
- $\displaystyle \frac{dy}{dx}$
- $\displaystyle \frac{d}{dx}[f(x)]$

**学习目标 CHA-2.C**：确定曲线在给定点的切线方程。

函数在一点的导数是该点处函数图形的**切线斜率**。

> **例**：若 $f(2)=5$ 且 $f'(2)=3$，则切线方程为：
> $$y - 5 = 3(x - 2)$$

---

## 2.3 估计函数在一点的导数（Estimating Derivatives of a Function at a Point）

**学习目标 CHA-2.D**：估计导数。

- 一点处的导数可以从表格或图形给出的信息中**估计**。
- 技术可用于计算或估计函数在一点的导数值。

> **例**：从对称差商估计：$f'(a) \approx \frac{f(a+h)-f(a-h)}{2h}$

---

## 2.4 连接可微性与连续性（Connecting Differentiability and Continuity）

**持久理解 FUN-2**：认识到函数的导数本身可能也是一个函数，使我们能够发展关于两者相关行为的知识。

**学习目标 FUN-2.A**：解释可微性与连续性的关系。

> **核心定理**：如果函数在一点**可微**，则它在该点**连续**。反之不成立——连续函数可能在某点不可微。
>
> 💡 等价逆否命题：如果函数在一点不连续，则它在该点不可微。

**连续但不可微的情况**（示例）：
1. 差商的左右极限不相等，如 $f(x)=|x|$ 在 $x=0$ 处
2. 切线垂直且没有斜率，如 $f(x)=\sqrt[3]{x}$ 在 $x=0$ 处

---

## 2.5 应用幂法则（Applying the Power Rule）

**持久理解 FUN-3**：认识到应用导数法则的机会可以简化微分过程。

**学习目标 FUN-3.A**：计算常见函数的导数。

**幂法则**：

$$\frac{d}{dx}[x^r] = r x^{r-1}$$

其中 $r$ 为任意实数。

> **例**：
> - $\frac{d}{dx}[x^5] = 5x^4$
> - $\frac{d}{dx}[x^{-2}] = -2x^{-3}$
> - $\frac{d}{dx}[x^{1/2}] = \frac{1}{2}x^{-1/2} = \frac{1}{2\sqrt{x}}$

---

## 2.6 导数法则：常数、和、差与常数倍（Derivative Rules: Constant, Sum, Difference, and Constant Multiple）

**基本导数法则**：

| 法则 | 公式 |
|------|------|
| 常数法则 | $\displaystyle \frac{d}{dx}[c] = 0$ |
| 常数倍法则 | $\displaystyle \frac{d}{dx}[c \cdot f(x)] = c \cdot f'(x)$ |
| 和法则 | $\displaystyle \frac{d}{dx}[f(x) + g(x)] = f'(x) + g'(x)$ |
| 差法则 | $\displaystyle \frac{d}{dx}[f(x) - g(x)] = f'(x) - g'(x)$ |

**幂法则与上述法则结合**可用于求**多项式函数**的导数。

> **例**：$\frac{d}{dx}[3x^4 - 2x^2 + 5x - 7] = 12x^3 - 4x + 5$

---

## 2.7 $\cos x$、$\sin x$、$e^x$ 和 $\ln x$ 的导数（Derivatives of cos x, sin x, e^x, and ln x）

**基本导数公式**：

$$\frac{d}{dx}[\sin x] = \cos x \qquad \frac{d}{dx}[\cos x] = -\sin x$$

$$\frac{d}{dx}[e^x] = e^x \qquad \frac{d}{dx}[\ln x] = \frac{1}{x}$$

**持久理解 LIM-3**：使用定义、定理和性质进行推理可用于确定极限。

**学习目标 LIM-3.A**：将极限解释为导数的定义。在某些情况下，识别出已知导数的函数的导数定义的表达式，为确定极限提供策略。

> **例**：$\displaystyle \lim_{h \to 0} \frac{\sin(\pi+h)-\sin(\pi)}{h} = \cos(\pi) = -1$（这就是 $\sin x$ 在 $x=\pi$ 处的导数定义！）

---

## 2.8 积法则（The Product Rule）

**学习目标 FUN-3.B**：计算可微函数的积和商的导数。

**积法则**：

$$\frac{d}{dx}[f(x) \cdot g(x)] = f'(x)g(x) + f(x)g'(x)$$

> **例**：$\frac{d}{dx}[x^2 \sin x] = 2x \cdot \sin x + x^2 \cdot \cos x$

⚠️ **常见错误**：将积的导数误认为是导数的积——$f'g'$ 是错的！

---

## 2.9 商法则（The Quotient Rule）

**商法则**：

$$\frac{d}{dx}\left[\frac{f(x)}{g(x)}\right] = \frac{f'(x)g(x) - f(x)g'(x)}{[g(x)]^2}$$

前提是 $g(x) \neq 0$。

> **例**：$\frac{d}{dx}\left[\frac{x}{x^2+1}\right] = \frac{1 \cdot (x^2+1) - x \cdot 2x}{(x^2+1)^2} = \frac{x^2+1-2x^2}{(x^2+1)^2} = \frac{1-x^2}{(x^2+1)^2}$

---

## 2.10 求正切、余切、正割和余割函数的导数（Finding the Derivatives of Tangent, Cotangent, Secant, and/or Cosecant Functions）

利用三角恒等式将 $\tan x$、$\cot x$、$\sec x$ 和 $\csc x$ 重新表达为 $\sin x$ 和 $\cos x$ 的商，然后用商法则求导：

$$\frac{d}{dx}[\tan x] = \sec^2 x \qquad \frac{d}{dx}[\cot x] = -\csc^2 x$$

$$\frac{d}{dx}[\sec x] = \sec x \tan x \qquad \frac{d}{dx}[\csc x] = -\csc x \cot x$$

---

# 📘 Unit 3：微分：复合函数、隐函数与反函数（Differentiation: Composite, Implicit, and Inverse Functions）

| 项目 | AB | BC |
|------|-----|-----|
| **考试权重** | 9–13% | 4–7% |
| **建议课时** | ~10–11 课时 | ~8–9 课时 |
| **涉及核心概念** | FUN |

---

## 3.1 链式法则（The Chain Rule）

**学习目标 FUN-3.C**：计算可微函数的复合函数的导数。

**链式法则**提供了微分复合函数的方法。

若 $y = f(g(x))$，令 $u = g(x)$，则：

$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx} = f'(g(x)) \cdot g'(x)$$

> **例**：
> - $\frac{d}{dx}[\sin(4x)] = \cos(4x) \cdot 4 = 4\cos(4x)$
> - $\frac{d}{dx}[(x^2+1)^5] = 5(x^2+1)^4 \cdot 2x = 10x(x^2+1)^4$

⚠️ **常见错误**：忘记乘以内部函数的导数（"what's inside"）。

---

## 3.2 隐函数微分（Implicit Differentiation）

**学习目标 FUN-3.D**：计算隐式定义函数的导数。

**链式法则是隐函数微分的基础**。

当 $y$ 被隐式定义为 $x$ 的函数时，对等式两边关于 $x$ 求导，将 $y$ 视为 $x$ 的函数，然后解出 $\frac{dy}{dx}$。

> **例**：$x^2 + y^2 = 25$
>
> $\frac{d}{dx}[x^2] + \frac{d}{dx}[y^2] = \frac{d}{dx}[25]$
>
> $2x + 2y \cdot \frac{dy}{dx} = 0$
>
> $\frac{dy}{dx} = -\frac{x}{y}$

---

## 3.3 反函数的微分（Differentiating Inverse Functions）

**学习目标 FUN-3.E**：计算反函数和反三角函数的导数。

如果 $f$ 是可微函数，$f^{-1}$ 是其反函数，且 $f'(f^{-1}(x)) \neq 0$，则：

$$\frac{d}{dx}[f^{-1}(x)] = \frac{1}{f'(f^{-1}(x))}$$

> **例**：若 $f(2)=5$ 且 $f'(2)=3$，则 $(f^{-1})'(5) = \frac{1}{f'(2)} = \frac{1}{3}$。

---

## 3.4 反三角函数的微分（Differentiating Inverse Trigonometric Functions）

$$\frac{d}{dx}[\sin^{-1} x] = \frac{1}{\sqrt{1-x^2}} \quad (-1 < x < 1)$$

$$\frac{d}{dx}[\cos^{-1} x] = -\frac{1}{\sqrt{1-x^2}} \quad (-1 < x < 1)$$

$$\frac{d}{dx}[\tan^{-1} x] = \frac{1}{1+x^2}$$

$$\frac{d}{dx}[\sec^{-1} x] = \frac{1}{|x|\sqrt{x^2-1}} \quad (|x| > 1)$$

---

## 3.5 选择计算导数的方法（Selecting Procedures for Calculating Derivatives）

本主题专注于**选择**计算导数的适当方法的技能。学生应练习何时以及如何应用所有与计算导数相关的学习目标。当多种法则适用时，学生可能难以确定运算顺序。

**选择策略**：
- 是否为基本函数？$\Rightarrow$ 直接使用已知导数公式
- 是否为复合函数？$\Rightarrow$ 链式法则
- 是否为两个函数的积？$\Rightarrow$ 积法则
- 是否为两个函数的商？$\Rightarrow$ 商法则
- 是否为隐函数？$\Rightarrow$ 隐函数微分
- 是否为反函数？$\Rightarrow$ 反函数导数公式

---

## 3.6 计算高阶导数（Calculating Higher-Order Derivatives）

**学习目标 FUN-3.F**：确定函数的高阶导数。

对 $f'$ 求导得到 $f''$（二阶导数），前提是 $f'$ 的导数存在；重复此过程可得到函数的更高阶导数。

**记号**：
- $f''(x)$，$y''$，$\displaystyle \frac{d^2y}{dx^2}$ — 二阶导数
- $f^{(n)}(x)$，$\displaystyle \frac{d^n y}{dx^n}$ — $n$ 阶导数

---

# 📘 Unit 4：微分的情境应用（Contextual Applications of Differentiation）

| 项目 | AB | BC |
|------|-----|-----|
| **考试权重** | 10–15% | 6–9% |
| **建议课时** | ~10–11 课时 | ~6–7 课时 |
| **涉及核心概念** | CHA, LIM |

---

## 4.1 在情境中解释导数的意义（Interpreting the Meaning of the Derivative in Context）

**持久理解 CHA-3**：导数使我们能够解决涉及变化率的现实问题。

**学习目标 CHA-3.A**：在情境中解释导数的意义。

- 函数的导数可以解释为相对于其自变量的**瞬时变化率**。
- 导数可用于表达应用情境中的变化率信息。
- $f'(x)$ 的单位是 $f$ 的单位除以 $x$ 的单位。

> **例**：若 $P(t)$ 表示 $t$ 年时的人口（人），则 $P'(t)$ 的单位是"人/年"，$P'(5)=1200$ 表示在第 5 年人口以每年 1200 人的速率增长。

---

## 4.2 直线运动：连接位置、速度和加速度（Straight-Line Motion: Connecting Position, Velocity, and Acceleration）

**学习目标 CHA-3.B**：计算应用情境中的变化率。

导数可用于解决**直线运动问题**，涉及位置、速率、速度和加速度：

- **位置**：$s(t)$
- **速度**：$v(t) = s'(t)$
- **加速度**：$a(t) = v'(t) = s''(t)$
- **速率**：$|v(t)|$

---

## 4.3 非运动应用情境中的变化率（Rates of Change in Applied Contexts Other Than Motion）

**学习目标 CHA-3.C**：解释应用情境中的变化率。

导数可用于解决涉及应用情境中变化率的问题。学生应学会识别不同情境问题中的**共同底层结构**。

---

## 4.4 相关变化率导论（Introduction to Related Rates）

**学习目标 CHA-3.D**：计算应用情境中的相关变化率。

- **链式法则是相关变化率问题中对变量关于同一自变量求导的基础**。
- 其他微分法则（如积法则和商法则）可能也需要用于对所有变量关于同一自变量求导。

基本思路：识别所有变量，建立联系方程，对时间 $t$ 隐式求导。

---

## 4.5 解决相关变化率问题（Solving Related Rates Problems）

**学习目标 CHA-3.E**：在应用情境中解释相关变化率。

导数可用于解决相关变化率问题——即通过将某一量的变化率与其他已知变化率的量关联起来，来求出该量的变化率。

**标准解题流程**：
1. 画图并标注变量
2. 写出联系各变量的方程
3. 对时间 $t$ 隐式求导（使用链式法则）
4. 代入已知值和变化率
5. 解出要求的变化率
6. 在情境中解释结果（包含单位）

> **例**：半径为 $r$ 的气球以 $\frac{dr}{dt}=2$ cm/s 的速度膨胀。当 $r=5$ cm 时，体积 $V=\frac{4}{3}\pi r^3$ 的变化率是多少？
>
> $\frac{dV}{dt} = 4\pi r^2 \frac{dr}{dt} = 4\pi(5)^2(2) = 200\pi$ cm³/s

---

## 4.6 用局部线性化和线性化逼近函数值（Approximating Values of a Function Using Local Linearity and Linearization）

**学习目标 CHA-3.F**：使用切线方程逼近曲线上的值。

- **切线是函数在切点附近的局部线性逼近的图形**。
- 对于切线逼近，函数在切点附近的行为可能决定切线值是**低估**还是**高估**对应的函数值。
  - 若函数在切点附近为**凹向上（concave up）**，则切线为**低估**
  - 若函数在切点附近为**凹向下（concave down）**，则切线为**高估**

**线性化**公式：

$$L(x) = f(a) + f'(a)(x-a)$$

> **例**：用线性化逼近 $\sqrt{4.1}$。
>
> 取 $f(x)=\sqrt{x}$，$a=4$，则 $f'(x)=\frac{1}{2\sqrt{x}}$，$f'(4)=\frac{1}{4}$
>
> $L(x) = 2 + \frac{1}{4}(x-4)$，所以 $\sqrt{4.1} \approx L(4.1) = 2 + \frac{1}{4}(0.1) = 2.025$

---

## 4.7 用洛必达法则确定不定式的极限（Using L'Hospital's Rule for Determining Limits of Indeterminate Forms）

**持久理解 LIM-4**：洛必达法则允许我们确定某些不定式的极限。

**学习目标 LIM-4.A**：确定导致不定式的函数的极限。

- 当两个函数的比值在极限中趋于 $\frac{0}{0}$ 或 $\frac{\infty}{\infty}$ 时，这种形式称为**不定式**。
- 不定式 $\frac{0}{0}$ 或 $\frac{\infty}{\infty}$ 的极限可使用**洛必达法则**求值：

如果 $\displaystyle \lim_{x \to a} f(x) = 0$ 且 $\displaystyle \lim_{x \to a} g(x) = 0$（或两者都趋于 $\pm\infty$），且 $\displaystyle \lim_{x \to a} \frac{f'(x)}{g'(x)}$ 存在，则：

$$\lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}$$

> ⚠️ **重点**：洛必达法则的结论涉及分子和分母各自导数的比值，**而不是**比值的导数。应用前**必须验证**其形式为 $\frac{0}{0}$ 或 $\frac{\infty}{\infty}$。

> **排除声明**：其他不定形式（如 $0 \cdot \infty$、$\infty - \infty$、$1^\infty$、$0^0$、$\infty^0$）**不在 AP 考试范围内**。

> **例**：$\displaystyle \lim_{x \to 0} \frac{\sin x}{x} \xrightarrow{\frac{0}{0}} \lim_{x \to 0} \frac{\cos x}{1} = 1$

---

# 📘 Unit 5：微分的分析应用（Analytical Applications of Differentiation）

| 项目 | AB | BC |
|------|-----|-----|
| **考试权重** | **15–18%** ⭐（AB 最高之一） | 8–11% |
| **建议课时** | ~15–16 课时 | ~10–11 课时 |
| **涉及核心概念** | FUN |

---

## 5.1 使用中值定理（Using the Mean Value Theorem — MVT）

**学习目标 FUN-1.B**：通过应用中值定理证明关于函数在区间上的结论。

> **中值定理（MVT）**：如果函数 $f$ 在闭区间 $[a, b]$ 上连续且在开区间 $(a, b)$ 上可微，则 MVT 保证在开区间内存在一点 $c$，使得该点的瞬时变化率等于区间上的平均变化率：
>
> $$f'(c) = \frac{f(b) - f(a)}{b - a}$$

**⚠️ 重要**：使用 MVT 时必须验证**两个条件**——连续性和可微性——都已满足，然后才能得出存在 $c$ 的结论。

---

## 5.2 极值定理、全局与局部极值、临界点（Extreme Value Theorem, Global Versus Local Extrema, and Critical Points）

**学习目标 FUN-1.C**：通过应用极值定理证明关于函数的结论。

> **极值定理（EVT）**：如果函数 $f$ 在闭区间 $[a, b]$ 上连续，则 EVT 保证 $f$ 在该区间上至少有一个最小值和至少一个最大值。

**临界点**：函数中一阶导数等于零或不存在的点。

$$\text{临界点：} x = c \text{ 满足 } f'(c) = 0 \text{ 或 } f'(c) \text{ 不存在}$$

所有**局部（相对）极值**都出现在函数的临界点，但并非所有临界点都是局部极值。

---

## 5.3 确定函数的增减区间（Determining Intervals on Which a Function Is Increasing or Decreasing）

**持久理解 FUN-4**：函数的导数可用于理解函数的某些行为。

**学习目标 FUN-4.A**：根据导数的行为证明关于函数行为的结论。

- 如果在某个区间上 $f'(x) > 0$，则 $f$ 在该区间上**递增**。
- 如果在某个区间上 $f'(x) < 0$，则 $f$ 在该区间上**递减**。

---

## 5.4 用一阶导数检验确定相对（局部）极值（Using the First Derivative Test to Determine Relative (Local) Extrema）

**学习目标 FUN-4.A**（续）：一阶导数可确定函数相对（局部）极值的位置。

**一阶导数检验**：若 $c$ 是临界点且 $f$ 在 $c$ 处连续：
- 若 $f'$ 在 $c$ 处由正变负，则 $f$ 在 $c$ 处有**局部最大值**
- 若 $f'$ 在 $c$ 处由负变正，则 $f$ 在 $c$ 处有**局部最小值**
- 若 $f'$ 在 $c$ 处符号不变，则 $c$ 处无极值

---

## 5.5 用候选检验法确定绝对（全局）极值（Using the Candidates Test to Determine Absolute (Global) Extrema）

**学习目标 FUN-4.A**（续）：函数在闭区间上的绝对（全局）极值**只能出现在临界点或端点**。

**候选检验法（Candidates Test）**：
1. 找出区间内 $f$ 的所有临界点
2. 计算 $f$ 在所有临界点和端点处的值
3. 比较这些值——最大者为绝对最大值，最小者为绝对最小值

---

## 5.6 确定函数的凹凸性（Determining Concavity of Functions over Their Domains）

**学习目标 FUN-4.A**（续）：
- 函数图形在开区间上为**凹向上**，当且仅当函数的导函数在该区间上**递增**。
- 函数图形在开区间上为**凹向下**，当且仅当函数的导函数在该区间上**递减**。
- 利用**二阶导数**：若 $f''(x) > 0$，则凹向上；若 $f''(x) < 0$，则凹向下。
- 二阶导数可用于定位函数图形的**拐点**（图形改变凹凸性的点）。

---

## 5.7 用二阶导数检验确定极值（Using the Second Derivative Test to Determine Extrema）

**学习目标 FUN-4.A**（续）：
- 二阶导数可确定临界点是局部最大值还是局部最小值的位置：

若 $f'(c)=0$ 且 $f''(c) < 0$，则 $f$ 在 $x=c$ 处有**局部最大值**。
若 $f'(c)=0$ 且 $f''(c) > 0$，则 $f$ 在 $x=c$ 处有**局部最小值**。
若 $f''(c)=0$，则检验**无效**，需用一阶导数检验。

- 当连续函数在区间内只有一个临界点，且该临界点对应相对极值时，该临界点也对应区间上的**绝对（全局）极值**。

---

## 5.8 绘制函数及其导数的图形（Sketching Graphs of Functions and Their Derivatives）

**学习目标 FUN-4.A**（续）：
- 函数及其导数的关键特征可以被识别并与它们的图形、数值和解析表征相关联。
- 来自 $f'$ 和 $f''$ 的图形、数值和解析信息可用于**预测和解释** $f$ 的行为。

| $f$ 的特征 | 通过 $f'$ 判断 | 通过 $f''$ 判断 |
|------------|---------------|---------------|
| 递增 | $f' > 0$ | — |
| 递减 | $f' < 0$ | — |
| 局部最大值 | $f'$ 由正变负 | $f'' < 0$ |
| 局部最小值 | $f'$ 由负变正 | $f'' > 0$ |
| 凹向上 | — | $f'' > 0$ |
| 凹向下 | — | $f'' < 0$ |
| 拐点 | — | $f''$ 改变符号 |

---

## 5.9 连接函数、一阶导数和二阶导数（Connecting a Function, Its First Derivative, and Its Second Derivative）

**学习目标 FUN-4.A**（续）：$f$、$f'$ 和 $f''$ 图形的关键特征相互关联。

**核心关系总结**：

| $f'$ 的性质 | 对 $f$ 的意义 | $f''$ 的性质 | 对 $f'$ 的意义 |
|------------|--------------|--------------|---------------|
| 正 | $f$ 递增 | 正 | $f'$ 递增，$f$ 凹向上 |
| 负 | $f$ 递减 | 负 | $f'$ 递减，$f$ 凹向下 |
| 零点且变号 | $f$ 有局部极值 | 零点且变号 | $f'$ 有局部极值（$f$ 有拐点） |

---

## 5.10 最优化问题导论（Introduction to Optimization Problems）

**学习目标 FUN-4.B**：在应用情境或函数分析中计算最小值和最大值。

导数可用于解决**最优化问题**——即在给定区间上求函数的最小值或最大值。

学生应学会识别不同情境问题中的共同底层结构。

---

## 5.11 解决最优化问题（Solving Optimization Problems）

**学习目标 FUN-4.C**：在应用情境中解释计算出的最小值和最大值。

函数的最小值和最大值在应用情境中具有特定含义。学生必须解释结果在**问题语境**中的意义。

**标准解题流程**：
1. 识别**目标函数**（要最大化/最小化的量）
2. 写出目标函数的表达式
3. 使用约束条件将目标函数化为**单变量函数**
4. 在适当的定义域上求导数、找临界点
5. 用一阶或二阶导数检验确认极值
6. **在情境中解释答案**（包含单位）

> **例**：用 100 米篱笆围一个矩形区域，求最大面积。
>
> 设长为 $l$，宽为 $w$，则 $2l+2w=100 \Rightarrow l+w=50$。面积 $A=lw=l(50-l)=50l-l^2$。
>
> $A'(l)=50-2l=0 \Rightarrow l=25$，$w=25$。$A''(25)=-2<0$，所以 $l=25$ 时取得最大值。
>
> 最大面积 $=25 \times 25 = 625$ 平方米。

---

## 5.12 探索隐函数关系的行为（Exploring Behaviors of Implicit Relations）

**学习目标 FUN-4.D**：确定隐式关系的临界点。

隐式关系上一点处一阶导数等于零或不存在，则是该函数的**临界点**。

**学习目标 FUN-4.E**：基于导数的证据证明关于隐式定义函数行为的结论。

- 导数的应用可以扩展到隐式定义的函数。
- 涉及隐函数微分的二阶导数可能是 $x$、$y$ 和 $\frac{dy}{dx}$ 的关系式。

> **例**：已知 $x^2 + xy + y^2 = 7$，通过隐函数微分可得 $\frac{dy}{dx} = -\frac{2x+y}{x+2y}$。令 $\frac{dy}{dx}=0$ 可得 $y = -2x$，代入原方程即可找到临界点。

---

# 📊 附录：第 1–5 单元知识体系总览

```
┌─────────────────────────────────────────────────────────────────┐
│                     第 1–5 单元知识体系                             │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Unit 1: 极限与连续性（极限的定义、图形/数值/解析求极限、连续性、IVT）       │
│        ↓                                                      │
│  Unit 2: 微分定义与基本法则（导数定义、幂/积/商法则、三角/指数/对数导数）       │
│        ↓                                                      │
│  Unit 3: 复合/隐/反函数微分（链式法则、隐函数微分、反函数导数）              │
│        ↓                                                      │
│  Unit 4: 微分的应用（运动/相关变化率/线性化/洛必达法则）                   │
│        ↓                                                      │
│  Unit 5: 微分的分析应用（MVT/EVT/增减/极值/凹凸/拐点/最优化）              │
│                                                                  │
├─────────────────────────────────────────────────────────────────┤
│  三大核心概念（Big Ideas）的螺旋贯穿：                                │
│  • CHA（变化）→ 变化率、累积变化                                     │
│  • LIM（极限）→ 极限定义、连续性、洛必达法则、渐近线                      │
│  • FUN（函数分析）→ 导数分析函数行为、最优                              │
└─────────────────────────────────────────────────────────────────┘
```

---
