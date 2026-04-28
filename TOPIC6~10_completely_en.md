# 📚 AP Calculus AB & BC — Units 6–10 Comprehensive Self-Study Guide (Extended Edition)

---

> **Conventions Used**
> - 🟦 **AB = Blue**: Content required for both AB and BC
> - 🟪 **BC = Purple**: BC-only content
> - Each topic is tagged with its corresponding **Enduring Understanding** code (e.g., LIM-5, FUN-6)
> - All formulas are presented in $\LaTeX$

---

# Part I: The Foundation of Integration — From Discrete to Continuous

---

## Module A: From Accumulation of Change to the Definite Integral

---

### 🟦 A1 The Intuition of Accumulation of Change (6.1 | CHA-4) — Deep Dive

#### 🧠 Core Intuition: Why Can Integration "Accumulate"?

Imagine you're driving a car. Your speed $v(t)$ at each instant tells you: **if you maintain this current speed, how far you'll go per unit time**.

- At time $t$, your instantaneous velocity is $v(t)$ (miles per hour)
- Over an extremely short time interval $dt$, the distance you travel ≈ $v(t) \cdot dt$
- Adding up all these "tiny distances" from $a$ to $b$ gives the total distance

**This is the essence of the definite integral**: accumulating the effect of a rate of change over time.

#### 📊 Multiple Representations

| Representation | Expression | Interpretation |
|------|------|------|
| **Verbal** | "The integral of velocity = displacement" | Accumulation of rate of change gives net change |
| **Graphical** | Area under the velocity curve | Area = displacement |
| **Numerical** | Riemann sums | Discrete approximation of continuous |
| **Analytical** | $\int_a^b v(t)\,dt$ | Symbolic precise expression |

#### ⚠️ Common Mistake: Displacement vs. Total Distance

This is one of **the most critical confusions** on the AP exam:

```
Displacement = ∫v(t)dt          ← Can be positive or negative (direction-sensitive)
Total Distance = ∫|v(t)|dt      ← Always positive (direction-insensitive)
```

> **🎯 Exam Tip**: In free-response questions, if the problem asks for "total distance traveled," you **must** integrate $|v(t)|$, not $v(t)$. Forgetting the absolute value will cost you points.

---

### 🟦 A2 Riemann Sums: Discrete Approximations of the Continuous (6.2–6.3 | LIM-5) — Deep Dive

#### 🧠 The Essence of Riemann Sums

The core idea of Riemann sums is: **break a complex problem into a sum of many simple problems**.

To find the area under a curve, we can't calculate it directly—because the curve isn't a rectangle. But we can:
1. Slice the region into many thin strips
2. Approximate each strip with a rectangle
3. Sum all rectangles ≈ true area
4. The finer the slices, the more accurate the approximation

#### 📝 Detailed Comparison of Four Riemann Sums

Suppose we want to approximate $\int_a^b f(x)\,dx$, dividing $[a, b]$ into $n$ equal-width subintervals, $\Delta x = \frac{b-a}{n}$.

**Left Riemann Sum (LRS)**:
$$L_n = \sum_{i=1}^{n} f(x_{i-1}) \Delta x$$
where $x_i = a + i\Delta x$.

> Uses the **left endpoint** height of each subinterval. If $f$ is increasing, LRS underestimates; if $f$ is decreasing, LRS overestimates.

**Right Riemann Sum (RRS)**:
$$R_n = \sum_{i=1}^{n} f(x_i) \Delta x$$

> Uses the **right endpoint** height of each subinterval. If $f$ is increasing, RRS overestimates; if $f$ is decreasing, RRS underestimates.

**Midpoint Riemann Sum (MPS)**:
$$M_n = \sum_{i=1}^{n} f\left(\frac{x_{i-1} + x_i}{2}\right) \Delta x$$

> Uses the **midpoint** height of each subinterval. Usually the most accurate—error decays as $\frac{1}{n^2}$ (while left/right decay as $\frac{1}{n}$).

**Trapezoidal Sum**:
$$T_n = \sum_{i=1}^{n} \frac{f(x_{i-1}) + f(x_i)}{2} \Delta x$$

> Approximates each subinterval with a **trapezoid**. Note $T_n = \frac{L_n + R_n}{2}$ (the average of left and right sums).

#### 📊 Overestimate/Underestimate Summary Table

| Behavior of $f$ | Left Sum | Right Sum | Midpoint | Trapezoidal |
|----------|------|------|------|------|
| Increasing | Underestimate | Overestimate | — | — |
| Decreasing | Overestimate | Underestimate | — | — |
| Concave Up | — | — | Underestimate | Overestimate |
| Concave Down | — | — | Overestimate | Underestimate |

> **🎯 Exam Tip**: In AP free-response questions, if asked to "explain whether this is an overestimate or underestimate," your justification **must** reference the monotonicity or concavity of the function.

#### 📝 Complete Example: Comparing Four Riemann Sums

Approximate $\int_0^2 x^2\,dx$, $n = 4$.

| Method | Calculation | Result |
|------|---------|------|
| Left | $0.5[f(0)+f(0.5)+f(1)+f(1.5)] = 0.5(0+0.25+1+2.25)$ | **1.75** (underestimate✅, since $f$ is increasing) |
| Right | $0.5[f(0.5)+f(1)+f(1.5)+f(2)] = 0.5(0.25+1+2.25+4)$ | **3.75** (overestimate✅, since $f$ is increasing) |
| Midpoint | $0.5[f(0.25)+f(0.75)+f(1.25)+f(1.75)] = 0.5(0.0625+0.5625+1.5625+3.0625)$ | **2.625** (closest to true value) |
| Trapezoidal | $(1.75+3.75)/2$ | **2.75** |
| **True Value** | $\int_0^2 x^2\,dx = \frac{8}{3} \approx$ | **2.667** |

#### 🧠 From Riemann Sum to Definite Integral — The Idea of Limits

$$\int_a^b f(x)\,dx = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i^*) \Delta x$$

This limit definition is the **essence of calculus**: using limits to transform discrete approximations into precise continuous values.

---

### 🟦 A3 Properties of the Definite Integral (6.6 | FUN-6) — Deep Dive

#### 🧠 Why Learn These Properties?

Properties of definite integrals aren't a burden to memorize—they are **weapons for problem-solving**. On the AP exam, you'll frequently need to decompose a complex integral into a combination of simpler ones.

#### 📝 Detailed Property Explanations with Examples

**Property ①: Constant Multiple**
$$\int_a^b c f(x)\,dx = c\int_a^b f(x)\,dx$$

**Property ②: Sum/Difference**
$$\int_a^b [f(x) \pm g(x)]\,dx = \int_a^b f(x)\,dx \pm \int_a^b g(x)\,dx$$

**Combined Example**:
$$\int_1^3 [4f(x) - 2g(x)]\,dx = 4\int_1^3 f(x)\,dx - 2\int_1^3 g(x)\,dx$$

**Property ③: Reversing Limits Changes Sign**
$$\int_a^b f(x)\,dx = -\int_b^a f(x)\,dx$$

> **⚠️ Common Mistake**: Many students forget this property and make errors when dealing with $\int_0^{-2}$ situations. The order of the limits matters!

**Property ④: Zero Interval**
$$\int_a^a f(x)\,dx = 0$$

**Property ⑤: Interval Additivity**
$$\int_a^b f(x)\,dx + \int_b^c f(x)\,dx = \int_a^c f(x)\,dx$$

> **🎯 Exam Tip**: This is one of the most frequently used properties on the AP exam. When given piecewise information, you'll almost always need it to piece everything together.

**Example**: Given $\int_1^3 f(x)\,dx = 5$, $\int_3^5 f(x)\,dx = 2$, $\int_1^5 g(x)\,dx = 10$, find $\int_1^5 [3f(x) + g(x)]\,dx$.

**Step-by-step**:
$$\int_1^5 [3f(x) + g(x)]\,dx = 3\int_1^5 f(x)\,dx + \int_1^5 g(x)\,dx$$
$$\int_1^5 f(x)\,dx = \int_1^3 f(x)\,dx + \int_3^5 f(x)\,dx = 5 + 2 = 7$$
$$\therefore 3 \times 7 + 10 = 31$$

**Property ⑥: Geometric Method**

Sometimes a definite integral can be evaluated directly using geometric area formulas, without any integration.

**Example**: $\int_{-2}^2 \sqrt{4 - x^2}\,dx$ represents the area of a semicircle of radius 2 = $\frac{1}{2}\pi(2)^2 = 2\pi$.

**Property ⑦: Even and Odd Functions** (not explicitly listed in the CED but very useful in practice)

- If $f$ is even ($f(-x) = f(x)$): $\int_{-a}^a f(x)\,dx = 2\int_0^a f(x)\,dx$
- If $f$ is odd ($f(-x) = -f(x)$): $\int_{-a}^a f(x)\,dx = 0$

---

## Module B: The Fundamental Theorem of Calculus — Connecting Differentiation and Integration

---

### 🟦 B1 FTC Part 1: Differentiating an Integral Returns the Original Function (6.4–6.5 | FUN-5) — Deep Dive

#### 🧠 Intuitive Understanding: What Does FTC Part 1 Say?

Imagine an "area accumulator" function $g(x) = \int_a^x f(t)\,dt$:

