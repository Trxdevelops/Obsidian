---
tags: [sistemas-distribuidos]
fecha: 2026-09-21
asignatura: Sistemas Distribuidos
---

# Cluster Computing

Varios ordenadores (nodos) trabajan en paralelo como si fueran uno solo, con el objetivo de aumentar la potencia y la disponibilidad.

- **Alto rendimiento**: las tareas se dividen entre nodos y se procesan en paralelo.
- **Tolerancia a fallos**: si un nodo falla, los demás pueden asumir su carga.
- **Escalabilidad horizontal**: se añaden más nodos en lugar de sustituir la máquina, a diferencia de la computación centralizada.

## Tipos

- **Clusters de alto rendimiento**: optimizados para maximizar la velocidad de procesamiento en tareas complejas.
- **Clusters de alta disponibilidad**: priorizan que el sistema no caiga, con redundancia ante fallos.
- **Clusters de balanceo de carga**: distribuyen las peticiones entre nodos para evitar cuellos de botella.

## Limitaciones

- **Coste y mantenimiento**: mantener los nodos operativos y sincronizados tiene un coste elevado.
- **Escalabilidad limitada ante demanda creciente**: añadir nodos no siempre es inmediato ni sencillo.
- **Fronteras administrativas**: compartir recursos o datos entre distintas organizaciones es complejo.

> [!note] Origen del Cycle Scavenging
> Los entornos de Cluster fueron el primer contexto en el que se aplicó el [[Cycle Scavenging]], técnica que luego sentaría las bases del Grid y el Cloud Computing.
