Below is a complete detailed exposition of **AP Calculus AB/BC** **Units 1–5**, written strictly according to the structure and content of the Course and Exam Description.

---

# 📘 Unit 1: Limits and Continuity

| Item | AB | BC |
|------|-----|-----|
| **Exam Weight** | 10–12% | 4–7% |
| **Suggested Class Periods** | ~22–23 periods | ~13–14 periods |
| **Big Ideas Involved** | CHA, LIM, FUN |

---

## 1.1 Introducing Calculus: Can Change Occur at an Instant?

**Enduring Understanding**: Calculus allows us to generalize knowledge about motion to a diverse set of problems involving change.

**Learning Objective CHA-1.A**: Interpret the rate of change at an instant in terms of the average rates of change over intervals containing that instant.

**Essential Knowledge**:
- Calculus uses **limits** to understand and model dynamic change.
- Because an average rate of change divides the change in one variable by the change in another, the average rate of change is **undefined** when the change in the independent variable is zero.
- The **concept of limits** allows us to define instantaneous rates of change in terms of average rates of change.

> **Example**: Consider the function $f(t)$ representing the distance (in meters) a car has traveled at time $t$ seconds. The average velocity between $t=2$ seconds and $t=2.1$ seconds is $\frac{f(2.1)-f(2)}{0.1}$ m/s. As the time interval approaches zero, the limit of this average velocity is the **instantaneous velocity** at $t=2$.

---

## 1.2 Defining Limits and Using Limit Notation

**Enduring Understanding LIM-1**: Reasoning with definitions, theorems, and properties can be used to justify claims about limits.

**Learning Objective LIM-1.A**: Represent limits analytically using correct notation.

> **Definition**: Given a function $f$, the limit of $f(x)$ as $x$ approaches $c$ is the real number $R$ if $f(x)$ can be made arbitrarily close to $R$ by taking $x$ sufficiently close to $c$ (but not equal to $c$). If the limit exists and is a real number, the standard notation is:
>
> $$\lim_{x \to c} f(x) = R$$

**Learning Objective LIM-1.B**: Interpret limits expressed with analytic notation. Limits can be expressed in multiple ways, including graphically, numerically, and analytically.

> ⚠️ **Exclusion Statement**: The $\varepsilon$-$\delta$ definition is **NOT within the scope of the AP Exam**.

**Correct Notation**:
- $\lim_{x \to c} f(x) = L$ — Two-sided limit
- $\lim_{x \to c^-} f(x)$ — Left-hand limit
- $\lim_{x \to c^+} f(x)$ — Right-hand limit

---

## 1.3 Estimating Limit Values from Graphs

**Learning Objective LIM-1.C**: Estimate limits of functions.

- The concept of a limit includes **one-sided limits**.
- Graphical information about a function can be used to estimate limits.
- Due to scale issues, graphical representations of a function **may miss important function behavior**.
- For some functions at certain $x$ values, **the limit may not exist**. Several cases where limits do not exist:
  1. The function is **unbounded** (tends to infinity)
  2. The function **oscillates** near that value
  3. **The left-hand limit does not equal the right-hand limit**

> **Examples** (as listed in the document):
> - $\displaystyle \lim_{x \to 0} \frac{1}{x^2}$ does not exist (unbounded)
> - $\displaystyle \lim_{x \to 0} \frac{|x|}{x}$ does not exist (left and right limits differ)
> - $\displaystyle \lim_{x \to 0} \sin\left(\frac{1}{x}\right)$ does not exist (oscillation)
> - $\displaystyle \lim_{x \to 0} \frac{1}{x}$ does not exist (left and right limits differ)

---

## 1.4 Estimating Limit Values from Tables

**Learning Objective LIM-1.C** (continued): Numerical information can be used to estimate limits.

When estimating limits from tables, observe the value that $f(x)$ approaches as $x$ gets closer and closer to $c$.

> **Example**: Given the tabular data:
> | $x$ | 1.9 | 1.99 | 1.999 | 2.001 | 2.01 | 2.1 |
> |-----|------|-------|-------|-------|------|------|
> | $f(x)$ | 3.71 | 3.9701 | 3.997 | 4.003 | 4.0301 | 4.31 |
>
> We can estimate $\displaystyle \lim_{x \to 2} f(x) \approx 4$.

---

## 1.5 Determining Limits Using Algebraic Properties of Limits

**Learning Objective LIM-1.D**: Determine limits of functions using limit theorems.

**Algebraic Properties of Limits**: Let $\lim_{x \to c} f(x) = L$, $\lim_{x \to c} g(x) = M$, then:

