---
tags: [ia, regresion-lineal, ejemplo]
asignatura: Inteligencia Artificial
tema: Tema 4
---

# Ejemplo de la frutería

Parte de [[Regresion Lineal]]. Intuición de por qué el DataFrame es una matriz de coeficientes ampliada.

## Tickets sin comisión

| manzanas | uvas | total |
|---|---|---|
| 3 | 3 | 21 € |
| 5 | 2 | 20 € |
| 8 | 6 | 46 € |

$$y = \beta_{\text{manzana}} x_1 + \beta_{\text{uvas}} x_2$$

> [!note] Ojo al vocabulario
> Este ejemplo está sobredeterminado; sin componente de ruido bastarían dos filas. Y como hay dos variables independientes, esto ya es formalmente una [[Regresion Lineal Multiple]].

## De dónde sale $\beta_0$
Si pagamos con tarjeta y hay una comisión fija de 2 € por transacción, aparece una columna nueva que vale 1 en todas las filas (los totales pasan a 23 €, 22 € y 48 €):

$$y = \beta_{\text{manzana}} x_1 + \beta_{\text{uvas}} x_2 + \beta_0$$

> [!info] Interpretación
> Ese término constante es nuestro $\beta_0$: una columna de unos cuyo coeficiente es el mismo para todas las filas.

## Resolver el sistema (sin comisión)

$$3a + 3g = 21 \qquad 5a + 2g = 20 \qquad 8a + 6g = 46$$

Con $a$ = precio de una manzana y $g$ = precio de un racimo, cada ticket es una ecuación. Dos caminos que dan el mismo resultado:

1. **Eliminación**: dividiendo la primera entre 3 queda $a + g = 7$. Sustituyendo $g = 7 - a$ en la segunda: $5a + 14 - 2a = 20$, o sea $3a = 6$, luego $a = 2$ y $g = 5$.
2. **Ecuación normal**: $X^TX = [[98, 67], [67, 49]]$ y $X^Ty = [531, 379]$. Con $\det(X^TX) = 313$: $\beta = (1/313)\cdot[626, 1565] = [2, 5]$.

> [!info] Resultado
> Una manzana cuesta 2 € y un racimo 5 €. La tercera ecuación no se ha usado: sirve de comprobación, $8(2) + 6(5) = 46$ ✓. Sin ruido, bastaban dos filas.

Detalle del cálculo matricial: [[Ecuacion Normal]].

## Con 30 tickets y descuentos
Con 30 tickets en los que el frutero redondea y aplica descuentos, la recta se convierte en un plano y sus dos pendientes son los precios: 1,90 € la manzana y 5,17 € el racimo, frente a los 2 € y 5 € verdaderos. Los segmentos verticales entre punto y plano son los **residuos**.

> [!info] En n dimensiones
> El plano pasa a ser un hiperplano afín de $n$ dimensiones (afín porque no tiene por qué pasar por el origen).
