# 📘 AP Calculus AB/BC Units 1–5 Self-Study Guide

---

## 🧭 Self-Study Roadmap

```
Step 1: Limit Concepts → Step 2: Continuity & Discontinuities → Step 3: Infinite Limits & Asymptotes
    ↓
Step 4: Definition of Derivative → Step 5: Basic Differentiation Rules → Step 6: Composite/Implicit Differentiation
    ↓
Step 7: Contextual Applications (Motion/Related Rates) → Step 8: L'Hospital's Rule & Linearization
    ↓
Step 9: Analyzing Functions with Derivatives (Inc/Dec/Extrema/Concavity) → Step 10: Optimization & Implicit Relations
```

---

# UNIT 1: Limits and Continuity

> **Prerequisites**: You need to be proficient in algebraic manipulations (factoring, rationalizing), basic trigonometric identities, and fundamental function concepts (domain, range, graphs).

---

## 1.1 Introducing Calculus: Can Change Occur at an Instant?

### 📌 Core Concept

Calculus seeks to answer a fundamental question: **Can change be measured at an instant?**

In everyday life, it's easy to calculate the **average rate of change**:

$$\text{Average velocity} = \frac{\text{displacement}}{\text{time}} = \frac{\Delta s}{\Delta t}$$

But when we want to know the velocity at a **single instant**—like the speedometer reading "60 km/h"—this "instant" implies $\Delta t = 0$, and division by zero is undefined.

### 📐 Core Idea

Calculus resolves this dilemma using **limits**:

1. Take increasingly smaller intervals $[a, a+h]$
2. Compute the average rate of change over each interval $\frac{f(a+h)-f(a)}{h}$
3. Observe what value this ratio approaches as $h \to 0$

### 💡 Key Insight

> **CHA-1.A.1**: Calculus uses limits to understand and model dynamic change.
>
> **CHA-1.A.2**: Because an average rate of change divides the change in one variable by the change in another, the average rate of change is undefined at a point where the change in the independent variable would be zero.
>
> **CHA-1.A.3**: The limit concept allows us to define instantaneous rate of change in terms of average rates of change.

### 🧩 Self-Study Checkpoint

When studying 1.1, you don't need to do any calculations. Just understand this core idea: **Instantaneous rate of change = the limit of average rates of change as the interval approaches zero**. This idea is the foundation of all of calculus.

---

## 1.2 Defining Limits and Using Limit Notation

### 📌 Prerequisite Knowledge

Before reading this section, make sure you understand the intuitive meaning of "approach"—what happens to $f(x)$ as $x$ gets closer and closer to $c$.

### 📐 Formal Definition

> **LIM-1.A.1**: Given a function $f$, the limit of $f(x)$ as $x$ approaches $c$ is a real number $R$ if $f(x)$ can be made arbitrarily close to $R$ by taking $x$ sufficiently close to $c$ (but not equal to $c$). If the limit exists and is a real number, the common notation is:
>
> $$\lim_{x \to c} f(x) = R$$

**Key Point**: The limit concerns the behavior of $f(x)$ as $x$ **approaches** $c$, **not** the value of $f(x)$ **at** $c$. The function need not even be defined at $c$.

### 📝 Notation Details

| Notation | How to Read | Meaning |
|----------|-------------|---------|
| $\displaystyle \lim_{x \to c} f(x) = L$ | The limit of $f(x)$ as $x$ approaches $c$ is $L$ | $x$ approaches $c$ from both sides |
| $\displaystyle \lim_{x \to c^-} f(x) = L$ | The limit of $f(x)$ as $x$ approaches $c$ from the left is $L$ | $x < c$ |
| $\displaystyle \lim_{x \to c^+} f(x) = L$ | The limit of $f(x)$ as $x$ approaches $c$ from the right is $L$ | $x > c$ |

### 🔑 Condition for Limit Existence

**Theorem**: $\displaystyle \lim_{x \to c} f(x)$ exists if and only if $\displaystyle \lim_{x \to c^-} f(x) = \lim_{x \to c^+} f(x)$ (the left-hand and right-hand limits are equal and both are finite real numbers).

### ⚠️ Exclusion Statement

> The epsilon-delta definition of a limit is **not assessed on the AP Calculus AB or BC Exam**. You only need to understand the intuitive definition above.

---

## 1.3 Estimating Limit Values from Graphs

### 📌 Why Estimate from Graphs?

Not all limits can be found algebraically. Sometimes we need to "read" limits from a graph.

### 📐 Core Knowledge

> **LIM-1.C.1**: The concept of a limit includes one-sided limits.
>
> **LIM-1.C.2**: Graphical information about a function can be used to estimate limits.

### 🔍 Step-by-Step Graphical Method

When estimating $\lim_{x \to c} f(x)$ from a graph:

1. From the left side of $x=c$, trace along the graph toward $c$ and observe what $y$-value is approached
2. From the right side of $x=c$, trace along the graph toward $c$ and observe what $y$-value is approached
3. If both sides approach the **same value**, that value is the limit

### ⚠️ Important Warning

> **LIM-1.C.3**: Because of issues of scale, graphical representations of functions may miss important function behavior.

This means: **Don't fully trust graphs**. Graphs may hide details due to resolution or scaling issues. Always verify with algebraic or numerical methods.

### ❌ Three Cases Where Limits Do Not Exist

> **LIM-1.C.4**: A limit might not exist for some functions at particular values of $x$. Classic examples include:

| Case | Example | Explanation |
|------|---------|-------------|
| **Unbounded (goes to infinity)** | $\displaystyle \lim_{x \to 0} \frac{1}{x^2}$ | Function values go to infinity, not a finite real number |
| **Left and right limits differ** | $\displaystyle \lim_{x \to 0} \frac{|x|}{x}$ | Left limit $= -1$, right limit $= 1$ |
| **Oscillation** | $\displaystyle \lim_{x \to 0} \sin\left(\frac{1}{x}\right)$ | Function oscillates wildly between $-1$ and $1$, never approaching any single value |

---

## 1.4 Estimating Limit Values from Tables

### 📌 Method

When estimating $\lim_{x \to c} f(x)$ from a table:

1. Observe the values of $f(x)$ as $x$ approaches $c$ from the left
2. Observe the values of $f(x)$ as $x$ approaches $c$ from the right
3. If both sides approach the same number, that number is the estimated limit

### 📊 Example

Estimate $\displaystyle \lim_{x \to 2} \frac{x^2-1}{x-1}$:

| $x$ | 1.9 | 1.99 | 1.999 | 2.001 | 2.01 | 2.1 |
|-----|-----|------|-------|-------|------|-----|
| $f(x)$ | 2.9 | 2.99 | 2.999 | 3.001 | 3.01 | 3.1 |

Observe that as $x$ gets closer to $2$, $f(x)$ gets closer to $3$. Therefore $\displaystyle \lim_{x \to 2} \frac{x^2-1}{x-1} = 3$.

> **LIM-1.C.5**: Numerical information can be used to estimate limits.

### 🧩 Self-Study Tip

Practice understanding every limit problem from **three perspectives**: graphical, numerical (tabular), and analytical (algebraic). This is the "multiple representations" skill emphasized on the AP Exam.

---

## 1.5 Determining Limits Using Algebraic Properties of Limits

### 📌 Why Algebraic Properties?

Graphs and tables only give **estimates**. Algebraic properties allow us to **calculate limits exactly**.

### 📐 Limit Theorems

> **LIM-1.D.1**: One-sided limits can be determined analytically or graphically.
>
> **LIM-1.D.2**: Limits of sums, differences, products, quotients, and composite functions can be found using limit theorems.

Let $\displaystyle \lim_{x \to c} f(x) = L$ and $\displaystyle \lim_{x \to c} g(x) = M$. Then:

