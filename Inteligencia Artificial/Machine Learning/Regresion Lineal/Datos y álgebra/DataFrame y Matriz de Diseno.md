---
tags: [ia, regresion-lineal, algebra, datos]
asignatura: Inteligencia Artificial
tema: Tema 4
---

# El DataFrame y la matriz de diseño

Parte de [[Regresion Lineal]].

## Dónde viven los datos
Con datos tabulares, los datos se almacenan normalmente en un **DataFrame (df)**: una columna por feature (`feature_1`, `feature_2`, …) más la columna `target`.

> [!note] En deep learning
> Es más habitual almacenarlos en arrays de numpy o en tensores.

## El DataFrame como sistema de ecuaciones
Podemos tratar el DataFrame como un sistema de ecuaciones lineales en el que los valores $x_{mn}$ son los coeficientes:

$$
\begin{aligned}
\beta_1 x_{0,1} + \beta_0 \cdot 1 &= y_0 \\
\beta_1 x_{1,1} + \beta_0 \cdot 1 &= y_1 \\
\beta_1 x_{2,1} + \beta_0 \cdot 1 &= y_2
\end{aligned}
$$

Donde:

- $x_{i,1}$: valor de la feature 1 en la fila $i$
- $y_i$: target de la fila $i$
- la columna de unos acompaña siempre a $\beta_0$

Queremos hallar los $\beta_0$ y $\beta_1$ asociados a cada columna. La columna de constantes se puede crear con `statsmodels.add_constant`.

## Escrito en forma matricial

$$
\mathbf{X} = \begin{bmatrix} x_0 & 1 \\ x_1 & 1 \\ \vdots & \vdots \\ x_m & 1 \end{bmatrix}, \quad
\beta = \begin{bmatrix} \beta_1 \\ \beta_0 \end{bmatrix}, \quad
\mathbf{y} = \begin{bmatrix} y_0 \\ y_1 \\ \vdots \\ y_m \end{bmatrix}
$$

Donde:

- $\mathbf{X}$: **matriz de diseño** (*design matrix*); su segunda columna son los unos del término independiente
- $\beta$: vector de incógnitas (parámetros)
- $\mathbf{y}$: vector de targets
- $m$: número de filas (observaciones)

Todo el modelo se reduce a $\mathbf{X}\beta = \mathbf{y}$.