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