| Property | Formula | Mnemonic |
|----------|---------|----------|
| **Sum** | $\displaystyle \lim_{x \to c} [f(x)+g(x)] = L + M$ | "Limit of sum = sum of limits" |
| **Difference** | $\displaystyle \lim_{x \to c} [f(x)-g(x)] = L - M$ | "Limit of difference = difference of limits" |
| **Product** | $\displaystyle \lim_{x \to c} [f(x)g(x)] = L \cdot M$ | "Limit of product = product of limits" |
| **Quotient** | $\displaystyle \lim_{x \to c} \frac{f(x)}{g(x)} = \frac{L}{M}$ ($M \neq 0$) | "Limit of quotient = quotient of limits" |
| **Constant Multiple** | $\displaystyle \lim_{x \to c} [k \cdot f(x)] = k \cdot L$ | |
| **Power** | $\displaystyle \lim_{x \to c} [f(x)]^n = L^n$ | |

### 🚀 Self-Study Strategy

**Direct Substitution**: For most "well-behaved" functions (polynomials, rational functions, trigonometric functions, etc.), the limit is simply the function value—**provided that substitution yields a definite real number**.

> **Example**: $\displaystyle \lim_{x \to 3} (x^2 + 2x - 1) = 3^2 + 2(3) - 1 = 9 + 6 - 1 = 14$

---

## 1.6 Determining Limits Using Algebraic Manipulation

### 📌 When Is Algebraic Manipulation Needed?

When **direct substitution** yields $\frac{0}{0}$ (called an **indeterminate form**), we must first algebraically transform the expression before substituting.

### 📐 Three Core Techniques

> **LIM-1.E.1**: It may be necessary or helpful to rearrange expressions into equivalent forms before evaluating limits.

#### Technique 1: Factoring and Canceling Common Factors

Use when: numerator and denominator are both polynomials, and substitution gives $\frac{0}{0}$

> **Example**: $\displaystyle \lim_{x \to 2} \frac{x^2 - 4}{x - 2}$
>
> Direct substitution: $\frac{4-4}{2-2} = \frac{0}{0}$ (indeterminate)
>
> Factor: $\frac{x^2-4}{x-2} = \frac{(x-2)(x+2)}{x-2} = x+2$ (for $x \neq 2$)
>
> Therefore $\displaystyle \lim_{x \to 2} \frac{x^2-4}{x-2} = \lim_{x \to 2} (x+2) = 4$

#### Technique 2: Multiplying by the Conjugate

Use when: numerator or denominator contains radicals, and substitution gives $\frac{0}{0}$

> **Example**: $\displaystyle \lim_{x \to 4} \frac{\sqrt{x} - 2}{x - 4}$
>
> Direct substitution: $\frac{2-2}{4-4} = \frac{0}{0}$
>
> Multiply by the conjugate: $\frac{\sqrt{x} - 2}{x-4} \cdot \frac{\sqrt{x} + 2}{\sqrt{x} + 2} = \frac{x-4}{(x-4)(\sqrt{x}+2)} = \frac{1}{\sqrt{x}+2}$
>
> Therefore $\displaystyle \lim_{x \to 4} \frac{\sqrt{x} - 2}{x - 4} = \lim_{x \to 4} \frac{1}{\sqrt{x}+2} = \frac{1}{4}$

#### Technique 3: Using Trigonometric Identities

Use when: the expression involves trigonometric functions and gives $\frac{0}{0}$

> **Example**: $\displaystyle \lim_{x \to 0} \frac{\sin(3x)}{x}$
>
> Note that $\displaystyle \lim_{x \to 0} \frac{\sin(kx)}{kx} = 1$, so:
>
> $\displaystyle \frac{\sin(3x)}{x} = 3 \cdot \frac{\sin(3x)}{3x} \to 3 \cdot 1 = 3$

### 🧩 Self-Study Strategy Flowchart

```
Given a limit problem:
  ↓
Direct substitution → yields a real number? → Done!
  ↓
Yields 0/0?
  ↓
Rational function? → Factor and cancel
Contains radicals? → Multiply by conjugate
Contains trig functions? → Use trig identities
  ↓
None of the above? → Consider the Squeeze Theorem (1.8)
```

---

## 1.7 Selecting Procedures for Determining Limits

### 📌 Integrated Practice

This section is about **synthesizing** all the methods learned in 1.5 and 1.6. You need to be able to **identify** which method to use based on the form of the limit expression.

### 🎯 Self-Study Task

When studying this section, you should be able to answer:

1. Can this limit be evaluated by direct substitution?
2. If not, what type of $\frac{0}{0}$ form is it?
3. Should I use factoring, the conjugate, or trig identities?
4. Can the Squeeze Theorem be applied?

---

## 1.8 Determining Limits Using the Squeeze Theorem

### 📌 When to Use

Use the Squeeze Theorem when a function is "squeezed" between two other functions whose limits are known.

### 📐 Theorem Statement

> **LIM-1.E.2**: The limit of a function may be found by using the squeeze theorem.

> **Squeeze Theorem**: If $g(x) \leq f(x) \leq h(x)$ for all $x$ in an interval containing $c$ (except possibly at $c$ itself), and
>
> $$\lim_{x \to c} g(x) = \lim_{x \to c} h(x) = L$$
>
> then $\displaystyle \lim_{x \to c} f(x) = L$.

**Intuitive understanding**: If both the top and bottom slices of a sandwich are pressed to the same position, the filling in between must be there too.

### 🔑 AP Exam Focus

The Squeeze Theorem can be used to prove two **important limits**:

$$\lim_{x \to 0} \frac{\sin x}{x} = 1 \quad \text{and} \quad \lim_{x \to 0} \frac{1 - \cos x}{x} = 0$$

These two limits are crucial for understanding derivatives of trigonometric functions.

### 📝 Proof Sketch

For $\displaystyle \lim_{x \to 0} \frac{\sin x}{x}$:

When $x$ is close to $0$ (with $x > 0$), we have $\cos x \leq \frac{\sin x}{x} \leq 1$.

Since $\displaystyle \lim_{x \to 0} \cos x = 1$ and $\displaystyle \lim_{x \to 0} 1 = 1$,

by the Squeeze Theorem, $\displaystyle \lim_{x \to 0} \frac{\sin x}{x} = 1$.

---

## 1.9 Connecting Multiple Representations of Limits

### 📌 Comprehensive Skill Practice

This section introduces no new knowledge. Instead, it requires you to freely translate between **graphical, numerical, analytical, and verbal** representations.

### 🎯 Self-Checklist

Can you do each of the following?

- ✅ Given the analytical expression $\lim_{x \to c} f(x) = L$, sketch a corresponding graph (showing $y$ approaching $L$ as $x$ approaches $c$)
- ✅ Given a graph, read off the limit value
- ✅ Given a table of data, estimate the limit value
- ✅ Describe the meaning of a limit in words

---

## 1.10 Exploring Types of Discontinuities

### 📌 From Limits to Continuity

Now we apply the concept of limits to analyzing a function's **continuity**.

### 📐 Three Types of Discontinuities

> **LIM-2.A.1**: Types of discontinuities include removable discontinuities, jump discontinuities, and discontinuities due to vertical asymptotes.

| Type | Limit Behavior | Graphical Feature | Example |
|------|----------------|-------------------|---------|
| **Removable** | $\lim_{x \to c} f(x)$ exists, but $f(c)$ either doesn't equal that limit or is undefined | A "hole" in the graph | $f(x)=\frac{x^2-1}{x-1}$ at $x=1$ |
| **Jump** | Left and right limits both exist but are not equal | The graph "jumps" at $c$ | $f(x)=\frac{|x|}{x}$ at $x=0$ |
| **Infinite** | At least one side goes to $\pm\infty$ | Vertical asymptote | $f(x)=\frac{1}{x}$ at $x=0$ |

---

## 1.11 Defining Continuity at a Point

### 📐 Three Conditions for Continuity

> **LIM-2.A.2**: A function $f$ is continuous at $x=c$ provided that:

