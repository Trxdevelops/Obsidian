---
tags: [ia, regresion-lineal, extensiones]
asignatura: Inteligencia Artificial
tema: Tema 4
---

# Regresión polinómica

Parte de [[Regresion Lineal]].

Casi nunca (…en realidad, nunca) la relación entre $x$ e $y$ es una línea recta. Podemos añadir términos de potencia:

$$\hat{y}(X) = \beta_2 x^2 + \beta_1 x + \beta_0$$

Donde:

- $x^2$: nueva feature construida a partir de $x$
- $\beta_2, \beta_1, \beta_0$: parámetros del modelo

```python
df["x_squared"] = df["x"]**2
```

> [!info] Con esta nueva feature introducimos curvatura en el modelo.

## Sigue siendo un modelo lineal
Ojo: esto sigue siendo una **función lineal en términos de $\beta$**. En el ejemplo de la frutería es como añadir una columna más (piñas = manzanas²):

| piñas | manzanas | uvas | total |
|---|---|---|---|
| 9 | 3 | 3 | 21 € |
| 25 | 5 | 2 | 20 € |
| 64 | 8 | 6 | 46 € |

> [!warning] Cuidado
> Los polinomios de grado alto tienen colas inestables: ver [[Interpolacion y Extrapolacion]].

