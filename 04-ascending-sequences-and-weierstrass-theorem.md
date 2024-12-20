---

numbering:
  enumerator: 1.4.%s

---

# 1.4 Ограниченные последовательности

## Ограниченные множества и принцип полноты Вейерштрасса

Прежде всего нам понадобятся следующие определения:

:::{prf:definition}
:label: upper-lower-bound
Пусть $A \subseteq \mathbb{R}$ — непустое подмножество. Число $a$ называется **верхней гранью** множества $A$, если $x\le a$ для любого $x \in A$. Если есть хотя бы одна верхняя грань, то говорят, что множество $A$ **ограниченно сверху.** Наименьшая из всех верхних граней множества $A$ называется **точной верхней гранью** множества $A$ и обозначается $\mathrm{sup}(A)$ (=супремум).

Число $a'$ называется **нижней гранью** множества $A$, если $x \ge a'$ для каждого $x \in A$. Если есть хотя бы одна нижняя грань, то множество называют **ограниченным снизу**. Наибольшая из нижних граней множества $A$ называется **точной нижней гранью** множества $A$ и обозначается $\mathrm{inf}(A)$ (= инфимум).

Ограниченное и сверху, и снизу множество называется **ограниченным.**
:::

:::{warning}
Из определения не следует, что супремум или инфимум существуют, ведь, скажем, для подмножества $A:= \{x>0, x^2 < 2\}$ множества $\mathbb{Q}$, число $\sqrt{2} = \sup (A)$, но $\sqrt{2} \notin \mathbb{Q}$, т. е. в $\mathbb{Q}$ не у каждого подмножества есть супремум. 
:::

:::{prf:theorem} Принцип полноты Вейерштрасса
:name: W=complete
Если $A\subseteq \mathbb{R}$ — непустое и ограниченное сверху (снизу) множество, то $\mathrm{sup}(A)$ (**соотв.** $\mathrm{inf}(A)$) существует.
:::
:::{prf:proof}
:class: dropdown
:nonumber:
Докажем эту теорему только в случае ограниченного сверху множества, так как другой случай доказывается аналогично.

Пусть $B$ есть множество всех верхних граней множества $A$, тогда из условия об ограниченности сверху множества $A$ следует, что $B \ne \varnothing$. Далее из конструкции $B$ вытекает, что $A\le B$ (т. е. $A$ левее чем $B$). Тогда по аксиоме о полноте получаем, что существует $c \in \mathbb{R}$ такой, что $A \le c \le B$. Тогда, во-первых, $c$ — какая-то верхняя грань для $A$, а, во-вторых, $c$ меньше или равен  любому из элементов множества $B$, т. е. $c = \mathrm{sup}(A)$, что и требовалось доказать.
:::



:::{prf:example}
Пусть $A := (0,1]$. Тогда, например, числа $1.0000001, 2, 10, 9823750219581$ — его верхние грани. А, например, числа $0, -0.1111111, -8347027408751$ — его нижние грани.

Пусть $\mathrm{sup}(A) = a$. Рассмотрим варианты:

1. если $a >1$, то тогда $x<a$ для любого $x\in A$, т. е. $a \ne \mathrm{sup}(A)$;
2. если $a<0$, то тогда $a<x$ для любого $x \in A$, т. е. $a \ne \mathrm{sup}(A)$;
3. если $0<a<1$, то тогда $a < \frac{a+1}{2}$ и к тому же $\frac{a+1}{2}<1$, т. е. $a \ne \mathrm{sup}(A)$; 
4. таким образом, остаётся только один вариант, $a = 1.$

Это можно также доказать следующим образом. Действительно, если $1-\delta = \mathrm{sup}(A)$, где $\delta > 0$, то рассмотрев $x:=1-\frac{\delta}{2}$ мы видим что $x\in A$ и $1-\delta < x$. Это и означает что ни при каких $\delta >0$, число $1 - \delta$ не может быть супремумом.

Аналогично можно показать, что $0 = \mathrm{inf}(A).$
:::

## Ограниченные последовательности и теорема Вейерштрасса

Вернёмся к последовательностям.

:::{prf:definition}
:label: bounded-sequence
Последовательность $(a_n)$ называется **ограниченной**, если существуют такие $A,B \in \mathbb{R}$, что $A\le a_n \le B$ для всех $n\in\mathbb{N}.$
:::

