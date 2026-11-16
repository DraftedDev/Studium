# Definition
=> *Eine reelle Funktion $f: D \to \mathbb{R}$ ordnet jedem $x \in D$ genau ein $y=f(x) \in \mathbb{R}$ zu.*
- $D$: Definitionsbereich $D \in R$ (x-Achse).
- $x$: Variable.
- $W$: Wertebereich $W = \{f(x) | x \in D\} \in \mathbb{R}$ (y-Achse).
---
- Verschiebung um $a$ nach oben/unten: $y=f(x)+a$
- Verschiebung um $a>0$ nach rechts: $y=f(x-a)$
- Verschiebung um $a$ nach links: $y=f(x-a)$
- Spiegeln an der x-Achse: $y=-f(x)$
- Spiegeln an der y-Achse: $y = f(-x)$
# Heaviside Funktion
$$
H(x) = \begin{cases}
0, \quad x \geq 0 \\
1, \quad x < 0 
\end{cases}, \quad D=\mathbb{R}
$$
# Verkettung
- $\mathbb{R} \stackrel{f}{\longrightarrow} \mathbb{R} \stackrel{g}{\longrightarrow} \mathbb{R}$
- $x \to f(x) \to g(f(x)) \implies \text{(gof)}$
# Umkehrfunktion
- Gegeben $y=f(x)$, suche $f^{-1}(x)$ mit: 
	- => $(fof^{-1})(x)=x$ 
	- => $(f^{-1}of)(x)=x$
- **Algorithmus:**
	- Tausche $x \leftrightarrow y$ => $y=f(x) \longrightarrow x=f(y)$
	- Löse $x=f(y)$ nach $y$ auf.
- **Graphisch:**
![[Reelle Funktionen-1794828640726.webp|416]]
## Satz
=> $f^{-1}(x)$ existiert auf $D_{f}$, falls es zu jedem $y \in W_{f}$ genau ein $x \in D_{f}$ gibt mit $y=f(x)$. D.h. es gilt ein 1:1-Zusammenhang zwischen $D_{f}$ und $W_{f}$. Der Graph $f^{-1}$ wird durch Spiegelung an $y=x$ erhalten.
# Spezielle Funktionen
## Potenzfunktionen
=> $f(x)=x^n, \quad n \in N_{>0}$
- s.m.w. auf $D_{f}=[0,\infty], \quad W_{f}=[0,\infty]$
	=> Es gilt $f^{-1}: [0,\infty]\to[0,\infty]$
### Definition
=> Die Umkehrfunktion von $f:[0,\infty]\to[0,\infty]$, $f(x)=x^n$, $n \geq 1$ heißt n-te Wurzel $f^{-1}(x)=\sqrt[n]{x}=x^{\frac{1}{n}}$.
### Satz
=> $x^n=a, \quad a \in \mathbb{R}, \quad x \in \mathbb{R}$
$$
\text{n gerade } \implies \begin{cases}
\mathbb{L} = \{\sqrt[n]{ a }, -\sqrt[n]{ a }\}, \quad a \geq 0 \\
\mathbb{L} = \varnothing, \quad a < 0
\end{cases} \\
\text{n gerade } \implies \begin{cases}
\mathbb{L} = \{\sqrt[n]{ a }\}, \quad a \geq 0 \\
\mathbb{L} = \{-\sqrt[n]{ -a }\}, \quad a < 0
\end{cases}
$$
## Exponentialfunktion / Logarithmus
$$
a > 0, \quad n \in \mathbb{Z}, \quad m \in \mathbb{N}_{>0} \\
\implies a^{\frac{n}{m}} = \sqrt[m]{ a^n }
$$
### Definition
=> $b \in \mathbb{R}, \quad a > 0$. Wähle Folge $(b_{n})^\infty_{n=0}, \quad b_{n} \in \mathbb{Q}, \quad \lim_{n \to \infty}(b_{n}=b)$, setze $a^b = \lim_{n\to\infty}(a^{b_{n}})$.
### Eigenschaften $a^x$
- $a>1: \quad W_{f}=(0,\infty)$ s.m.w. => $f^{-1}$ existiert.
- $a=1: \quad W_{f}=\{1\}$ => $f^{-1}$ existiert *nicht*.
- $0<a<1: \quad W_{f}=(0,\infty)$ s.m.f. => $f^{-1}$ existiert.
### Definition
Die Umkehrfunktion von $f: \mathbb{R} \to (0, \infty), \quad f(x)=a^x, \quad a>0, \quad a \neq 1$ heißt:
=> $\log_{a}(0,\infty) \to \mathbb{R}$ => "Logarithmus zur Basis $a$".
=> $a^{\log_{a}(x)}=x, \quad \log_{a}(a^x)=x$
### $e$-Funktion
$a = e$ Eulerzahl: $e^x$ "Exponentialfunktion".
$\log_{e}(x)=\ln(x)$: "natürlicher Logarithmus".
### Rechenregeln
$$
e^{x+y} = e^x \cdot e^y; \quad (e^x)^y = e^{x \cdot y}; \quad e^{-x} = \frac{1}{e^x}; \quad e^0 = 1 \\ \\
\ln(x \cdot y) = \ln(x) + \ln(y); \quad \ln(x^y) = y \cdot \ln(x); \quad -\ln(x) = \ln\left( \frac{1}{x} \right); \quad \ln(0) = 1
$$
$$
\log_{a}(x) = \frac{\ln(x)}{\ln(a)}
$$
