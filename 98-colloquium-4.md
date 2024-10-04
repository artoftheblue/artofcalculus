# Коллоквиум IV

## Вопросы по 0,5 каждый

1. Что такое [знакочередующийся ряд](#def4-1)?
2. Что такое [абсолютно сходящийся ряд](#def4-2)?
3. Что такое [безусловно сходящийся ряд](#def4-3)?
4. Пусть $f:\mathbb{R} \to \mathbb{R}$ — дифференцируемая функция, что значит [выражение](#def4-4) $\mathrm{d}f = f'\cdot \mathrm{d}x$?
5. Почему градиент [это не вектор, а ковектор](#def45) (=функционал)?
6. Что такое [линейная дифференциальная форма](#def46)?
7. Что значит, что функция $F(x)$ это [интеграл](#int1) для функции $f(x)$ на каком-то промежутке?
8. Что такое [неопределённый интеграл](#int2)?
9. Что такое [рациональная функция от одной переменной](#rational_func)?
10. Что называют [правильной](#def4101) и [простой](#def4102) дробями в поле $\mathbb{R}(x)?$
11. Что такое [разбиение промежутка](#definition-4-11) и что значит, что одно выражение [тоньше](#fiber) другого? (тонкота!)
12. Что такое [ступенчатая функция](#def412)? Как она выражается через характеристические функции?
13. Что такое [интеграл от ступенчатой функции на промежутке](#def413)?
14. Что такое [верхний и нижний интегралы](#Riemann_int) от ограниченной функции на промежутке? 
15. Что такое [интеграл Римана](#int_of_bounded) от ограниченной функции на промежутке?
16. Что такое [верхняя и нижняя сумма Римана](#def416) для ограниченной функции на промежутке? 
17. Что значит выражение [**ограниченная на промежутке функция интегрируема на нём по Риману**](#int_of_bounded)? Приведите пример не интегрируемой по Риману функции.


## Теоремы и тому подобное за 2,5 балла каждое.

1. Докажите [признак Лейбница](#Leibnitz_for_series) для знакочередующихся рядов. [Док-во.](#theorem-4-1)
2. Пусть дан ряд $(x_n)$. Если сходится ряд $(|x_n|)$, то ряд $(x_n)$ тоже сходится. [Докажите.](#theorem-4-2)
3.  Если ряд абсолютно сходится, то при любой перестановке его элементов абсолютная сходимость полученного нового ряда не нарушается и более того, его сумма остаётся прежней. [Докажите.](#theorem-4-3) 
4.   Если ряд $(x_n)$ сходится условно, (т.е. ряд $(|x_n|)$ расходится), то оба ряда $(x_n^+)$, $(x_n^-)$ расходятся, при этом $\lim_{n\to \infty }x_n^+ = \lim_{n \to \infty}x_n^- = 0.$ [Докажите.](#theorem-4-4)
5.  Пусть ряд $(x_n)$ сходится условно, тогда для любого числа $\alpha \in \mathbb{R}$, а также если $\alpha = \pm \infty$ можно так переставить элементы этого ряда, что сумма полученного таким образом ряда будет равна $\alpha.$ [Докажите.](#theorem-4-5) [**Это только для сына папы Алика!!!**]
6. Докажите, что
$$
\int \Bigl(\alpha f(x) + \beta g(x) \Bigr) \mathrm{d}x = \alpha \int f(x) \mathrm{d}x +\beta \int g(x) \mathrm{d}x,
$$
где $\alpha, \beta \in \mathbb{R}.$ [Док-во.](#theorem-4-6)
7.  Пусть $u = u(x)$, $v= v(x)$ — две функции от $x$, имеющие непрерывные производные $u'= u'(x)$, $v' = v'(x)$. Тогда имеет место формула
$$
\int u \mathrm{d}v = uv - \int v \mathrm{d}u. 
$$ [Докажите.](#theorem-4-7)

8. Каждая правильная дробь может быть представлена в виде суммы конечного числа простых дробей. [Докажите.](#theorem-4-8)
9.  Для каждого $n\ge 1$ рассмотрим форму
$$
\omega_n: = \frac{\mathrm{d}x}{(x^2 + \alpha^2)^n},
$$
тогда
$$
\int \omega_{n+1} = \frac{1}{2n\alpha^2}\cdot \frac{x}{(x^2 + \alpha^2)^n} + \frac{2n-1}{2n\alpha^2} \cdot\int \omega_n, \qquad \int \omega_1 = \frac{1}{\alpha} \cdot \arctan\left( \frac{x}{\alpha}\right) + C.
$$
[Докажите.](#theorem-4-9)
10.  Интеграл от формы $\frac{Ax + B}{(x^2 + ax + b)^n}\mathrm{d}x$ выражается через рациональные функции и функции $\ln$, $\arctan$. [Докажите.](#theorem-4-10)

11.  Пусть $I \subsetneq \mathbb{R}$ — промежуток и пусть $f:I \to \mathbb{R}$ — ступенчатая функция относительно разбиения $\lambda(I)$, тогда если имеем разбиение $\lambda'(I)$, которое тоньше, чем $\lambda(I)$, то
$$
\int_{\lambda(I)}f = \int_{\lambda'(I)}f.
$$ [Докажите.](#theorem-4-11)

12. [Докажите](#theorem-4-12) следующее

Пусть $I \subsetneq \mathbb{R}$ — промежуток и $f,g:I \to \mathbb{R}$ — две ступенчатые функции на нём.

:::{seealso} Пункты на доказательство
1. $$
\int_I( f \pm  g) =  \int_I f  \pm  \int_I g , \qquad \alpha, \beta \in \mathbb{R}.
$$
2. Если $f(x) \ge g(x)$ для всех $x \in I$, то
$$
\int_I f \ge \int_I g.
$$

3. Если $f(x) = \alpha$ для всех $x \in I$, то
$$
\int_I f = \alpha \cdot |I|.
$$
4. Если $I \subseteq J$ и если $\varphi: J \to \mathbb{R}$ функция, определённая следующим образом
$$
\varphi(x) : = \begin{cases}
f(x) & x \in I,\\
0 & x \notin I,
\end{cases}
$$
тогда $\varphi(x)$ — ступенчатая на $J$ и 
$$\int_J\varphi   = \int_I f.$$

5. Пусть $\{A,B\}$ — разбиение промежутка $I$, тогда если функции $f|_A:A \to \mathbb{R}$, $f|_B:B \to \mathbb{R}$ ступенчаты на $A$ и $B$ соответственно, то
$$
\int_I f  = \int_A f|_A  + \int_B f|_B .
$$
:::


13.   Пусть $f:I \to \mathbb{R}$ — ограниченная функция на промежутке $I \subsetneq \mathbb{R}$, числами $a,b$,**т.е.,** $a \le f(x) \le b$ для всех $x \in I$. Тогда
$$
a\cdot |I| \le \inf \int_I f  \le \sup \int_I f \le b \cdot |I|.
$$ [Докажите.](#theorem-4-13)

14. Пусть $f: I \to \mathbb{R}$ — ступенчатая функция на ограниченном промежутке $I \subsetneq \mathbb{R}$, тогда она интегрируема по Риману, и более того интеграл Римана от неё это то же самое, что и интеграл от ступенчатой функции. [Докажите.](#theorem-4-14)

15. [Докажите](#theorem-4-15) следующее.     Пусть $I \subsetneq \mathbb{R}$ — ограниченный промежуток и пусть $f,g: I \to \mathbb{R}$ — ограниченные функции на нём и при этом они интегрируемы на нём по Риману.

:::{seealso} Пункты на доказательство
1. Функция $f+g$ интегрируема на $I$ и более того
$$
\int_I (f+g) = \int_I f + \int_I g.
$$
2. Для любого $\alpha \in \mathbb{R}$, функция $\alpha\cdot f$ — интегрируема на $I$ и более того
$$
\int_I \alpha\cdot f = \alpha \cdot \int_I f.
$$
3. Функция $f-g$ интегрируема на $I$ и более того
$$
\int_I(f-g)  = \int_I f - \int_I g.
$$
4. Если $f(x) \ge 0$ для всех $x\in I$, то
$$
\int_I f \ge 0.
$$
5. Если $f(x) \ge g(x)$ для всех $x \in I$, то
$$
\int_I f \ge \int_I g.
$$
6. Если $f(x) = \alpha$ для всех $x \in I$, то
$$
\int_I f = \alpha\cdot |I|.
$$
7. Пусть $J \subsetneq \mathbb{R}$ — ограниченный промежуток, и $I \subseteq J$ и пусть $\varphi:J \to \mathbb{R}$ — функция определённая следующим образом
$$
\varphi(x): = \begin{cases}
f(x), & x\in I,\\
0, & x \notin I.
\end{cases}
$$
Тогда $\varphi$ — интегрируема на $J$ и более того
$$
\int_J \varphi = \int_I f.
$$
8. Пусть $\{A,B\}$ — разбиение $I$, тогда функции $f|_A$, $f|_B$ — интегрируемы на $A$, $B$ соответственно и более того
$$
\int_I f = \int_A f|_A + \int_B f|_B.
$$
:::

16. Докажите [первую фундаментальную теорему анализа](#first_fundamental_theorem). [Док-во.](#theorem-4-16)
17. Докажите [вторую фундаментальную теорему анализа](#second_fundamental_theorem). [Док-во.](#theorem-4-17)