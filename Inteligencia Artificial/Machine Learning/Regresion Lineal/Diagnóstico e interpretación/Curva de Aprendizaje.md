---
tags: [ia, regresion-lineal, diagnostico, practica]
asignatura: Inteligencia Artificial
tema: Tema 4
---

# La curva de aprendizaje: ¿cuántos datos necesitamos?

Parte de [[Regresion Lineal]].

Curva de aprendizaje en una dimensión: MSE frente al número de muestras de entrenamiento.

- $\mathbb{E}[\text{out-of-sample}]$: empieza muy alto con 2-3 muestras y baja rápido hasta acercarse por arriba a la varianza del ruido.
- $\mathbb{E}[\text{in-sample}]$: empieza en 0 y sube hasta acercarse por abajo a la varianza del ruido.
- La **varianza del ruido** es la asíntota que separa ambas curvas.

## Ajustar con muy pocas muestras

> [!warning] Con dos muestras
> La recta ajustada puede ir en dirección **contraria** a la verdadera. Con cuatro ya apunta bien, aunque con la pendiente corta.

## Sesión práctica: la curva de aprendizaje
Calcular una curva de aprendizaje empírica para una regresión lineal.

1. **Población**: crear un dataset sintético con población «infinita» (`n_rows ≈ 30.000`) donde $y = (\beta_1 x_1 + \beta_0) + \varepsilon$, con $\varepsilon \sim N(0, \sigma^2)$.
2. **Bucle**: para `n_samples ∈ [2, …, 20]`: extraer $n$ muestras al azar, ajustar una recta por OLS ($\hat{y} = \beta_1 x_1 + \beta_0$), guardar el MSE dentro de la muestra junto con $\beta_1$ y $\beta_0$, aplicar el modelo a toda la población y guardar el MSE fuera de muestra. Repetir 30.000 veces.
3. **Análisis**: dibujar la curva de aprendizaje, comparar $\mathbb{E}[\beta_1]$ y $\mathbb{E}[\beta_0]$ con los valores «verdaderos», y calcular $\text{Var}(\beta_1)$ y $\text{Var}(\beta_0)$ para comparar sus tamaños relativos.

Relacionado: [[Minimos Cuadrados Ordinarios]] · [[Hipotesis de la Regresion Lineal]]
