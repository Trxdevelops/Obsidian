---
tags: [sistemas-distribuidos]
fecha: 2026-09-22
asignatura: Sistemas Distribuidos
---

# Memoria en un sistema distribuido

Un sistema de memoria distribuida se compone de un conjunto de nodos independientes, conectados entre sí por una red de comunicaciones. Cada nodo tiene su propia memoria local: no existe memoria compartida, por lo que los datos se intercambian mediante paso de mensajes (ver [[Sistemas distribuidos]]).

## Aportes del DDP

- **Tolerancia a fallos**: si un nodo falla, una unidad replicada puede asumir su responsabilidad.
- **Compartición de recursos**: el hardware y software más caro puede compartirse entre usuarios, y las bases de datos pueden mantenerse distribuidas.
- **Escalabilidad incremental**: es posible añadir nuevos nodos sin reemplazar los ya existentes, lo que facilita adaptar el sistema a mayores cargas de trabajo.
- **Paralelismo**: permite resolver problemas más grandes dividiéndolos en tareas pequeñas repartidas entre nodos.
