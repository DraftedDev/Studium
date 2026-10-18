 Fakultäten
$5! = 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 120$
$0! = 1$ - Nachdefiniert
# Binominalkoeffizient
Für $k,n \in \mathbb{N}, k \leq n, \text{heißt} \binom{n}{k} = \frac{n!}{k!(n-k)!}$ 
=> $n$ über $k$ => $n$ über Binominalkoeffizient
- **Bsp:** $\binom{5}{3} = \frac{5!}{3!2!} = 10$
## Pascalsches Dreieck
$$
\begin{matrix}
        &   &   & 1 &   &   &   \\
        &   & 1 &   & 1 &   &   \\
        & 1 &   & 2 &   & 1 &   \\
    1   &   & 3 &   & 3 &   & 1
\end{matrix}
\quad=\quad
\begin{matrix}
        &   &   & \binom{0}{0} &   &   &   \\
        &   & \binom{1}{1} &   & \binom{1}{0} &   &   \\
        & \binom{2}{2} &   & \binom{2}{1} &   & \binom{2}{0} &   \\
    \binom{3}{3}   &   & \binom{3}{2} &   & \binom{3}{1} &   & \binom{3}{0}
\end{matrix}
$$
# Binomische Sätze
$$
(a+b)^n = \sum_{k=0}^{n}{\binom{n}{k}a^k b^{n-k}} 
$$
**Bsp:**
- $(a+b)^2 = 1 \cdot a^2 + 2 a b + 1 \cdot b^2$
- $(a+b)^3 = a^3 + 3 a^2 b + 3 a b^3 + b^3$
- $(a+b)^4 = a^4 + 4 a^3 b + 6 a^2 b^2 + 4 a b^4+ b^4$