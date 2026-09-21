---
tags: [sistemas-distribuidos]
fecha: 2026-09-21
asignatura: Sistemas Distribuidos
---

# Sistemas Distribuidos

Un sistema distribuido es un conjunto de computadores independientes que, comunicándose únicamente por red (paso de mensajes), se presentan al usuario como si fueran uno solo. Cada nodo funciona de forma autónoma, no hay memoria ni reloj global compartido, y los fallos pueden ser parciales: puede caer un nodo sin que el sistema entero deje de funcionar.

- **Sin memoria ni reloj global**: cada nodo funciona de forma autónoma.
- **Paso de mensajes**: única forma de comunicación entre nodos.
- **Fallos parciales**: puede caer un nodo sin que el sistema entero deje de funcionar.
- **Transparencia**: el usuario no percibe que hay múltiples máquinas detrás.

## Modelos de sistemas distribuidos

Según cómo se organizan y comunican los nodos, distinguimos varios modelos:

- [[Computación Centralizada]]
- [[Cluster Computing]]
- [[Internet Computing]]
- [[Grid Computing]]
- [[Cloud Computing]]

[[Comparativa Modelos Distribuidos]]