- When $x$ moves a tiny amount to the right ($dx$), how much does $g$ increase?
- The increase is a small area: height $f(x)$ × width $dx$
- So $\frac{dg}{dx} = f(x)$

**Mathematical Statement**:
$$\frac{d}{dx}\int_a^x f(t)\,dt = f(x)$$

#### 📝 Three Common Exam Variations

**Variation 1: Direct Application**

$$\frac{d}{dx}\int_0^x \sin(t^2)\,dt = \sin(x^2)$$

**Variation 2: Upper Limit is a Function (Chain Rule Required)**

$$\frac{d}{dx}\int_0^{x^2} \sin(t^2)\,dt = \sin((x^2)^2) \cdot 2x = 2x\sin(x^4)$$

**Variation 3: Both Limits Are Functions**

$$\frac{d}{dx}\int_{\cos x}^{x^3} e^{t^2}\,dt = e^{(x^3)^2} \cdot 3x^2 - e^{(\cos x)^2} \cdot (-\sin x) = 3x^2 e^{x^6} + \sin x \cdot e^{\cos^2 x}$$

#### 🧠 Why Do People Make Mistakes Here?

**Common Mistake**: Forgetting to differentiate the upper limit (chain rule).

> **📝 Self-Study Tip**: Every time you see $\frac{d}{dx}\int_a^{h(x)} f(t)\,dt$, think "plug in the upper limit × derivative of upper limit" minus "plug in the lower limit × derivative of lower limit."

---

### 🟦 B2 FTC Part 2: Evaluating Definite Integrals Using Antiderivatives (6.7 | FUN-6) — Deep Dive

#### 🧠 Intuitive Understanding

FTC Part 2 says: if you know an antiderivative of a function, then computing the definite integral is simply the difference of that antiderivative at the upper and lower limits.

$$\int_a^b f(x)\,dx = F(b) - F(a),\ \text{where } F' = f$$

This means: **you don't need Riemann sums to compute integrals—just find an antiderivative.**

#### 📝 Complete Solution Procedure (Should Become Second Nature)

```
Step 1: Identify the integrand f(x)
Step 2: Find an antiderivative F(x) of f(x)
Step 3: Compute F(b) - F(a)
Step 4: If there are units, state the units
```

**Example**: $\int_1^4 \frac{1}{x}\,dx$

| Step | Operation | Result |
|------|------|------|
| 1 | Identify $f(x) = 1/x$ | — |
| 2 | Antiderivative $F(x) = \ln|x|$ | — |
| 3 | Plug in $F(4) - F(1)$ | $\ln 4 - \ln 1 = \ln 4$ |
| 4 | Done | $\ln 4$ |

---

### 🟦 B3 Analyzing Accumulation Functions (6.5 | FUN-5) — Deep Dive

#### 📝 Systematic Analysis Method

Given $g(x) = \int_a^x f(t)\,dt$, you can infer all properties of $g$ from the graph of $f$:

| To analyze $g$'s... | Look at $f$'s... | Relationship |
|-----------------|-----------------|---------|
| Increasing/decreasing | Sign of $f(x)$ | $g' = f$ |
| Extreme points | $f(x) = 0$ crossing the $x$-axis | $g' = 0$ |
| Concavity | Sign of $f'(x)$ | $g'' = f'$ |
| Inflection points | $f'(x) = 0$ crossing the $x$-axis | $g'' = 0$ |
| Function values | Area under $f$ | $g(x) = \int_a^x f(t)\,dt$ |

#### 📊 Graphical Analysis Example

Suppose the graph of $f(t)$ has the following behavior:

| Interval | Behavior of $f(t)$ | Corresponding behavior of $g(x)$ |
|------|---------------|-------------------|
| $[0, 2]$ | $f(t) > 0$ | $g$ is increasing |
| $[2, 4]$ | $f(t) < 0$ | $g$ is decreasing |
| $t = 2$ | $f(t) = 0$ (positive → negative) | $g$ has a local maximum at $x=2$ |
| $[0, 1]$ | $f$ is increasing | $g$ is concave up |
| $[1, 3]$ | $f$ is decreasing | $g$ is concave down |

> **🎯 Exam Tip**: AP free-response questions often provide the graph of $f'$ (or $f$) and ask you to infer the behavior of $f$ (or the accumulation function). You **must explicitly reference the sign of the derivative** as your reasoning.

---

## Module C: Antiderivative (Indefinite Integral) Techniques

---

### 🟦 C1 Basic Antiderivative Formulas (6.8 | FUN-6) — Deep Dive

#### 🧠 Correspondence Between Derivatives and Antiderivatives

The secret to mastering antiderivatives is: **antiderivatives are just derivative formulas read backwards**.

| Derivative Formula (You Know This) | Antiderivative Formula (Reverse It) |
|---------------------|---------------------|
| $\frac{d}{dx}(x^{n+1}) = (n+1)x^n$ | $\int x^n\,dx = \frac{x^{n+1}}{n+1} + C$ |
| $\frac{d}{dx}(\ln|x|) = \frac{1}{x}$ | $\int \frac{1}{x}\,dx = \ln|x| + C$ |
| $\frac{d}{dx}(e^x) = e^x$ | $\int e^x\,dx = e^x + C$ |
| $\frac{d}{dx}(-\cos x) = \sin x$ | $\int \sin x\,dx = -\cos x + C$ |
| $\frac{d}{dx}(\sin x) = \cos x$ | $\int \cos x\,dx = \sin x + C$ |
| $\frac{d}{dx}(\tan x) = \sec^2 x$ | $\int \sec^2 x\,dx = \tan x + C$ |

#### ⚠️ Common Mistake: Forgetting $+C$

Forgetting to add the constant $C$ is one of the most common point deductions in indefinite integrals. AP scoring guidelines explicitly require the constant $C$.

> **📝 Self-Study Tip**: After writing any indefinite integral answer, develop the habit of checking whether you've included $+C$.

#### ⚠️ Common Mistake: The Absolute Value in $\int \frac{1}{x}\,dx$

$$\int \frac{1}{x}\,dx = \ln|x| + C \quad (\text{not } \ln x + C)$$

The absolute value ensures the domain includes negative $x$. However, if the context clearly specifies $x > 0$, writing $\ln x + C$ is acceptable.

---

### 🟦 C2 $u$-Substitution (6.9 | FUN-6) — Deep Dive

#### 🧠 The Essence of Substitution

$u$-substitution is the **reverse of the chain rule**:

- Chain rule: $\frac{d}{dx}[F(g(x))] = F'(g(x)) \cdot g'(x)$
- Reverse: $\int F'(g(x)) \cdot g'(x)\,dx = F(g(x)) + C$

So the trick of $u$-substitution is: **find the "inner function" $g(x)$, let $u = g(x)$, and see whether $g'(x)\,dx$ appears (or differs by only a constant factor).**

#### 📝 Complete Solution Procedure

```
Step 1: Choose an inner function u = g(x)
Step 2: Compute du = g'(x)·dx
Step 3: Rewrite the entire integral in terms of u and du
Step 4: Integrate with respect to u
Step 5: Substitute back to g(x)
```

#### 📝 Step-by-Step Example

**Find $\int x \cos(x^2)\,dx$**

| Step | Operation | Result |
|------|------|------|
| Step 1 | Let $u = x^2$ (inner function) | $u = x^2$ |
| Step 2 | $du = 2x\,dx$ | $x\,dx = \frac{du}{2}$ |
| Step 3 | Rewrite integral | $\int \cos u \cdot \frac{du}{2} = \frac{1}{2}\int \cos u\,du$ |
| Step 4 | Integrate with respect to $u$ | $\frac{1}{2}\sin u + C$ |
| Step 5 | Substitute back to $x$ | $\frac{1}{2}\sin(x^2) + C$ |

#### ⚠️ Common Mistake: Forgetting to Change Limits in Definite Integrals

$$\int_0^1 2x e^{x^2}\,dx \quad \text{Let } u = x^2$$

**Correct** (changing limits simultaneously):
$$x = 0 \Rightarrow u = 0,\quad x = 1 \Rightarrow u = 1$$
$$\int_0^1 2x e^{x^2}\,dx = \int_0^1 e^u\,du = [e^u]_0^1 = e - 1$$

**Wrong** (keeping the original limits but integrating in $u$):
$$\int_0^1 2x e^{x^2}\,dx \neq \int_0^1 e^u\,du \ \text{(This would give } e^0 - e^0 = 0)$$

> **🎯 Exam Tip**: In AP scoring, if you perform $u$-substitution on a definite integral without changing the limits, points will typically be deducted.

#### 📝 Adjusting for a Constant Factor

Sometimes $g'(x)$ doesn't appear exactly, but differs by only a constant factor:

**Find $\int x\sqrt{x^2 + 1}\,dx$**

$$\text{Let } u = x^2 + 1,\ du = 2x\,dx \Rightarrow x\,dx = \frac{du}{2}$$
$$\int x\sqrt{x^2 + 1}\,dx = \int \sqrt{u} \cdot \frac{du}{2} = \frac{1}{2}\int u^{1/2}\,du = \frac{1}{2} \cdot \frac{u^{3/2}}{3/2} + C = \frac{1}{3}u^{3/2} + C = \frac{1}{3}(x^2+1)^{3/2} + C$$