| Property | Formula |
|------|------|
| Sum | $\displaystyle \lim_{x \to c} [f(x) + g(x)] = L + M$ |
| Difference | $\displaystyle \lim_{x \to c} [f(x) - g(x)] = L - M$ |
| Product | $\displaystyle \lim_{x \to c} [f(x) \cdot g(x)] = L \cdot M$ |
| Quotient | $\displaystyle \lim_{x \to c} \frac{f(x)}{g(x)} = \frac{L}{M}$ ($M \neq 0$) |
| Constant Multiple | $\displaystyle \lim_{x \to c} [k \cdot f(x)] = k \cdot L$ |
| Composite Function | If $g$ is continuous at $L$, then $\displaystyle \lim_{x \to c} f(g(x)) = f(\lim_{x \to c} g(x))$ |

---

## 1.6 Determining Limits Using Algebraic Manipulation

**Learning Objective LIM-1.E**: Determine limits of functions using equivalent expressions or the Squeeze Theorem.

It may be necessary or helpful to rearrange an expression into an equivalent form before finding a limit.

**Common Techniques**:
1. **Factor and cancel common factors** (rational functions)
2. **Multiply by the conjugate** (functions involving radicals)
3. **Use equivalent forms of trigonometric functions**

---

## 1.7 Selecting Procedures for Determining Limits

This topic focuses on the skill of **selecting** the appropriate procedure for determining limits. Students should practice when and how to apply all learning objectives related to determining limits.

**Strategy Selection Flowchart**:
- Does direct substitution work? $\Rightarrow$ Yes $\Rightarrow$ Done
- $\frac{0}{0}$ form $\Rightarrow$ Factor/cancel, multiply by conjugate, trigonometric identities
- $\frac{k}{0}$ form ($k\neq 0$) $\Rightarrow$ Infinite limit, check for vertical asymptote
- Involves $\sin x / x$ $\Rightarrow$ Squeeze Theorem

---

## 1.8 Determining Limits Using the Squeeze Theorem

**Learning Objective LIM-1.E** (continued): The Squeeze Theorem can be used to find limits of functions.

**Squeeze Theorem**: If $g(x) \leq f(x) \leq h(x)$ on an interval containing $c$ (except possibly at $c$ itself), and $\displaystyle \lim_{x \to c} g(x) = \lim_{x \to c} h(x) = L$, then $\displaystyle \lim_{x \to c} f(x) = L$.

> **Example**: The Squeeze Theorem can be used to prove two important limits:
>
> $$\lim_{x \to 0} \frac{\sin x}{x} = 1 \quad \text{and} \quad \lim_{x \to 0} \frac{1 - \cos x}{x} = 0$$

---

## 1.9 Connecting Multiple Representations of Limits

This topic focuses on **connecting representations**. Students should practice translating mathematical information within a single representation or across multiple representations.

---

## 1.10 Exploring Types of Discontinuities

**Enduring Understanding LIM-2**: Reasoning with definitions, theorems, and properties can be used to justify claims about continuity.

**Learning Objective LIM-2.A**: Use definitions to prove conclusions about continuity at a point.

**Three Types of Discontinuities**:
1. **Removable**: The limit exists but $f(c)$ is not equal to that limit or $f(c)$ is undefined
2. **Jump**: Left-hand and right-hand limits exist but are not equal
3. **Infinite (due to vertical asymptote)**: The limit tends to $\pm\infty$

---

## 1.11 Defining Continuity at a Point

**Learning Objective LIM-2.A** (continued): A function $f$ is continuous at $x=c$ if and only if:

1. $f(c)$ **exists** ($c$ is in the domain)
2. $\displaystyle \lim_{x \to c} f(x)$ **exists**
3. $\displaystyle \lim_{x \to c} f(x) = f(c)$

**⚠️ All three conditions must be satisfied simultaneously!**

---

## 1.12 Confirming Continuity over an Interval

**Learning Objective LIM-2.B**: Determine intervals on which a function is continuous.

- A function is continuous on an interval if and only if it is continuous at **every point** in that interval.
- **Polynomial, rational, power, exponential, logarithmic, and trigonometric functions** are continuous at all points in their domains.

---

## 1.13 Removing Discontinuities

**Learning Objective LIM-2.C**: Determine values of $x$ or solve for parameters that make discontinuous functions continuous (if possible).

- If the limit of a function exists at a point of discontinuity in its graph, the discontinuity can be **removed** by defining or redefining the function value at that point to equal the limit value.
- For a piecewise function to be continuous at the boundary of its domain, the expressions on both sides of the boundary must have the same value at that point, and that value must equal the function value at that point.

> **Example**: Let $f(x) = \begin{cases} \frac{x^2-1}{x-1}, & x \neq 1 \\ k, & x = 1 \end{cases}$
>
> For $f$ to be continuous at $x=1$, we need $\displaystyle \lim_{x \to 1} \frac{x^2-1}{x-1} = \lim_{x \to 1} (x+1) = 2$, so $k=2$.

---

