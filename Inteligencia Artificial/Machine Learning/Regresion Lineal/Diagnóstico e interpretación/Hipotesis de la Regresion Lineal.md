---
tags: [ia, regresion-lineal, diagnostico]
asignatura: Inteligencia Artificial
tema: Tema 4
---

# Las cuatro hipótesis de una buena regresión lineal

Parte de [[Regresion Lineal]].

## 1. Linealidad
La primera y la más importante: la regresión lineal funciona mejor cuando la relación entre la variable independiente ($x$) y la dependiente ($y$) es **realmente lineal**.

> [!warning] Si no lo es
> Con datos claramente curvados (p. ej. una parábola), el ajuste sale plano: $\beta_1 = 0$. El modelo no captura nada.

## Las otras tres: sobre los residuos
Para obtener resultados fiables de los coeficientes y de los intervalos de confianza, los residuos (los errores) deben ser:

### 2. i.i.d.
Independientes e idénticamente distribuidos: cada error es independiente de los demás (no hay autocorrelación).

### 3. Gaussianos
Pertenecen a una distribución normal:

$$\forall i \in n, \quad \varepsilon_i \sim N(0, \sigma^2)$$

Donde:

- $\varepsilon_i$: residuo de la observación $i$
- $\sigma^2$: varianza del ruido

### 4. Homocedásticos
Los errores tienen varianza constante: la varianza no depende de $x$.

Ver [[Heterocedasticidad]] para el caso en que esto falla.

## Inspección visual
Para el EDA podemos usar `seaborn.lmplot`, que muestra el intervalo de confianza del ajuste:

```python
sns.lmplot(x=X, y=y, data=data, ci=95)
```

Relacionado: [[Modelo de Regresion Lineal]] · [[Explicabilidad de los Coeficientes]]
