# AP Calculus AB & BC — Units 6–10 Comprehensive Summary

---

# UNIT 6: Integration and Accumulation of Change

> **Exam Weight**: AB 17–20% / BC 17–20% (Highest-weighted unit in both exams)
> **Suggested Class Periods**: AB ~18–20 / BC ~15–16
> **Dominant Big Ideas**: CHA (Change), LIM (Limits), FUN (Analysis of Functions)
> **Corresponding Enduring Understandings**: LIM-5, LIM-6, FUN-5, FUN-6

---

## 6.1 Exploring Accumulations of Change

**Core Idea**: The essence of integration is "accumulation"—accumulating a rate of change yields the net change in a quantity. This topic builds the intuitive connection between a rate of change and the accumulated quantity.

**Key Knowledge**:
- If we know the **rate of change** $f'(x)$ of a quantity, then the **net change** in that quantity over $[a, b]$ is $f(b) - f(a)$, which can be expressed as a definite integral of $f'$.
- This addresses the fundamental question: "Why can a definite integral represent area?" — because area is itself the accumulation of infinitely many "heights" (function values) times "widths" ($dx$).

**Example**: If a car's velocity function is $v(t)$ (miles per hour), then $\int_a^b v(t)\,dt$ represents the total distance traveled from time $a$ to $b$ (miles). The physical meaning is "accumulating the rate of change (velocity) to obtain the net change (displacement)."

---

## 6.2 Approximating Areas with Riemann Sums

**Enduring Understanding LIM-5**: Definite integrals can be approximated using geometric and numerical methods.

**Key Knowledge**:
- Definite integrals can be approximated using **left Riemann sums, right Riemann sums, midpoint Riemann sums**, or **trapezoidal sums**.
- Approximations can be based on either **uniform** or **nonuniform partitions**.
- Depending on the behavior of the function, one can determine whether an approximation is an **underestimate** or **overestimate**:
  - If $f$ is **increasing** on the interval: left Riemann sum $\Rightarrow$ underestimate; right Riemann sum $\Rightarrow$ overestimate.
  - If $f$ is **decreasing** on the interval: left Riemann sum $\Rightarrow$ overestimate; right Riemann sum $\Rightarrow$ underestimate.
  - Midpoint Riemann sums are generally more accurate than left/right sums.
  - Trapezoidal sum: if $f$ is **concave down**, the trapezoidal sum is an overestimate; if **concave up**, it is an underestimate.

**Example**: Approximate $\int_0^2 x^2\,dx$ using a right Riemann sum with $n = 4$ subintervals.
$$\Delta x = \frac{2-0}{4} = 0.5,\quad \text{Right sum} = 0.5[f(0.5) + f(1) + f(1.5) + f(2)] = 0.5(0.25 + 1 + 2.25 + 4) = 3.75$$
True value is $\frac{8}{3} \approx 2.667$; the right Riemann sum is an overestimate (since $f$ is increasing).

---

## 6.3 Riemann Sums, Summation Notation, and Definite Integral Notation

**Key Knowledge**:
- Definition of a Riemann sum: partition $[a, b]$ into $n$ subintervals, each of width $\Delta x_i$, pick a point $x_i^*$ in the $i$th subinterval:
  $$\sum_{i=1}^{n} f(x_i^*) \Delta x_i$$
- As the maximum subinterval width approaches $0$ (i.e., $n \to \infty$), the limit of Riemann sums is the **definite integral**:
  $$\int_a^b f(x)\,dx = \lim_{\max \Delta x_i \to 0} \sum_{i=1}^{n} f(x_i^*) \Delta x_i$$
- The $dx$ in $\int_a^b f(x)\,dx$ corresponds to $\Delta x$ in the Riemann sum, and $f(x)$ corresponds to $f(x_i^*)$.

**Example**: Express $\lim_{n \to \infty} \sum_{i=1}^{n} \frac{3}{n}\left(2 + \frac{3i}{n}\right)^2$ as a definite integral.
$$\text{Let } \Delta x = \frac{3}{n},\ x_i = 2 + \frac{3i}{n},\ \text{then } \int_2^5 x^2\,dx$$

---

## 6.4 The Fundamental Theorem of Calculus and Accumulation Functions

**Enduring Understanding FUN-5**: The Fundamental Theorem of Calculus connects differentiation and integration.

**Key Knowledge**:
- **FTC Part 1**: If $f$ is continuous on an interval containing $a$, then:
  $$\frac{d}{dx}\int_a^x f(t)\,dt = f(x)$$
  where $x$ is in the interval.
- This theorem shows that **integration and differentiation are inverse operations**—differentiating an accumulation function returns the original integrand.
- This allows us to define new functions via integrals, e.g., $g(x) = \int_0^x e^{-t^2}\,dt$ (a function with no elementary antiderivative).

**Example**: Find $\frac{d}{dx}\int_0^{x^2} \sin(t^2)\,dt$.
$$\text{Let } u = x^2,\ \frac{d}{dx}\int_0^{x^2} \sin(t^2)\,dt = \sin(u^2) \cdot \frac{du}{dx} = \sin(x^4) \cdot 2x$$

---

## 6.5 Interpreting the Behavior of Accumulation Functions Involving Area

