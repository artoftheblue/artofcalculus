# Отображения

Пусть $X,Y$ — два множества, $R(x,y)$ — отношение между $x \in X$, $y \in Y$. **График** $\Gamma(R)$ отношения $R$ определяется следующим образом
$$
X \times Y \supseteq \Gamma(R) : = \{(x,y) \, :\, (x,y) \in R\}.
$$

Пусть $X,Y$ — два множества, $R(x,y)$ — отношение между $x \in X$, $y \in Y$. Говорят, что $R$ **функционально по $y$**, если для **каждого** $x\in X$ существует **один и только один** такой элемент $y\in Y$, что $R(x,y)$ истинно.

График $F$ такого отношения называется **функциональным графиком** в $X \times Y$. Его можно также охарактеризовать следующим образом: для каждого $x \in X$ существует один и только один такой элемент $y \in Y$, что $(x,y) \in R$; этот элемент называется **значением** $F$ в $x$ и обозначается символом $F(x)$.

Функциональный график в $X \times Y$ называется также **отображением $X$ в $Y$** или **функцией, определённой в $X$ и принимающей значения в $Y.$**

Мы также будем записывать такое отображение в виде $F:X \to Y$, понимая под этим, что каждому $x \in X$ ставится в соответствие ровно один $y = F(x)\in Y$. Множество $F(X) \subseteq Y$, определённое как $\{F(x), \, x \in X\}$, называется образом отображения $F$ и иногда будет обозначаться как $\mathrm{Im}(F).$ Далее, множество $F^{-1}(Y) \subseteq X$, определённое как
$$
F^{-1}(Y):= \{x \in X\, :\, F(x) \in Y\},
$$
называется **прообразом** отображения $F.$