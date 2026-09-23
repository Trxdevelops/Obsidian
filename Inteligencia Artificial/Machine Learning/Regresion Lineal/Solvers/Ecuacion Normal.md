---
tags: [ia, regresion-lineal, solver, algebra]
asignatura: Inteligencia Artificial
tema: Tema 4
---

# La ecuación normal

Parte de [[Regresion Lineal]]. Solver basado en álgebra lineal, válido para cualquier número de features.

$$\beta = (X^T X)^{-1} X^T y$$

Donde:

- $X$: matriz de diseño (ver [[DataFrame y Matriz de Diseno]])
- $y$: vector de targets
- $\beta$: vector de parámetros
- $X^T X$: **matriz de Gram** o matriz normal

Es la solución en **forma cerrada** de la ecuación matricial $X\beta = y$.

```python
X1 = np.column_stack(( X, np.ones(len(X)) ))
betas = np.linalg.inv(X1.T @ X1) @ X1.T @ y
print("beta_n,...,beta_0", betas)
```

> [!warning] Fíjate
> En la primera línea se introduce explícitamente el término constante (la columna de unos).

## Paso a paso con el ejemplo de la frutería
Ver [[Ejemplo de la Fruteria]] para el planteamiento.

```
      [ 3  3 ]        [ 21 ]       [ a ]
X  =  [ 5  2 ]   y =  [ 20 ]   B = [ g ]
      [ 8  6 ]        [ 46 ]

X^T  = [ 3  5  8 ]      (la traspuesta: filas por columnas)
       [ 3  2  6 ]

X^T X = [ 3*3 + 5*5 + 8*8   3*3 + 5*2 + 8*6 ]   [ 98  67 ]
        [ 3*3 + 2*5 + 6*8   3*3 + 2*2 + 6*6 ] = [ 67  49 ]

X^T y = [ 3*21 + 5*20 + 8*46 ]   [ 531 ]
        [ 3*21 + 2*20 + 6*46 ] = [ 379 ]
```

> [!info] Propiedad
> $X^TX$ siempre sale cuadrada y simétrica: fíjate en que el 67 aparece dos veces. Su tamaño lo fija el número de features, no el de filas.

> [!note] Recordatorio
> La inversa de una matriz 2×2 es $[[a, b], [c, d]]^{-1} = \frac{1}{ad - bc} \cdot [[d, -b], [-c, a]]$. Se intercambian los elementos de la diagonal principal, se cambia el signo a la otra y se divide todo por el determinante.

```
det(X^T X) = 98*49 - 67*67 = 4802 - 4489 = 313

(X^T X)^-1 = (1/313) * [  49  -67 ]
                       [ -67   98 ]

B = (X^T X)^-1 * X^T y
  = (1/313) * [  49*531 - 67*379 ] = (1/313) * [  626 ] = [ 2 ]
              [ -67*531 + 98*379 ]             [ 1565 ]   [ 5 ]
```

$a = 2$ € la manzana y $g = 5$ € el racimo: el mismo resultado que por eliminación, con un procedimiento mecánico válido para cualquier número de features.

## El mismo cálculo en Python

```python
import numpy as np

# una fila por ticket: manzanas, uvas
X = np.array([[3, 3],
              [5, 2],
              [8, 6]])
y = np.array([21, 20, 46])   # total en euros

# ecuacion normal: beta = (X.T X)^-1 X.T y
beta = np.linalg.inv(X.T @ X) @ X.T @ y
print(beta)                  # [2. 5.]
```

> [!warning] En producción
> Se usa `np.linalg.lstsq(X, y, rcond=None)`: mismo resultado, pero resolviendo por descomposición QR en vez de invertir, que es numéricamente más estable.

Relacionado: [[Minimos Cuadrados Ordinarios]] · [[Regresion Lineal en Python]]