**Key Knowledge**:
- The behavior of $g(x) = \int_a^x f(t)\,dt$ can be inferred by analyzing $f$:
  - $g$ is increasing iff $f(x) > 0$.
  - $g$ is decreasing iff $f(x) < 0$.
  - $g$ has extrema where $f(x) = 0$ (since $g'(x) = f(x) = 0$).
  - The concavity of $g$ is determined by $f'(x)$ (i.e., $g''(x)$).
- This analysis can be performed using graphical, numerical, analytical, and verbal representations.

---

## 6.6 Applying Properties of Definite Integrals

**Enduring Understanding FUN-6**: Recognizing opportunities to apply knowledge of geometry and mathematical rules can simplify integration.

**Key Knowledge** (Properties of Definite Integrals):
1. Constant multiple: $\int_a^b c f(x)\,dx = c\int_a^b f(x)\,dx$
2. Sum/difference: $\int_a^b [f(x) \pm g(x)]\,dx = \int_a^b f(x)\,dx \pm \int_a^b g(x)\,dx$
3. Reversal of limits: $\int_a^b f(x)\,dx = -\int_b^a f(x)\,dx$
4. Zero-width interval: $\int_a^a f(x)\,dx = 0$
5. Adjacent intervals: $\int_a^b f(x)\,dx + \int_b^c f(x)\,dx = \int_a^c f(x)\,dx$
6. Some definite integrals can be evaluated using geometry (areas of triangles, rectangles, semicircles, etc.).
7. The definition of the definite integral can be extended to functions with **removable or jump discontinuities**.

**Example**: Given $\int_1^3 f(x)\,dx = 5$ and $\int_3^5 f(x)\,dx = 2$, find $\int_1^5 3f(x)\,dx$.
$$\int_1^5 3f(x)\,dx = 3\int_1^5 f(x)\,dx = 3\left(\int_1^3 f(x)\,dx + \int_3^5 f(x)\,dx\right) = 3(5 + 2) = 21$$

---

## 6.7 The Fundamental Theorem of Calculus and Definite Integrals

**Key Knowledge**:
- **FTC Part 2**: If $f$ is continuous on $[a, b]$ and $F$ is an antiderivative of $f$ (i.e., $F' = f$), then:
  $$\int_a^b f(x)\,dx = F(b) - F(a)$$
- An antiderivative of $f$ is a function $g$ such that $g'(x) = f(x)$.
- If $f$ is continuous on an interval containing $a$, then $F(x) = \int_a^x f(t)\,dt$ is an antiderivative of $f$ for $x$ in the interval.

**Example**: Evaluate $\int_0^{\pi} \sin x\,dx$.
$$\int_0^{\pi} \sin x\,dx = [-\cos x]_0^{\pi} = (-\cos\pi) - (-\cos 0) = (-(-1)) - (-1) = 1 + 1 = 2$$

---

## 6.8 Finding Antiderivatives and Indefinite Integrals: Basic Rules and Notation

**Key Knowledge**:
- The indefinite integral: $\int f(x)\,dx = F(x) + C$, where $F'(x) = f(x)$ and $C$ is any constant.
- Differentiation rules provide the foundation for finding antiderivatives.
- Many functions **do not have closed-form antiderivatives** (e.g., $e^{-x^2}$, $\frac{\sin x}{x}$).

**Basic Antiderivative Formulas** (derived by reversing derivative rules):
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

---

## 6.9 Integrating Using Substitution

**Key Knowledge**:
- Substitution of variables ($u$-substitution) is a technique for finding antiderivatives, fundamentally the **reverse of the chain rule**.
- For indefinite integrals: $\int f(g(x)) \cdot g'(x)\,dx = \int f(u)\,du$, where $u = g(x)$, $du = g'(x)\,dx$.
- For definite integrals, substitution requires **corresponding changes to the limits of integration**:
  $$\int_a^b f(g(x)) \cdot g'(x)\,dx = \int_{g(a)}^{g(b)} f(u)\,du$$

**Example**: Evaluate $\int_0^1 2x e^{x^2}\,dx$.
$$\text{Let } u = x^2,\ du = 2x\,dx,\ \text{when } x=0 \Rightarrow u=0,\ x=1 \Rightarrow u=1$$
$$\int_0^1 2x e^{x^2}\,dx = \int_0^1 e^u\,du = [e^u]_0^1 = e - 1$$

---

## 6.10 Integrating Functions Using Long Division and Completing the Square

**Key Knowledge**:
- For integrals of the form $\int \frac{P(x)}{Q(x)}\,dx$ where $P$ and $Q$ are polynomials: if the degree of the numerator $\geq$ the degree of the denominator, first perform **polynomial long division** to rewrite as "polynomial $+$ proper rational function."
- For integrals with quadratic denominators, use **completing the square** to rewrite in the form $(x + a)^2 + b^2$ or $(x + a)^2 - b^2$, then apply $\arctan$ or $\ln$ formulas.

**Example**: Evaluate $\int \frac{x^2}{x+1}\,dx$.
$$\frac{x^2}{x+1} = x - 1 + \frac{1}{x+1}\ (\text{long division})$$
$$\int \frac{x^2}{x+1}\,dx = \int \left(x - 1 + \frac{1}{x+1}\right)dx = \frac{x^2}{2} - x + \ln|x+1| + C$$

**Example**: Evaluate $\int \frac{1}{x^2 + 4x + 13}\,dx$.
$$x^2 + 4x + 13 = (x^2 + 4x + 4) + 9 = (x+2)^2 + 3^2$$
$$\int \frac{1}{(x+2)^2 + 3^2}\,dx = \frac{1}{3}\arctan\left(\frac{x+2}{3}\right) + C$$

---

## 🔸 6.11 Integrating Using Integration by Parts — BC ONLY

**Key Knowledge**:
- Integration by parts is the **reverse of the product rule**, with the formula:
  $$\int u\,dv = uv - \int v\,du$$
- The key is choosing appropriate $u$ and $dv$. A common mnemonic is **LIATE** (priority order for $u$): **L**ogarithms, **I**nverse trigonometric, **A**lgebraic, **T**rigonometric, **E**xponential.
- Sometimes multiple applications are needed, or the process may cycle.

**Example**: Evaluate $\int x e^x\,dx$.
$$\text{Let } u = x,\ dv = e^x\,dx \Rightarrow du = dx,\ v = e^x$$
$$\int x e^x\,dx = x e^x - \int e^x\,dx = x e^x - e^x + C$$

---

## 🔸 6.12 Integrating Using Linear Partial Fractions — BC ONLY

**Key Knowledge**:
- Some rational functions can be decomposed into sums of ratios of **linear, nonrepeating factors**, to which basic integration techniques can be applied.
- Decomposition form: if the denominator factors as $(x - r_1)(x - r_2)\cdots$, then:
  $$\frac{P(x)}{(x-r_1)(x-r_2)} = \frac{A}{x-r_1} + \frac{B}{x-r_2}$$

**Example**: Evaluate $\int \frac{1}{x^2 - 1}\,dx$.
$$\frac{1}{x^2-1} = \frac{1}{(x-1)(x+1)} = \frac{1/2}{x-1} - \frac{1/2}{x+1}$$
$$\int \frac{1}{x^2-1}\,dx = \frac{1}{2}\ln|x-1| - \frac{1}{2}\ln|x+1| + C = \frac{1}{2}\ln\left|\frac{x-1}{x+1}\right| + C$$

---

## 🔸 6.13 Evaluating Improper Integrals — BC ONLY

**Enduring Understanding LIM-6**: The use of limits allows us to show that the areas of unbounded regions may be finite.

**Key Knowledge**:
- An improper integral is an integral with one or both limits **infinite**, or with an **unbounded integrand** on the interval of integration.
- Improper integrals can be evaluated using **limits of definite integrals**:
  - $\int_a^\infty f(x)\,dx = \lim_{t \to \infty} \int_a^t f(x)\,dx$
  - $\int_a^b f(x)\,dx$ (with $f$ unbounded at $b$) $= \lim_{t \to b^-} \int_a^t f(x)\,dx$
- If the limit exists and is finite, the integral **converges**; otherwise it **diverges**.

**Example**: Determine whether $\int_1^\infty \frac{1}{x^2}\,dx$ converges.
$$\int_1^\infty \frac{1}{x^2}\,dx = \lim_{t \to \infty} \int_1^t x^{-2}\,dx = \lim_{t \to \infty} \left[-x^{-1}\right]_1^t = \lim_{t \to \infty} \left(-\frac{1}{t} + 1\right) = 1$$
Thus the improper integral converges to $1$.

---

## 6.14 Selecting Techniques for Antidifferentiation

This topic focuses on **selecting an appropriate procedure** for antidifferentiation. Students should practice determining when and how to apply all learning objectives related to antidifferentiation. The forms to consider include:
- Direct application of basic formulas
- $u$-substitution
- Integration by parts (BC)
- Partial fractions (BC)
- Long division and completing the square
- Trigonometric identities for simplification

---

# UNIT 7: Differential Equations

> **Exam Weight**: AB 6–12% / BC 6–9%
> **Suggested Class Periods**: AB ~8–9 / BC ~9–10
> **Dominant Big Idea**: FUN (Analysis of Functions)
> **Corresponding Enduring Understanding**: FUN-7

**Unit Overview**: Students will learn to set up and solve separable differential equations. Slope fields can represent solution curves, building the understanding that there are infinitely many general solutions (differing only by a constant of integration). A unique particular solution can be found given an initial condition. By writing and solving differential equations leading to exponential growth/decay and logistic growth (BC) models, students deepen their understanding of these models.

---

## 7.1 Modeling Situations with Differential Equations

**Key Knowledge**:
- Differential equations relate a function of an independent variable to the function's derivatives. For example: "The rate of change of a quantity is proportional to the size of the quantity" translates to $\frac{dy}{dt} = ky$.
- Translating verbal statements into differential equations is a core applied skill.

**Example**: "The rate of change of the mass of salt $S$ in a container equals the difference between the inflow rate and the outflow rate" $\Rightarrow \frac{dS}{dt} = \text{inflow rate} - \text{outflow rate}$.

---

## 7.2 Verifying Solutions for Differential Equations

**Key Knowledge**:
- Derivatives can be used to verify that a function is a solution to a given differential equation.
- There may be **infinitely many general solutions** to a differential equation.

**Example**: Verify that $y = Ce^{2x}$ is a solution to $\frac{dy}{dx} = 2y$.
$$\frac{dy}{dx} = 2Ce^{2x} = 2(Ce^{2x}) = 2y \quad \checkmark$$

---

## 7.3 Sketching Slope Fields

**Key Knowledge**:
- A slope field is a **graphical representation** of a differential equation on a finite set of points in the plane.
- At each point $(x, y)$, draw a short segment with slope $\frac{dy}{dx} = f(x, y)$.
- Slope fields provide information about the behavior of solutions to first-order differential equations.

**Example**: For $\frac{dy}{dx} = x$, at every point $(1, y)$ the slope is $1$, at every point $(-2, y)$ the slope is $-2$.

---

## 7.4 Reasoning Using Slope Fields

**Key Knowledge**:
- Solutions to differential equations are functions or families of functions.
- Solution curves follow the direction of the slope field.
- Given a point (initial condition), a particular solution curve can be traced through the slope field.

---

## 🔸 7.5 Approximating Solutions Using Euler's Method — BC ONLY

**Key Knowledge**:
- Euler's method provides a procedure for approximating a solution to a differential equation (or a point on a solution curve) using **tangent line approximations**.
- Given $\frac{dy}{dx} = f(x, y)$ with initial condition $(x_0, y_0)$ and step size $h$:
  $$x_{n+1} = x_n + h$$
  $$y_{n+1} = y_n + h \cdot f(x_n, y_n)$$
- Euler's method essentially approximates the solution curve with a sequence of tangent line segments.

**Example**: Use Euler's method with step size $h = 0.5$ to approximate $y(1)$ for $\frac{dy}{dx} = x + y$, $y(0) = 1$.

| $n$ | $x_n$ | $y_n$ | $f(x_n, y_n)$ | $y_{n+1}$ |
|-----|-------|-------|---------------|-----------|
| 0 | 0 | 1 | 1 | $1 + 0.5(1) = 1.5$ |
| 1 | 0.5 | 1.5 | 2.0 | $1.5 + 0.5(2) = 2.5$ |
| 2 | 1.0 | 2.5 | — | — |

Thus $y(1) \approx 2.5$.

---

## 7.6 Finding General Solutions Using Separation of Variables

**Key Knowledge**:
- Some differential equations can be solved by **separation of variables**: move all terms involving $y$ to one side and all terms involving $x$ to the other.
  $$\frac{dy}{dx} = g(x)h(y) \Rightarrow \frac{dy}{h(y)} = g(x)\,dx$$
- Then integrate both sides to obtain the general solution (with one arbitrary constant $C$).

**Example**: Find the general solution to $\frac{dy}{dx} = 2xy$.
$$\frac{dy}{y} = 2x\,dx \Rightarrow \int \frac{dy}{y} = \int 2x\,dx \Rightarrow \ln|y| = x^2 + C \Rightarrow y = \pm e^{x^2 + C} = Ae^{x^2}$$

---

## 7.7 Finding Particular Solutions Using Initial Conditions and Separation of Variables

**Key Knowledge**:
- A general solution may describe infinitely many solutions to a differential equation. There is only **one particular solution** passing through a given point.
- The function $F$ defined by $F(x) = y_0 + \int_{x_0}^x f(t)\,dt$ is a particular solution to $\frac{dy}{dx} = f(x)$ satisfying $F(x_0) = y_0$.
- Solutions to differential equations may be subject to **domain restrictions**.

**Example**: Find the particular solution to $\frac{dy}{dx} = 2xy$ satisfying $y(0) = 3$.
$$\text{From the general solution } y = Ae^{x^2},\ \text{substitute } x = 0,\ y = 3 \Rightarrow 3 = A \cdot e^0 = A \Rightarrow y = 3e^{x^2}$$

---

## 7.8 Exponential Models with Differential Equations

**Key Knowledge**:
- The model for exponential growth and decay arising from "The rate of change of a quantity is proportional to the size of the quantity" is:
  $$\frac{dy}{dt} = ky$$
- With initial condition $y = y_0$ when $t = 0$, the solution is:
  $$y = y_0 e^{kt}$$
- When $k > 0$: **exponential growth**; when $k < 0$: **exponential decay**.
- Applications include: population growth, radioactive decay, Newton's law of cooling, continuously compounded interest, etc.

---

## 🔸 7.9 Logistic Models with Differential Equations — BC ONLY

**Key Knowledge**:
- The model for logistic growth arising from "The rate of change of a quantity is jointly proportional to the size of the quantity and the difference between the quantity and the carrying capacity" is:
  $$\frac{dy}{dt} = ky(a - y)$$
  where $a$ is the **carrying capacity** (the limiting value as $t \to \infty$).
- The logistic differential equation and initial conditions can be interpreted **without solving**:
  - When $y$ is near $0$, the growth rate is approximately exponential.
  - When $y$ is near $a$, the growth rate approaches $0$.
- The carrying capacity can be determined as the limit of the dependent variable as the independent variable approaches infinity.
- The dependent variable changes **fastest** when $y = \frac{a}{2}$ (half the carrying capacity).

---

# UNIT 8: Applications of Integration

> **Exam Weight**: AB 10–15% / BC 6–9%
> **Suggested Class Periods**: AB ~19–20 / BC ~13–14
> **Dominant Big Idea**: CHA (Change)
> **Corresponding Enduring Understandings**: CHA-4, CHA-5, CHA-6

**Unit Overview**: Students will learn to find the average value of a function, model particle motion and net change using integrals, and determine areas, volumes, and arc lengths (BC) defined by function graphs. The overarching idea is that area, volume, and length problems are all **limiting cases of Riemann sums**—this saves students from memorizing a long list of seemingly unrelated formulas.

---

## 8.1 Finding the Average Value of a Function on an Interval

**Key Knowledge**:
- The average value of a continuous function $f$ over $[a, b]$ is:
  $$\text{Average value} = \frac{1}{b-a}\int_a^b f(x)\,dx$$
- Note the distinction from the **average rate of change** $\frac{f(b)-f(a)}{b-a}$ — the average value averages the function values themselves, while the average rate of change is a slope.

**Example**: Find the average value of $f(x) = \sin x$ on $[0, \pi]$.
$$\frac{1}{\pi - 0}\int_0^{\pi} \sin x\,dx = \frac{1}{\pi}[-\cos x]_0^{\pi} = \frac{1}{\pi}(1 + 1) = \frac{2}{\pi}$$

---

## 8.2 Connecting Position, Velocity, and Acceleration of Functions Using Integrals

**Key Knowledge**:
- For a particle in **rectilinear motion** over a time interval $[a, b]$:
  - **Displacement** $= \int_a^b v(t)\,dt$ (the definite integral of velocity)
  - **Total distance traveled** $= \int_a^b |v(t)|\,dt$ (the definite integral of speed)

---

## 8.3 Using Accumulation Functions and Definite Integrals in Applied Contexts

**Key Knowledge**:
- A function defined as an integral represents an **accumulation of a rate of change**.
- The definite integral of the rate of change of a quantity over an interval gives the **net change** of that quantity over that interval.
- Applications include: water flow (in/out), population change, energy consumption, income, and many other contexts.

---

## 8.4 Finding the Area Between Curves Expressed as Functions of $x$

**Key Knowledge**:
- Areas of regions in the plane can be calculated with definite integrals.
- If $f(x) \geq g(x)$ on $[a, b]$, the area between $y = f(x)$ and $y = g(x)$ is:
  $$\text{Area} = \int_a^b [f(x) - g(x)]\,dx$$

**Example**: Find the area between $y = x$ and $y = x^2$.
$$\text{Intersection: } x = x^2 \Rightarrow x = 0, 1$$
$$\text{Area} = \int_0^1 (x - x^2)\,dx = \left[\frac{x^2}{2} - \frac{x^3}{3}\right]_0^1 = \frac{1}{2} - \frac{1}{3} = \frac{1}{6}$$

---

## 8.5 Finding the Area Between Curves Expressed as Functions of $y$

**Key Knowledge**:
- Areas of regions in the plane can also be calculated using functions of $y$.
- If $x = f(y) \geq x = g(y)$ on $[c, d]$, the area is:
  $$\text{Area} = \int_c^d [f(y) - g(y)]\,dy$$
- This approach is more convenient when the region is easier to describe in terms of $y$ (e.g., boundaries are of the form $x = \text{function of } y$).

---

## 8.6 Finding the Area Between Curves That Intersect at More Than Two Points

**Key Knowledge**:
- When a region is bounded by curves intersecting at multiple points, the area may be calculated using a **sum of two or more definite integrals**, or by evaluating the definite integral of the **absolute value of the difference** of two functions:
  $$\text{Area} = \int_a^b |f(x) - g(x)|\,dx$$
- The key is correctly identifying which function is on top in each subinterval.

---

## 8.7 Volumes with Cross Sections: Squares and Rectangles

**Key Knowledge**:
- Volumes of solids with known cross-sectional shapes can be found using definite integrals and the area formulas for those shapes.
- If the cross-sectional area perpendicular to the $x$-axis is $A(x)$, then:
  $$V = \int_a^b A(x)\,dx$$
- Square cross sections: $A(x) = [s(x)]^2$, where $s(x)$ is the side length (typically the difference between the upper and lower functions).

---

## 8.8 Volumes with Cross Sections: Triangles and Semicircles

**Key Knowledge**:
- Triangular cross sections (commonly isosceles right triangles): $A(x) = \frac{1}{2}[s(x)]^2$ (when the two legs are equal).
- Semicircular cross sections: $A(x) = \frac{\pi}{2}[r(x)]^2$, where $r(x)$ is the radius.
- Other geometrically defined cross sections can also be handled using definite integrals and appropriate area formulas.

---

## 8.9 Volume with Disc Method: Revolving Around the $x$- or $y$-Axis

**Key Knowledge**:
- **Disc Method**: Volumes of solids of revolution around the $x$- or $y$-axis can be found using definite integrals.
- Around the $x$-axis: $V = \pi \int_a^b [R(x)]^2\,dx$, where $R(x)$ is the distance from the curve to the $x$-axis.
- Around the $y$-axis: $V = \pi \int_c^d [R(y)]^2\,dy$, where $R(y)$ is the distance from the curve to the $y$-axis.

**Example**: Find the volume of the solid obtained by rotating $y = \sqrt{x}$ on $[0, 4]$ about the $x$-axis.
$$V = \pi \int_0^4 (\sqrt{x})^2\,dx = \pi \int_0^4 x\,dx = \pi \left[\frac{x^2}{2}\right]_0^4 = 8\pi$$

---

## 8.10 Volume with Disc Method: Revolving Around Other Axes

**Key Knowledge**:
- Solids of revolution can be formed around **any horizontal or vertical line** in the plane.
- The key is adjusting the **radius** for the axis offset:
  - Around horizontal line $y = c$: $R(x) = |f(x) - c|$
  - Around vertical line $x = d$: $R(y) = |g(y) - d|$

---

## 8.11 Volume with Washer Method: Revolving Around the $x$- or $y$-Axis

**Key Knowledge**:
- **Washer Method**: Used when the rotated region has a hollow interior (the cross-sections are ring-shaped).
- Around the $x$-axis: $V = \pi \int_a^b \left([R_{\text{outer}}(x)]^2 - [R_{\text{inner}}(x)]^2\right)dx$
- Around the $y$-axis: $V = \pi \int_c^d \left([R_{\text{outer}}(y)]^2 - [R_{\text{inner}}(y)]^2\right)dy$

---

## 8.12 Volume with Washer Method: Revolving Around Other Axes

**Key Knowledge**:
- The washer method can be extended to revolution around any horizontal or vertical line, with careful determination of outer and inner radii accounting for the axis position.

---

## 🔸 8.13 The Arc Length of a Smooth, Planar Curve and Distance Traveled — BC ONLY

**Enduring Understanding CHA-6**: Definite integrals allow us to solve problems involving the accumulation of change in length over an interval.

**Key Knowledge**:
- The length of a planar curve defined by a function $y = f(x)$ can be calculated using a definite integral:
  $$L = \int_a^b \sqrt{1 + [f'(x)]^2}\,dx$$
- For a curve defined parametrically by $x = x(t)$, $y = y(t)$:
  $$L = \int_a^b \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}\,dt$$
- This also equals the total distance traveled by a particle moving along the curve over the time interval $[a, b]$.

---

# UNIT 9: Parametric Equations, Polar Coordinates, and Vector-Valued Functions — BC ONLY

> **Exam Weight**: BC 11–12%
> **Suggested Class Periods**: BC ~10–11
> **Dominant Big Ideas**: CHA (Change), FUN (Analysis of Functions)

**Unit Overview**: Students will build on their understanding of straight-line motion to solve problems in which particles are moving along curves in the plane. They will define parametric equations and vector-valued functions to describe planar motion and apply calculus to motion problems. Polar equations are a special case of parametric equations. This unit should be treated as an opportunity to **reinforce past learning and transfer knowledge to new situations**, rather than as a new list of facts to memorize.

---

## 9.1 Defining and Differentiating Parametric Equations

**Key Knowledge**:
- Parametric equations represent a curve using a parameter $t$: $x = f(t)$, $y = g(t)$.
- The derivative $\frac{dy}{dx}$ is found using the chain rule:
  $$\frac{dy}{dx} = \frac{dy/dt}{dx/dt},\quad \text{provided } \frac{dx}{dt} \neq 0$$
- Intuition: the rate of change of $y$ with respect to $x$ equals the rate of change of $y$ with respect to $t$ divided by the rate of change of $x$ with respect to $t$.

---

## 9.2 Second Derivatives of Parametric Equations

**Key Knowledge**:
- The second derivative $\frac{d^2y}{dx^2}$ for parametric curves requires a two-step process:
  $$\frac{d^2y}{dx^2} = \frac{d}{dx}\left(\frac{dy}{dx}\right) = \frac{\frac{d}{dt}\left(\frac{dy}{dx}\right)}{\frac{dx}{dt}}$$
- First differentiate $\frac{dy}{dx}$ (which is a function of $t$) with respect to $t$, then divide by $\frac{dx}{dt}$.

---

## 9.3 Finding Arc Lengths of Curves Given by Parametric Equations

**Key Knowledge**:
- The arc length of a parametric curve is:
  $$L = \int_a^b \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}\,dt$$
- This is essentially dividing the curve into infinitely many small segments, each of whose length is given by the Pythagorean theorem.

---

## 9.4 Defining and Differentiating Vector-Valued Functions

**Key Knowledge**:
- Vector-valued function: $\mathbf{r}(t) = \langle f(t), g(t) \rangle$ or $\mathbf{r}(t) = f(t)\mathbf{i} + g(t)\mathbf{j}$.
- Derivative: $\mathbf{r}'(t) = \langle f'(t), g'(t) \rangle$, representing the **velocity vector**.
- The direction of the velocity vector is tangent to the curve.

---

## 9.5 Integrating Vector-Valued Functions

**Key Knowledge**:
- Integration of a vector-valued function is performed component-wise:
  $$\int_a^b \mathbf{r}(t)\,dt = \left\langle \int_a^b f(t)\,dt, \int_a^b g(t)\,dt \right\rangle$$
- The definite integral gives the **displacement vector**.

---

## 9.6 Solving Motion Problems Using Parametric and Vector-Valued Functions

**Key Knowledge**:
- Position: $\mathbf{r}(t) = \langle x(t), y(t) \rangle$
- Velocity: $\mathbf{v}(t) = \mathbf{r}'(t) = \langle x'(t), y'(t) \rangle$
- Speed: $\text{speed} = |\mathbf{v}(t)| = \sqrt{[x'(t)]^2 + [y'(t)]^2}$
- Acceleration: $\mathbf{a}(t) = \mathbf{v}'(t) = \langle x''(t), y''(t) \rangle$
- Total distance traveled: $\int_a^b |\mathbf{v}(t)|\,dt = \int_a^b \sqrt{[x'(t)]^2 + [y'(t)]^2}\,dt$

---

## 9.7 Defining Polar Coordinates and Differentiating in Polar Form

**Key Knowledge**:
- Conversion between polar $(r, \theta)$ and Cartesian coordinates: $x = r\cos\theta$, $y = r\sin\theta$.
- A polar curve $r = f(\theta)$ can be treated as a parametric curve: $x = f(\theta)\cos\theta$, $y = f(\theta)\sin\theta$, with parameter $\theta$.
- Finding $\frac{dy}{dx}$ in polar form:
  $$\frac{dy}{dx} = \frac{dy/d\theta}{dx/d\theta} = \frac{f'(\theta)\sin\theta + f(\theta)\cos\theta}{f'(\theta)\cos\theta - f(\theta)\sin\theta}$$

---

## 9.8 Find the Area of a Polar Region or the Area Bounded by a Single Polar Curve

**Key Knowledge**:
- The area bounded by a polar curve $r = f(\theta)$ from $\theta = \alpha$ to $\theta = \beta$ is:
  $$\text{Area} = \frac{1}{2}\int_\alpha^\beta [f(\theta)]^2\,d\theta$$
- Note that this formula comes from dividing the region into infinitely many **circular sectors** (not rectangles), where the area of a sector is $\frac{1}{2}r^2\Delta\theta$.

---

## 9.9 Finding the Area of the Region Bounded by Two Polar Curves

**Key Knowledge**:
- The area between two polar curves $r = f(\theta)$ (outer) and $r = g(\theta)$ (inner) is:
  $$\text{Area} = \frac{1}{2}\int_\alpha^\beta \left([f(\theta)]^2 - [g(\theta)]^2\right)d\theta$$
- The key is finding the intersection points of the two curves (to determine the limits of integration).

---

# UNIT 10: Infinite Sequences and Series — BC ONLY

> **Exam Weight**: BC 17–18% (Highest-weighted unit in BC)
> **Suggested Class Periods**: BC ~17–18
> **Dominant Big Idea**: LIM (Limits)
> **Corresponding Enduring Understandings**: LIM-7, LIM-8

**Unit Overview**: Infinite sequences and series represent one of the most abstract and profound topics in calculus. Students will learn to determine series convergence (7 tests), understand power series and their intervals of convergence, and approximate functions using Taylor and Maclaurin series. The core idea is "representing a finite value using the sum of infinitely many terms."

---

## 10.1 Defining Convergent and Divergent Infinite Series

**Key Knowledge**:
- For an infinite series $\sum_{n=1}^\infty a_n$, define the **partial sum** $S_N = \sum_{n=1}^N a_n$.
- If $\lim_{N \to \infty} S_N$ exists and is finite, the series **converges** to that value; otherwise it **diverges**.

---

## 10.2 Working with Geometric Series

**Key Knowledge**:
- A geometric series has a constant ratio between successive terms: $\sum_{n=0}^\infty ar^n = a + ar + ar^2 + \cdots$
- If $|r| < 1$, the series converges to:
  $$\sum_{n=0}^\infty ar^n = \frac{a}{1 - r}$$
- If $|r| \geq 1$, the series diverges.

**Example**: Find $\sum_{n=0}^\infty \left(\frac{1}{2}\right)^n$.
$$a = 1,\ r = \frac{1}{2},\ |r| < 1 \Rightarrow \text{sum} = \frac{1}{1 - 1/2} = 2$$

---

## 10.3 The $n$th Term Test for Divergence

**Key Knowledge**:
- If $\lim_{n \to \infty} a_n \neq 0$, then the series $\sum a_n$ **diverges**.
- ⚠️ The converse is NOT true: if $\lim_{n \to \infty} a_n = 0$, we **cannot** conclude convergence (the harmonic series is a counterexample).

---

## 10.4 Integral Test for Convergence

**Key Knowledge**:
- If $f$ is continuous, positive, and decreasing on $[1, \infty)$, and $a_n = f(n)$, then:
  - $\sum_{n=1}^\infty a_n$ converges iff $\int_1^\infty f(x)\,dx$ converges.
- This is particularly useful for establishing convergence of $p$-series.

---

## 10.5 Harmonic Series and $p$-Series

**Key Knowledge**:
- $p$-series: $\sum_{n=1}^\infty \frac{1}{n^p}$
  - Converges when $p > 1$
  - Diverges when $p \leq 1$
- The harmonic series ($p = 1$): $\sum_{n=1}^\infty \frac{1}{n}$ diverges (even though $\frac{1}{n} \to 0$).

---

## 10.6 Comparison Tests for Convergence

**Key Knowledge**:
- **Direct Comparison Test**: If $0 \leq a_n \leq b_n$ for all $n$, then:
  - $\sum b_n$ converges $\Rightarrow$ $\sum a_n$ converges
  - $\sum a_n$ diverges $\Rightarrow$ $\sum b_n$ diverges
- **Limit Comparison Test**: If $\lim_{n \to \infty} \frac{a_n}{b_n} = c > 0$ (a finite positive number), then $\sum a_n$ and $\sum b_n$ have the same convergence behavior.

**Example**: Determine convergence of $\sum_{n=1}^\infty \frac{1}{n^2 + 1}$.
$$\frac{1}{n^2 + 1} < \frac{1}{n^2},\ \sum \frac{1}{n^2}\ \text{converges ($p=2>1$)} \Rightarrow \sum \frac{1}{n^2+1}\ \text{converges}$$

---

## 10.7 Alternating Series Test for Convergence

**Key Knowledge**:
- An alternating series has the form $\sum_{n=1}^\infty (-1)^{n-1} b_n$ (where $b_n > 0$).
- The series converges if both conditions hold:
  1. $b_{n+1} \leq b_n$ (terms are decreasing)
  2. $\lim_{n \to \infty} b_n = 0$

---

## 10.8 Ratio Test for Convergence

**Key Knowledge**:
- Let $L = \lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right|$. Then:
  - If $L < 1$: the series **converges absolutely**
  - If $L > 1$: the series **diverges**
  - If $L = 1$: the test is **inconclusive** (use another method)
- The ratio test is particularly effective for series involving factorials or exponential functions.

---

## 10.9 Determining Absolute or Conditional Convergence

**Key Knowledge**:
- If $\sum |a_n|$ converges, then $\sum a_n$ **converges absolutely**.
- If $\sum a_n$ converges but $\sum |a_n|$ diverges, then $\sum a_n$ **converges conditionally**.
- Absolutely convergent series can have their terms rearranged without changing the sum; conditionally convergent series cannot.

---

## 10.10 Alternating Series Error Bound

**Key Knowledge**:
- For a convergent alternating series satisfying the alternating series test conditions, the error in approximating the sum $S$ by the $N$th partial sum $S_N$ is bounded by the absolute value of the first omitted term:
  $$|S - S_N| \leq b_{N+1}$$

---

## 10.11 Finding Taylor Polynomial Approximations of Functions

**Key Knowledge**:
- The $n$th-degree Taylor polynomial for $f$ at $x = a$ is:
  $$P_n(x) = f(a) + f'(a)(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \cdots + \frac{f^{(n)}(a)}{n!}(x-a)^n$$
- When $a = 0$, it is called a **Maclaurin polynomial**.

**Example**: The 3rd-degree Maclaurin polynomial for $f(x) = e^x$ at $x = 0$:
$$P_3(x) = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!}$$

---

## 10.12 Lagrange Error Bound

**Key Knowledge**:
- For the Taylor polynomial $P_n(x)$ approximating $f(x)$, the error satisfies:
  $$|f(x) - P_n(x)| \leq \frac{M}{(n+1)!}|x-a|^{n+1}$$
  where $M$ is the maximum value of $|f^{(n+1)}(z)|$ between $x$ and $a$.
- This formula provides an **upper bound** for the approximation error.

---

## 10.13 Radius and Interval of Convergence of Power Series

**Key Knowledge**:
- A power series is of the form $\sum_{n=0}^\infty c_n (x - a)^n$.
- There exists a **radius of convergence** $R$ ($0 \leq R \leq \infty$) such that:
  - For $|x - a| < R$: the series **converges absolutely**
  - For $|x - a| > R$: the series **diverges**
  - At $|x - a| = R$: the endpoints must be **tested individually**
- The ratio test is typically used to find $R$.

---

## 10.14 Finding Taylor or Maclaurin Series for a Function

**Key Knowledge**:
- The Taylor series for $f$ at $x = a$ is:
  $$\sum_{n=0}^\infty \frac{f^{(n)}(a)}{n!}(x - a)^n$$
- **Essential Maclaurin series to memorize**:
  - $e^x = \sum_{n=0}^\infty \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots$
  - $\sin x = \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \cdots$
  - $\cos x = \sum_{n=0}^\infty \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \cdots$
  - $\frac{1}{1-x} = \sum_{n=0}^\infty x^n = 1 + x + x^2 + x^3 + \cdots$ for $|x| < 1$
  - $\ln(1+x) = \sum_{n=1}^\infty \frac{(-1)^{n-1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \cdots$ for $-1 < x \leq 1$

---

## 10.15 Representing Functions as Power Series

**Key Knowledge**:
- Functions can be represented as power series by performing **algebraic operations** (substitution, differentiation, integration) on known series.
- These operations maintain convergence within the interior of the interval of convergence (endpoints may change).

**Example**: Find the power series for $\frac{1}{1 + x^2}$.
$$\frac{1}{1 + x^2} = \frac{1}{1 - (-x^2)} = \sum_{n=0}^\infty (-x^2)^n = \sum_{n=0}^\infty (-1)^n x^{2n}$$
Interval of convergence: $|x| < 1$.

Furthermore, integrating from $0$ to $x$ gives the series for $\arctan x$:
$$\arctan x = \int_0^x \frac{1}{1+t^2}\,dt = \sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{2n+1}$$

---

# 📊 AB vs BC Comparison — Units 6–10

| Aspect | AB (Units 6–8) | BC (Units 6–10) |
|--------|----------------|-----------------|
| **Unit 6 (Integration)** | Basic techniques: substitution, long division, completing the square | AB content + integration by parts, partial fractions, improper integrals |
| **Unit 7 (Differential Equations)** | Slope fields, separation of variables, exponential models | AB content + Euler's method, logistic models |
| **Unit 8 (Integration Applications)** | Avg value, motion, area, volume (disc/washer/cross sections) | AB content + arc length |
| **Unit 9 (Parametric/Polar/Vector)** | ❌ Not tested | ✅ Full unit |
| **Unit 10 (Infinite Series)** | ❌ Not tested | ✅ Full unit (7 convergence tests + Taylor series) |
| **Integration weight** | 17–20% (highest) | 17–20% (tied for highest) |
| **Core philosophy** | Integration as an accumulation tool for geometric and physical problems | AB foundation + advanced integration techniques + planar curves + series theory |