## 1.14 Connecting Infinite Limits and Vertical Asymptotes

**Learning Objective LIM-2.D**: Use limits involving infinity to describe the behavior of functions.

- The concept of a limit can be extended to **infinite limits**.
- **Asymptotic and unbounded behavior** of functions can be described and explained using limits.

If $\displaystyle \lim_{x \to c} f(x) = \pm\infty$, then the line $x=c$ is a **vertical asymptote** of $f$.

---

## 1.15 Connecting Limits at Infinity and Horizontal Asymptotes

**Learning Objective LIM-2.D** (continued):
- The concept of a limit can be extended to **limits at infinity**.
- **Limits at infinity describe end behavior**.
- The relative magnitudes of functions and their rates of change can be compared using limits.

If $\displaystyle \lim_{x \to \infty} f(x) = L$ or $\displaystyle \lim_{x \to -\infty} f(x) = L$, then the line $y=L$ is a **horizontal asymptote** of $f$.

> **Example**: $\displaystyle \lim_{x \to \infty} \frac{3x^2+2x}{x^2-1} = 3$, so $y=3$ is a horizontal asymptote.

---

## 1.16 Working with the Intermediate Value Theorem (IVT)

**Enduring Understanding FUN-1**: Existence theorems allow us to draw conclusions about the behavior of a function on an interval without precisely locating it.

**Learning Objective FUN-1.A**: Use the Intermediate Value Theorem to explain the behavior of a function on an interval.

> **Intermediate Value Theorem (IVT)**: If $f$ is continuous on the closed interval $[a, b]$ and $d$ is some number between $f(a)$ and $f(b)$, then the IVT guarantees that there is at least one number $c$ between $a$ and $b$ such that $f(c) = d$.

---

# 📘 Unit 2: Differentiation: Definition and Fundamental Properties

| Item | AB | BC |
|------|-----|-----|
| **Exam Weight** | 10–12% | 4–7% |
| **Suggested Class Periods** | ~13–14 periods | ~9–10 periods |
| **Big Ideas Involved** | CHA, FUN, LIM |

---

## 2.1 Defining Average and Instantaneous Rates of Change at a Point

**Enduring Understanding CHA-2**: The derivative allows us to determine the rate of change at an instant by applying limits to knowledge about rates of change over intervals.

**Learning Objective CHA-2.A**: Determine average rates of change using difference quotients.

**Two equivalent forms** of the **average rate of change**:

$$\frac{f(a+h) - f(a)}{h} \quad \text{or} \quad \frac{f(x) - f(a)}{x - a}$$

**Learning Objective CHA-2.B**: Represent the derivative of a function as the limit of a difference quotient.

**Definition** of the **instantaneous rate of change** (i.e., the derivative):

$$f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h} = \lim_{x \to a} \frac{f(x) - f(a)}{x - a}$$

provided this limit exists.

---

## 2.2 Defining the Derivative of a Function and Using Derivative Notation

**Learning Objective CHA-2.B** (continued):

The **derivative function** of $f$ is defined as:

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

provided this limit exists.

**Derivative Notation** (if $y = f(x)$):
- $f'(x)$
- $y'$
- $\displaystyle \frac{dy}{dx}$
- $\displaystyle \frac{d}{dx}[f(x)]$

**Learning Objective CHA-2.C**: Determine the equation of a tangent line at a given point on a curve.

The derivative of a function at a point is the **slope of the tangent line** to the graph of the function at that point.

> **Example**: If $f(2)=5$ and $f'(2)=3$, then the equation of the tangent line is:
> $$y - 5 = 3(x - 2)$$

---

## 2.3 Estimating Derivatives of a Function at a Point

**Learning Objective CHA-2.D**: Estimate derivatives.

- The derivative at a point can be **estimated** from information given in tables or graphs.
- Technology can be used to compute or estimate the value of a derivative of a function at a point.

> **Example**: Estimating using the symmetric difference quotient: $f'(a) \approx \frac{f(a+h)-f(a-h)}{2h}$

---

## 2.4 Connecting Differentiability and Continuity

**Enduring Understanding FUN-2**: Recognizing that the derivative of a function is itself a function allows us to develop knowledge about the related behavior of both.

**Learning Objective FUN-2.A**: Explain the relationship between differentiability and continuity.

> **Core Theorem**: If a function is **differentiable** at a point, then it is **continuous** at that point. The converse is not true — a continuous function may not be differentiable at a point.
>
> 💡 Equivalent contrapositive: If a function is not continuous at a point, then it is not differentiable at that point.

**Cases where a function is continuous but not differentiable** (examples):
1. The left-hand and right-hand limits of the difference quotient are not equal, e.g., $f(x)=|x|$ at $x=0$
2. The tangent line is vertical and has no slope, e.g., $f(x)=\sqrt[3]{x}$ at $x=0$

