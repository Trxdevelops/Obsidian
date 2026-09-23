---
tags: [ia, regresion-lineal, diagnostico]
asignatura: Inteligencia Artificial
tema: Tema 4
---

# Heterocedasticidad

Parte de [[Hipotesis de la Regresion Lineal]].

Ocurre cuando la varianza de los residuos **no es constante**, sino que depende de $x$. Al dibujar `y_true - y_pred` frente a $x$ se ve el típico embudo: los residuos se abren cada vez más a medida que crece $x$.

> [!warning] Posible «solución»
> Aplicar una transformación, por ejemplo el logaritmo o la raíz cuadrada de la variable dependiente ($y$). No es tan buena idea si hay más de una variable independiente.

Relacionado: [[Hipotesis de la Regresion Lineal]]
