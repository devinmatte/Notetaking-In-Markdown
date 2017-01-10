# Section 3 Calculus Notes

An interior point of the domain of a function $f$ where $f'$ is zero or undefined is a critical point of $f$

Places where $f$ can possibly have an extreme value (local or global)
1. Critical Points
2. End points of the domain of $f$

Example
----
Find absolute max/min of $f(x)=10x(2-ln(x))$ on $[1, e^2]$

#### Step 1: Find Critical Points
$$
f'(x) = \frac{d}{dx}(10x)(2-ln(x)) + 10x \frac{d}{dx}(2-ln(x))
$$
$$
f'(x) = 10(2-ln(x)) + 10x(\frac{-1}{x}) = 0
$$
$$
10-10(ln(x)) = 0 \to ln(x) = 1 \to x = e
$$

#### Step 2: Evaluate Function

##### Critical Points:
$$
f(e) = 10e(2-ln(e)) = 10e
$$

##### End Points:
$$
f(1) = 10(1)(2-ln(1)) = 20
$$
$$
f(e^2) = 10(e^2)(2-ln(e^2)) = 0
$$

##### Absolute Max at $x=e$
##### Absolute Min at $x=e^2$

----

Example
----
Find absolute max/min of $f(x) = x^{\frac{2}{3}}$ on $[-2, 3]$

#### Step 1: Find Critical Points
$$
f'(x) = \frac{2}{3}x^{\frac{-1}{3}} \neq 0
$$
$$
f'(x) = \frac{2}{3x^{\frac{1}{3}}}
$$
Undefined at $x=0$

#### Step 2: Evaluate Function

##### Critical Points:
$$
f(0) = 0
$$

##### End Points:
$$
f(-2) = -2^{2^\frac{1}{3}} = \sqrt[3]{4}
$$
$$
f(3) = 3^{2^\frac{1}{3}} = \sqrt[3]{9}
$$

##### Absolute Max at $x=3$
##### Absolute Min at $x=0$

----

How to find the absolute extrema of a continuous function on a closed interval.

1. Evaluate $f$ at all critical points and endpoints
2. Take the largest and smallest these values

### First Derivative Test for Local Extrema

Help us determine if critical point is a local max/min.

Suppose $c$ is a critical point

1. If $f'$ change from negative to positive at $c$, then $f$ has a local min at $x = c$.
2. If $f'$ changes rom positive to negative at $c$, then $f$ has a local max at $x = c$.
3. If $f'$ does not change sign at $c$, then no local extremum at $c$


Example
----
$$
f(x) = x^{\frac{1}{3}}(x-4)
$$
$$
f'(x) = \frac{1}{3}x^{\frac{-2}{3}}(x-4) + x^{\frac{1}{3}}(1)
$$
$$
f'(x) = \frac{x-4}{3x^{\frac{2}{3}}}
$$
$$
f'(x) = \frac{1}{3}x^{\frac{1}{3}} -\frac{4}{3x^{\frac{2}{3}}} + x^{\frac{1}{3}} \to f'(x) \frac{4}{3}x^{\frac{1}{3}} - \frac{4}{3x^{\frac{2}{3}}}
$$

##### Critical Point $x=0$

$$
x^{\frac{1}{3}}-\frac{1}{x^{\frac{2}{3}}} = 0
$$
$$
\frac{x^{\frac{1}{3}}}{1} = \frac{1}{x^{\frac{2}{3}}}
$$
$$
x^{\frac{1}{3}} * x^{\frac{2}{3}} = x = 1
$$

##### Critical Point $x=1$

----

##### Second Derivative tells you how a function bends/turns

The turning or bending behavior defines concavity of the curve.

| Decreasing      | Increasing      |
|:----------------|:----------------|
| $f'$ decreasing | $f'$ increasing |
| $f'' < 0$       | $f'' > 0$       |
| Concave down    | Concave up      |

The graph of a differentiable function $y=f(x)$ is

1. Concave up on an open interval $I \Leftrightarrow f'' > 0$ on $I$
2. Concave down on an open interval $I$ if $f'$ is decreasing on $I \Leftrightarrow f'' < 0$ on $I$
3. Contains an inflection point if the concavity is changing

Example
----
Characterize the bending of $f(x)=x^4$
$$
f'(x) = 4x^3
$$
$$
f''(x) = 12x^2 > 0 \to x \neq 0
$$
$$
(-\infty,0) \cup (0, \infty)
$$
At inflection points either $f''(c)=0$ or $f''(c)$ does not exist

----

