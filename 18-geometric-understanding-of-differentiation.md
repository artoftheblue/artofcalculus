# Геометрический смысл дифференциала функции

Мы начнём с рассмотрения функции от одной переменной. 

:::{prf:theorem}
Пусть функция $f(x)$ дифференцируема в точке $x_1$, а прямая $\ell$, проходящая через точки $(x_1,y_1)$, $(x_2,y_2)$, где $y_1 = f(x_1)$, $y_2 = f(x_2)$, задаётся уравнением $y = k(x_2) (x - x_1 ) + y_1$. Тогда
$$
\lim_{x_2 \to x_1} k(x_2) = f'(x_1).
$$
:::

```{figure} ./images/line_and_f'.jpg
Прямая $\ell$, проходящая через точки $(x_1,y_1)$, $(x_2,y_2)$, где $y_1 = f(x_1)$, $y_2 = f(x_2)$
```

:::{prf:proof}
:class: dropdown
:nonumber:
Рассматриваемая прямая задаётся уравнением 
$$
y = \frac{f(x_2) - f(x_1)}{x_2 - x_1}(x-x_1) +y_1,
$$
поэтому
$$
k(x_2)  = \frac{f(x_2) - f(x_1)}{x_2 - x_1}.
$$

Тогда из определения производной следует, что
$$
\lim_{x_2 \to x_1}k(x_2) = f'(x_1).
$$
:::

:::{prf:definition}
Прямую $y = f'(x_0)(x-x_0) + f(x_0)$ называют **касательной** к графику $y = f(x)$ в точке $(x_0, f(x_0)).$
:::

```{figure} ./images/tan_and_f.jpg

Таким образом, если функция $f(x)$ дифференцируема в точке $x_0$, то её можно приблизить линейной функцией $f'(x_0)(x-x_0) +f(x_0)$, при этом $o(|h|)$ показывает, насколько далеко это приближение.
```