---

## 2.5 Applying the Power Rule

**Enduring Understanding FUN-3**: Recognizing opportunities to apply derivative rules can simplify the differentiation process.

**Learning Objective FUN-3.A**: Calculate derivatives of common functions.

**Power Rule**:

$$\frac{d}{dx}[x^r] = r x^{r-1}$$

where $r$ is any real number.

> **Examples**:
> - $\frac{d}{dx}[x^5] = 5x^4$
> - $\frac{d}{dx}[x^{-2}] = -2x^{-3}$
> - $\frac{d}{dx}[x^{1/2}] = \frac{1}{2}x^{-1/2} = \frac{1}{2\sqrt{x}}$

---

## 2.6 Derivative Rules: Constant, Sum, Difference, and Constant Multiple

**Basic Derivative Rules**:

| Rule | Formula |
|------|------|
| Constant Rule | $\displaystyle \frac{d}{dx}[c] = 0$ |
| Constant Multiple Rule | $\displaystyle \frac{d}{dx}[c \cdot f(x)] = c \cdot f'(x)$ |
| Sum Rule | $\displaystyle \frac{d}{dx}[f(x) + g(x)] = f'(x) + g'(x)$ |
| Difference Rule | $\displaystyle \frac{d}{dx}[f(x) - g(x)] = f'(x) - g'(x)$ |

**The Power Rule combined with the above rules** can be used to find derivatives of **polynomial functions**.

> **Example**: $\frac{d}{dx}[3x^4 - 2x^2 + 5x - 7] = 12x^3 - 4x + 5$

---

## 2.7 Derivatives of $\cos x$, $\sin x$, $e^x$, and $\ln x$

**Basic Derivative Formulas**:

$$\frac{d}{dx}[\sin x] = \cos x \qquad \frac{d}{dx}[\cos x] = -\sin x$$

$$\frac{d}{dx}[e^x] = e^x \qquad \frac{d}{dx}[\ln x] = \frac{1}{x}$$

**Enduring Understanding LIM-3**: Reasoning with definitions, theorems, and properties can be used to determine limits.

**Learning Objective LIM-3.A**: Interpret limits as the definition of a derivative. Recognizing the expression for the limit definition of the derivative of a known function provides a strategy for determining limits in certain cases.

> **Example**: $\displaystyle \lim_{h \to 0} \frac{\sin(\pi+h)-\sin(\pi)}{h} = \cos(\pi) = -1$ (This is precisely the derivative definition of $\sin x$ at $x=\pi$!)

---

## 2.8 The Product Rule

**Learning Objective FUN-3.B**: Calculate derivatives of products and quotients of differentiable functions.

**Product Rule**:

$$\frac{d}{dx}[f(x) \cdot g(x)] = f'(x)g(x) + f(x)g'(x)$$

> **Example**: $\frac{d}{dx}[x^2 \sin x] = 2x \cdot \sin x + x^2 \cdot \cos x$

⚠️ **Common Mistake**: Thinking the derivative of a product is the product of the derivatives — $f'g'$ is wrong!

---

## 2.9 The Quotient Rule

**Quotient Rule**:

$$\frac{d}{dx}\left[\frac{f(x)}{g(x)}\right] = \frac{f'(x)g(x) - f(x)g'(x)}{[g(x)]^2}$$

provided $g(x) \neq 0$.

> **Example**: $\frac{d}{dx}\left[\frac{x}{x^2+1}\right] = \frac{1 \cdot (x^2+1) - x \cdot 2x}{(x^2+1)^2} = \frac{x^2+1-2x^2}{(x^2+1)^2} = \frac{1-x^2}{(x^2+1)^2}$

---

## 2.10 Finding the Derivatives of Tangent, Cotangent, Secant, and/or Cosecant Functions

Using trigonometric identities to rewrite $\tan x$, $\cot x$, $\sec x$, and $\csc x$ as quotients of $\sin x$ and $\cos x$, then differentiating using the Quotient Rule:

$$\frac{d}{dx}[\tan x] = \sec^2 x \qquad \frac{d}{dx}[\cot x] = -\csc^2 x$$

$$\frac{d}{dx}[\sec x] = \sec x \tan x \qquad \frac{d}{dx}[\csc x] = -\csc x \cot x$$

---

# 📘 Unit 3: Differentiation: Composite, Implicit, and Inverse Functions

| Item | AB | BC |
|------|-----|-----|
| **Exam Weight** | 9–13% | 4–7% |
| **Suggested Class Periods** | ~10–11 periods | ~8–9 periods |
| **Big Ideas Involved** | FUN |

---

## 3.1 The Chain Rule

**Learning Objective FUN-3.C**: Calculate derivatives of compositions of differentiable functions.

**The Chain Rule** provides a method for differentiating composite functions.

