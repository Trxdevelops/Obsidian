---
tags: [sistemas-distribuidos]
fecha: 2026-09-21
asignatura: Sistemas Distribuidos
---

# Cloud Computing

Los recursos (cómputo, almacenamiento, red, etc.) se ofrecen como servicios a través de Internet, gestionados por un proveedor externo.

- **Elasticidad y escalabilidad**: los recursos se ajustan dinámicamente según la demanda.
- **Pago por uso**: se paga solo por lo que se consume, no por poseer la infraestructura.
- **Autoservicio bajo demanda**: el usuario solicita recursos cuando los necesita, sin intervención del proveedor.
- **Virtualización y automatización**: abstraen el hardware y permiten aprovisionar recursos dinámicamente.
- **Alta disponibilidad**: los proveedores garantizan uptime (tiempo que el sistema permanece operativo y accesible) mediante redundancia y replicación.
- **Sin gestión de infraestructura**: el usuario no administra el hardware subyacente.

## Por qué nació el Cloud

Antes del Cloud, los servidores se dimensionaban para soportar los picos de demanda, lo que los dejaba infrautilizados el resto del tiempo. Esto generaba altos costes de adquisición, mantenimiento y energía, y poca capacidad de respuesta ante aumentos de carga.

La solución fue combinar **virtualización y automatización** para que la infraestructura pudiera adaptarse dinámicamente a la demanda, pagando solo por lo que se usa.

> [!note] Añadido
> El Cloud no inventa la computación distribuida: convierte los recursos en servicios elásticos, automatizados y consumibles bajo demanda. Sus bases las sentaron [[Cycle Scavenging]], [[Cluster Computing]], [[Internet Computing]] y [[Grid Computing]].

## Hitos históricos

| Año | Hito |
|-----|------|
| 2006 | Amazon presenta AWS (Amazon Web Services) |
| 2008 | Eucalyptus, primera plataforma cloud open source |
| Poco después | Google App Engine, Windows Azure, OpenNebula, OpenStack |