$$
\boxed{f(c) \text{ exists} \quad \text{and} \quad \lim_{x \to c} f(x) \text{ exists} \quad \text{and} \quad \lim_{x \to c} f(x) = f(c)}
$$

**All three conditions must be satisfied!**

### 🔍 Analyzing Discontinuities by Condition

Review the three types from 1.10:

| Discontinuity Type | Condition 1: $f(c)$ exists? | Condition 2: limit exists? | Condition 3: equal? |
|-------------------|:--------------------------:|:-------------------------:|:-------------------:|
| Removable | ❌ or ✅ | ✅ | ❌ |
| Jump | ✅ | ❌ | — |
| Infinite | ❌ or ✅ | ❌ | — |

---

## 1.12 Confirming Continuity over an Interval

### 📐 Definition of Continuity on an Interval

> **LIM-2.B.1**: A function is continuous on an interval if the function is continuous at each point in the interval.

### 📝 Important Result

> **LIM-2.B.2**: Polynomial, rational, power, exponential, logarithmic, and trigonometric functions are continuous on all points in their domains.

This means:
- Polynomial functions are continuous everywhere on $(-\infty, \infty)$
- $f(x)=\frac{1}{x}$ is continuous on $(-\infty, 0)$ and $(0, \infty)$ (but not at $x=0$ since $0$ is not in its domain)
- $f(x)=\sqrt{x}$ is continuous on $[0, \infty)$

---

## 1.13 Removing Discontinuities

### 📌 When Can a Discontinuity Be Removed?

> **LIM-2.C.1**: If the limit of a function exists at a discontinuity in its graph, then it is possible to remove the discontinuity by defining or redefining the value of the function at that point so it equals the value of the limit of the function as $x$ approaches that point.

**Only removable discontinuities can be removed.**

### 📐 Continuity of Piecewise Functions

> **LIM-2.C.2**: In order for a piecewise-defined function to be continuous at a boundary to the partition of its domain, the value of the expression defining the function on one side of the boundary must equal the value of the expression defining the other side of the boundary, as well as the value of the function at the boundary.

### 💡 Self-Study Example

> **Example**: Let $f(x) = \begin{cases} \frac{x^2-1}{x-1}, & x \neq 1 \\ k, & x = 1 \end{cases}$
>
> For $f$ to be continuous at $x=1$, we need:
>
> $\displaystyle \lim_{x \to 1} \frac{x^2-1}{x-1} = \lim_{x \to 1} \frac{(x-1)(x+1)}{x-1} = \lim_{x \to 1} (x+1) = 2$
>
> Therefore $k=2$.

---

## 1.14 Connecting Infinite Limits and Vertical Asymptotes

### 📌 From Finite to Infinite

So far, all limits we've discussed have been finite. Now we extend the concept of limits to **infinity**.

> **LIM-2.D.1**: The concept of a limit can be extended to include infinite limits.
>
> **LIM-2.D.2**: Asymptotic and unbounded behavior of functions can be described and explained using limits.

### 📐 Determining Vertical Asymptotes

The line $x=c$ is a **vertical asymptote** of $f$ if and only if:

$$\lim_{x \to c^-} f(x) = \pm\infty \quad \text{or} \quad \lim_{x \to c^+} f(x) = \pm\infty$$

> **Example**: $f(x) = \frac{1}{x-2}$
>
> $\displaystyle \lim_{x \to 2^-} \frac{1}{x-2} = -\infty$, $\displaystyle \lim_{x \to 2^+} \frac{1}{x-2} = \infty$
>
> Therefore $x=2$ is a vertical asymptote.

---

## 1.15 Connecting Limits at Infinity and Horizontal Asymptotes

### 📌 Looking Toward Infinity

> **LIM-2.D.3**: The concept of a limit can be extended to include limits at infinity.
>
> **LIM-2.D.4**: Limits at infinity describe end behavior.
>
> **LIM-2.D.5**: Relative magnitudes of functions and their rates of change can be compared using limits.

### 📐 Determining Horizontal Asymptotes

The line $y=L$ is a **horizontal asymptote** of $f$ if and only if:

$$\lim_{x \to \infty} f(x) = L \quad \text{or} \quad \lim_{x \to -\infty} f(x) = L$$

### 📝 Limits of Rational Functions at Infinity

For $f(x) = \frac{a_n x^n + \cdots}{b_m x^m + \cdots}$:
- If $n < m$: $\displaystyle \lim_{x \to \pm\infty} f(x) = 0$ (horizontal asymptote $y=0$)
- If $n = m$: $\displaystyle \lim_{x \to \pm\infty} f(x) = \frac{a_n}{b_m}$ (horizontal asymptote $y = \frac{a_n}{b_m}$)
- If $n > m$: the limit is $\pm\infty$ (no horizontal asymptote)

> **Example**: $\displaystyle \lim_{x \to \infty} \frac{3x^2+2x+1}{x^2-5} = \frac{3}{1} = 3$, horizontal asymptote $y=3$

---

## 1.16 Working with the Intermediate Value Theorem (IVT)

### 📌 Entering the World of Existence Theorems

IVT is our **first existence theorem**—it tells us that something **exists**, but not exactly **where**.

> **Enduring Understanding FUN-1**: Existence theorems allow us to draw conclusions about a function's behavior on an interval without precisely locating that behavior.

### 📐 Theorem Statement

> **FUN-1.A.1**: If $f$ is a continuous function on the closed interval $[a, b]$ and $d$ is a number between $f(a)$ and $f(b)$, then the Intermediate Value Theorem guarantees that there is at least one number $c$ between $a$ and $b$, such that $f(c) = d$.

**Intuitive understanding**: If you walk from the first floor to the second floor, at some moment you must have passed through every height between the first and second floors.

### ⚠️ Steps for Applying IVT

1. **Confirm $f$ is continuous on $[a, b]$** (this is the prerequisite condition for IVT!)
2. Confirm $d$ is between $f(a)$ and $f(b)$ (i.e., $f(a) < d < f(b)$ or $f(b) < d < f(a)$)
3. **Conclusion**: There exists $c \in (a, b)$ such that $f(c) = d$

### 💡 Self-Study Example

> **Example**: Show that $f(x)=x^3-4x+1$ has a root (a value $c$ such that $f(c)=0$) on $[0, 2]$.
>
> - $f$ is a polynomial, so it is continuous on $[0, 2]$ ✅
> - $f(0) = 1 > 0$, $f(2) = 8-8+1 = 1 > 0$ ❌
>
> Wait! $f(0)$ and $f(2)$ are both positive, and $0$ is not between them. So IVT **does not apply**. We need an interval where the function values at the endpoints have opposite signs.
>
> Try $[0, 1]$: $f(0)=1>0$, $f(1)=1-4+1=-2<0$
>
> Since $f$ is continuous on $[0, 1]$, and $f(0)=1>0$, $f(1)=-2<0$, and $0$ is between $-2$ and $1$, by IVT there exists $c \in (0, 1)$ such that $f(c)=0$.

---

# UNIT 2: Differentiation: Definition and Fundamental Properties

> **Prerequisites**: Complete Unit 1 (limit concepts). You need to be proficient in calculating limits, especially $\frac{0}{0}$ indeterminate forms.

---

## 2.1 Defining Average and Instantaneous Rates of Change at a Point

### 📌 Bridge from Unit 1

In 1.1 we learned the core idea of calculus: **Instantaneous rate of change is the limit of average rates of change**. Now we formalize this idea.

### 📐 Average Rate of Change

> **CHA-2.A.1**: The difference quotients $\displaystyle \frac{f(a+h)-f(a)}{h}$ and $\displaystyle \frac{f(x)-f(a)}{x-a}$ express the average rate of change of a function over an interval.

**Geometric meaning**: The slope of the **secant line** connecting the points $(a, f(a))$ and $(a+h, f(a+h))$.

### 📐 Instantaneous Rate of Change (Definition of Derivative)