If $y = f(g(x))$, let $u = g(x)$, then:

$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx} = f'(g(x)) \cdot g'(x)$$

> **Examples**:
> - $\frac{d}{dx}[\sin(4x)] = \cos(4x) \cdot 4 = 4\cos(4x)$
> - $\frac{d}{dx}[(x^2+1)^5] = 5(x^2+1)^4 \cdot 2x = 10x(x^2+1)^4$

⚠️ **Common Mistake**: Forgetting to multiply by the derivative of the inner function ("what's inside").

---

## 3.2 Implicit Differentiation

**Learning Objective FUN-3.D**: Calculate derivatives of implicitly defined functions.

**The Chain Rule is the foundation of implicit differentiation.**

When $y$ is implicitly defined as a function of $x$, differentiate both sides of the equation with respect to $x$, treating $y$ as a function of $x$, then solve for $\frac{dy}{dx}$.

> **Example**: $x^2 + y^2 = 25$
>
> $\frac{d}{dx}[x^2] + \frac{d}{dx}[y^2] = \frac{d}{dx}[25]$
>
> $2x + 2y \cdot \frac{dy}{dx} = 0$
>
> $\frac{dy}{dx} = -\frac{x}{y}$

---

## 3.3 Differentiating Inverse Functions

**Learning Objective FUN-3.E**: Calculate derivatives of inverse and inverse trigonometric functions.

If $f$ is a differentiable function, $f^{-1}$ is its inverse function, and $f'(f^{-1}(x)) \neq 0$, then:

