# Folgen
$$
\begin{array}{c|c}
    a_{0} & a_{1} & a_{2} & a_{3} & a_{4} & a_{5} \\
    \hline
    -1 & 0 & -1 & 5 & 4 & 7
\end{array}
$$
**Def:** Eine Folge ist eine Zuordnung $\mathbb{N} \implies \mathbb{R}$, d.h. zu jedem $\mathbb{N}$ gibt es ein $a_{k} \in \mathbb{R}$
**Bsp:** $(a_{k})^{\infty}_{k=0} = 0, 1, 2, 3, 4, 5 \implies a_{k} = k$
## Monotonie
### (Streng) Monoton Wachsend
Für alle $n_{1}<n_{2}$ gilt: $a_{n_{1}} \leq a_{n_{2}}$
**Streng:** Unaufhaltsam wachsen ($a_{n_{1}} < a_{n_{2}}$)
### (Streng) Monoton Fallend
Für alle $n_{1} < n_{2}$ gilt: $a_{n_{1}} \geq a_{n_{2}}$
**Steng:** Unaufhaltsam fallend ($a_{n_{1}} > a_{n_{2}}$)
### Beispiele
- $(a_{k})^\infty_{k=0} = -1, 0, -1, 5, 4, 0, 0, 0$ => Nicht Monoton
- $(a_{k})^\infty_{k=0} = 0,1,2,3$ => Streng Monoton Wachsend
- $(a_{k})^\infty_{k=0} = 5,3,2,1$ => Streng Monoton Fallend
- $(a_{k})^\infty_{k=0} = 0,1,2,2,3,3$ => Monoton Wachsend
# Konvergenz & Divergenz
## Konvergenz
Eine Folge $(a_{k})^\infty_{k=0}$ ist konvergent gegen einen festen Grenzwert $a \in \mathbb{R}$, wenn gilt:
$$
\lim_{ n \to \infty } a_{n} = a
$$
- **Bsp:** $a_{n} = 1 + \frac{1}{n}$ konvergiert gegen $1$.
## Divergenz
### Bestimmte Divergenz
Eine Folge $(a_{k})^\infty_{k=0}$ ist bestimmt divergent nach $\pm \infty$, wenn die Folge über jeden möglichen Grenzwert weiter wächst/fällt.
- **Divergenz nach $+\infty$:**  $\lim_{ n \to \infty } a_{n} = \infty$
- **Divergenz nach $-\infty$:**  $\lim_{ n \to \infty } a_{n} = -\infty$
### Unbestimmte Divergenz
Einige Folge $(a_{k})^\infty_{k=0}$ ist unbestimmt divergent, wenn $\lim_{ n \to \infty } a_{n}$ sich weder gegen einen festen Grenzwert, noch gegen $\pm \infty$ bewegt.
- **Bsp:** $a_{n} = (-1)^n = \{1;-1;1;-1;1;-1;1\}$
