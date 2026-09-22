---
tags: [sistemas-distribuidos]
fecha: 2026-09-22
asignatura: Sistemas Distribuidos
---

# Llamadas a Procedimientos Remotos

## Paso de mensajes

En los [[Sistemas distribuidos]], los procesos se comunican y se sincronizan mediante el **paso de mensajes**. Cada proceso envía mensajes a otros procesos de la red y recibe mensajes de ellos, utilizando unas funciones básicas.

Los mensajes pueden contener datos, peticiones de servicio o cualquier información necesaria para la aplicación.

> [!info] Idea clave
> El paso de mensajes permite la comunicación entre procesos en diferentes nodos. Es el mecanismo básico de comunicación en sistemas distribuidos y la base sobre la que se construyen mecanismos más avanzados, como las llamadas a procedimientos remotos (RPC).

### Send

Manda un mensaje a un nodo de la red, con los parámetros necesarios para ejecutar la petición.

```c
send(nodo_id, datos)
```

- `nodo_id`: identificador del nodo destino.
- `datos`: buffer con la información a enviar.
- Opcionalmente, se puede enviar a todos los nodos (**broadcast**).

### Receive

Recibe un mensaje emitido por otro nodo, normalmente a través de un buffer de recepción.

```c
receive(nodo_id, buffer)
```

- `nodo_id`: identificador del nodo del que se quiere recibir.
- `buffer`: memoria donde se almacena el mensaje recibido.
- Opcionalmente, se puede recibir de todos los nodos.

## Tipos de comunicación

### Según la fiabilidad

Los mensajes pueden ofrecer diferentes niveles de garantías de entrega.

- **Comunicación fiable**: garantiza que el mensaje llega a destino. Puede incluir mecanismos de retransmisión, confirmaciones (ACK) y control de errores. Es la opción más habitual.
- **Comunicación no fiable**: no garantiza que el mensaje llegue. Puede haber pérdidas, duplicados o desorden de mensajes. Se utiliza cuando la aplicación tolera estas situaciones o implementa sus propios mecanismos de control.

### Según el comportamiento de la llamada

Las funciones de envío y recepción pueden ser bloqueantes o no bloqueantes.

| | **Llamadas bloqueantes** | **Llamadas no bloqueantes** |
|---|---|---|
| **Comportamiento** | `send`/`receive` no devuelve el control hasta que el mensaje ha sido enviado (o recibido) | `send`/`receive` devuelve el control lo antes posible; el mensaje se coloca en la cola de envío |
| **Proceso llamante** | Permanece parado esperando | Continúa ejecutando trabajo útil |
| **Seguimiento** | No necesita, la llamada termina cuando acaba la operación | Se obtiene un "recibo" o identificador para consultar más tarde si ha finalizado |
| **Ventaja** | Más sencillo de programar | Permite solapar comunicación y computación, aprovechando mejor la CPU |
| **Inconveniente** | Puede desaprovechar tiempo de CPU mientras se realiza la comunicación | Más complejo de programar |
| **Cuándo usarlo** | Aplicaciones sencillas, o cuando la espera no supone un problema | Para solapar comunicación y computación; muy importante en redes lentas |

> [!warning] A tener en cuenta
> Elegir el tipo de comunicación adecuado (fiable/no fiable, bloqueante/no bloqueante) depende de los requisitos de la aplicación y del entorno de red.