> **CHA-2.B.1**: The instantaneous rate of change of a function at $x=a$ can be expressed by:
>
> $$f'(a) = \lim_{h \to 0} \frac{f(a+h)-f(a)}{h} \quad \text{or} \quad f'(a) = \lim_{x \to a} \frac{f(x)-f(a)}{x-a}$$
>
> provided the limit exists. These are equivalent forms of the definition of the derivative.

**Geometric meaning**: The slope of the **tangent line** to the graph of $f$ at $x=a$.

### 💡 Self-Study Example

> **Example**: Use the definition to find the derivative of $f(x)=x^2$ at $x=3$.
>
> $$f'(3) = \lim_{h \to 0} \frac{(3+h)^2 - 3^2}{h} = \lim_{h \to 0} \frac{9+6h+h^2-9}{h} = \lim_{h \to 0} \frac{6h+h^2}{h} = \lim_{h \to 0} (6+h) = 6$$

---

## 2.2 Defining the Derivative of a Function and Using Derivative Notation

### 📌 From One Point to the Entire Function

Section 2.1 covered the derivative at a **single point**. Now we generalize to the derivative as a **function**.

### 📐 Definition of the Derivative Function

> **CHA-2.B.2**: The derivative of $f$ is the function whose value at $x$ is:
>
> $$f'(x) = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h}$$
>
> provided this limit exists.

### 📝 Notation for Derivatives

> **CHA-2.B.3**: For $y = f(x)$, notations for the derivative include:
>
> $$f'(x), \quad y', \quad \frac{dy}{dx}, \quad \frac{d}{dx}[f(x)]$$

### 📐 Equation of the Tangent Line

> **CHA-2.C.1**: The derivative of a function at a point is the slope of the line tangent to a graph of the function at that point.

Tangent line equation:

$$y - f(a) = f'(a)(x - a)$$

> **Example**: Find the tangent line to $f(x)=x^2$ at $x=3$.
>
> $f(3)=9$, $f'(3)=6$, so the tangent line is $y-9 = 6(x-3)$, or $y=6x-9$.

---

## 2.3 Estimating Derivatives of a Function at a Point

### 📌 When Is Estimation Needed?

When we don't have an algebraic formula for the function, only tabular data or a graph, we need to estimate the derivative.

### 📐 Estimation Methods

> **CHA-2.D.1**: The derivative at a point can be estimated from information given in tables or graphs.
>
> **CHA-2.D.2**: Technology can be used to calculate or estimate the value of a derivative of a function at a point.

**Table estimation**: Use the symmetric difference quotient

$$f'(a) \approx \frac{f(a+h) - f(a-h)}{2h}$$

**Graphical estimation**: Draw the tangent line at $x=a$ and estimate its slope ($\frac{\text{rise}}{\text{run}}$)

---

## 2.4 Connecting Differentiability and Continuity: Determining When Derivatives Do and Do Not Exist

### 📌 The Relationship Between Differentiability and Continuity

> **Enduring Understanding FUN-2**: Recognizing that a function's derivative may also be a function allows us to develop knowledge about the related behaviors of both.

### 📐 Core Theorem

> **FUN-2.A.1**: If a function is differentiable at a point, then it is continuous at that point.

The **contrapositive** of this theorem is very useful:

> 🚨 If a function is not continuous at a point, then it is **not differentiable** at that point.

### ⚠️ The Converse Is Not True

> **FUN-2.A.2**: A continuous function may fail to be differentiable at a point in its domain.

Common cases of non-differentiability despite continuity:

| Case | Example | Reason |
|------|---------|--------|
| **Corner (cusp)** | $f(x)=|x|$ at $x=0$ | Left and right derivatives are not equal |
| **Vertical tangent** | $f(x)=\sqrt[3]{x}$ at $x=0$ | Tangent line is vertical, slope is infinite |

---

## 2.5 Applying the Power Rule

### 📌 Introducing Differentiation Formulas

From here on, we will no longer use the limit definition to differentiate (that's too slow). Instead, we use **differentiation rules**.

> **Enduring Understanding FUN-3**: Recognizing opportunities to apply derivative rules can simplify differentiation.

### 📐 The Power Rule

> **FUN-3.A.1**: Direct application of the definition of the derivative and specific rules can be used to calculate the derivative for functions of the form $f(x)=x^r$.

**Power Rule**:

$$\boxed{\frac{d}{dx}[x^r] = r x^{r-1}}$$

where $r$ is any real number (integer, fraction, or negative number).

### 💡 Self-Study Examples

| Function | Derivative |
|----------|------------|
| $f(x)=x^5$ | $f'(x)=5x^4$ |
| $f(x)=x^{-3}$ | $f'(x)=-3x^{-4}$ |
| $f(x)=x^{1/2}=\sqrt{x}$ | $f'(x)=\frac{1}{2}x^{-1/2}=\frac{1}{2\sqrt{x}}$ |
| $f(x)=x$ | $f'(x)=1$ |
| $f(x)=1$ | $f'(x)=0$ |

---

## 2.6 Derivative Rules: Constant, Sum, Difference, and Constant Multiple

### 📐 Basic Rules

> **FUN-3.A.2**: Sums, differences, and constant multiples of functions can be differentiated using derivative rules.
>
> **FUN-3.A.3**: The power rule combined with sum, difference, and constant multiple properties can be used to find the derivatives for polynomial functions.

| Rule | Formula |
|------|---------|
| **Constant Rule** | $\displaystyle \frac{d}{dx}[c] = 0$ |
| **Constant Multiple Rule** | $\displaystyle \frac{d}{dx}[c \cdot f(x)] = c \cdot f'(x)$ |
| **Sum Rule** | $\displaystyle \frac{d}{dx}[f(x) + g(x)] = f'(x) + g'(x)$ |
| **Difference Rule** | $\displaystyle \frac{d}{dx}[f(x) - g(x)] = f'(x) - g'(x)$ |

### 💡 Self-Study Example

> **Example**: Find the derivative of $f(x)=3x^4 - 2x^2 + 5x - 7$.
>
> Differentiate term by term:
> - $\frac{d}{dx}[3x^4] = 3 \cdot 4x^3 = 12x^3$
> - $\frac{d}{dx}[-2x^2] = -2 \cdot 2x = -4x$
> - $\frac{d}{dx}[5x] = 5$
> - $\frac{d}{dx}[-7] = 0$
>
> Therefore $f'(x) = 12x^3 - 4x + 5$.

---

## 2.7 Derivatives of $\cos x$, $\sin x$, $e^x$, and $\ln x$

### 📐 Basic Derivative Formulas

> **FUN-3.A.4**: Specific rules can be used to find the derivatives for sine, cosine, exponential, and logarithmic functions.

$$\boxed{\frac{d}{dx}[\sin x] = \cos x \qquad \frac{d}{dx}[\cos x] = -\sin x}$$

$$\boxed{\frac{d}{dx}[e^x] = e^x \qquad \frac{d}{dx}[\ln x] = \frac{1}{x}}$$

> 💡 $e^x$ is the most "friendly" function—its derivative equals itself!

### 📌 Connecting Limits and Derivatives

> **LIM-3.A.1**: In some cases, recognizing an expression for the definition of the derivative of a function whose derivative is known offers a strategy for determining a limit.

> **Example**: $\displaystyle \lim_{h \to 0} \frac{\sin(\pi+h)-\sin(\pi)}{h}$
>
> This is precisely the definition of the derivative of $\sin x$ at $x=\pi$! So the limit $= \cos(\pi) = -1$.

---

## 2.8 The Product Rule

### 📐 The Rule

> **FUN-3.B.1**: Derivatives of products of differentiable functions can be found using the product rule.

$$\boxed{\frac{d}{dx}[f(x)g(x)] = f'(x)g(x) + f(x)g'(x)}$$

**Mnemonic**: "First times derivative of second plus second times derivative of first" or "derivative of the first times the second plus the first times derivative of the second"

### ⚠️ Common Mistake

**Wrong**: $(fg)' = f'g'$ ❌
**Correct**: $(fg)' = f'g + fg'$ ✅

### 💡 Self-Study Example

> **Example**: Find the derivative of $h(x)=x^2\sin x$.
>
> Let $f(x)=x^2$, $g(x)=\sin x$
>
> $f'(x)=2x$, $g'(x)=\cos x$
>
> $h'(x) = f'(x)g(x) + f(x)g'(x) = 2x \cdot \sin x + x^2 \cdot \cos x$

---

## 2.9 The Quotient Rule

### 📐 The Rule

> **FUN-3.B.2**: Derivatives of quotients of differentiable functions can be found using the quotient rule.

$$\boxed{\frac{d}{dx}\left[\frac{f(x)}{g(x)}\right] = \frac{f'(x)g(x) - f(x)g'(x)}{[g(x)]^2}} \quad (g(x) \neq 0)$$

**Mnemonic**: "Low d-high minus high d-low, over the square of what's below" (where "low" = denominator, "high" = numerator)

### 💡 Self-Study Example

> **Example**: Find the derivative of $h(x)=\frac{x}{x^2+1}$.
>
> Let $f(x)=x$, $g(x)=x^2+1$
>
> $f'(x)=1$, $g'(x)=2x$
>
> $h'(x) = \frac{1 \cdot (x^2+1) - x \cdot 2x}{(x^2+1)^2} = \frac{x^2+1-2x^2}{(x^2+1)^2} = \frac{1-x^2}{(x^2+1)^2}$

---

## 2.10 Finding the Derivatives of Tangent, Cotangent, Secant, and/or Cosecant Functions

### 📌 Strategy

> **FUN-3.B.3**: Rearranging tangent, cotangent, secant, and cosecant functions using identities allows differentiation using derivative rules.

Rewrite $\tan x$, $\cot x$, $\sec x$, and $\csc x$ as quotients of $\sin x$ and $\cos x$, then apply the quotient rule:

| Function | Equivalent Form | Derivative |
|----------|----------------|------------|
| $\tan x$ | $\frac{\sin x}{\cos x}$ | $\sec^2 x$ |
| $\cot x$ | $\frac{\cos x}{\sin x}$ | $-\csc^2 x$ |
| $\sec x$ | $\frac{1}{\cos x}$ | $\sec x \tan x$ |
| $\csc x$ | $\frac{1}{\sin x}$ | $-\csc x \cot x$ |

### 📝 Derivation Example: $\tan x$

$$\frac{d}{dx}[\tan x] = \frac{d}{dx}\left[\frac{\sin x}{\cos x}\right] = \frac{\cos x \cdot \cos x - \sin x \cdot (-\sin x)}{\cos^2 x} = \frac{\cos^2 x + \sin^2 x}{\cos^2 x} = \frac{1}{\cos^2 x} = \sec^2 x$$

---

# UNIT 3: Differentiation: Composite, Implicit, and Inverse Functions

> **Prerequisites**: Master all differentiation rules from Unit 2 (power, product, quotient, trig, exponential, logarithmic).

---

## 3.1 The Chain Rule

### 📌 When to Use

Use the chain rule when a function is **composite** (one function nested inside another).

### 📐 The Rule

> **FUN-3.C.1**: The chain rule provides a way to differentiate composite functions.

$$\boxed{\frac{d}{dx}[f(g(x))] = f'(g(x)) \cdot g'(x)}$$

Or in Leibniz notation:

$$\boxed{\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}}$$

