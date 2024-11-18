---

numbering:
  enumerator: 4.1.%s

---

# 4.1. Понятие непрерывного отображения на прямой

## Отображения
Пусть $X,Y$ — два множества, $R(x,y)$ — отношение между $x \in X$, $y \in Y$. **График** $\Gamma(R)$ отношения $R$ определяется следующим образом:
$$
X \times Y \supseteq \Gamma(R) : = \{(x,y) \, :\, (x,y) \in R\}.
$$

Пусть $X,Y$ — два множества, $R(x,y)$ — отношение между $x \in X$, $y \in Y$. Говорят, что $R$ **функционально по $y$**, если для **каждого** $x\in X$ существует **один и только один** такой элемент $y\in Y$, что $R(x,y)$ истинно.

График $F$ такого отношения называется **функциональным графиком** в $X \times Y$. Его можно также охарактеризовать следующим образом:  для каждого $x \in X$ существует один и только один такой элемент $y \in Y$, что $(x,y) \in R$; этот элемент называется **значением** $F$ в $x$ и обозначается символом $F(x)$.

:::{prf:definition}
Функциональный график в $X \times Y$ называется также **отображением $X$ в $Y$** или **функцией, определённой в $X$ и принимающей значения в $Y.$**    
:::

Мы также будем записывать такое отображение в виде $F:X \to Y$, понимая под этим, что каждому $x \in X$ ставится в соответствие ровно один $y  = F(x)\in Y$.

:::{warning}
Таким образом, мы считаем, что $F$ определено на всём $X.$ 
:::

Мы переформулируем определение отображения в более удобном для нас виде.

:::{prf:definition}
Отображением множества $X$ в множество $Y$ называется тройка $(X,Y,F)$, составленная из $X,Y$, и правила $F$, ставящего в соответствие **каждому** элементу множества $X$ некоторый элемент множества $Y$.
:::

Множество $F(X) \subseteq Y$, определённое как $\{F(x), \, x \in F\}$, называется образом отображения $F$ и иногда будет обозначаться как $\mathrm{Im}(F).$ Далее, множество $F^{-1}(Y) \subseteq X$, определённое как
$$
F^{-1}(Y):= \{x \in X\, :\, F(x) \in Y\},
$$
называется **прообразом** отображения $F.$

Нам понадобятся следующие свойства прообразов:

:::{prf:proposition}
:name: good_for_preimage
Если $F: X \to Y$ — отображение, то справедливы следующие включения

1. Для любого $A \subseteq X$, $A \subseteq F^{-1}(F(A))$,
2. для любого $B \subseteq Y$, $F(F^{-1}(B)) \subseteq B.$

:::

:::{warning}
Тем не менее, следуя фольклорной традиции, мы будем называть функцией отображение, которое принимает числовые значения, т.е. когда образ отображения — это некоторое подмножество в $\mathbb{R}.$
:::

Приведём некоторые важные для нас свойства отображений.

:::{prf:proposition}
:name: good_for_maps
Пусть $F:X \to Y$ — отображение между двумя непустыми множествами и пусть $(A_\lambda)_{\lambda \in \Lambda}$, $(B_\mu)_{\mu \in M}$ — семейство подмножеств в $X$ и $Y$, соответственно. Тогда верны равенства

\begin{align}
& \mbox{если $A \subseteq A'$, то $F(A) \subseteq F(A')$},\\ 
& F\left( \bigcup_{\lambda \in \Lambda} A_\lambda \right) = \bigcup_{\lambda \in \Lambda} F(A_\lambda), \label{F(U)=UF} \\
& F^{-1} \left( \bigcup_{\mu \in M} B_\mu \right) = \bigcup_{\mu \in M} F^{-1}(B_\mu) \\
& F^{-1} \left( \bigcap_{\mu \in M} B_\mu \right) = \bigcap_{\mu \in M} F^{-1}(B_\mu)
\end{align}

:::


## Непрерывные отображения

Приведём цитату:[^hash49-1]

> Если принять, что математическое понятие окрестности соответствует интуитивной идее "близости", то определение непрерывности можно выразить ещё наглядней, сказав, что точка $f(x)$, где $f$ — непрерывное отображение, сколь угодно близка к точке $f(x_0)$, как только точка $x$ достаточно близка к $x_0$.

:::{prf:definition}
:name: def_of_cont_on_sets_on_R
Пусть $X,Y \subseteq \mathbb{R}$ — два подмножества. Функция $f: X  \to Y$ называется **непрерывной в точке $x_0 \in X$**, если для каждой окрестности $\mathscr{W}(f(x_0)) \subseteq Y$ точки $f(x_0) \in Y$ существует такая окрестность $\mathscr{U}(x_0)\subseteq X$ точки $x_0$, что $f(\mathscr{U}(x_0)) \subseteq \mathscr{W}(f(x_0))$.

