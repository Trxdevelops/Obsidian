---
tags: [sistemas-distribuidos]
fecha: 2026-09-21
asignatura: Sistemas Distribuidos
---

# Grid Computing

Integra múltiples recursos de diferentes organizaciones para resolver tareas complejas de alto coste computacional. Orientado a grandes volúmenes de cómputo y datos, y a la colaboración entre distintas organizaciones.

- **Gran capacidad de procesamiento**: combina la potencia de muchos nodos distribuidos geográficamente.
- **Uso de recursos distribuidos**: los nodos pertenecen a organizaciones distintas y se comparten de forma coordinada.
- **Escalabilidad y tolerancia a fallos**: al estar tan distribuido, la caída de un nodo apenas afecta al conjunto.
- **Middleware de gestión de recursos**: software especializado (como Globus) abstrae la heterogeneidad y coordina el acceso a los recursos del grid.

> [!note] Añadido
> El Grid Computing puede entenderse como una fusión entre [[Cluster Computing]] e [[Internet Computing]]: toma el procesamiento paralelo de alto rendimiento del Cluster y lo extiende entre organizaciones distintas a través de la red, como hace Internet Computing.

## Limitaciones

- **Heterogeneidad de recursos y redes**: los nodos son de distintas organizaciones, con hardware, SO y configuraciones diferentes.
- **Seguridad, autenticación y autorización**: gestionar identidades y permisos entre dominios distintos es complejo.
- **Coordinación entre distintos dominios administrativos**: cada organización tiene sus propias políticas, lo que dificulta la cooperación.
- **Dependencia de middleware**: se necesita software especializado para abstraer toda esa heterogeneidad.
- **Latencia y fiabilidad de la red**: al estar los nodos geográficamente dispersos, la red es un cuello de botella frecuente.
