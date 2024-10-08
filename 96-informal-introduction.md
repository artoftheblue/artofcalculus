# Неформальное введение

Понятие определённого интеграла восходит ещё к Архимеду. Мы рассмотрим неформальное введение, где объясним суть проблемы.

Пусть дана функция $f: \mathbb{R} \to \mathbb{R}^1$, которая непрерывна на отрезке $[a,b]$. Будем писать $y  = f(x)$ и будем считать, что функция на этом отрезке принимает только положительные значения. Рассмотрим фигуру $ABCD$ (см. рис.[](#int_a_b1)), ограниченную кривой $y=f(x)$, двумя ординатами $x = a$, $x =b$ и отрезком оси $Ox.$ Подобные фигуры называются **криволинейными трапециями**.

Рассмотрим теперь задачу о нахождении площади плоской криволинейной трапеции $ABCD$ (см. рис.[](#int_a_b1))

```{figure} ./int_a_b1.jpg
:label: int_a_b1
Площадь фигуры $ABCD$ примерно равна сумме площадей разноцветных прямоугольников, и чем их больше, тем точнее будет ответ.
```

Разделим основание $AB$ нашей фигуры произвольным образом на части и проведём ординаты, соответствующие точкам деления; тогда криволинейная трапеция разобьётся на ряд полосок. 

Заменим теперь приближённо каждую полоску некоторым прямоугольником, основание которого то же, что и у полоски, а высота совпадает с одной из ординат полоски. Таким образом, криволинейная фигура заменится некоторой ступенчатой фигурой, составленной из отдельных прямоугольников. 

Обозначим абсциссы точек деления через
$$
x_0 : = a < x_1 < x_2 < \cdots < x_i < x_{i+1} < \cdots < x_n =:b.
$$

Будем нумеровать прямоугольники числами $0,1,2,\ldots, n-1$ и пусть $S_i$ — площадь $i$-го прямоугольника. Ясно, что $S_i = y_i \Delta x_i$, где $\Delta x_i: = x_{i+1} - x_i.$

Тогда приближённое значение площади криволинейной трапеции $S_{ABCD}$ равно
$$
S_{ABCD} \approx \sum_{k = 0}^{n-1} y_k \Delta x_k.
$$

Тогда можно предположить, что при убывании всех $\Delta x_i$ к нулю мы будем получать более точное значение, т.е. другими словами мы хотим сказать, что точное значение площади это следующий предел
$$
S_{ABCD} = \lim_{\substack{\Delta x_1 \to 0 \\ \vdots \\ \Delta x_{n-1} \to 0}} \sum_{k = 0}^{n-1} y_k \Delta x_k.
$$

Для обозначения предела такой суммы вида и был Лейбницем введён символ интеграла, т.е.
$$
\int_a^b f(x) \mathrm{d}x : = \lim_{\substack{\Delta x_1 \to 0 \\ \vdots \\ \Delta x_{n-1} \to 0}} \sum_{k = 0}^{n-1} y_k \Delta x_k.
$$