:::{prf:lemma}
:name: lim-bounded_for_sequence
Если у последовательности $(a_n)$ есть предел $\lim_{n \to \infty} a_n = a$, то она ограничена.
:::

:::{prf:proof}
:class: dropdown
:nonumber:
Действительно, согласно определению предела (см. [определение](#limit_of_sequence)), для любого $\varepsilon>0$ найдётся такой номер $N$, что для всех $n \ge N$ выполняются неравенства
$$
a- \varepsilon < a_n < a+\varepsilon.
$$

Пусть $\varepsilon = 1$ и пусть $N_1$ это такой номер, что для всех $n\ge N_1$ мы имеем
$$
a-1 < a_n < a+1.
$$

Тогда пусть $R: = \max \{a_1, \ldots, a_{N_1 -1}, a+1\}$, и $L: = \min \{a_1,\ldots, a_{N_1 -1}, a-1\}$, тогда для всех $n\ge 1$, получаем
$$
L \le a_n \le R
$$
**т.е.** последовательность $(a_n)$ — ограничена.
:::

:::{prf:definition}
:label: non-descending-non-ascending-sequence
Говорят, что последовательность $(a_n)$ **не убывает** (соответственно, **не возрастает**), если $a_n \le a_{n+1}$ (соответственно, $a_n \ge a_{n+1}$) для всех $n \ge 1.$ Последовательность, которая либо не убывает, либо не возрастает называется **монотонной.**
:::


:::{prf:theorem} Вейерштрасс
:name: Weierstrass
Если последовательность не убывает (не возрастает) и ограничена сверху (снизу), то существует предел $\lim_{n \to \infty}a_n$, который равен $\mathrm{sup}(a_n)$ (соотв. $\mathrm{inf}(a_n)$).
:::

:::{prf:proof}
:class: dropdown
:nonumber:
Будем доказывать только для не убывающих последовательностей, потому что для невозрастающих рассуждения аналогичные.

Так как последовательность $(a_n)$ ограничена сверху, то по принципу полноты Вейерштрасса существует $\mathrm{sup}(a_n) = a$. Это означает, что для любого $\varepsilon >0$, $a-\varepsilon \ne \mathrm{sup}(a_n)$, т. е. существует такой $N$, что $a_N >a -\varepsilon$.

Далее, так как $a_n \le a_{n+1}$ (так как по предположению последовательность не убывающая), то все $a_{N+1}, a_{N+2}, \ldots > a -\varepsilon$. Так как $a = \mathrm{sup}(a_n)$, то $a_n \le a$ для всех $n$. Таким образом, для всех $n > N$, мы получаем $a- \varepsilon < a_n \le a$. Очевидно, что $a < a+\varepsilon$. Другими словами, мы для любого $\varepsilon >0$ нашли такое $N$, что для всех $n>N$ $a -\varepsilon < a_n < a + \varepsilon$, т. е. $|a_n - a| < \varepsilon$. Но это и означает, что $\lim_{n \to \infty}a_n = a$, что и требовалось доказать.
:::

:::{prf:example}
Рассмотрим последовательность $a_{n+1} = \frac{1}{2}\left(a_n + \frac{2}{a_n} \right)$, $a_1 = 2$. 

Покажем, что она ограничена снизу: для этого воспользуемся неравенством $\frac{x+y}{2} \ge \sqrt{xy}$. Имеем
$$
a_{n+1} = c \ge \frac{1}{2}\cdot 2 \cdot \sqrt{a_n \cdot \frac{2}{a_n}} = \sqrt{2},
$$
т.е. $a_n \ge \sqrt{2}$ для всех $n \ge 1$.

Покажем, что она невозрастающая, т. е. для всех $n\ge 1$, $a_{n} \ge a_{n+1}$.

Имеем
$$\begin{align*}
a_{n+1} - a_n &= \frac{1}{2}\left(a_n + \frac{2}{a_n} \right) - a_n \\
&= \frac{a_n}{2} + \frac{1}{a_n} - a_n \\
&= -\frac{a_n}{2} + \frac{1}{a_n} \\
&= -\frac{1}{2}\cdot\left( \frac{a_n^2 - 2}{a_n^2}\right),
\end{align*}$$
так как $a_n \ge \sqrt{2}$, то $a_{n+1} - a_n \le 0$, т.е. $a_{n} \ge a_{n+1}$, а это значит, что она не возрастает. 

Таким образом, по теореме Вейерштрасса эта последовательность имеет предел. Пусть $\lim_{n\to \infty}a_n =a$, тогда по [теореме](#a+b,ca,ab) получаем
$$\begin{align*}
a &= \lim_{n \to \infty}a_{n+1} \\
&=\lim_{n \to \infty} \frac{1}{2} \left(a_n+ \frac{2}{a_n} \right) \\
&=  \frac{1}{2}\left( \lim_{n \to \infty} a_n + \frac{2}{\lim_{n \to \infty} a_n} \right) \\
&=\frac{1}{2}\left( a + \frac{2}{a}\right).
\end{align*}$$

Мы получили квадратное уравнение $a = \frac{1}{2}\left(a + \frac{2}{a} \right)$, откуда $a^2 = 2$. С учётом $a_n \ge \sqrt{2}$ получаем, что $a = \sqrt{2}$. Итак, $\lim_{n \to \infty}a_n = \sqrt{2}.$
:::



:::{prf:example}
Рассмотрим последовательность $e_n =\left(1 + \frac{1}{n} \right)^n$.

Имеем
$$\begin{align*}
e_n &= \left(1 + \frac{1}{n} \right)^n = \sum_{k=0}^n \binom{n}{k} \frac{1}{n^k}\\
&=1 + 1 + \frac{1}{2!} \cdot \frac{n(n-1)}{n^2} + \frac{1}{3!}\cdot \frac{n(n-1)(n-2)}{n^3} + \cdots \\
&+ \frac{1}{(n-1)!} \cdot \frac{n(n-1)\cdots (n-(n-2))}{n^{n-1}} + \frac{1}{n!} \frac{n(n-1)\cdots (n-(n-1))}{n^n} \\
&=2 + \frac{1}{2} \cdot 1\cdot \left(1-\frac{1}{n} \right) + \frac{1}{3!} \cdot 1 \cdot \left(1 - \frac{1}{n} \right) \left(1 - \frac{2}{n} \right) + \cdots \\
&+ \frac{1}{(n-1)!} \cdot 1 \cdot \left(1 - \frac{1}{n} \right) \left(1 - \frac{2}{n} \right) \cdots \left(1 - \frac{n-2}{n} \right) + \frac{1}{n!} \cdot 1 \cdot \left(1 - \frac{1}{n} \right) \cdots \left(1 - \frac{n-1}{n} \right)
\end{align*}$$

Заметим прежде всего, что так как $\frac{m}{n} >0$, то все $e_n >0$. Далее имеем
$$\begin{align*}
e_{n+1} &= 2 + \frac{1}{2}\cdot 1 \cdot\left(1 - \frac{1}{n+1} \right) + \frac{1}{3!} \cdot \left(1 - \frac{1}{n+1} \right)\left(1 - \frac{2}{n+1} \right) + \cdots \\
&+ \frac{1}{n!} \cdot 1 \cdot \left(1 - \frac{1}{n+1} \right) \left(1 - \frac{2}{n+1} \right) \cdots \left(1 - \frac{n-1}{n+1} \right) + \frac{1}{(n+1)!} \cdot 1 \cdot \left(1 - \frac{1}{n+1} \right) \cdots \left(1 - \frac{n}{n+1} \right).
\end{align*}$$

Так как $1 - \frac{t}{n} < 1 - \frac{t}{n+1}$, то $e_n \le e_{n+1}$. С другой стороны, каждая скобка $1- \frac{t}{n} <1$, тогда
$$
e_n \le \sum_{k=0}^n \frac{1}{k!} \le \sum_{k=0}^n \frac{1}{2^{k-1}} = 2 + 1 + \frac{1}{2} + \frac{1}{4} + \cdots + \frac{1}{2^{n-1}} \le 4.
$$
здесь мы воспользовались неравенством $k! \ge 2^{k-1}$. Таким образом, наша последовательность не убывает и ограничена сверху, а значит, по теореме Вейерштрасса у неё есть предел. Этот предел называется **число Эйлера** и обозначается через $e$, при этом $e \approx 2.7182818284590452353602874713527.$

:::