---
tags: [sistemas-distribuidos, resumen]
fecha: 2026-09-21
asignatura: Sistemas Distribuidos
---

# Comparativa de Modelos Distribuidos

| | [[Computación Centralizada]] | [[Cluster Computing]] | [[Grid Computing]] | [[Internet Computing]] | [[Cloud Computing]] |
|---|---|---|---|---|---|
| **Nodos** | Un único nodo (mainframe) | Normalmente próximos | Geográficamente distribuidos | Geográficamente distribuidos | Geográficamente distribuidos (datacenters) |
| **Administración** | Una organización | Una organización | Varias organizaciones | Participantes/organizaciones independientes | Un proveedor externo |
| **Coordinador central** | Es el propio sistema | Habitualmente sí | Puede existir coordinación | Depende de la arquitectura | Sí (el proveedor) |
| **Hardware** | Homogéneo / mainframe | Relativamente homogéneo | Heterogéneo | Heterogéneo | Heterogéneo / virtualizado |
| **Red principal** | No aplica | Red local de alta velocidad | Internet / WAN | Internet | Internet |
| **Escala geográfica** | Local | Local / datacenter | Regional o mundial | Mundial | Mundial |
| **Objetivo** | Centralizar todo el cómputo y almacenamiento | Sumar capacidad de cómputo | Compartir recursos distribuidos | Ejecutar aplicaciones/servicios distribuidos a través de Internet | Ofrecer recursos como servicio bajo demanda |
| **Organización típica** | Mainframe / terminales | Coordinada | Federación de recursos | Cliente/Servidor, P2P, etc. | IaaS, PaaS, SaaS |
| **Ejemplos** | IBM mainframe, time-sharing | HPC, renderizado, supercomputación | Proyectos científicos distribuidos | Web, servicios online, sistemas P2P | AWS, Azure, Google Cloud |