---

### 🟦 C3 Long Division and Completing the Square (6.10 | FUN-6) — Deep Dive

#### 🧠 When to Use Long Division?

When the integrand is $\frac{\text{polynomial}}{\text{polynomial}}$ and **the degree of the numerator ≥ the degree of the denominator**, first simplify using long division.

**How to recognize**: Compare the highest-degree term in the numerator and denominator.

#### 📝 Long Division Complete Example

**Find $\int \frac{x^3 + 2x}{x - 1}\,dx$**

**Step 1: Perform polynomial long division**
```
          x² + x + 3
    ──────────────
x-1 │ x³ + 0x² + 2x + 0
      x³ - x²
      ────────
           x² + 2x
           x² - x
           ──────
               3x + 0
               3x - 3
               ─────
                    3
```

So $\frac{x^3 + 2x}{x - 1} = x^2 + x + 3 + \frac{3}{x-1}$.

**Step 2: Integrate**
$$\int \left(x^2 + x + 3 + \frac{3}{x-1}\right)dx = \frac{x^3}{3} + \frac{x^2}{2} + 3x + 3\ln|x-1| + C$$

#### 🧠 When to Use Completing the Square?

When the denominator is a quadratic $ax^2 + bx + c$ that cannot be factored (discriminant $b^2 - 4ac < 0$), completing the square will always convert it into the form "square + constant."

**Core technique**: $x^2 + bx = (x + \frac{b}{2})^2 - (\frac{b}{2})^2$

#### 📝 Completing the Square Complete Example

**Find $\int \frac{1}{x^2 + 6x + 25}\,dx$**

**Step 1: Complete the square**
$$x^2 + 6x + 25 = (x^2 + 6x + 9) + 16 = (x + 3)^2 + 4^2$$

**Step 2: Apply $\int \frac{1}{u^2 + a^2}\,du = \frac{1}{a}\arctan\left(\frac{u}{a}\right) + C$**
$$\int \frac{1}{(x+3)^2 + 4^2}\,dx = \frac{1}{4}\arctan\left(\frac{x+3}{4}\right) + C$$

---

### 🟪 C4 Integration by Parts (6.11 | FUN-6) — BC ONLY Deep Dive

#### 🧠 Origin of Integration by Parts — From the Product Rule

Product rule: $(uv)' = u'v + uv'$

Rearrange: $uv' = (uv)' - u'v$

Integrate both sides: $\int uv'\,dx = uv - \int u'v\,dx$

Writing $dv = v'\,dx$ and $du = u'\,dx$:
$$\int u\,dv = uv - \int v\,du$$

#### 📝 The LIATE Rule Explained

Priority order for choosing $u$ (higher priority = choose as $u$ first):

| Type | Letter | Examples | Reason |
|------|------|---------|------|
| **L**ogarithmic | L | $\ln x$, $\log_2 x$ | Becomes simpler after differentiation |
| **I**nverse trig | I | $\arcsin x$, $\arctan x$ | Becomes simpler after differentiation |
| **A**lgebraic | A | $x^n$, $x^2$ | Degree decreases after differentiation |
| **T**rigonometric | T | $\sin x$, $\cos x$ | Doesn't become more complex |
| **E**xponential | E | $e^x$, $a^x$ | Doesn't change after differentiation |

#### 📝 Three Typical Scenarios

**Scenario 1: Polynomial × Exponential/Trigonometric** (A in LIATE)

**Example**: $\int x e^x\,dx$

| Step | Operation |
|------|---------|
| Choose | $u = x$ (A), $dv = e^x\,dx$ (E) |
| Differentiate | $du = dx$ |
| Integrate | $v = e^x$ |
| Substitute | $\int x e^x\,dx = x e^x - \int e^x\,dx = x e^x - e^x + C$ |

**Scenario 2: Logarithm × Polynomial** (L in LIATE)

**Example**: $\int \ln x\,dx$

| Step | Operation |
|------|---------|
| Choose | $u = \ln x$ (L), $dv = dx$ (A) |
| Differentiate | $du = \frac{1}{x}\,dx$ |
| Integrate | $v = x$ |
| Substitute | $\int \ln x\,dx = x\ln x - \int x \cdot \frac{1}{x}\,dx = x\ln x - \int dx = x\ln x - x + C$ |

**Scenario 3: Requires Multiple Iterations**

**Example**: $\int x^2 e^x\,dx$

First time: $u = x^2,\ dv = e^x\,dx$ → $x^2 e^x - \int 2x e^x\,dx$

Second time (on the remainder): $u = 2x,\ dv = e^x\,dx$ → $x^2 e^x - (2x e^x - \int 2 e^x\,dx)$

Final: $x^2 e^x - 2x e^x + 2e^x + C$

#### ⚠️ Common Mistake: Sign Errors

The **minus sign** in the formula $\int u\,dv = uv - \int v\,du$ is frequently forgotten. I recommend saying it aloud every time: "u times v minus the integral of v times du."

---

### 🟪 C5 Partial Fractions (6.12 | FUN-6) — BC ONLY Deep Dive

#### 🧠 The Logic of Partial Fractions

$\frac{1}{x^2 - 1}$ is hard to integrate directly, but $\frac{1/2}{x-1} - \frac{1/2}{x+1}$ is easy.

The goal of partial fractions is: **decompose a complex rational function into a sum of simple fractions**.

#### 📝 Complete Solution Procedure

**Example**: Find $\int \frac{3x + 5}{x^2 - x - 2}\,dx$

**Step 1: Factor the denominator**
$$x^2 - x - 2 = (x-2)(x+1)$$

**Step 2: Set up the partial fraction decomposition**
$$\frac{3x + 5}{(x-2)(x+1)} = \frac{A}{x-2} + \frac{B}{x+1}$$

**Step 3: Multiply both sides by the denominator to find $A$ and $B$**
$$3x + 5 = A(x+1) + B(x-2)$$

**Step 4: Solve for $A$ and $B$**
- Let $x = 2$: $3(2)+5 = A(3) + B(0) \Rightarrow A = \frac{11}{3}$
- Let $x = -1$: $3(-1)+5 = A(0) + B(-3) \Rightarrow B = -\frac{2}{3}$

**Step 5: Integrate**
$$\int \left(\frac{11/3}{x-2} - \frac{2/3}{x+1}\right)dx = \frac{11}{3}\ln|x-2| - \frac{2}{3}\ln|x+1| + C$$

> **🎯 Exam Tip**: On the AP BC exam, partial fractions only involve **linear non-repeating factors**. You do not need to handle repeated factors or quadratic factors.

---

### 🟪 C6 Improper Integrals (6.13 | LIM-6) — BC ONLY Deep Dive

#### 🧠 Intuition Behind Improper Integrals

Your intuition might say: an area extending to infinity must be infinite—but sometimes it isn't!

**Example**: $\int_1^\infty \frac{1}{x^2}\,dx = 1$ (a finite value!)

Why does this happen? Because $\frac{1}{x^2}$ decays fast enough when $x$ is large—fast enough that the total area is "squeezed" into a finite value.

#### 📝 Two Types of Improper Integrals

**Type 1: Infinite Limits**

| Situation | Definition |
|------|------|
| $\int_a^\infty f(x)\,dx$ | $\lim_{t \to \infty} \int_a^t f(x)\,dx$ |
| $\int_{-\infty}^b f(x)\,dx$ | $\lim_{t \to -\infty} \int_t^b f(x)\,dx$ |
| $\int_{-\infty}^\infty f(x)\,dx$ | $\int_{-\infty}^c f(x)\,dx + \int_c^\infty f(x)\,dx$ (both parts must converge) |

**Type 2: Unbounded Integrand**

| Situation | Definition |
|------|------|
| $f$ is unbounded at $b$ | $\lim_{t \to b^-} \int_a^t f(x)\,dx$ |
| $f$ is unbounded at $a$ | $\lim_{t \to a^+} \int_t^b f(x)\,dx$ |
| $f$ is unbounded at interior $c$ | $\int_a^c f(x)\,dx + \int_c^b f(x)\,dx$ (both parts must converge) |

#### 📝 Complete Evaluation Procedure

**Example**: Determine whether $\int_0^\infty \frac{1}{1+x^2}\,dx$ converges.

```
Step 1: Identify type → Infinite limit (upper limit ∞)
Step 2: Rewrite as limit → ∫₀^∞ 1/(1+x²)dx = lim_{t→∞} ∫₀^t 1/(1+x²)dx
Step 3: Compute the definite integral → [arctan x]_0^t = arctan t - arctan 0 = arctan t
Step 4: Take the limit → lim_{t→∞} arctan t = π/2
Step 5: Conclusion → Converges to π/2
```

#### ⚠️ Common Mistake: Confusing Convergence and Divergence

| Integral | Result | Converges? |
|------|------|--------|
| $\int_1^\infty x^{-2}\,dx$ | $1$ | ✅ Converges |
| $\int_1^\infty x^{-1}\,dx$ | $\infty$ | ❌ Diverges |
| $\int_1^\infty x^{-0.5}\,dx$ | $\infty$ | ❌ Diverges |
| $\int_1^\infty e^{-x}\,dx$ | $1/e$ | ✅ Converges |
| $\int_0^1 x^{-0.5}\,dx$ | $2$ | ✅ Converges |
| $\int_0^1 x^{-1}\,dx$ | $\infty$ | ❌ Diverges |
| $\int_0^1 x^{-2}\,dx$ | $\infty$ | ❌ Diverges |

