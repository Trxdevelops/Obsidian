---
tags: [ia, regresion-lineal, mas-dimensiones]
asignatura: Inteligencia Artificial
tema: Tema 4
---

# Regresión lineal múltiple

Parte de [[Regresion Lineal]].

## Dos variables independientes
Con dos features la recta se ha convertido en un **plano**.

> [!info] En n dimensiones
> Pasa a ser un **hiperplano afín** de $n$ dimensiones (afín porque no tiene por qué pasar por el origen).


## Con n features

$$
\mathbf{X} = \begin{bmatrix}
x_{0n} & \cdots & x_{01} & 1 \\
x_{1n} & \cdots & x_{11} & 1 \\
\vdots & \ddots & \vdots & \vdots \\
x_{mn} & \cdots & x_{m1} & 1
\end{bmatrix}, \quad
\beta = \begin{bmatrix} \beta_n \\ \vdots \\ \beta_1 \\ \beta_0 \end{bmatrix}, \quad
\mathbf{y} = \begin{bmatrix} y_0 \\ y_1 \\ \vdots \\ y_m \end{bmatrix}
$$

Donde:

- $n$: número de features
- $m$: número de filas (observaciones)
- $x_{ij}$: valor de la feature $j$ en la fila $i$
- la última columna de unos corresponde a $\beta_0$

> [!info] Notación matricial
> Todo el modelo se reduce a $X\beta = y$.

