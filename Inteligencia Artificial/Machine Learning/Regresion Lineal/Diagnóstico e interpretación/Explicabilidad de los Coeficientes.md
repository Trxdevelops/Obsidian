---
tags: [ia, regresion-lineal, interpretacion]
asignatura: Inteligencia Artificial
tema: Tema 4
---

# Explicabilidad e interpretación de los coeficientes

Parte de [[Regresion Lineal]].

Los $\beta_1$, es decir, las inclinaciones, aportan información valiosa sobre la **importancia relativa (el peso) de cada feature**.

> [!info] Ejemplo
> Si una feature tiene $\beta_1 = 0$, entonces esa feature no forma parte del modelo y no influye en absoluto a la hora de predecir $\hat{y}$.

> [!example] La gran ventaja
> Frente a modelos más potentes: el modelo se puede leer y explicar a una persona que no sea técnica.

## Dos cautelas al interpretar los coeficientes

### 1. Escala
Para interpretar correctamente la importancia relativa de los coeficientes ($\beta$) es imprescindible que **todas las features estén en la misma escala**.

### 2. Incertidumbre
Se pueden calcular los intervalos de confianza (CI) de los coeficientes, por ejemplo con `statsmodels.regression.linear_model.OLS` y `conf_int`.

> [!warning] Un coeficiente sin intervalo de confianza es un número sin contexto: no sabes si es sólido o si es ruido.