**Pattern Summary**:
- $\int_1^\infty x^{-p}\,dx$ converges **iff** $p > 1$
- $\int_0^1 x^{-p}\,dx$ converges **iff** $p < 1$

---

### 🟦 C7 Choosing Antidifferentiation Techniques (6.14 | FUN-6) — Decision Framework

#### 📝 Complete Decision Tree

When faced with an indefinite integral, ask yourself these questions in order:

```
Q1: Can this function be integrated directly using basic formulas?
  ├─ Yes → Integrate directly
  └─ No → Q2

Q2: Is there an "inner function" whose derivative appears (almost) in the integral?
  ├─ Yes → u-substitution
  └─ No → Q3

Q3: Is the integrand a rational function (polynomial fraction)?
  ├─ Numerator degree ≥ denominator degree → Long division first → back to Q1/Q2
  └─ Numerator degree < denominator degree → Q4

Q4: Can the denominator be factored? (BC)
  ├─ Yes → Partial fractions
  └─ No → Complete the square → arctan or ln form

Q5: Is the integrand a product of two different types of functions? (BC)
  ├─ Yes → Integration by parts
  └─ No → Check if trigonometric identities can simplify

Q6: Is the integral improper? (BC) → Use limits
```

---

## Module D: Applications of Integration

---

### 🟦 D1 Average Value of a Function (8.1 | CHA-4) — Deep Dive

#### 🧠 Why Is the Average Value Formula $\frac{1}{b-a}\int_a^b f(x)\,dx$?

A continuous function has infinitely many values. We can't compute an average the way we do with discrete data (summing and dividing by count). But we can think of it this way:

The "average value" is a constant $M$ such that the accumulation of $M$ over $[a, b]$ equals the accumulation of $f(x)$ over $[a, b]$.

That is: $M \cdot (b-a) = \int_a^b f(x)\,dx$

So: $M = \frac{1}{b-a}\int_a^b f(x)\,dx$

#### ⚠️ Confusion with Average Rate of Change

This is one of the most common confusions on the AP exam:

| Concept | Formula | Meaning |
|------|------|------|
| **Average Value** | $\frac{1}{b-a}\int_a^b f(x)\,dx$ | The average of the function values themselves |
| **Average Rate of Change** | $\frac{f(b)-f(a)}{b-a}$ | The average slope from $a$ to $b$ |

**How to distinguish?**
- If the problem says "average value of $f$" → use the integral
- If the problem says "average rate of change of $f$" → use the difference quotient

#### 📝 Complete Example

Find the average value of $f(x) = 3x^2$ on $[1, 4]$.

$$\text{Average value} = \frac{1}{4-1}\int_1^4 3x^2\,dx = \frac{1}{3}[x^3]_1^4 = \frac{1}{3}(64 - 1) = \frac{63}{3} = 21$$

---

### 🟦 D2 Motion Along a Line (8.2 | CHA-4) — Deep Dive

#### 📊 Complete Relationships Among Position, Velocity, and Acceleration

```
Position s(t)
  │ Differentiate: s'(t) = v(t)
  ▼
Velocity v(t)        ← Differential perspective
  │ Differentiate: v'(t) = a(t)
  ▼
Acceleration a(t)

Position s(t)        
  ▲ Integrate: s(t) = s(t₀) + ∫_{t₀}^t v(u)du
  │
Velocity v(t)        ← Integral perspective
  ▲ Integrate: v(t) = v(t₀) + ∫_{t₀}^t a(u)du
  │
Acceleration a(t)
```

#### 📝 Four Common Problem Types

**Type 1: Given $v(t)$, find displacement**
$$s(b) - s(a) = \int_a^b v(t)\,dt$$

**Type 2: Given $v(t)$, find total distance**
$$\text{Total distance} = \int_a^b |v(t)|\,dt$$

**📝 Detailed Steps for Total Distance**:
1. Find all $t$ where $v(t) = 0$ (when velocity changes sign)
2. On each interval where $v(t)$ has a constant sign, integrate $|v(t)| = \pm v(t)$
3. Sum the results from all intervals

**Type 3: Given $a(t)$ and initial conditions, find $v(t)$**
$$v(t) = v(t_0) + \int_{t_0}^t a(u)\,du$$

**Type 4: Comprehensive — Given $a(t)$ and ICs, find $s(t)$**
$$v(t) = v(t_0) + \int_{t_0}^t a(u)\,du$$
$$s(t) = s(t_0) + \int_{t_0}^t v(u)\,du$$

#### ⚠️ Common Mistake: Total Distance vs. Displacement

> **🎯 Exam Tip**: In AP free-response questions, if the problem says "total distance traveled," you **must** integrate $|v(t)|$. If it says "net change in position" or "displacement," integrate $v(t)$. Confusing these two can cost you the entire problem.

---

### 🟦 D3 Contextual Applications of Accumulated Change (8.3 | CHA-4) — Deep Dive

#### 🧠 Core Idea: Definite Integral = Net Change

If $F'(t) = f(t)$ is the rate of change, then:
$$F(b) - F(a) = \int_a^b f(t)\,dt$$

This is called the **Net Change Theorem**.

#### 📝 Application Contexts Summary

| Context | Rate of Change | Meaning of the Integral |
|------|--------|-----------|
| Water flowing into/out of a tank | $R_{\text{in}}(t) - R_{\text{out}}(t)$ | Net change in water volume |
| Population growth | $P'(t)$ | Net change in population |
| Bank account | Interest rate | Total interest earned |
| Energy consumption | Power (watts) | Total energy (joules) |
| Carbon-14 decay | Decay rate | Total amount decayed |
| Snow accumulation | Snowfall rate | Total snowfall |
| Blood flow | Flow rate | Total blood volume |

#### 📝 Typical AP Problem

**Example**: Water flows into a tank at a rate of $R(t) = 20 + 5\sin t$ gallons per hour. The tank initially contains 100 gallons of water. Find the amount of water at $t = 3$ hours.

$$V(3) = V(0) + \int_0^3 R(t)\,dt = 100 + \int_0^3 (20 + 5\sin t)\,dt$$
$$= 100 + [20t - 5\cos t]_0^3 = 100 + (60 - 5\cos 3) - (0 - 5)$$
$$= 100 + 65 - 5\cos 3 = 165 - 5\cos 3 \text{ gallons}$$

---

### 🟦 D4 Area Between Curves (8.4–8.6 | CHA-5) — Deep Dive

#### 🧠 The Essence of Area

Area $\int_a^b [\text{upper function} - \text{lower function}]\,dx$ is essentially: at each $x$, take a vertical line segment whose length is upper minus lower, then "accumulate" these lengths.

#### 📝 Three Scenarios and How to Handle Them

**Scenario 1: $x$ is the independent variable, upper function is clear**
$$A = \int_a^b [f(x) - g(x)]\,dx,\ \text{where } f(x) \geq g(x) \text{ on } [a, b]$$

**Scenario 2: $y$ is the independent variable**
$$A = \int_c^d [f(y) - g(y)]\,dy,\ \text{where } f(y) \geq g(y) \text{ on } [c, d]$$

**Scenario 3: Curves intersect multiple times, the upper function changes**
$$A = \int_a^b |f(x) - g(x)|\,dx$$
or piecewise: $A = \int_a^c [f(x)-g(x)]\,dx + \int_c^b [g(x)-f(x)]\,dx$

#### 📝 Complete Solution Procedure (with $x$ as variable)

```
Step 1: Find all intersection points → determine limits of integration
Step 2: On each subinterval, determine which function is on top
Step 3: For each subinterval, integrate (top - bottom)
Step 4: Sum the results from all subintervals
```

**Example**: Find the area between $y = x$ and $y = x^3$.

**Step 1: Find intersections**
$$x = x^3 \Rightarrow x^3 - x = 0 \Rightarrow x(x^2 - 1) = 0 \Rightarrow x = -1, 0, 1$$

**Step 2: Determine the upper function**
- On $[-1, 0]$: test $x = -0.5$, $x = -0.5$, $x^3 = -0.125$, so $x^3 > x$
- On $[0, 1]$: test $x = 0.5$, $x = 0.5$, $x^3 = 0.125$, so $x > x^3$

So:
- $[-1, 0]$: top = $x^3$, bottom = $x$, difference = $x^3 - x$
- $[0, 1]$: top = $x$, bottom = $x^3$, difference = $x - x^3$

**Step 3: Integrate**
$$A = \int_{-1}^0 (x^3 - x)\,dx + \int_0^1 (x - x^3)\,dx$$
$$= \left[\frac{x^4}{4} - \frac{x^2}{2}\right]_{-1}^0 + \left[\frac{x^2}{2} - \frac{x^4}{4}\right]_0^1$$
$$= (0 - 0) - \left(\frac{1}{4} - \frac{1}{2}\right) + \left(\frac{1}{2} - \frac{1}{4}\right) - 0$$
$$= \left(-\frac{1}{4} + \frac{1}{2}\right) + \left(\frac{1}{2} - \frac{1}{4}\right) = \frac{1}{4} + \frac{1}{4} = \frac{1}{2}$$

