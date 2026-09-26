---
tags: [ia, regresion-lineal, modelo]
asignatura: Inteligencia Artificial
tema: Tema 4
---

# El modelo de regresión lineal

Parte de [[Regresion Lineal]].

$$y = \beta_1 x + \beta_0 + \varepsilon, \quad \mathbb{E}[\varepsilon] = 0, \quad \text{p. ej. } \varepsilon \sim N(0, \sigma^2)$$

Donde:

- $y$: variable dependiente (real, observada)
- $\beta_1$: parámetro ajustable asociado a la feature $x$, su pendiente (peso / *weight*)
- $\beta_0$: término de intersección (sesgo / *bias*)
- $\varepsilon$: término de error o ruido, de media cero
- $\sigma^2$: varianza del ruido

Por cada «feature» $x$ hay un parámetro ajustable $\beta_1$, más un único término de intersección $\beta_0$.

> [!info] Es un modelo paramétrico
> Asumimos que la relación entre la variable dependiente y las independientes es lineal, y que el ruido procede de una distribución paramétrica (gaussiana).

