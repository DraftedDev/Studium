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

5. $(f(g(x)))' = f'(g(x)) \cdot g'(x)$

6. $\left( \frac{f(x)}{g(x)} \right)' = \frac{f'(x)g(x) - f(x)g'(x)}{g^2(x)}$

7. **Speziell:**
	- $(e^x)' = e^x$
	- $(\sin(x))' = \cos(x)$
	- $(\cos(x))' = -\sin(x)$
	- $(\tan(x))' = 1 + \tan^2(x) = \frac{1}{\cos^2(x)}$
	- $(\ln(x))' = \frac{1}{x}$
	- $(f^{-1}(x))' = \frac{1}{f'(f^{-1}(x))}$
# Tangentengleichung
Gegeben $f(x)$, $f'(x)$, $x_{0} \in D$
Steigung von $T_{f}(x)$ in $x_{0}$ ist $f'(x_{0})$.
$$
T_{f}(f) = f'(x_{0}) \cdot x + b \\ \\
T_{f}(0) = b
$$
=> Punkt einsetzen: $(x_{0}|f(x_{0}))$
=> $f(x_{0}) = f'(x_{0}) \cdot x_{0} + b \implies b = f(x_{0}) - f'(x_{0}) \cdot x_{0}$
=> Also: $T_{f}(x) = f'(x_{0}) \cdot (x-x_{0}) + f(x_{0})$

**Satz:** $f$ ist differenzierbar in $x_{0} \in D$, dann ist die Tangente an der Stelle $x_{0}$:
=> $T_{f}(x) = f'(x) \cdot (x-x_{0}) + f(x_{0})$
# Regeln von L'Hospital
**Satz:** $f(x), g(x)$ differenzierbar mit $g'(x) \neq 0$, 
Gegeben $a \in \mathbb{R} \cup \{\pm \infty\}$. Falls $\lim_{ x \to a }(f(x)) = 0$ und $\lim_{ x \to a }(g(x)) = 0$.
$$
\implies \lim_{ x \to a } \left( \frac{f(x)}{g(x)} \right) =^{\frac{0}{0}} \lim_{ x \to a } \left( \frac{f'(x)}{g'(x)} \right)
$$
# Extremwerte
=> $f(x) = 0$ -> Nullstelle.
=> $f(0)$ -> Y-Achsenabschnitt.
=> $f'(x) = 0$ -> Waagrechte Tangente.

**Def:** $f(x)$ hat in $x_{0}$ ein relatives/lokales Minimum bzw. Maximum, falls es eine Umgebung $I$ von $x_{0}$ gibt:
=> $f(x_{0}) \leq f(x)$ f.a. $x \in I$ (Minimum)
=> $f(x_{0}) \geq f(x)$ f.a. $x \in I$ (Maximum)

**Satz:** Ist $f(x)$ differenzierbar