**Mnemonic**: "Derivative of the outside (leaving the inside alone), times the derivative of the inside"

### 💡 Self-Study Examples

> **Example 1**: $f(x)=\sin(4x)$
>
> Outside: $\sin(u)$, $u=4x$
>
> $f'(x) = \cos(4x) \cdot 4 = 4\cos(4x)$

> **Example 2**: $f(x)=(x^2+1)^5$
>
> Outside: $u^5$, $u=x^2+1$
>
> $f'(x) = 5(x^2+1)^4 \cdot 2x = 10x(x^2+1)^4$

> **Example 3**: $f(x)=e^{3x}$
>
> Outside: $e^u$, $u=3x$
>
> $f'(x) = e^{3x} \cdot 3 = 3e^{3x}$

> **Example 4**: $f(x)=\ln(x^2+1)$
>
> Outside: $\ln u$, $u=x^2+1$
>
> $f'(x) = \frac{1}{x^2+1} \cdot 2x = \frac{2x}{x^2+1}$

### ⚠️ Common Mistake

**Wrong**: $\frac{d}{dx}[\sin(4x)] = \cos(4x)$ ❌
**Correct**: $\frac{d}{dx}[\sin(4x)] = \cos(4x) \cdot 4 = 4\cos(4x)$ ✅

> 💡 **Self-Study Tip**: Every time you use the chain rule, say to yourself: "times the derivative of what's inside."

---

## 3.2 Implicit Differentiation

### 📌 When to Use

When $y$ cannot be (or is not) explicitly written as a function of $x$ (i.e., $y$ is implicitly defined in terms of $x$).

> **FUN-3.D.1**: The chain rule is the basis for implicit differentiation.

### 📐 Method Steps

1. Differentiate **both sides** of the equation with respect to $x$
2. Treat $y$ as a function of $x$ (whenever differentiating a term with $y$, multiply by $\frac{dy}{dx}$)
3. Move all terms containing $\frac{dy}{dx}$ to one side, all other terms to the other side
4. Solve for $\frac{dy}{dx}$

### 💡 Self-Study Examples

> **Example 1**: $x^2 + y^2 = 25$
>
> Step 1: $\frac{d}{dx}[x^2] + \frac{d}{dx}[y^2] = \frac{d}{dx}[25]$
>
> Step 2: $2x + 2y \cdot \frac{dy}{dx} = 0$
>
> Step 3: $2y \cdot \frac{dy}{dx} = -2x$
>
> Step 4: $\frac{dy}{dx} = -\frac{x}{y}$

**Verification**: From $x^2+y^2=25$ we can write $y = \pm\sqrt{25-x^2}$ and differentiate directly to get the same result.

> **Example 2**: $xy + y^3 = 1$
>
> $\frac{d}{dx}[xy] + \frac{d}{dx}[y^3] = \frac{d}{dx}[1]$
>
> For $xy$, use product rule: $1 \cdot y + x \cdot \frac{dy}{dx}$
>
> For $y^3$, use chain rule: $3y^2 \cdot \frac{dy}{dx}$
>
> So: $y + x\frac{dy}{dx} + 3y^2\frac{dy}{dx} = 0$
>
> $x\frac{dy}{dx} + 3y^2\frac{dy}{dx} = -y$
>
> $\frac{dy}{dx}(x+3y^2) = -y$
>
> $\frac{dy}{dx} = -\frac{y}{x+3y^2}$

---

## 3.3 Differentiating Inverse Functions

### 📐 Formula

> **FUN-3.E.1**: The chain rule and definition of an inverse function can be used to find the derivative of an inverse function, provided the derivative exists.

If $f$ is differentiable, $f^{-1}$ is its inverse, and $f'(f^{-1}(x)) \neq 0$, then:

