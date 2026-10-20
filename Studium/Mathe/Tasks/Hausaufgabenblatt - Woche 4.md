**PS: Ich versuche langsam mit dem LaTeX Format Mathe-Zeug digital einzutragen. Ist keine KI ;)**
# Aufgabe 1
## a) Konvergente Folgen (mit Grenzwert)
$$
a_{n}= 3 n + 3^{-n} \\
= \lim_{ n \to \infty } (3n+3^{-n}) \\
= \lim_{ n \to \infty } (3n) = \infty \quad \text{und}
\lim_{ n \to \infty } (3^{-n}) = 0 \\
\to \lim_{ n \to \infty } (3 n + 3^{-n}) = \infty
$$
-> Der Term ist bestimmt divergent.

---
$$
b_{n} = 2 - \frac{3}{\sqrt{ n }} \\
= \lim_{ n \to \infty } \left( 2 - \frac{3}{\sqrt{ n }} \right) = \lim_{ n \to \infty } \left( 2^{\to 2} - \frac{3^{\to 3}}{\sqrt{ n }^{\to \infty}} \right) \\
\to \lim_{ n \to \infty } \left( 2 - \frac{3}{\sqrt{ n }} \right) = 2
$$
-> Der Term ist konvergent gegen $2$.

---
$$
c_{n} = \frac{(-1)^n}{2} + \frac{2}{n} \\
= \lim_{ n \to \infty } \left( \frac{(-1)^n}{2} + \frac{2}{n} \right) = \lim_{ n \to \infty } \left( \frac{(-1)^n \cdot n}{2 \cdot n} + \frac{4}{n \cdot 2} \right) \\
= \lim_{ n \to \infty } \left( \frac{(-1)^n \cdot n + 4}{2 \cdot n} \right) = \lim_{ n \to \infty } \left( \frac{n \cdot \left( (-1)^n + \frac{4}{n} \right)}{2 \cdot n} \right) \\
= \lim_{ n \to \infty } \left( \frac{((-1)^n)^{\to \pm 1}}{2^{\to 2}} \right) ^ {\to \pm \frac{1}{2}}
$$
-> Der Term ist divergent und schwingt zwischen $1$ und $-1$.
## b)
$$
a_{n} = 1 + \frac{3n^2-2}{n^2+n+1} \\
= \lim_{ n \to \infty } \left( 1 + \frac{3n^2-2}{n^2+n+1} \right) = \lim_{ n \to \infty } \left( 1 + \frac{n^2 \cdot \left( 3 - \frac{2}{n^2} \right)}{n^2 \cdot \left( 1 +\frac{1}{n} + \frac{1}{n^2} \right)} \right) \\
= \lim_{ n \to \infty } \left( 1 + \frac{3^{\to 3} - \left( \frac{2}{n^2} \right)^{\to 0}}{1^{\to 1} +\frac{1}{n}^{\to 0} + \frac{1}{n^2}^{\to 0}} \right) \\
\to \lim_{ n \to \infty } \left( 1 + \frac{3n^2 - 2}{n^2 + n + 1} \right) = 4
$$
---
$$
b_{n} = \left( 1 + \frac{1}{n} \right)^{2n + 1} \\
= \lim_{ n \to \infty } \left( \left( 1 + \frac{1}{n} \right)^{2n+1} \right)
$$
