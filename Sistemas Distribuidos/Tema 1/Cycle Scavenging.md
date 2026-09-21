---
tags: [sistemas-distribuidos]
fecha: 2026-09-21
asignatura: Sistemas Distribuidos
---

# Cycle Scavenging

Técnica surgida en los años 70-80 en redes locales de workstations que consiste en aprovechar los ciclos de CPU ociosos de máquinas existentes para ejecutar tareas de otros usuarios o procesos, en lugar de dedicar hardware exclusivo.

- **Recursos no dedicados**: las máquinas contribuyen cuando están ociosas, no son nodos exclusivos.
- **Bajo coste**: no requiere infraestructura nueva, aprovecha lo que ya existe.
- **Distribución de trabajos**: un servidor central recoge y reparte las tareas entre las máquinas disponibles.

## Limitaciones

- **Dependencia de ciclos ociosos**: solo hay capacidad de cómputo disponible cuando las máquinas no están siendo usadas activamente.
- **Rendimiento variable**: la potencia disponible fluctúa según la actividad de los usuarios locales.
- **No apto para tareas con alta comunicación entre nodos**: la latencia de una red local no garantiza la sincronización necesaria.
- **Interferencia con el usuario local**: la carga del usuario en su propia máquina reduce o interrumpe la contribución al sistema.

Sentó las bases de dos modelos posteriores:

- [[Grid Computing]]: formalizó la idea a gran escala, agregando recursos de distintas organizaciones.
- [[Cloud Computing]]: llevó el concepto al extremo, convirtiendo esa capacidad de cómputo en un servicio gestionado y bajo demanda.
