---
tags: [sistemas-distribuidos]
fecha: 2026-09-23
asignatura: Sistemas Distribuidos
---

# Stubs

> [!info] Definición
> Un **stub** es un módulo de código generado automáticamente que actúa como **intermediario entre la aplicación y la comunicación por red** en una RPC, abstrayendo y/o ocultando el paso de mensajes al programador, haciendo que las llamadas remotas aparenten ser locales.

## Tipos de stub

- **Stub cliente**: se encarga de convertir la llamada en un mensaje y enviarlo al servidor.
- **Stub servidor**: recibe el mensaje, reconstruye los parámetros y ejecuta el procedimiento real.