---

### 🟦 D5 Volume: Known Cross Sections (8.7–8.8 | CHA-5) — Deep Dive

#### 🧠 Core Idea

Volume = "stacking" cross-sectional areas.

$$V = \int_a^b A(x)\,dx$$

where $A(x)$ is the area of the cross-section perpendicular to the $x$-axis at position $x$.

#### 📝 Complete Solution Procedure

```
Step 1: Determine the direction of integration (perpendicular to which axis?)
Step 2: Write the cross-sectional area A(x) in terms of x
Step 3: Determine the limits of integration
Step 4: Integrate to find the volume
```

#### 📝 Four Types of Cross Sections Explained

**1. Square Cross Sections**

If the base boundaries are $y = f(x)$ (top) and $y = g(x)$ (bottom), the side length $s(x) = f(x) - g(x)$:
$$V = \int_a^b [f(x) - g(x)]^2\,dx$$

**2. Isosceles Right Triangle Cross Sections**

- Right angle on the $x$-axis (legs parallel to axes): $A(x) = \frac{1}{2}[f(x) - g(x)]^2$
- Hypotenuse on the $x$-axis: $A(x) = \frac{1}{2}\left(\frac{f(x)-g(x)}{2}\right)^2$ (be careful!)

**3. Semicircular Cross Sections**

Diameter on the $x$-axis, radius $r(x) = \frac{f(x)-g(x)}{2}$:
$$V = \int_a^b \frac{\pi}{2}[r(x)]^2\,dx = \int_a^b \frac{\pi}{2}\left(\frac{f(x)-g(x)}{2}\right)^2\,dx = \frac{\pi}{8}\int_a^b [f(x)-g(x)]^2\,dx$$

**4. Rectangular Cross Sections**

If the height $h(x)$ is given separately:
$$V = \int_a^b [f(x)-g(x)]\cdot h(x)\,dx$$

---

### 🟦 D6 Volume of Solids of Revolution (8.9–8.12 | CHA-5) — Deep Dive

#### 🧠 Choosing Between Disc and Washer Methods

| Condition | Method |
|------|------|
| Region touches the axis of rotation (no hole) | Disc Method |
| There's a gap between region and axis (hole in the middle) | Washer Method |

#### 📝 Disc Method Explained

**Revolving around the $x$-axis**: $R(x) = f(x)$ (distance from $x$-axis to the curve)
$$V = \pi \int_a^b [f(x)]^2\,dx$$

**Revolving around $y = c$**: $R(x) = |f(x) - c|$
$$V = \pi \int_a^b [f(x) - c]^2\,dx$$

> **📝 Self-Study Tip**: The radius of rotation = |distance from curve to axis of rotation|. If the curve is above the axis, $R(x) = f(x) - c$.

#### 📝 Washer Method Explained

**Revolving around the $x$-axis (hollow)**:
$$V = \pi \int_a^b ([R_{\text{outer}}(x)]^2 - [R_{\text{inner}}(x)]^2)\,dx$$

where $R_{\text{outer}}$ = distance from outer curve to axis, $R_{\text{inner}}$ = distance from inner curve to axis.

**Revolving around $y = c$ (hollow)**:
$$V = \pi \int_a^b ([\text{upper curve} - c]^2 - [\text{lower curve} - c]^2)\,dx$$

Or more generally: $V = \pi \int_a^b ([f_{\text{far}}(x) - c]^2 - [f_{\text{near}}(x) - c]^2)\,dx$

#### 📝 Complete Example: Washer Method

Find the volume of the solid generated by revolving the region bounded by $y = x$ and $y = x^2$ around the $x$-axis ($y = 0$).

**Step 1: Find intersections**
$$x = x^2 \Rightarrow x = 0, 1$$

**Step 2: Determine outer and inner radii**
On $[0, 1]$: $x \geq x^2$
- Outer curve: $y = x$, $R_{\text{out}} = x$
- Inner curve: $y = x^2$, $R_{\text{in}} = x^2$

**Step 3: Integrate**
$$V = \pi \int_0^1 (x^2 - (x^2)^2)\,dx = \pi \int_0^1 (x^2 - x^4)\,dx = \pi\left[\frac{x^3}{3} - \frac{x^5}{5}\right]_0^1 = \pi\left(\frac{1}{3} - \frac{1}{5}\right) = \frac{2\pi}{15}$$

#### ⚠️ Common Mistake: Confusing the $x$-axis and $y$-axis

- Revolving around the $x$-axis → integrate with respect to $x$
- Revolving around the $y$-axis → integrate with respect to $y$

If revolving around the $y$-axis but the function is given as $y = f(x)$, you first need to solve for $x = g(y)$.

---

### 🟪 D7 Arc Length (8.13 | CHA-6) — BC ONLY Deep Dive

#### 🧠 Derivation of the Arc Length Formula

Imagine cutting a curve into infinitely many tiny pieces. Each small piece can be approximated as the hypotenuse of a right triangle:
$$ds = \sqrt{(dx)^2 + (dy)^2} = \sqrt{1 + \left(\frac{dy}{dx}\right)^2}\,dx$$