Отображение $f$ называется **непрерывным в $E$** (или просто непрерывным), если оно непрерывно в каждой точке пространства $E.$
:::

:::{warning}
Нужно обратить внимание, что окрестность $\mathscr{U}(x_0)$ подразумевается **открытым множеством в множестве $X$**, а окрестность $\mathscr{W}(f(x_0))$ — **открытое множество в множестве $Y$.**
:::

:::{prf:lemma}
:name: contious_on_R
Функция $f:\mathbb{R} \to \mathbb{R}$ непрерывна в точке $x_0$ тогда и только тогда, когда для любой $\varepsilon$-окрестности $\mathscr{B}_\varepsilon(f(x_0))$ точки $f(x_0)$ найдётся такая $\delta$-окрестность $\mathscr{B}_\delta(x_0)$ точки $x_0$, что 
$$
f\bigl(\mathscr{B}_\delta(x_0) \bigr) \subseteq \mathscr{B}_\varepsilon(f(x_0)).
$$
:::

:::{seealso}
Другими словами, **ДЛЯ ЛЮБОГО** интервала вида $(f(x_0)-\varepsilon, f(x_0) + \varepsilon)$ **ВСЕГДА** можно подобрать такое $\delta>0$, что функция отображает **ЦЕЛИКОМ ВЕСЬ** интервал $(x_0- \delta, x_0 + \delta)$ во внутрь интервала  $(f(x_0)-\varepsilon, f(x_0) + \varepsilon)$.
:::

:::{figure} ./images/continous.png
:name: continous
:align: center
Пример графика непрерывной функции; для любой $\varepsilon$-{cyan}`окрестности` точки $f(x_0)$ найдётся $\delta$-{green}`окрестность` точки $x_0$, такая, что функция $f$ полностью отобразит эту $\delta$-{green}`окрестность` в $\varepsilon$-{cyan}`окрестность`.
:::

