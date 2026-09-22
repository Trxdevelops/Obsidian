---
tags: [sistemas-distribuidos]
fecha: 2026-09-22
asignatura: Sistemas Distribuidos
---

# Programación en un sistema distribuido

Programar para un sistema distribuido cambia respecto a la programación en una sola máquina: los procesos se ejecutan en nodos independientes y deben coordinarse explícitamente (ver [[Sistemas distribuidos]]).

## Cambios notables

- **Sin acceso directo a memoria remota**: los procesos no pueden acceder directamente a la memoria de otro nodo, la comunicación e intercambio de información ha de realizarse a través de la red.
- **Roles diferenciados**: los procesos distribuidos suelen asumir distintos roles dentro del sistema. Dos organizaciones habituales son **maestro-esclavo**, donde un proceso maestro reparte el trabajo entre varios esclavos que le devuelven el resultado, y **cliente-servidor**, donde el servidor ofrece un recurso o servicio y el cliente inicia la comunicación para solicitarlo (ver [[Modelo Cliente Servidor]]).
- **Sincronización**: cuando se comparten recursos, los sistemas deben sincronizarse para evitar conflictos.
