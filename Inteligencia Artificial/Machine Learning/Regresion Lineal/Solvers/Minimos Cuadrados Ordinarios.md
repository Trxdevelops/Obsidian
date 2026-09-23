---
tags: [ia, regresion-lineal, solver]
asignatura: Inteligencia Artificial
tema: Tema 4
---

# Mínimos cuadrados ordinarios (OLS)

Parte de [[Regresion Lineal]]. Solver para el caso simple.

$$\hat{y} = \beta_1 x + \beta_0$$

$$\beta_1 = \frac{\sum\left((x_i - \bar{x})(y_i - \bar{y})\right)}{\sum\left((x_i - \bar{x})^2\right)}$$

$$\beta_0 = \bar{y} - \beta_1 \bar{x}$$

Donde:

- $x_i$, $y_i$: valores de la observación $i$
- $\bar{x}$, $\bar{y}$: medias de $x$ e $y$
- $\beta_1$: pendiente ajustada
- $\beta_0$: término independiente ajustado

> [!info] Historia
> La técnica de los mínimos cuadrados fue inventada por Carl Friedrich Gauss y Adrien-Marie Legendre en torno a 1802-1809.

## Sesión práctica
**ML_OLS_numpy** (notebook en Kaggle). Objetivo: convertir las ecuaciones de los mínimos cuadrados ordinarios en código Python e inspeccionar visualmente el resultado.

Relacionado: [[Ecuacion Normal]] · [[Regresion Lineal en Python]]
