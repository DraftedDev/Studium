Gegeben $f: D \to \mathbb{R}, x_{0} \in D$.
Spezielle Gerade $y = mx + b$
$$
m = \frac{\Delta y}{\Delta x} = \frac{f(x_{0}+\Delta x) - f(x_{0})}{\Delta x} \\ \\
\Delta x \neq 0
$$
# Definition
Die Funktion $f: D \to \mathbb{R}$ heißt:
- **1):** "in $x_{0} \in D$ differenzierbar", falls:
	$f'(x_{0}) = \lim_{ \Delta x \to 0 }\left( \frac{f(x_{0}+\Delta x) - f(x_{0})}{\Delta x} \right)$ existiert.
- **2):** "differenzierbar", falls differenzierbar in allen $x_{0} \in D$. Dann $f'(x)$ "1. Ableitung".

Bsp. $f(x) = mx+b \implies f'(x) = m \quad D \in \mathbb{R}$
Denn: $x_{0} \in D$
$$
f'(x_{0}) = \lim_{ \Delta x \to 0 } \left( \frac{(m \cdot (x_{0} + \Delta x) + b) - (m \cdot x_{0} + b)}{\Delta x} \right) \\ \\
= \lim_{ \Delta x \to 0 } \left( \frac{mx_{0} + m \cdot \Delta x + b - m \cdot x_{0} - b}{\Delta x} \right) \\ \\
= \lim_{ \Delta x \to 0 } \left( \frac{m \cdot \Delta x}{\Delta x} \right) = m
$$
# Regeln
1. $(x^n)' = n \cdot x^{n-1}$ mit $n \in \mathbb{N}$

2. $(a \cdot f(x))' = a \cdot f'(x)$ mit $a \in \mathbb{R}$

3. $(f(x) + g(x))' = f'(x) + g'(x)$

4. $(f(x) \cdot g(x))' = f'(x) \cdot g(x) + f(x) \cdot g'(x)$

5. $(u(v(x)))' = u'(v(x)) \cdot v'(x)$

6. 