Example
----

Sketch a graph of a function with the following conditions:

1. Vertical Asymptote at $x=0$
2. $f'(x) > 0$ if $x<-2$
3. $f'(x) < 0$ if $x>-2$ $x \neq 0$
4. $f''(x) < 0$ if $x<0$
5. $f''(x) > 0$ if $x>0$

----

### Second Derivative Test
Suppose $f''$ is continuous near $c$

1. If $f'(c)=0$ and $f''(c) > 0$, then $f$ has a local minimum at $x=c$
2. If $f'(c)=0$ and $f''(c) < 0$, then $f$ has a local maximum at $x=c$

Suppose $y=f(x)$ is continuous on a closed interval $[a,b]$ and differentiable on $(a,b)$.
Then there is at least one point in $(a,b)$ at which $\frac{f(b)-f(a)}{b-a} = f(c)$

Example
----
A Trucker handed in a ticket at a toll booth showing that in 2 hours she had covered 159 miles on a toll road with a speed limit of $65mph$. The trucker was cited for speeding. Why?
$$
\frac{159}{2} = 80mph
$$

----

#### Show:
If $f'(x) = g'(x)$ for all $x$ in an interval $(a,b)$, then $(f-g)(x)$ is constant on $(a,b)$

$(f-g)(x) = f(x)-g(x) = k$, where $k$ is constant let $F(x) = f(x)-g(x)$. We need to show $F(x)=k$ for all $x \in (a,b)$

We know $F(x)$ is differentiable on $(a,b)$

$F'(x) = f'(x)-g'(x) = 0$ for all $x \in (a,b)$

Let $x_1$ and $x_2$ be any numbers in $(a,b)$ such that $x_1 < x_2$

We know $F(x)$ is differentiable $(x_1, x_2)$ and continuous on $[x_1, x_2]$. By the **Mean Value Theorem**, we know there exists $c \in (x_1, x_2)$ such that:

$$
\frac{F(x_2)-F(x_1)}{x_2 - x_1} = F'(c) = 0
$$

#### Show:
$F(x_1) = F(x_0)$
Because $F$ has the same value at any two numbers $x_1$, and $x_2$ in $(a,b)$, $F(x) = k$. Thus $f(x)-g(x) = k$

Linear Approximation
=====
Linear Approximation of $f$ at $x=a$ is
$$
f(x) \approx f(a) + f'(x)(x-a)
$$
Linearization of $f$ at $a$:
$$
L(x) = f(a) + f'(a)(x-a)
$$
When $\theta$ is close to $0$
$$
\sin (\theta) \approx \theta
$$
$$
f(\theta) = \sin (\theta) \to f'(\theta) = \cos (\theta)
$$
$$
f(0) = \sin(0) = 0 \to f'(0) = 1
$$
$$
L(\theta) = f(0) + f'(0)(\theta-0) = \theta
$$

Newton's Method
====

We are looking for $x$ such that f(x) = 0

Newton's Method helps us approximate $x$

$f(r) = 0 \to$ I am Looking for $r$

As $x_3$ and $x_2$ get closer together, the closer you are to $r$

$$
f(x) \approx f(x_1) + f'(x_1)(x-x_1)
$$
$$
0 = f(x_1) + f'(x_1)(x-x_1)
$$
$$
x_1 - \frac{f(x_1)}{f'(x_1)}
$$
We keep going to generate a sequence of numbers $x_1, x_2, x_3, x_4,..., x_n$
In most cases, the number $x_n$ becomes closer and closer to the root!

In-Class Problem
----

$\theta(t)$ be the angle of direct sight of airplane at the time

$L(t)$ is the distance the airplane (mi) is away from the island at the time $t$

We are looking for $\frac{dL}{dt}$
$$
\frac{d\theta}{dt} = \frac{2}{3} * \frac{60 sec}{1 min} * \frac{60 min}{1 hr} = \frac{2}{3} * 3600 \frac{deg}{hr} * \frac{\pi}{180} = \frac{2400\pi}{180}\frac{rad}{hr}
$$
Relationship between variables:
$$
\tan(\theta(t)) = \frac{\frac{1200}{528}}{L{t)}} = \frac{1200}{528}[L(t)]^{-1}
$$
Take Derivative:
$$
\sec^{2}(\theta(t)) \frac{d\theta}{dt} = \frac{-1200}{528}[L(t)]^{-2} \frac{dL}{dt}
$$
$$
(-\sec^2\theta)(\frac{d\theta}{dt})(\frac{528}{1200})L^2 = \frac{dL}{dt}
$$

