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