Summing all pieces and taking the limit:
$$L = \int_a^b \sqrt{1 + [f'(x)]^2}\,dx$$

#### 📝 Two Forms of Arc Length

**Rectangular form** ($y = f(x)$):
$$L = \int_a^b \sqrt{1 + [f'(x)]^2}\,dx$$

**Parametric form** ($x = x(t), y = y(t)$):
$$L = \int_a^b \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}\,dt$$

---

# Part II: Differential Equations

---

## Module E: Differential Equations (Unit 7)

---

### 🟦 E1-E2 Setting Up and Verifying Differential Equations (7.1–7.2 | FUN-7) — Deep Dive

#### 🧠 Definition of a Differential Equation

A differential equation is an equation that involves an **unknown function and its derivative(s)**. It describes not the function itself, but the **law of change** of the function.

**Sentence Translation**: "The rate of change of a quantity is proportional to its size" → $\frac{dy}{dt} = ky$

#### 📝 Common Verbal → Equation Translations

| Verbal Description | Differential Equation |
|----------|---------|
| "Rate of change is proportional to $x$" | $\frac{dy}{dx} = kx$ |
| "Rate of change is proportional to $y$" | $\frac{dy}{dx} = ky$ |
| "Rate of change is proportional to the product of $x$ and $y$" | $\frac{dy}{dx} = kxy$ |
| "Rate of change is proportional to $y$ and $(a-y)$" | $\frac{dy}{dt} = ky(a-y)$ |
| "Rate of change is a function of $x$ and $y$" | $\frac{dy}{dx} = f(x,y)$ |

#### 📝 Steps for Verifying a Solution

**Example**: Verify that $y = 3e^{2x}$ is a solution to $\frac{dy}{dx} = 2y$ and satisfies $y(0) = 3$.

```
Step 1: Compute the derivative → y' = 6e^{2x}
Step 2: Substitute into the DE → 6e^{2x} = 2(3e^{2x}) = 6e^{2x} ✅
Step 3: Check the initial condition → y(0) = 3e^{0} = 3 ✅
```

> **🎯 Exam Tip**: On the AP exam, verifying a solution requires writing out the differentiation steps completely. You cannot skip steps or just state by observation.

---

### 🟦 E3-E4 Slope Fields (7.3–7.4 | FUN-7) — Deep Dive

#### 🧠 How to Interpret Slope Fields

Each small line segment in a slope field at point $(x, y)$ has slope $f(x, y)$. A solution curve is **tangent** to the slope at every point.

**From a slope field, you can infer**:
- The general direction of solution curves
- Equilibrium solutions — horizontal lines where slope = 0
- How solution curves diverge/converge with different initial conditions

#### 📝 From Differential Equation to Slope Field

**Example**: Compute slopes for $\frac{dy}{dx} = x - y$ at several points.

| $(x, y)$ | Slope $x - y$ |
|----------|-------------|
| $(0, 0)$ | $0$ |
| $(1, 0)$ | $1$ |
| $(0, 1)$ | $-1$ |
| $(1, 1)$ | $0$ |
| $(2, 1)$ | $1$ |

---

### 🟪 E5 Euler's Method (7.5 | FUN-7) — BC ONLY Deep Dive

#### 🧠 The Essence of Euler's Method

Euler's method approximates a solution curve using a **sequence of tangent line segments**. You start at the initial point, walk a short distance along the tangent line to a new point, then from that new point walk along its tangent line, and so on.

#### 📝 Algorithm Step by Step

Given $\frac{dy}{dx} = f(x, y)$, $(x_0, y_0)$, step size $h$:

$$x_{n+1} = x_n + h$$
$$y_{n+1} = y_n + h \cdot f(x_n, y_n)$$

> **🎯 Exam Tip**: On the AP exam, Euler's method typically only requires 2-3 steps. Scoring focuses on whether you've correctly applied the iterative formula, not on the numerical precision of the final value.

#### 📝 Complete Example

Use Euler's method with $h = 0.2$ to approximate $y(0.6)$ for $\frac{dy}{dx} = x + y$, $y(0) = 1$.

| $n$ | $x_n$ | $y_n$ | $f(x_n, y_n) = x_n + y_n$ | $y_{n+1} = y_n + h \cdot f$ |
|-----|-------|-------|---------------------------|----------------------------|
| 0 | 0 | 1.0 | 1.0 | $1.0 + 0.2(1.0) = 1.2$ |
| 1 | 0.2 | 1.2 | 1.4 | $1.2 + 0.2(1.4) = 1.48$ |
| 2 | 0.4 | 1.48 | 1.88 | $1.48 + 0.2(1.88) = 1.856$ |
| 3 | 0.6 | 1.856 | — | — |

So $y(0.6) \approx 1.856$.

---

### 🟦 E6-E7 Separation of Variables (7.6–7.7 | FUN-7) — Deep Dive

#### 📝 Standard Solution Procedure (Should Become Second Nature)

```
Step 1: Separate variables
  → Move all terms containing y (including dy) to the left side,
     all terms containing x (including dx) to the right side
  → Form: g(y)dy = h(x)dx

Step 2: Integrate both sides
  → ∫g(y)dy = ∫h(x)dx
  → Obtain G(y) = H(x) + C

Step 3: Substitute the initial condition to find C
  → Plug (x₀, y₀) into G(y) = H(x) + C

Step 4: Solve for y (if possible)
  → Either explicit form y = f(x) or implicit form
```

#### 📝 Complete Example

Find the particular solution to $\frac{dy}{dx} = 2xy$ satisfying $y(0) = 3$.

| Step | Operation | Result |
|------|------|------|
| 1 | Separate variables | $\frac{dy}{y} = 2x\,dx$ |
| 2 | Integrate both sides | $\ln|y| = x^2 + C$ |
| 3 | Substitute $x=0, y=3$ | $\ln 3 = 0 + C \Rightarrow C = \ln 3$ |
| 4 | Solve for $y$ | $\ln|y| = x^2 + \ln 3 \Rightarrow y = 3e^{x^2}$ |

#### ⚠️ Common Mistakes

**Mistake 1: Forgetting the constant $C$**
- This is the most critical error. In AP scoring, missing the constant $C$ will cost nearly all the points for that step.

**Mistake 2: Not separating variables properly**
- $\frac{dy}{dx} = 2xy$ must become $\frac{dy}{y} = 2x\,dx$. You cannot directly integrate $\int \frac{dy}{dx}\,dx = \int 2xy\,dx$.

**Mistake 3: Mishandling $\ln$ and exponentials**
- $\ln|y| = x^2 + C$ should **not** become $y = e^{x^2} + e^C$. The correct step is $y = \pm e^{x^2 + C} = \pm e^C \cdot e^{x^2} = Ae^{x^2}$.

---

### 🟦 E8 Exponential Growth and Decay (7.8 | FUN-7) — Deep Dive

#### 🧠 Intuition Behind the Model

"The rate of change is proportional to the size" means: **the bigger it gets, the faster it grows** (growth); or **the smaller it gets, the slower it decays** (decay).

This is why exponential growth produces a "J-shaped" curve, while exponential decay approaches zero asymptotically without ever reaching it.

#### 📝 Key Formula and Derivation

$$\frac{dy}{dt} = ky$$

$$\int \frac{dy}{y} = \int k\,dt \Rightarrow \ln|y| = kt + C \Rightarrow y = Ae^{kt}$$

Plug in $t = 0$, $y = y_0$: $A = y_0$

$$\boxed{y(t) = y_0 e^{kt}}$$

#### 📝 Applications by Type

| Scenario | Sign of $k$ | Application |
|------|---------|------|
| Population growth | $k > 0$ | $P(t) = P_0 e^{kt}$ |
| Radioactive decay | $k < 0$ | $A(t) = A_0 e^{-kt}$ |
| Continuous compounding | $k > 0$ | $A(t) = P e^{rt}$ |
| Newton's Law of Cooling | $k < 0$ | $T(t) = T_{\text{ambient}} + (T_0 - T_{\text{ambient}})e^{-kt}$ |

#### 📝 Half-Life Problems

The half-life $T_{1/2}$ of a radioactive substance satisfies $A(T_{1/2}) = \frac{1}{2}A_0$:

$$\frac{1}{2}A_0 = A_0 e^{-kT_{1/2}} \Rightarrow \frac{1}{2} = e^{-kT_{1/2}} \Rightarrow -kT_{1/2} = \ln\frac{1}{2} = -\ln 2$$

$$\boxed{T_{1/2} = \frac{\ln 2}{k}}$$

**Example**: A substance has a half-life of 10 years. Initially 100g, find the mass after $t$ years.

$$k = \frac{\ln 2}{10} \Rightarrow m(t) = 100 e^{-(\ln 2)t/10} = 100 \cdot 2^{-t/10}$$

---

### 🟪 E9 The Logistic Growth Model (7.9 | FUN-7) — BC ONLY Deep Dive

#### 🧠 Intuition Behind the Model

Exponential growth assumes "unlimited resources" — which doesn't hold in reality. Logistic growth incorporates a **carrying capacity** $K$: when the population approaches $K$, resources become scarce and the growth rate decreases.

**Differential Equation**:
$$\frac{dy}{dt} = ky\left(1 - \frac{y}{K}\right) \quad \text{equivalent to } \frac{dy}{dt} = \frac{k}{K}y(K - y)$$

#### 📝 Properties You Can Infer Without Solving

| Condition | Property |
|------|------|
| $y$ is much smaller than $K$ | $\frac{dy}{dt} \approx ky$, approximately exponential growth |
| $y = K/2$ | Maximum growth rate (inflection point of the S-curve) |
| $y = K$ | $\frac{dy}{dt} = 0$, equilibrium reached |
| $y > K$ | $\frac{dy}{dt} < 0$, population decreases toward $K$ |
| $t \to \infty$ | $y \to K$ |

#### 📝 S-Curve Characteristics

```
y
↑
K ──────────────── asymptote
|          ↗
|       ↗
|    ↗
| ↗             ← inflection point at y = K/2
|
0 ──────────────→ t
```

#### 📝 Sample Application

**Example**: A fish population in a lake satisfies $\frac{dP}{dt} = 0.02P(1000 - P)$, $P(0) = 100$.

(a) What is the carrying capacity?
- As $P$ approaches $K$, the growth rate approaches 0, so $K = 1000$.

(b) At what population does the fish population grow fastest?
- $P = \frac{K}{2} = 500$.

---

# Part III: Plane Curves (BC Only)

---

## Module F: Parametric Equations, Polar Coordinates, and Vector-Valued Functions (Unit 9)

---

### 🟪 F1 Parametric Equations and Derivatives (9.1–9.2 | CHA-3) — Deep Dive

#### 🧠 Why Do We Need Parametric Equations?

Some curves (like circles or cycloids) cannot be expressed as $y = f(x)$ (because a single $x$ corresponds to multiple $y$ values). Parametric equations solve this by introducing a third variable $t$ (the parameter):

$$x = f(t),\quad y = g(t)$$

Now both $x$ and $y$ are functions of $t$, and the curve is defined by the set of points $\{(f(t), g(t)) : t \in I\}$.

#### 📝 Derivation of the First Derivative via Chain Rule

$$\frac{dy}{dt} = \frac{dy}{dx} \cdot \frac{dx}{dt} \quad \Rightarrow \quad \frac{dy}{dx} = \frac{dy/dt}{dx/dt}$$

Provided: $\frac{dx}{dt} \neq 0$.

#### 📝 Correct Calculation of the Second Derivative

**⚠️ Wrong approach**: Differentiate $\frac{dy}{dx}$ directly with respect to $t$.

**Correct approach**:
$$\frac{d^2y}{dx^2} = \frac{d}{dx}\left(\frac{dy}{dx}\right) = \frac{\frac{d}{dt}\left(\frac{dy}{dx}\right)}{\frac{dx}{dt}}$$

> **📝 Self-Study Tip**: Every time you need $\frac{d^2y}{dx^2}$, first differentiate $\frac{dy}{dx}$ (which is a function of $t$) with respect to $t$, then divide by $\frac{dx}{dt}$.

**Complete Example**: $x = t^2$, $y = t^3$, find $\frac{dy}{dx}$ and $\frac{d^2y}{dx^2}$ at $t = 2$.

$$\frac{dy}{dx} = \frac{3t^2}{2t} = \frac{3t}{2},\quad \text{at } t=2:\ \frac{dy}{dx} = 3$$

$$\frac{d^2y}{dx^2} = \frac{\frac{d}{dt}(3t/2)}{2t} = \frac{3/2}{2t} = \frac{3}{4t},\quad \text{at } t=2:\ \frac{d^2y}{dx^2} = \frac{3}{8}$$

---

### 🟪 F2 Vector-Valued Functions and Motion (9.4–9.6 | CHA-3, FUN-8) — Deep Dive

#### 📝 Complete Relationships Among the Five Core Quantities

| Quantity | Symbol | Formula | Relation to Parametric Equations |
|----|------|------|-----------------|
| **Position** | $\mathbf{r}(t)$ | $\langle x(t), y(t) \rangle$ | — |
| **Velocity** | $\mathbf{v}(t)$ | $\mathbf{r}'(t) = \langle x'(t), y'(t) \rangle$ | Derivative of position |
| **Speed** | $\text{speed}(t)$ | $|\mathbf{v}(t)| = \sqrt{[x'(t)]^2 + [y'(t)]^2}$ | Magnitude of velocity |
| **Acceleration** | $\mathbf{a}(t)$ | $\mathbf{v}'(t) = \langle x''(t), y''(t) \rangle$ | Derivative of velocity |
| **Displacement** | $\Delta\mathbf{r}$ | $\int_a^b \mathbf{v}(t)\,dt$ | Integrate each component |
| **Total Distance** | $D$ | $\int_a^b |\mathbf{v}(t)|\,dt$ | Integral of speed |

#### 📝 Determining Whether Speed is Increasing or Decreasing

This is a common AP exam topic:

- Speed is **increasing** iff $\frac{d}{dt}(|\mathbf{v}(t)|) > 0$, i.e., $\mathbf{v}(t) \cdot \mathbf{a}(t) > 0$ (velocity and acceleration are in the same direction)
- Speed is **decreasing** iff $\mathbf{v}(t) \cdot \mathbf{a}(t) < 0$ (velocity and acceleration are in opposite directions)

**Intuitive understanding**: If acceleration is in the same direction as velocity, the object speeds up; if opposite, it slows down.

> **🎯 Exam Tip**: On the AP exam, you cannot simply say "speed is increasing because acceleration is positive." You must state the **directional relationship** between velocity and acceleration.

---

### 🟪 F3 Polar Coordinates (9.7–9.9 | FUN-3, CHA-5) — Deep Dive

#### 🧠 Intuition Behind Polar Coordinates

Rectangular coordinates describe a point as "how far east, how far north." Polar coordinates describe a point as "how far from the origin, in which direction."

$r = f(\theta)$ means: at angle $\theta$, the distance from the origin is $f(\theta)$.

#### 📝 Derivatives in Polar Form

Treat $x = r\cos\theta = f(\theta)\cos\theta$, $y = r\sin\theta = f(\theta)\sin\theta$ as parametric equations with parameter $\theta$:

$$\frac{dy}{dx} = \frac{dy/d\theta}{dx/d\theta} = \frac{f'(\theta)\sin\theta + f(\theta)\cos\theta}{f'(\theta)\cos\theta - f(\theta)\sin\theta}$$

#### 📝 Derivation of the Polar Area Formula

In polar coordinates, regions are divided into **sectors** rather than rectangles.

Area of a sector with radius $r$ and angle $\Delta\theta$ = $\frac{1}{2}r^2\Delta\theta$.

Therefore:
$$A = \frac{1}{2}\int_{\alpha}^{\beta} [f(\theta)]^2\,d\theta$$

#### 📝 Common Polar Curves

| Equation | Name | Shape |
|------|------|---------|
| $r = a$ | Circle | Radius $a$, centered at origin |
| $r = a\cos\theta$ | Circle | Diameter $a$, centered at $(a/2, 0)$ |
| $r = a\sin\theta$ | Circle | Diameter $a$, centered at $(0, a/2)$ |
| $r = a + b\cos\theta$ | Limaçon | $a = b$ = cardioid, $a > b$ = dimpled |
| $r = a\cos(n\theta)$ | Rose | $n$ petals if $n$ odd, $2n$ petals if $n$ even |
| $r^2 = a^2\cos(2\theta)$ | Lemniscate | Figure-eight shape |

#### 📝 Complete Area Calculation Example

Find the area enclosed by the polar curve $r = 1 + \cos\theta$.

$$A = \frac{1}{2}\int_0^{2\pi} (1 + \cos\theta)^2\,d\theta = \frac{1}{2}\int_0^{2\pi} (1 + 2\cos\theta + \cos^2\theta)\,d\theta$$
$$= \frac{1}{2}\int_0^{2\pi} \left(1 + 2\cos\theta + \frac{1+\cos 2\theta}{2}\right)d\theta = \frac{1}{2}\int_0^{2\pi} \left(\frac{3}{2} + 2\cos\theta + \frac{1}{2}\cos 2\theta\right)d\theta$$
$$= \frac{1}{2}\left[\frac{3}{2}\theta + 2\sin\theta + \frac{1}{4}\sin 2\theta\right]_0^{2\pi} = \frac{1}{2}\left(\frac{3}{2} \cdot 2\pi\right) = \frac{3\pi}{2}$$

---

# Part IV: Infinite Sequences and Series (BC Only)

---

## Module G: Series Convergence Tests (First Half of Unit 10)

---

### 🟪 G1 Basic Concepts of Series (10.1 | LIM-7) — Deep Dive

#### 🧠 The Central Paradox of Infinite Series

"Adding infinitely many terms, yet the result is a finite number" — this sounds counterintuitive, but it does happen.

**Key concept**: Partial sums $S_N = \sum_{n=1}^N a_n$.

If the sequence of partial sums $\{S_N\}$ approaches a finite limit $S$ as $N \to \infty$, then the series converges to $S$.

**Analogy**: Imagine walking toward a wall. In the first second you cover half the distance, in the next second half of the remaining distance, and so on. You never quite reach the wall (there's always half remaining), but the total distance you've traveled approaches the full distance.

---

### 🟪 G2 Geometric Series (10.2 | LIM-7) — Deep Dive

#### 📝 Complete Analysis of Geometric Series

**Definition**: $\sum_{n=0}^\infty ar^n = a + ar + ar^2 + ar^3 + \cdots$

**Roles of $a$ and $r$**:
- $a$ is the first term
- $r$ is the common ratio — the ratio between consecutive terms

**Convergence**:
- $|r| < 1$: Converges
- $|r| \geq 1$: Diverges

**Derivation of the Sum Formula** (helps with memorization):
$$S_N = a + ar + ar^2 + \cdots + ar^{N-1}$$
$$rS_N = ar + ar^2 + \cdots + ar^{N-1} + ar^N$$
$$S_N - rS_N = a - ar^N \Rightarrow S_N = \frac{a(1 - r^N)}{1 - r}$$
When $|r| < 1$, $r^N \to 0$, so $S_\infty = \frac{a}{1 - r}$.

---

### 🟪 G3-G8 Quick Reference: Seven Convergence Tests

| Test | Conditions | Conclusion | When to Use |
|------|---------|------|---------|
| **$n$th Term Test** | All series | $\lim a_n \neq 0 \Rightarrow$ Diverges | First — quickly eliminates divergent series |
| **Integral Test** | $a_n = f(n)$, $f$ continuous, positive, decreasing | $\int f(x)\,dx$ conv. $\Leftrightarrow$ $\sum a_n$ conv. | When $a_n$ is a simple function form |
| **$p$-Series** | $\sum \frac{1}{n^p}$ | $p > 1$ conv., $p \leq 1$ div. | Directly identify a $p$-series |
| **Direct Comparison** | $a_n \geq 0$ | Compare with known series | Obvious comparison candidate |
| **Limit Comparison** | $a_n, b_n \geq 0$ | $\lim a_n/b_n = c \neq 0$ $\Rightarrow$ same convergence | Complex fractions with no obvious direct comparison |
| **Alternating Series** | $(-1)^n b_n$, $b_n \downarrow 0$ | Converges | Series with alternating signs |
| **Ratio Test** | Contains $n!$ or $a^n$ | $L < 1$ conv., $L > 1$ div. | Series with factorials/exponentials |

> **🎯 Exam Tip**: On the AP exam, applying any convergence test requires **explicitly stating that the conditions are satisfied**. For example, the alternating series test requires you to state "$b_n$ is decreasing and approaches 0."

---

### 🟪 G9 Absolute vs. Conditional Convergence (10.9 | LIM-7)

#### 📝 Decision Flowchart

```
Given series ∑a_n
    ↓
Does ∑|a_n| converge?
    ├─ Yes → ∑a_n is absolutely convergent (and therefore convergent)
    └─ No → Does ∑a_n converge?
              ├─ Yes → ∑a_n is conditionally convergent
              └─ No → ∑a_n diverges
```

**Examples**:
- $\sum \frac{(-1)^{n-1}}{n^2}$: $\sum \frac{1}{n^2}$ converges ($p=2>1$) → **Absolutely convergent**
- $\sum \frac{(-1)^{n-1}}{n}$: $\sum \frac{1}{n}$ diverges, but the alternating harmonic series converges → **Conditionally convergent**

---

### 🟪 G10 Alternating Series Error Bound (10.10 | LIM-7)

#### 📝 Intuitive Understanding

When approximating the sum $S$ of a convergent alternating series by $S_N$, the error is no larger than the absolute value of the first omitted term:
$$|S - S_N| \leq b_{N+1}$$

**Example**: Approximate $\sum_{n=1}^\infty \frac{(-1)^{n-1}}{n} = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots$ using the first 2 terms.

$S_2 = 1 - \frac{1}{2} = 0.5$, error $\leq b_3 = \frac{1}{3} \approx 0.333$.

---

## Module H: Power Series and Taylor Series (Second Half of Unit 10)

---

### 🟪 H1 Taylor Polynomials (10.11 | LIM-8) — Deep Dive

#### 🧠 Core Idea Behind Taylor Polynomials

"Approximate any smooth function using polynomials."

An $n$th-degree polynomial has $n+1$ coefficients. To make it as similar as possible to $f(x)$ near $x = a$, we require that the polynomial and $f(x)$ have exactly the same value, first derivative, second derivative, ..., and $n$th derivative at $x = a$.

#### 📝 Derivation of the Coefficient Formula

Let $P_n(x) = c_0 + c_1(x-a) + c_2(x-a)^2 + \cdots + c_n(x-a)^n$

Require $P_n(a) = f(a)$, $P_n'(a) = f'(a)$, $\ldots$, $P_n^{(n)}(a) = f^{(n)}(a)$:

$$P_n(a) = c_0 = f(a) \Rightarrow c_0 = f(a)$$
$$P_n'(a) = c_1 = f'(a) \Rightarrow c_1 = f'(a)$$
$$P_n''(a) = 2c_2 = f''(a) \Rightarrow c_2 = \frac{f''(a)}{2!}$$
$$\vdots$$
$$P_n^{(n)}(a) = n! c_n = f^{(n)}(a) \Rightarrow c_n = \frac{f^{(n)}(a)}{n!}$$

#### 📝 Complete Example: 3rd-Order Maclaurin Polynomial for $e^x$

| $n$ | $f^{(n)}(0)$ | Coefficient $f^{(n)}(0)/n!$ | Term |
|-----|-------------|---------------------|----|
| 0 | $e^0 = 1$ | $1/0! = 1$ | $1$ |
| 1 | $e^0 = 1$ | $1/1! = 1$ | $x$ |
| 2 | $e^0 = 1$ | $1/2! = 1/2$ | $x^2/2$ |
| 3 | $e^0 = 1$ | $1/3! = 1/6$ | $x^3/6$ |

$$P_3(x) = 1 + x + \frac{x^2}{2} + \frac{x^3}{6}$$

---

### 🟪 H2 Lagrange Error Bound (10.12 | LIM-8)

#### 📝 Formula Explained

$$|f(x) - P_n(x)| \leq \frac{M}{(n+1)!}|x-a|^{n+1}$$

where $M = \max\{|f^{(n+1)}(z)|: z \text{ is between } x \text{ and } a\}$.

**Understanding**:
- The error depends on the **size of the $(n+1)$st derivative** ($M$) and the **distance from the center** ($|x-a|^{n+1}$).
- The higher the degree $n$, the smaller the error (since $(n+1)!$ grows extremely fast).
- The closer to the center, the smaller the error.

> **🎯 Exam Tip**: On the AP exam, when using the Lagrange error bound, you need to find a reasonable upper bound for $M$ (usually achieved at an endpoint of the interval).

---

### 🟪 H3 Radius and Interval of Convergence of Power Series (10.13 | LIM-8)

#### 📝 Complete Solution Procedure

```
Step 1: Apply the ratio test to the power series ∑c_n(x-a)^n
  → lim |c_{n+1}(x-a)^{n+1} / (c_n(x-a)^n)| = lim |c_{n+1}/c_n|·|x-a|
  → Set the limit < 1, solve for |x-a| < R
  → R is the radius of convergence

Step 2: Test the endpoints x = a-R and x = a+R separately
  → Substitute the endpoint value into the series
  → Use a known convergence test to determine convergence/divergence
  → Determine whether the interval is open, closed, or half-open

Step 3: Write the interval of convergence
```

**Example**: Find the radius and interval of convergence of $\sum_{n=1}^\infty \frac{x^n}{n}$.

$$\left|\frac{a_{n+1}}{a_n}\right| = \left|\frac{x^{n+1}/(n+1)}{x^n/n}\right| = |x| \cdot \frac{n}{n+1} \to |x|$$

$|x| < 1 \Rightarrow R = 1$ (radius of convergence)

**Endpoint testing**:
- $x = 1$: $\sum \frac{1}{n}$ diverges (harmonic series)
- $x = -1$: $\sum \frac{(-1)^n}{n}$ converges (alternating series test)

Interval of convergence: $[-1, 1)$

---

### 🟪 H4-H5 Common Series and Representing Functions as Power Series (10.14–10.15 | LIM-8)

#### 📝 Five Fundamental Series (Must Memorize)

**1. Geometric Series**
$$\frac{1}{1-x} = \sum_{n=0}^\infty x^n = 1 + x + x^2 + x^3 + \cdots,\quad |x| < 1$$

**2. Exponential Function**
$$e^x = \sum_{n=0}^\infty \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots$$

**3. Sine Function**
$$\sin x = \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots$$

**4. Cosine Function**
$$\cos x = \sum_{n=0}^\infty \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots$$

**5. Natural Logarithm**
$$\ln(1+x) = \sum_{n=1}^\infty \frac{(-1)^{n-1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots,\quad -1 < x \leq 1$$

#### 📝 Four Operations for Constructing New Series from Known Ones

**Operation 1: Algebraic Substitution**

$$e^{-x^2} = \sum_{n=0}^\infty \frac{(-x^2)^n}{n!} = \sum_{n=0}^\infty \frac{(-1)^n x^{2n}}{n!}$$

**Operation 2: Multiplication/Division**

$$\frac{e^x - 1}{x} = \frac{1}{x}\left(\sum_{n=0}^\infty \frac{x^n}{n!} - 1\right) = \frac{1}{x}\sum_{n=1}^\infty \frac{x^n}{n!} = \sum_{n=1}^\infty \frac{x^{n-1}}{n!} = \sum_{n=0}^\infty \frac{x^n}{(n+1)!}$$

**Operation 3: Term-by-Term Differentiation**

$$\frac{1}{(1-x)^2} = \frac{d}{dx}\left(\frac{1}{1-x}\right) = \frac{d}{dx}\sum_{n=0}^\infty x^n = \sum_{n=1}^\infty nx^{n-1} = \sum_{n=0}^\infty (n+1)x^n$$

**Operation 4: Term-by-Term Integration**

$$\arctan x = \int_0^x \frac{1}{1+t^2}\,dt = \int_0^x \sum_{n=0}^\infty (-t^2)^n\,dt = \int_0^x \sum_{n=0}^\infty (-1)^n t^{2n}\,dt$$
$$= \sum_{n=0}^\infty (-1)^n \int_0^x t^{2n}\,dt = \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{2n+1}$$

> **🎯 Exam Tip**: Term-by-term differentiation and integration do **not** change the radius of convergence (though the endpoint behavior may change).

#### 📝 Complete Generation Example

Find the Maclaurin series for $f(x) = \ln(1+x^2)$.

**Method 1**: Use the known series $\ln(1+u) = \sum_{n=1}^\infty \frac{(-1)^{n-1} u^n}{n}$, substitute $u = x^2$:
$$\ln(1+x^2) = \sum_{n=1}^\infty \frac{(-1)^{n-1} (x^2)^n}{n} = \sum_{n=1}^\infty \frac{(-1)^{n-1} x^{2n}}{n}$$

**Method 2**: Use integration
$$\frac{d}{dx}\ln(1+x^2) = \frac{2x}{1+x^2} = 2x \cdot \frac{1}{1-(-x^2)} = 2x \sum_{n=0}^\infty (-x^2)^n = 2\sum_{n=0}^\infty (-1)^n x^{2n+1}$$
$$\ln(1+x^2) = \int 2\sum_{n=0}^\infty (-1)^n x^{2n+1}\,dx = 2\sum_{n=0}^\infty (-1)^n \frac{x^{2n+2}}{2n+2} + C$$
Plug in $x = 0$ to get $\ln 1 = 0 = C$, so:
$$\ln(1+x^2) = \sum_{n=0}^\infty \frac{(-1)^n x^{2n+2}}{n+1} = \sum_{n=1}^\infty \frac{(-1)^{n-1} x^{2n}}{n}$$

Both methods yield the same result.

---

# 📊 Self-Study Schedule: Units 6–10

| Week | Content | Key Outcomes |
|------|---------|------|
| **Week 1** | Module A+B: Riemann Sums → FTC (6.1–6.7) | Compute definite integrals, understand FTC, analyze accumulation functions |
| **Week 2** | Module C: Antidifferentiation Techniques (6.8–6.14) | Master all integration methods (BC: parts/partial fractions/improper) |
| **Week 3** | Module D: Applications of Integration (8.1–8.13) | Find area, volume (disc/washer/cross sections), arc length (BC) |
| **Week 4** | Module E: Differential Equations (7.1–7.9) | Separation of variables, slope fields, Euler (BC), logistic (BC) |
| **Week 5** | Module F: Parametric/Polar/Vector (9.1–9.9) ⚠️ BC | Derivatives, arc length, area, motion problems |
| **Week 6** | Module G: Convergence Tests (10.1–10.10) ⚠️ BC | Apply 7 tests, determine absolute/conditional convergence |
| **Week 7** | Module H: Taylor/Power Series (10.11–10.15) ⚠️ BC | Expand Taylor series, find interval of convergence, error bounds |
| **Week 8** | Comprehensive Review + Practice Exams | Integrate all knowledge |

---

This comprehensive English guide extends every core topic in Units 6–10 with deeper intuition, common error analysis, detailed step-by-step procedures, and exam tips. All content is aligned with the AP Calculus AB/BC Course and Exam Description's Enduring Understandings. Let me know if you'd like further expansion on any specific topic!