$$\boxed{\frac{d}{dx}[f^{-1}(x)] = \frac{1}{f'(f^{-1}(x))}}$$

### 💡 Self-Study Example

> **Example**: Given $f(2)=5$ and $f'(2)=3$, find $(f^{-1})'(5)$.
>
> $(f^{-1})'(5) = \frac{1}{f'(f^{-1}(5))} = \frac{1}{f'(2)} = \frac{1}{3}$

**Geometric Meaning**: The graphs of a function and its inverse are symmetric about the line $y=x$. Therefore, the slopes of their tangent lines at corresponding points are reciprocals.

---

## 3.4 Differentiating Inverse Trigonometric Functions

### 📐 Formulas

> **FUN-3.E.2**: The chain rule applied with the definition of an inverse function, or the formula for the derivative of an inverse function, can be used to find the derivatives of inverse trigonometric functions.

$$\frac{d}{dx}[\sin^{-1} x] = \frac{1}{\sqrt{1-x^2}} \quad (-1 < x < 1)$$

$$\frac{d}{dx}[\cos^{-1} x] = -\frac{1}{\sqrt{1-x^2}} \quad (-1 < x < 1)$$

$$\frac{d}{dx}[\tan^{-1} x] = \frac{1}{1+x^2}$$

$$\frac{d}{dx}[\sec^{-1} x] = \frac{1}{|x|\sqrt{x^2-1}} \quad (|x| > 1)$$

> 💡 **Memory Tip**:
> - $\sin^{-1}$ has a positive derivative, $\cos^{-1}$ has its negative
> - $\tan^{-1}$ is the simplest: $\frac{1}{1+x^2}$

### 💡 Self-Study Example

> **Example**: $f(x) = \tan^{-1}(x^2)$
>
> $f'(x) = \frac{1}{1+(x^2)^2} \cdot 2x = \frac{2x}{1+x^4}$

---

## 3.5 Selecting Procedures for Calculating Derivatives

### 📌 Integrated Practice

This section trains you to **identify** which differentiation rule(s) to apply for a given function.

### 🎯 Decision Framework

When facing a differentiation problem:

1. Look at the overall structure: is it a **composite function**? $\Rightarrow$ Chain rule
2. Is it a **product** of two functions? $\Rightarrow$ Product rule
3. Is it a **quotient** of two functions? $\Rightarrow$ Quotient rule
4. Is it an **implicit function**? $\Rightarrow$ Implicit differentiation
5. Is it an **inverse function**? $\Rightarrow$ Inverse function formula

> ⚠️ When **multiple rules** apply simultaneously, pay attention to the **order of operations**: handle the outermost structure first, then work inward.

### 💡 Example

> **Example**: $f(x)=\sin^2(x^3+1) = [\sin(x^3+1)]^2$
>
> Outermost: $u^2$ (power rule), middle: $\sin(v)$ (trig), innermost: $v=x^3+1$ (polynomial)
>
> $f'(x) = 2\sin(x^3+1) \cdot \cos(x^3+1) \cdot 3x^2 = 6x^2\sin(x^3+1)\cos(x^3+1)$

---

## 3.6 Calculating Higher-Order Derivatives

### 📐 Definition

> **FUN-3.F.1**: Differentiating $f'$ produces the second derivative $f''$, provided the derivative of $f'$ exists; repeating this process produces higher-order derivatives of $f$.

### 📝 Notation

> **FUN-3.F.2**: For $y = f(x)$, notations for the second derivative include:

$$f''(x), \quad y'', \quad \frac{d^2y}{dx^2}$$

Higher-order derivatives:

$$f^{(n)}(x), \quad \frac{d^n y}{dx^n}$$

### 💡 Self-Study Example

> **Example**: $f(x) = x^4 - 3x^2 + 2$
>
> $f'(x) = 4x^3 - 6x$
>
> $f''(x) = 12x^2 - 6$
>
> $f'''(x) = 24x$
>
> $f^{(4)}(x) = 24$
>
> $f^{(5)}(x) = 0$

---

# UNIT 4: Contextual Applications of Differentiation

> **Prerequisites**: Master all differentiation techniques from Units 2–3. You should be able to differentiate any function **automatically**.

---

## 4.1 Interpreting the Meaning of the Derivative in Context

### 📌 Entering the "Real World"

> **Enduring Understanding CHA-3**: Derivatives allow us to solve real-world problems involving rates of change.

### 📐 Three Elements for Interpreting a Derivative

> **CHA-3.A.1**: The derivative of a function can be interpreted as the instantaneous rate of change with respect to its independent variable.
>
> **CHA-3.A.2**: The derivative can be used to express information about rates of change in applied contexts.
>
> **CHA-3.A.3**: The unit for $f'(x)$ is the unit for $f$ divided by the unit for $x$.

### 💡 Self-Study Example

> **Example**: Let $P(t)$ represent the population of a city (in people) at time $t$ (in years).
>
> $P'(5) = 1200$ means:
> - At time $t=5$ years, the population is increasing at a rate of 1200 people per year
> - Unit: $\frac{\text{people}}{\text{year}}$

**Key**: It's not enough to say "the derivative equals something." You must state **at what moment**, **what quantity** is changing, and **at what rate**.

---

## 4.2 Straight-Line Motion: Connecting Position, Velocity, and Acceleration

### 📐 Physical Quantities

> **CHA-3.B.1**: The derivative can be used to solve rectilinear motion problems involving position, speed, velocity, and acceleration.

| Physical Quantity | Symbol | Relationship to Position |
|------------------|--------|------------------------|
| **Position** | $s(t)$ | — |
| **Velocity** | $v(t)$ | $v(t) = s'(t)$ |
| **Acceleration** | $a(t)$ | $a(t) = v'(t) = s''(t)$ |
| **Speed** | $\text{speed}$ | $\text{speed} = \|v(t)\|$ |

### 💡 Important Conceptual Distinctions

| Situation | Meaning |
|-----------|---------|
| $v(t) > 0$ | Particle moves **right/forward** |
| $v(t) < 0$ | Particle moves **left/backward** |
| $a(t) > 0$ | Velocity is **increasing** |
| $a(t) < 0$ | Velocity is **decreasing** |

> ⚠️ $v(t) > 0$ and $a(t) > 0$: particle is **speeding up** (moving forward)
> ⚠️ $v(t) > 0$ and $a(t) < 0$: particle is **slowing down** (moving forward)
> ⚠️ $v(t) < 0$ and $a(t) < 0$: particle is **speeding up** (moving backward)

### 💡 Self-Study Example

> **Example**: A particle's position function is $s(t)=t^3-6t^2+9t$ ($t \geq 0$).
>
> $v(t)=s'(t)=3t^2-12t+9=3(t-1)(t-3)$
>
> For $0 \leq t < 1$: $v(t)>0$, particle moves right
> For $1 < t < 3$: $v(t)<0$, particle moves left
> For $t > 3$: $v(t)>0$, particle moves right

---

## 4.3 Rates of Change in Applied Contexts Other Than Motion

### 📌 General Mindset

> **CHA-3.C.1**: The derivative can be used to solve problems involving rates of change in applied contexts.

The concept of "rate" in calculus is **not limited** to physical motion. It applies to any type of change:

- Population growth rate (people/year)
- Inflation rate (dollars/year)
- Chemical reaction rate (moles/second)
- Water flow rate (cubic meters/minute)

**The key is identifying "what is changing" and "with respect to what."**

---

## 4.4 Introduction to Related Rates

### 📌 Core Idea

> **CHA-3.D.1**: The chain rule is the basis for differentiating variables in a related rates problem with respect to the same independent variable.
>
> **CHA-3.D.2**: Other differentiation rules, such as the product rule and the quotient rule, may also be necessary to differentiate all variables with respect to the same independent variable.

**Basic idea**: Several related quantities are all changing with respect to time. Given the rate of change of one quantity, find the rate of change of another.

---

## 4.5 Solving Related Rates Problems

### 📐 Standard Problem-Solving Procedure

> **CHA-3.E.1**: The derivative can be used to solve related rates problems; that is, finding a rate at which one quantity is changing by relating it to other quantities whose rates of change are known.

**Five-Step Method**:

1. **Draw a diagram** and label all variables (both known and unknown)
2. Write an **equation** relating the variables
3. Implicitly differentiate with respect to **time $t$** (using the chain rule)
4. Substitute known values and rates
5. Solve for the required rate, and **interpret in context** (include units)

### 💡 Self-Study Example

> **Example**: A spherical balloon is being inflated so that its radius $r$ increases at a rate of $\frac{dr}{dt}=2$ cm/s. How fast is the volume increasing when $r=5$ cm?
>
> Step 1 & 2: $V = \frac{4}{3}\pi r^3$
>
> Step 3: $\frac{dV}{dt} = 4\pi r^2 \frac{dr}{dt}$
>
> Step 4: Substitute $r=5$, $\frac{dr}{dt}=2$
>
> $\frac{dV}{dt} = 4\pi(5)^2(2) = 200\pi$
>
> Step 5: When $r=5$ cm, the volume is increasing at a rate of $200\pi$ cm³/s.

---

## 4.6 Approximating Values of a Function Using Local Linearity and Linearization

### 📐 Basic Idea

> **CHA-3.F.1**: The tangent line is the graph of a locally linear approximation of the function near the point of tangency.

**Linearization** formula:

$$L(x) = f(a) + f'(a)(x - a)$$

### 📐 Error Analysis

> **CHA-3.F.2**: For a tangent line approximation, the function's behavior near the point of tangency may determine whether a tangent line value is an underestimate or an overestimate of the corresponding function value.

- If the function is **concave up** near $a$ ($f''(x) > 0$), the tangent line value is an **underestimate**
- If the function is **concave down** near $a$ ($f''(x) < 0$), the tangent line value is an **overestimate**

### 💡 Self-Study Example

> **Example**: Use linearization to approximate $\sqrt{4.1}$.
>
> Let $f(x)=\sqrt{x}$, linearize at $a=4$.
>
> $f(4)=2$, $f'(x)=\frac{1}{2\sqrt{x}}$, $f'(4)=\frac{1}{4}$
>
> $L(x) = 2 + \frac{1}{4}(x-4)$
>
> $\sqrt{4.1} \approx L(4.1) = 2 + \frac{1}{4}(0.1) = 2.025$
>
> Since $f''(x)=-\frac{1}{4}x^{-3/2} < 0$ (concave down), $2.025$ is an **overestimate**.

---

## 4.7 Using L'Hospital's Rule for Determining Limits of Indeterminate Forms

### 📌 Review

In Unit 1, when we encountered $\frac{0}{0}$ forms, we used algebraic methods like factoring and conjugates. Now, with derivatives at our disposal, we have a more powerful tool.

### 📐 L'Hospital's Rule

> **LIM-4.A.1**: When the ratio of two functions tends to $\frac{0}{0}$ or $\frac{\infty}{\infty}$ in the limit, such forms are said to be indeterminate.
>
> **LIM-4.A.2**: Limits of the indeterminate forms $\frac{0}{0}$ or $\frac{\infty}{\infty}$ may be evaluated using L'Hospital's Rule.

If $\displaystyle \lim_{x \to a} f(x) = 0$ and $\displaystyle \lim_{x \to a} g(x) = 0$ (or both tend to $\pm\infty$), and $\displaystyle \lim_{x \to a} \frac{f'(x)}{g'(x)}$ exists, then:

$$\boxed{\lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}}$$

### ⚠️ Important Notes

1. **Must first verify** it's an indeterminate form $\frac{0}{0}$ or $\frac{\infty}{\infty}$ before applying
2. Differentiate the numerator and denominator **separately**—not the quotient as a whole
3. If after one application it's still indeterminate, you may **apply repeatedly**

### 💡 Self-Study Examples

> **Example 1**: $\displaystyle \lim_{x \to 0} \frac{\sin x}{x}$
>
> Verify: $\frac{\sin 0}{0} = \frac{0}{0}$ ✅
>
> $\displaystyle \lim_{x \to 0} \frac{\sin x}{x} \overset{\text{L'H}}{=} \lim_{x \to 0} \frac{\cos x}{1} = 1$

> **Example 2**: $\displaystyle \lim_{x \to \infty} \frac{x^2}{e^x}$
>
> Verify: $\frac{\infty}{\infty}$ ✅
>
> $\displaystyle \lim_{x \to \infty} \frac{x^2}{e^x} \overset{\text{L'H}}{=} \lim_{x \to \infty} \frac{2x}{e^x} \overset{\text{L'H}}{=} \lim_{x \to \infty} \frac{2}{e^x} = 0$

> ✅ **Conclusion**: The exponential function $e^x$ grows faster than any polynomial in the long run.

### ⚠️ Exclusion Statement

> Other indeterminate forms (such as $0 \cdot \infty$, $\infty - \infty$, $1^\infty$, $0^0$, $\infty^0$) are **not assessed on the AP Calculus AB or BC Exam**.

---

# UNIT 5: Analytical Applications of Differentiation

> **Prerequisites**: Master differentiation techniques. Understand the physical contexts from Unit 4. Now we "strip away the contextual details" and focus on abstract mathematical structures.

---

## 5.1 Using the Mean Value Theorem (MVT)

### 📌 The Second Existence Theorem

In 1.16 we learned IVT. Now we learn the **Mean Value Theorem (MVT)**.

### 📐 Theorem Statement

> **FUN-1.B.1**: If a function $f$ is continuous over the interval $[a, b]$ and differentiable over the interval $(a, b)$, then the Mean Value Theorem guarantees a point within that open interval where the instantaneous rate of change equals the average rate of change over the interval.

$$\boxed{f'(c) = \frac{f(b) - f(a)}{b - a}}$$

**Geometric Meaning**: At some point within the interval, the **slope of the tangent line** equals the **slope of the secant line** connecting the endpoints.

**Intuitive Understanding**: If you drive from city A to city B with an average speed of 80 km/h, then at **some moment** during your trip, your instantaneous speed was **exactly** 80 km/h.

### ⚠️ Steps for Applying MVT

1. **Confirm $f$ is continuous on $[a, b]$** ✅
2. **Confirm $f$ is differentiable on $(a, b)$** ✅
3. Compute $\frac{f(b)-f(a)}{b-a}$
4. **Conclusion**: There exists $c \in (a, b)$ such that $f'(c)$ equals that value

---

## 5.2 Extreme Value Theorem (EVT), Global Versus Local Extrema, and Critical Points

### 📐 Extreme Value Theorem (EVT)

> **FUN-1.C.1**: If a function $f$ is continuous over the interval $[a, b]$, then the Extreme Value Theorem guarantees that $f$ has at least one minimum value and at least one maximum value on $[a, b]$.

**⚠️ Two conditions are both necessary**: closed interval + continuity.

### 📐 Critical Points

> **FUN-1.C.2**: A point on a function where the first derivative equals zero or fails to exist is a critical point of the function.

$$x=c \text{ is a critical point} \iff f'(c)=0 \text{ or } f'(c) \text{ does not exist}$$

> **FUN-1.C.3**: All local (relative) extrema occur at critical points of a function, though not all critical points are local extrema.

**Counterexample**: $f(x)=x^3$ at $x=0$: $f'(0)=0$, but $x=0$ is neither a local maximum nor a local minimum.

---

## 5.3 Determining Intervals on Which a Function Is Increasing or Decreasing

### 📐 Basic Principle

> **FUN-4.A.1**: The first derivative of a function can provide information about the function and its graph, including intervals where the function is increasing or decreasing.

| Condition | Behavior of $f$ |
|-----------|----------------|
| $f'(x) > 0$ on interval $I$ | $f$ is **increasing** on $I$ |
| $f'(x) < 0$ on interval $I$ | $f$ is **decreasing** on $I$ |

### 📝 Self-Study Steps

1. Find $f'(x)$
2. Find critical points (where $f'(x)=0$ or does not exist)
3. Use critical points to divide the domain into intervals
4. Choose a **test point** in each interval and plug into $f'(x)$ to determine its sign

---

## 5.4 Using the First Derivative Test to Determine Relative (Local) Extrema

### 📐 First Derivative Test

> **FUN-4.A.2**: The first derivative of a function can determine the location of relative (local) extrema of the function.

Assume $c$ is a critical point and $f$ is continuous at $c$:

| Behavior of $f'$ at $c$ | Conclusion |
|------------------------|------------|
| Changes from positive to negative | $f$ has a **local maximum** at $c$ |
| Changes from negative to positive | $f$ has a **local minimum** at $c$ |
| Does not change sign | No extremum at $c$ |

---

## 5.5 Using the Candidates Test to Determine Absolute (Global) Extrema

### 📐 Candidates Test

> **FUN-4.A.3**: Absolute (global) extrema of a function on a closed interval can only occur at critical points or at endpoints.

**Method**:
1. Find all critical points within the interval
2. Evaluate $f$ at all critical points and endpoints
3. Compare—the largest value is the absolute maximum, the smallest is the absolute minimum

---

## 5.6 Determining Concavity of Functions over Their Domains

### 📐 Definition of Concavity

> **FUN-4.A.4**: The graph of a function is concave up (down) on an open interval if the function's derivative is increasing (decreasing) on that interval.

> **FUN-4.A.5**: The second derivative of a function provides information about the function and its graph, including intervals of upward or downward concavity.

| Condition | Concavity of $f$ |
|-----------|----------------|
| $f''(x) > 0$ on an interval | $f$ is **concave up** ($\cup$) on that interval |
| $f''(x) < 0$ on an interval | $f$ is **concave down** ($\cap$) on that interval |

> **FUN-4.A.6**: The second derivative of a function may be used to locate points of inflection for the graph of the original function (points where concavity changes).

---

## 5.7 Using the Second Derivative Test to Determine Extrema

### 📐 Second Derivative Test

> **FUN-4.A.7**: The second derivative of a function may determine whether a critical point is the location of a relative (local) maximum or minimum.

If $c$ is a critical point ($f'(c)=0$):

| Condition | Conclusion |
|-----------|------------|
| $f''(c) < 0$ | $f$ has a **local maximum** at $c$ |
| $f''(c) > 0$ | $f$ has a **local minimum** at $c$ |
| $f''(c) = 0$ | The test is **inconclusive**—use the First Derivative Test |

> **FUN-4.A.8**: When a continuous function has only one critical point on an interval on its domain and the critical point corresponds to a relative (local) extremum of the function on the interval, then that critical point also corresponds to the absolute (global) extremum of the function on the interval.

---

## 5.8 Sketching Graphs of Functions and Their Derivatives

### 📐 Key Features

> **FUN-4.A.9**: Key features of functions and their derivatives can be identified and related to their graphical, numerical, and analytical representations.
>
> **FUN-4.A.10**: Graphical, numerical, and analytical information from $f'$ and $f''$ can be used to predict and explain the behavior of $f$.

### 📝 Complete Analysis Framework

Given the equation of $f$, to sketch the graph of $f$:

1. **Find critical points**: solve $f'(x)=0$
2. **Determine increasing/decreasing**: using sign of $f'$
3. **Find local extrema**: First or Second Derivative Test
4. **Determine concavity**: using sign of $f''$
5. **Find inflection points**: $f''(x)=0$ and $f''$ changes sign
6. **Find asymptotes**: using limits at infinity and infinite limits
7. **Find intercepts**: $f(0)$ and solve $f(x)=0$

---

## 5.9 Connecting a Function, Its First Derivative, and Its Second Derivative

### 📐 Comprehensive Relationships

> **FUN-4.A.11**: Key features of the graphs of $f$, $f'$, and $f''$ are related to one another.

### 📊 Complete Correspondence Table

| Feature of $f$ | From $f'$ | From $f''$ |
|----------------|-----------|------------|
| Increasing | $f'(x) > 0$ | — |
| Decreasing | $f'(x) < 0$ | — |
| Local maximum | $f'$ changes from $+$ to $-$ | $f'' < 0$ |
| Local minimum | $f'$ changes from $-$ to $+$ | $f'' > 0$ |
| Concave up | — | $f''(x) > 0$ |
| Concave down | — | $f''(x) < 0$ |
| Inflection point | — | $f''$ changes sign |

### 💡 Self-Study Focus

When given a graph of $f'$ or $f''$, you can **deduce** the behavior of $f$:
- $f'$ is zero at $x=c$ $\implies$ $f$ has a **horizontal tangent** at $c$ (possibly an extremum)
- $f'$ is increasing $\implies$ $f'' > 0$ $\implies$ $f$ is concave up
- $f'$ is decreasing $\implies$ $f'' < 0$ $\implies$ $f$ is concave down

---

## 5.10 Introduction to Optimization Problems

### 📐 Core Idea

> **FUN-4.B.1**: The derivative can be used to solve optimization problems; that is, finding a minimum or maximum value of a function on a given interval.

The essence of an optimization problem: Under certain **constraints**, maximize or minimize some **target quantity**.

### Typical Structure

All optimization problems share the same underlying structure:
1. A quantity to maximize or minimize (the objective function)
2. One or more constraints (relating the variables)
3. Use the constraints to reduce the objective function to a single-variable function

---

## 5.11 Solving Optimization Problems

### 📐 Standard Procedure

> **FUN-4.C.1**: Minimum and maximum values of a function take on specific meanings in applied contexts.

**Six-Step Method**:

1. **Identify the objective**: What is to be maximized or minimized?
2. **Write an expression**: Express the objective in terms of variables
3. **Find constraints**: Identify relationships between variables
4. **Reduce to one variable**: Use constraints to eliminate extra variables
5. **Differentiate and find critical points**: Solve $f'(x)=0$
6. **Confirm and interpret**: Use the First/Second Derivative Test to verify, then explain the answer in context

### 💡 Self-Study Example

> **Example**: A farmer has 100 meters of fencing to enclose a rectangular area. Find the maximum possible area.
>
> Step 1: Maximize area $A$
> Step 2: $A = lw$ ($l$ = length, $w$ = width)
> Step 3: $2l+2w=100 \Rightarrow l+w=50$
> Step 4: $A(l) = l(50-l) = 50l - l^2$
> Step 5: $A'(l)=50-2l=0 \Rightarrow l=25$, $w=25$
> Step 6: $A''(25) = -2 < 0$, so it's a maximum. Maximum area $= 25 \times 25 = 625$ square meters.

---

## 5.12 Exploring Behaviors of Implicit Relations

### 📐 Applying Derivative Analysis to Implicit Functions

> **FUN-4.D.1**: A point on an implicit relation where the first derivative equals zero or does not exist is a critical point of the function.

> **FUN-4.E.1**: Applications of derivatives can be extended to implicitly defined functions.
>
> **FUN-4.E.2**: Second derivatives involving implicit differentiation may be relations of $x$, $y$, and $\frac{dy}{dx}$.

### 💡 Self-Study Example

> **Example**: $x^2 + xy + y^2 = 7$
>
> Find $\frac{dy}{dx}$:
>
> $2x + y + x\frac{dy}{dx} + 2y\frac{dy}{dx} = 0$
>
> $\frac{dy}{dx}(x+2y) = -2x-y$
>
> $\frac{dy}{dx} = -\frac{2x+y}{x+2y}$
>
> To find critical points, set $\frac{dy}{dx}=0$, i.e., $2x+y=0 \Rightarrow y=-2x$
>
> Substitute into the original equation: $x^2 + x(-2x) + (-2x)^2 = 7 \Rightarrow x^2-2x^2+4x^2=7 \Rightarrow 3x^2=7 \Rightarrow x=\pm\sqrt{\frac{7}{3}}$
>
> Find the corresponding $y$ values to obtain the critical points.

---

# 📋 Units 1–5 Self-Study Checklist

After completing the above, you should be able to:

- ✅ **Unit 1**: Find limits using graphs, tables, and algebraic methods; determine continuity; apply IVT
- ✅ **Unit 2**: Understand derivatives via the limit definition; fluently apply all basic differentiation rules
- ✅ **Unit 3**: Apply the chain rule; perform implicit differentiation; find derivatives of inverse and inverse trig functions
- ✅ **Unit 4**: Interpret derivatives in context; solve motion and related rates problems; use linearization and L'Hospital's Rule
- ✅ **Unit 5**: Apply MVT and EVT; analyze increasing/decreasing behavior, extrema, concavity, and inflection points; solve optimization problems