----

Optimization
====

Example
----

An open-top box is to be made by cutting small congruent squares from the corners of a $12in$ by $12in$ sheet of tin and bending up the sides.

How large should the squares cut from the corners be to make the box hold as much as possible?

Let $x$ be the length of the square cutout in inches.

We plan to maximize volume.

$$
V(x) = \binom{12-2x}{length}\binom{12-2x}{width}\binom{x}{height} = 12-2x)^2x
$$
For $0<=x<=6$

Find Critical Points:
$$
V'(x) = 2(12-2x)^1(-2)x + (12-2x)^2 * 1
$$
$$
V'(x) = (12-2x)(-4x+12-2x)
$$
$$
V'(x) = (12-2x)(-6x+12)
$$
$$
0 = (12-2x)(-6x+12)
$$
$$
0 = 12-2x \\ 0 = -6x+12
$$
Next we check volume at critical points/end Points
$$
V(0) = 0
$$
$$
V(6) = 0
$$
$$
V(2) = (8)^2 * 2 = 128in^3
$$
Volume is maximize $(128in^3)$

----

Example
----
A rectangle is to be inscribed in a semicircle of radius 2.

What is the largest area the rectangle can have and what are its dimensions?

### Steps
1. Draw a Picture
2. Introduce Variables
    - Let $x$ be the x-coordinate of corner of rectangle
    - $0 \leq x \leq 2$
    - Equation of a circle is $y^2 + x^2 = 4$
    - Top half of circle described by $y = \sqrt{4-x^2}$
3. Write an equation for unknown quantity
    $$
    A(x) = (2x)(\sqrt{4-x^2})
    $$
4. Find Critical points. Evaluate Function at critical points and end points.
    $$
    \frac{dA}{dx} = 2\sqrt{4-x^2} + 2x(\frac{2x}{2\sqrt{4-x^2}})
    $$
    $$
    2\sqrt{4-x^2} = \frac{2x^2}{\sqrt{4-x^2}}
    $$
    $$
    2(4-x^2) = 2x^2
    $$
    $$
    4 = 2x^2
    $$
    $$
    x = \sqrt{2}
    $$
##### Critical Point: $x=2$ and $x=\sqrt{2}$
##### End Points: $x=0$ and $x=2$

$$
A(2) = 0
$$
$$
A(0) = 0
$$
$$
A(\sqrt{2}) = 2\sqrt{2}\sqrt{4-\sqrt{2}^2} = 4
$$
The area has a maximum of 4 when the rectangle is $sqrt{4-x^2} = \sqrt{2}$ units high and $2x = 2\sqrt{2}$ units long

Sigma Notation
====
It is convenient to use the Greek letter $\Sigma$ to indicate sum.
$$
\sum_{k=1}^{n} a_k = a_1 + a_2 + a_3 + ... + a_n
$$
Compact way to write a sum with many terms
$$
\sum_{k=1}^{n} a_k
$$
Index $k$ starts at $k=1$

Index $k$ ends at $k=n$

Formula for the $k$th term

$k$ is called the index of summation

$$
\sum_{i = 0}^{4} 4^{-i} = \sum_{i = 0}^{4} \frac{1}{2^{2i}} = \sum_{k=1}^{5} 4^{-(k-1)}
$$

Example
----
Express the sum $8 - \frac{8}{3} + \frac{8}{9} - \frac{8}{27} + \frac{8}{81}$ in sigma notation
$$
\frac{8}{3^0} - \frac{8}{3^1} + \frac{8}{3^2} - \frac{8}{3^3} + \frac{8}{3^4}
$$
$$
= \sum_{k=0}^{4} \frac{8(-1)^k}{3^k} = \sum_{k=0}^{4} \frac{8}{(-3)^k}
$$

----

### Algebra Rules for Sums
1. Sum rule
$$
\sum_{k=1}^{n} (a_k + b_k) = (a_1 + b_1) + (a_2 + b_2) + (a_3 + b_3) + ... + (a_n + b_n) = \sum_{k=1}^{n} a_k + \sum_{k=1}^{n} b_k
$$
2. Difference rule
$$
\sum_{k=1}^{n} (a_k - b_k) = \sum_{k=1}^{n} a_k - \sum_{k=1}^{n} b_k
$$
3. Constant rule
$$
\sum_{k=1}^{n} c(a_k) = c(\sum_{k=1}^{n} (a_k))
$$
Where $c$ is Constant
4.
$$
\sum_{k=1}^{n} c = n(c)
$$
