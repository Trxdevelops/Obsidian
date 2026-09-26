---
tags: [sistemas-distribuidos]
fecha: 2026-09-23
asignatura: Sistemas Distribuidos
---

# RPC

> [!info] Definición
> Un **RPC** es una capa de abstracción que permite a un programa distribuido comunicarse con otro programa/proceso mediante **llamadas a procedimientos remotos**, ocultando gran parte de la comunicación en red.

## Ventajas de usar RPC

- **Interfaz sencilla**.
- **Comunicación generada automáticamente** ([[Stubs]]).
- Permite **abstraerse del entorno distribuido**.
- Facilita la **portabilidad** entre arquitecturas.

## Representación de parámetros en RPC

Para independizar la información enviada o recibida por cliente y servidor del lenguaje usado, se necesita un **formato común** para poder establecer un intercambio de información exitoso entre cliente y servidor. De nuevo, los [[Stubs]] se encargan de esto.

## Enlaces

- [[Sistemas distribuidos]]
- [[Modelo Cliente Servidor]]