$$\frac{d}{dx}[f^{-1}(x)] = \frac{1}{f'(f^{-1}(x))}$$

> **Example**: If $f(2)=5$ and $f'(2)=3$, then $(f^{-1})'(5) = \frac{1}{f'(2)} = \frac{1}{3}$.

---

## 3.4 Differentiating Inverse Trigonometric Functions

$$\frac{d}{dx}[\sin^{-1} x] = \frac{1}{\sqrt{1-x^2}} \quad (-1 < x < 1)$$

$$\frac{d}{dx}[\cos^{-1} x] = -\frac{1}{\sqrt{1-x^2}} \quad (-1 < x < 1)$$

$$\frac{d}{dx}[\tan^{-1} x] = \frac{1}{1+x^2}$$

$$\frac{d}{dx}[\sec^{-1} x] = \frac{1}{|x|\sqrt{x^2-1}} \quad (|x| > 1)$$

---

## 3.5 Selecting Procedures for Calculating Derivatives

This topic focuses on the skill of **selecting** the appropriate procedure for calculating derivatives. Students should practice when and how to apply all learning objectives related to calculating derivatives. When multiple rules apply, students may have difficulty determining the order of operations.

**Selection Strategy**:
- Is it a basic function? $\Rightarrow$ Use known derivative formulas directly
- Is it a composite function? $\Rightarrow$ Chain Rule
- Is it a product of two functions? $\Rightarrow$ Product Rule
- Is it a quotient of two functions? $\Rightarrow$ Quotient Rule
- Is it an implicit function? $\Rightarrow$ Implicit Differentiation
- Is it an inverse function? $\Rightarrow$ Inverse function derivative formula

---

## 3.6 Calculating Higher-Order Derivatives

**Learning Objective FUN-3.F**: Determine higher-order derivatives of a function.

Differentiating $f'$ yields $f''$ (the second derivative), provided the derivative of $f'$ exists; repeating this process yields higher-order derivatives of the function.

**Notation**:
- $f''(x)$, $y''$, $\displaystyle \frac{d^2y}{dx^2}$ — second derivative
- $f^{(n)}(x)$, $\displaystyle \frac{d^n y}{dx^n}$ — $n$th derivative

---

# 📘 Unit 4: Contextual Applications of Differentiation

| Item | AB | BC |
|------|-----|-----|
| **Exam Weight** | 10–15% | 6–9% |
| **Suggested Class Periods** | ~10–11 periods | ~6–7 periods |
| **Big Ideas Involved** | CHA, LIM |

---

## 4.1 Interpreting the Meaning of the Derivative in Context

**Enduring Understanding CHA-3**: The derivative allows us to solve real-world problems involving rates of change.

**Learning Objective CHA-3.A**: Interpret the meaning of the derivative in context.

- The derivative of a function can be interpreted as the **instantaneous rate of change** with respect to its independent variable.
- Derivatives can be used to express information about rates of change in applied contexts.
- The units of $f'(x)$ are the units of $f$ divided by the units of $x$.

> **Example**: If $P(t)$ represents the population (in people) at time $t$ (in years), then the units of $P'(t)$ are "people per year," and $P'(5)=1200$ means that in the 5th year, the population was growing at a rate of 1200 people per year.

---

## 4.2 Straight-Line Motion: Connecting Position, Velocity, and Acceleration

**Learning Objective CHA-3.B**: Calculate rates of change in applied contexts.

Derivatives can be used to solve **straight-line motion problems** involving position, speed, velocity, and acceleration:

- **Position**: $s(t)$
- **Velocity**: $v(t) = s'(t)$
- **Acceleration**: $a(t) = v'(t) = s''(t)$
- **Speed**: $|v(t)|$

---

## 4.3 Rates of Change in Applied Contexts Other Than Motion

**Learning Objective CHA-3.C**: Interpret rates of change in applied contexts.

Derivatives can be used to solve problems involving rates of change in applied contexts. Students should learn to recognize the **common underlying structure** across problems in different contexts.

---

## 4.4 Introduction to Related Rates

**Learning Objective CHA-3.D**: Calculate related rates in applied contexts.

- **The Chain Rule is the foundation for differentiating variables with respect to the same independent variable in related rates problems.**
- Other differentiation rules (such as the Product Rule and Quotient Rule) may also need to be used for differentiating all variables with respect to the same independent variable.

Basic approach: Identify all variables, establish a connecting equation, and implicitly differentiate with respect to time $t$.

---

## 4.5 Solving Related Rates Problems

**Learning Objective CHA-3.E**: Interpret related rates in applied contexts.

Derivatives can be used to solve related rates problems — that is, finding the rate of change of one quantity by relating it to other quantities whose rates of change are known.

**Standard Problem-Solving Process**:
1. Draw a diagram and label variables
2. Write an equation relating the variables
3. Implicitly differentiate with respect to time $t$ (use Chain Rule)
4. Substitute known values and rates
5. Solve for the required rate
6. Interpret the result in context (include units)

> **Example**: A balloon of radius $r$ is inflating at a rate of $\frac{dr}{dt}=2$ cm/s. When $r=5$ cm, what is the rate of change of volume $V=\frac{4}{3}\pi r^3$?
>
> $\frac{dV}{dt} = 4\pi r^2 \frac{dr}{dt} = 4\pi(5)^2(2) = 200\pi$ cm³/s

---

## 4.6 Approximating Values of a Function Using Local Linearity and Linearization

**Learning Objective CHA-3.F**: Use the equation of a tangent line to approximate values on a curve.

- **The tangent line is the graph of a local linear approximation of a function near the point of tangency.**
- For tangent line approximations, the behavior of the function near the point of tangency may determine whether the tangent value is an **underestimate** or **overestimate** of the corresponding function value.
  - If the function is **concave up** near the point of tangency, the tangent line gives an **underestimate**
  - If the function is **concave down** near the point of tangency, the tangent line gives an **overestimate**

**Linearization** formula:

$$L(x) = f(a) + f'(a)(x-a)$$

> **Example**: Approximate $\sqrt{4.1}$ using linearization.
>
> Let $f(x)=\sqrt{x}$, $a=4$, then $f'(x)=\frac{1}{2\sqrt{x}}$, $f'(4)=\frac{1}{4}$
>
> $L(x) = 2 + \frac{1}{4}(x-4)$, so $\sqrt{4.1} \approx L(4.1) = 2 + \frac{1}{4}(0.1) = 2.025$

---

## 4.7 Using L'Hospital's Rule for Determining Limits of Indeterminate Forms

**Enduring Understanding LIM-4**: L'Hospital's Rule allows us to determine certain limits of indeterminate forms.

**Learning Objective LIM-4.A**: Determine limits of functions that produce indeterminate forms.

- When the ratio of two functions tends to $\frac{0}{0}$ or $\frac{\infty}{\infty}$ in a limit, this form is called an **indeterminate form**.
- Limits of the indeterminate forms $\frac{0}{0}$ or $\frac{\infty}{\infty}$ can be evaluated using **L'Hospital's Rule**:

If $\displaystyle \lim_{x \to a} f(x) = 0$ and $\displaystyle \lim_{x \to a} g(x) = 0$ (or both tend to $\pm\infty$), and $\displaystyle \lim_{x \to a} \frac{f'(x)}{g'(x)}$ exists, then:

$$\lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}$$

> ⚠️ **Key Point**: L'Hospital's Rule involves the ratio of the derivatives of the numerator and denominator separately, **not** the derivative of the ratio. You **must verify** that the form is $\frac{0}{0}$ or $\frac{\infty}{\infty}$ before applying.

> **Exclusion Statement**: Other indeterminate forms (such as $0 \cdot \infty$, $\infty - \infty$, $1^\infty$, $0^0$, $\infty^0$) are **NOT within the scope of the AP Exam**.

> **Example**: $\displaystyle \lim_{x \to 0} \frac{\sin x}{x} \xrightarrow{\frac{0}{0}} \lim_{x \to 0} \frac{\cos x}{1} = 1$

---

# 📘 Unit 5: Analytical Applications of Differentiation

| Item | AB | BC |
|------|-----|-----|
| **Exam Weight** | **15–18%** ⭐ (Highest among AB units) | 8–11% |
| **Suggested Class Periods** | ~15–16 periods | ~10–11 periods |
| **Big Ideas Involved** | FUN |

---

## 5.1 Using the Mean Value Theorem (MVT)

**Learning Objective FUN-1.B**: Justify conclusions about a function on an interval by applying the Mean Value Theorem.

> **Mean Value Theorem (MVT)**: If function $f$ is continuous on the closed interval $[a, b]$ and differentiable on the open interval $(a, b)$, then the MVT guarantees there exists a point $c$ in the open interval such that the instantaneous rate of change at that point equals the average rate of change over the interval:
>
> $$f'(c) = \frac{f(b) - f(a)}{b - a}$$

**⚠️ Important**: When using the MVT, you must verify that **both conditions** — continuity and differentiability — are satisfied before concluding that $c$ exists.

---

## 5.2 Extreme Value Theorem, Global Versus Local Extrema, and Critical Points

**Learning Objective FUN-1.C**: Justify conclusions about functions by applying the Extreme Value Theorem.

> **Extreme Value Theorem (EVT)**: If function $f$ is continuous on the closed interval $[a, b]$, then the EVT guarantees that $f$ has at least one minimum and at least one maximum on that interval.

**Critical Points**: Points in a function where the first derivative is equal to zero or does not exist.

$$\text{Critical points: } x = c \text{ such that } f'(c) = 0 \text{ or } f'(c) \text{ does not exist}$$

All **local (relative) extrema** occur at critical points of a function, but not all critical points are local extrema.

---

## 5.3 Determining Intervals on Which a Function Is Increasing or Decreasing

**Enduring Understanding FUN-4**: The derivative of a function can be used to understand certain behaviors of the function.

**Learning Objective FUN-4.A**: Justify conclusions about the behavior of a function based on the behavior of its derivative.

- If $f'(x) > 0$ on an interval, then $f$ is **increasing** on that interval.
- If $f'(x) < 0$ on an interval, then $f$ is **decreasing** on that interval.

---

## 5.4 Using the First Derivative Test to Determine Relative (Local) Extrema

**Learning Objective FUN-4.A** (continued): The first derivative can determine the location of relative (local) extrema of a function.

**First Derivative Test**: If $c$ is a critical point and $f$ is continuous at $c$:
- If $f'$ changes from positive to negative at $c$, then $f$ has a **local maximum** at $c$
- If $f'$ changes from negative to positive at $c$, then $f$ has a **local minimum** at $c$
- If $f'$ does not change sign at $c$, then there is no extremum at $c$

---

## 5.5 Using the Candidates Test to Determine Absolute (Global) Extrema

**Learning Objective FUN-4.A** (continued): Absolute (global) extrema of a function on a closed interval can **only occur at critical points or endpoints**.

**Candidates Test**:
1. Find all critical points of $f$ within the interval
2. Evaluate $f$ at all critical points and endpoints
3. Compare these values — the largest is the absolute maximum, the smallest is the absolute minimum

---

## 5.6 Determining Concavity of Functions over Their Domains

**Learning Objective FUN-4.A** (continued):
- The graph of a function is **concave up** on an open interval if and only if the derivative of the function is **increasing** on that interval.
- The graph of a function is **concave down** on an open interval if and only if the derivative of the function is **decreasing** on that interval.
- Using the **second derivative**: If $f''(x) > 0$, then concave up; if $f''(x) < 0$, then concave down.
- The second derivative can be used to locate **points of inflection** (points where the concavity of the graph changes).

---

## 5.7 Using the Second Derivative Test to Determine Extrema

**Learning Objective FUN-4.A** (continued):
- The second derivative can determine whether a critical point is the location of a local maximum or local minimum:

If $f'(c)=0$ and $f''(c) < 0$, then $f$ has a **local maximum** at $x=c$.
If $f'(c)=0$ and $f''(c) > 0$, then $f$ has a **local minimum** at $x=c$.
If $f''(c)=0$, the test is **inconclusive**; use the First Derivative Test.

- When a continuous function has only one critical point within an interval, and that critical point corresponds to a relative extremum, it also corresponds to the **absolute (global) extremum** on that interval.

---

## 5.8 Sketching Graphs of Functions and Their Derivatives

**Learning Objective FUN-4.A** (continued):
- Key features of a function and its derivative can be identified and related to their graphical, numerical, and analytical representations.
- Graphical, numerical, and analytical information from $f'$ and $f''$ can be used to **predict and interpret** the behavior of $f$.

| Feature of $f$ | Determined by $f'$ | Determined by $f''$ |
|------------|---------------|---------------|
| Increasing | $f' > 0$ | — |
| Decreasing | $f' < 0$ | — |
| Local maximum | $f'$ changes from + to − | $f'' < 0$ |
| Local minimum | $f'$ changes from − to + | $f'' > 0$ |
| Concave up | — | $f'' > 0$ |
| Concave down | — | $f'' < 0$ |
| Point of inflection | — | $f''$ changes sign |

---

## 5.9 Connecting a Function, Its First Derivative, and Its Second Derivative

**Learning Objective FUN-4.A** (continued): Key features of the graphs of $f$, $f'$, and $f''$ are related to one another.

**Summary of Core Relationships**:

| Property of $f'$ | Meaning for $f$ | Property of $f''$ | Meaning for $f'$ |
|------------|--------------|--------------|---------------|
| Positive | $f$ increasing | Positive | $f'$ increasing, $f$ concave up |
| Negative | $f$ decreasing | Negative | $f'$ decreasing, $f$ concave down |
| Zero with sign change | $f$ has a local extremum | Zero with sign change | $f'$ has a local extremum ($f$ has an inflection point) |

---

## 5.10 Introduction to Optimization Problems

**Learning Objective FUN-4.B**: Calculate minimum and maximum values in applied contexts or function analysis.

Derivatives can be used to solve **optimization problems** — that is, finding the minimum or maximum value of a function on a given interval.

Students should learn to recognize the common underlying structure across problems in different contexts.

---

## 5.11 Solving Optimization Problems

**Learning Objective FUN-4.C**: Interpret calculated minimum and maximum values in applied contexts.

Minimum and maximum values of a function have specific meanings in applied contexts. Students must interpret results in the **context of the problem**.

**Standard Problem-Solving Process**:
1. Identify the **objective function** (the quantity to be maximized/minimized)
2. Write an expression for the objective function
3. Use constraints to express the objective function as a **function of a single variable**
4. Differentiate and find critical points over the appropriate domain
5. Use the First or Second Derivative Test to confirm extrema
6. **Interpret the answer in context** (include units)

> **Example**: Find the maximum area that can be enclosed by 100 meters of fencing for a rectangular region.
>
> Let length be $l$ and width be $w$, then $2l+2w=100 \Rightarrow l+w=50$. Area $A=lw=l(50-l)=50l-l^2$.
>
> $A'(l)=50-2l=0 \Rightarrow l=25$, $w=25$. $A''(25)=-2<0$, so the maximum occurs at $l=25$.
>
> Maximum area $=25 \times 25 = 625$ square meters.

---

## 5.12 Exploring Behaviors of Implicit Relations

**Learning Objective FUN-4.D**: Determine critical points of implicit relations.

A point on an implicit relation where the first derivative is equal to zero or does not exist is a **critical point** of the function.

**Learning Objective FUN-4.E**: Justify conclusions about the behavior of implicitly defined functions based on evidence from the derivative.

- Applications of derivatives can be extended to implicitly defined functions.
- The second derivative involving implicit differentiation may be expressed as a relation involving $x$, $y$, and $\frac{dy}{dx}$.

> **Example**: Given $x^2 + xy + y^2 = 7$, implicit differentiation gives $\frac{dy}{dx} = -\frac{2x+y}{x+2y}$. Setting $\frac{dy}{dx}=0$ yields $y = -2x$, and substituting back into the original equation allows us to find the critical points.

---

# 📊 Appendix: Overview of the Unit 1–5 Knowledge System

```
┌─────────────────────────────────────────────────────────────────┐
│                  Units 1–5 Knowledge System                          │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Unit 1: Limits & Continuity (definition, graphical/numerical/   │
│          analytical limits, continuity, IVT)                      │
│        ↓                                                      │
│  Unit 2: Definition & Basic Rules of Differentiation (derivative │
│          definition, power/product/quotient rules, trig/exp/log)  │
│        ↓                                                      │
│  Unit 3: Composite/Implicit/Inverse Differentiation (Chain Rule, │
│          implicit differentiation, inverse function derivatives)  │
│        ↓                                                      │
│  Unit 4: Contextual Applications (motion, related rates,         │
│          linearization, L'Hospital's Rule)                        │
│        ↓                                                      │
│  Unit 5: Analytical Applications (MVT/EVT, increasing/decreasing,│
│          extrema, concavity, inflection points, optimization)     │
│                                                                  │
├─────────────────────────────────────────────────────────────────┤
│  Three Big Ideas Spiraling Through:                                │
│  • CHA (Change) → Rates of change, accumulation of change        │
│  • LIM (Limits) → Limit definition, continuity, L'Hospital's,    │
│                   asymptotes                                      │
│  • FUN (Function Analysis) → Derivatives analyze function        │
│    behavior, optimization                                         │
└─────────────────────────────────────────────────────────────────┘
```