:::{prf:proof}
:class: dropdown
:nonumber:
Доказательство [](#contious_on_R)

(1) Пусть $f:\mathbb{R} \to \mathbb{R}$ — непрерывная функция, тогда она непрерывна в любой точке. Тогда для любой точки $x_0$ выполняются условия [](#def_of_cont_on_sets_on_R), а так как согласно [](#interval_is_open) множества $\mathscr{B}_\delta(x_0), \mathscr{B}_\varepsilon(f(x_0))$ открыты, то мы получаем включение $f\bigl(\mathscr{B}_\delta(x_0) \bigr) \subseteq \mathscr{B}_\varepsilon(f(x_0)).$

(2) Пусть теперь для любой точки $x \in \mathbb{R}$ и для любой $\varepsilon_y$-окрестности точки $y=f(x)$ всегда можно найти такую $\delta_x$-окрестность точки $x$, что $ f\bigl(\mathscr{B}_{\delta_x}(x) \bigr) \subseteq \mathscr{B}_{\varepsilon_y}(f(x))$. 

Рассмотрим теперь произвольную окрестность $\mathscr{W}$ точки $f(x_0)$, где $x_0$ — произвольная точка. Так как $\mathscr{W}$ — открытое в $\mathbb{R}$ множество, то согласно [](#open_in_R) и (#open=union_of_opens), можем записать

$$
\mathscr{W} = \bigcup_{y \in \mathscr{W}} \mathscr{B}_{\varepsilon_y}(y),
$$
а так как $y_0: = f(x_0) \in \mathscr{B}_{\varepsilon_{y_0}}(f(x_0))$, то согласно предположению, найдётся такая $\delta$-окрестность $\mathscr{B}_{\delta}(x_0)$, что $f(\mathscr{B}_{\delta}(x_0)) \subseteq \mathscr{B}_{\varepsilon_{y_0}}(y_0)$, а тогда и $f(\mathscr{B}_{\delta}(x_0)) \subseteq\mathscr{W}.$ Это завершает доказательство.
:::

:::{prf:corollary}
:name: reform_of_cont
Для того, чтобы функция $f:\mathbb{R} \to \mathbb{R}$ была непрерывной в точке $x_0$, необходимо и достаточно, чтобы для всякого $\varepsilon>0$ существовал такой $\delta >0$, что из $|x-x_0|<\delta$ следует $|f(x)-f(x_0)|<\varepsilon$.    
:::

:::{prf:proof}
:class: dropdown
:nonumber:
Действительно, для этого мы положим, что $\mathscr{W}(f(x_0)) = (f(x_0)-\varepsilon, f(x_0) + \varepsilon)$ и $\mathscr{U}(x_0) = (x_0-\delta,x_0 + \delta)$ в формулировке [](#contious_on_R).
:::

```{figure} ./images/non_continous.png
:name: non_continous
:align: center

Пример графика функции которая не является непрерывной в точке $x_0$; мы нашли такую $\varepsilon$-{cyan}`окрестность` точки $f(x_0)$, что никакая $\delta$-{green}`окрестность` точки $x$ целиком не отображается в эту $\varepsilon$-{cyan}`окрестность`.
```

:::{prf:remark}
:name: not_continous
Тогда если $f:\mathbb{R} \to \mathbb{R}$ не является непрерывной функцией  в точке $x_0$, то можно найти такую $\varepsilon$-окрестность $\mathscr{B}_\varepsilon(f(x_0))$ точки $f(x_0)$, что не существует $\delta$-окрестности $\mathscr{B}_\delta(x_0)$ точки $x_0$, что $f(\mathscr{B}_\delta(x_0)) \not \subseteq \mathscr{B}_\varepsilon(f(x_0))$. 
:::


:::{prf:example}
:name: x^2_is_continous
Пусть $f(x) = x^2$. Покажем, что эта функция непрерывна. Возьмём произвольную точку $x_0 \in \mathbb{R}$ и покажем, что $f$ непрерывна в этой точке. Согласно [](#reform_of_cont), нам нужно для любого $\varepsilon>0$ найти такое $\delta >0$, что из неравенства $|x- x_0|< \delta$ будет следовать неравенство $|x^2 - x_0^2|<\varepsilon.$

Имеем
$$\begin{align*}
|f(x)- f(x_0)| &=& |x^2 - x_0^2| \\
&=& |(x-x_0)(x+x_0)| \\
&=& |x-x_0| \cdot |x+x_0| \\
&=& |x-x_0|\cdot \left| (x-x_0) + 2x_0 \right| \\
&\le& |x-x_0| \cdot \left( |x-x_0| + 2 |x_0| \right).
\end{align*}$$

Поэтому если $|x-x_0|<\delta$ и если мы потребуем, чтобы $\delta (\delta + 2|x_0|)<\varepsilon$, то из неравенства $|x-x_0|<\delta$ будет следовать неравенство $|f(x)- f(x_0)| < \varepsilon$, что и доказывает непрерывность этой функции. 
:::

:::{prf:example}
:name: x^2sin(1x)
Покажем, что функция $f:\mathbb{R} \to \mathbb{R}$
$$
(x) = \begin{cases}
x^2 \sin \frac{1}{x}, & x \ne 0, \\
0, & x =0
\end{cases}
$$
непрерывнa в точке $0$.

Это значит, что для любого $\varepsilon >0$ мы должны найти такую $\delta >0$, что из неравенства $|x|<\delta$ будет следовать $|{f}(x) - {f}(0)| = |f(x)| <\varepsilon.$

Имеем 
$$
\left|{f}(x) -{f}(0)\right| = \left|x^2 \sin \frac{1}{x} - 0 \right| = \left|x^2 \sin \frac{1}{x}\right| \le |x^2| = x^2,
$$
поэтому если $x^2 <\varepsilon$, т. е. $-\sqrt{ \varepsilon} <x < \sqrt{\varepsilon}$, то и $|{f}(x) - {f}(0)| <\varepsilon$. Значит, для любого $0 < \delta < \sqrt{\varepsilon}$ из неравенства $|x|<\delta$ вытекает неравенство $|{f}(x) - {f}(0)|$, что и доказывает непрерывность в точке $0.$
:::

## Критерий непрерывности


:::{prf:theorem}
:name: preimage_of_open
Пусть $X,Y \subseteq \mathbb{R}$ — непустые подмножества на прямой. Функция $f:X \to Y$ непрерывна тогда и только тогда, когда прообраз любого открытого множества в $X$ является открытым множеством в $Y.$
:::

:::{prf:proof}
:class: dropdown
:nonumber:

(1) Пусть $f:X \to Y$ — непрерывная функция. Возьмём произвольное открытое множество $\mathscr{W} \subseteq Y$ и покажем, что множество $f^{-1}(\mathscr{W})$ открыто в $X$.

Пусть $x \in f^{-1}(\mathscr{W})$, тогда существует такой $y \in \mathscr{W}$, что $f(x) = y$. Далее, так как $\mathscr{W}$ является открытым множеством в $Y$, при этом $y\in \mathscr{W}$, $f(x) = y$, и $f$ — непрерывно в $x$, то согласно [](#def_of_cont_on_sets_on_R), найдётся такое открытое в $X$ множество $\mathscr{U} \subseteq X$, что $x \in \mathscr{U}$ и $f(\mathscr{U}) \subseteq \mathscr{W}.$ Тогда согласно [](#good_for_maps), получаем включение
$$
f^{-1}(f(\mathscr{U})) \subseteq f^{-1}(\mathscr{W}),
$$
наконец, согласно предложению [](#good_for_preimage), имеем
$$
\mathscr{U} \subseteq f^{-1}(f(\mathscr{U})) \subseteq f^{-1}(\mathscr{W}).
$$

Итак, мы получили следующее. Для любой точки $x \in f^{-1}(\mathscr{W})$ мы нашли такое открытое в $X$ множество $\mathscr{U}$, что

$$
x \in \mathscr{U} \subseteq f^{-1}(f(\mathscr{U})) \subseteq f^{-1}(\mathscr{W}).
$$
но тогда согласно [](#open_via_open) множество $f^{-1}(\mathscr{W})$ — открыто в $X.$


(2) Пусть прообраз любого открытого множества в $Y$ есть открытое множество в $X$. Пусть $f(x) = y$ и пусть $y \in \mathscr{W}$, где $\mathscr{W}$ — открытое множество в $Y$. Тогда $x \in f^{-1}(\mathscr{W})$, а так как мы предположили, что множество $f^{-1}(\mathscr{W})$ — открыто в $X$, то согласно [](#open_via_open), найдётся такое открытое множество $\mathscr{U}$ в $X$, что
$$
x \in \mathscr{U} \subseteq f^{-1}(\mathscr{W}).
$$

Так как $\mathscr{U} \subseteq f^{-1}(\mathscr{W})$, то согласно [](#good_for_maps), имеем $f(\mathscr{U}) \subseteq f(f^{-1}(\mathscr{W}))$. Наконец, согласно [](#good_for_preimage), $f(f^{-1}(\mathscr{W})) \subseteq \mathscr{W}$.

Итак, мы получили, что для любой точки $y\in Y$ и любого открытого множества $\mathscr{W}$ в $Y$ мы нашли такое открытое множество $\mathscr{U}$ в $X$, что 
$$
f(\mathscr{U}) \subseteq f(f^{-1}(\mathscr{W})) \subseteq \mathscr{W},
$$
т.е. $f(\mathscr{U}) \subseteq \mathscr{W}$, но согласно [](#def_of_cont_on_sets_on_R), это и означает непрерывность в точке $x$, а так как $x$ — произвольная точка, то это означает непрерывность на всём $X$.
:::

:::{warning}
Следует заметить, что образ открытого множества при непрерывном отображении, вообще говоря, **не будет** открытым множеством.
:::

:::{prf:example}
Вернёмся к [](#x^2_is_continous), $f:\mathbb{R} \to \mathbb{R}$, $f(x) = x^2$. Мы показали, что $f$ — непрерывная функция. Если мы рассмотрим теперь открытый интервал $(-1,1)$, то его образом при $f$ будет множество $[0,1)$, которое не открыто в $\mathbb{R}$ (см. Пример [](#(a,b)c(open))).
:::

:::{prf:theorem}
:name: comp_of_continous
Пусть $X,Y,Z \subseteq \mathbb{R}$ — непустые подмножества  и пусть $f:X \to Y$, $g:Y \to Z$ — функции. Если $f$ непрерывная в точке $x_0$ и $g$ непрерывная в точке $f(x_0)$, то функция $h = g \circ f$ непрерывная в точке $x_0.$ Если $f$ непрерывна на всём $X$ и $g$ непрерывная на всём $Y$, то $h$ непрерывная на всём $X.$
:::
:::{prf:proof}
:class: dropdown
:nonumber:
Второе утверждение, очевидно, следует из первого. Пусть $\mathscr{U}''$ — окрестность точки $h(x_0) =  g(f(x_0))$. Тогда из предположения о непрерывности и Теоремы [](#preimage_of_open) следует, что $\mathscr{U}':=g^{-1}(\mathscr{U}'')$ — открытое множество в $E'$, содержащее точку $f(x_0)$. Далее, так как $f$ непрерывно, то по [](#cap_of_intervals) прообраз $\mathscr{U}:=f^{-1}(\mathscr{U}')$ — открытое множество, содержащее точку $x_0$. Таким образом, $h^{-1}(\mathscr{U}'') = \mathscr{U}$ открытое, тогда по [](#preimage_of_open) $h$ непрерывно в точке $x_0$, что и завершает доказательство. 
:::


:::{prf:corollary}
:name: restriction
Если $f$ — отображение метрического пространства $E$ в метрическое пространство $E'$, непрерывное в точке $x_0$, и $A \subseteq E$, $A \ni x_0$, то сужение $f|_A:=f \circ \mathrm{in}_A$ также непрерывно в $x_0,$ где $\mathrm{in}_A:A \hookrightarrow E$ — вложение.
:::
:::{prf:proof}
:class: dropdown
:nonumber:
На самом деле, $f$ непрерывно в $x_0$ по условию, а $\mathrm{in}_A$ непрерывно в любой точке $a \in A$, тогда из предыдущей теоремы и следует утверждение.
:::

[^hash49-1]: см. Ж. Дьедонне "Основы современного анализа", стр. 57, §11