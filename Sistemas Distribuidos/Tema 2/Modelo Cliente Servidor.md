---
tags: [sistemas-distribuidos]
fecha: 2026-09-22
asignatura: Sistemas Distribuidos
---

# Modelo Cliente Servidor

Organización en la que un proceso servidor ofrece un recurso o servicio y un proceso cliente inicia la comunicación para solicitarlo (ver [[Programación en un sistema distribuido]]).

## Componentes

- **Cliente**: proceso que solicita un servicio al servidor. Proporciona una interfaz sencilla de manejar para el usuario final.

- **Interfaz de Programación (API)**: conjunto de funciones y programas que permiten la comunicación entre procesos cliente y procesos servidor. Define cómo se realizan las peticiones y qué respuestas se obtienen de ellas, facilitando el desarrollo de aplicaciones cliente-servidor.

- **Middleware**: capa de software intermedia que proporciona una visión uniforme del sistema distribuido. Incluye servicios, librerías y APIs que facilitan la comunicación y el acceso a los servicios independientemente de la plataforma.

- **Servidor**: proceso que ofrece uno o varios servicios a los clientes. Suele ser un sistema más complejo, gestiona los recursos compartidos (archivos, bases de datos, aplicaciones...) y puede atender simultáneamente a múltiples clientes.

## Tipos de procesamiento

Según dónde se realice el procesamiento, desde toda la carga en el servidor hasta toda la carga en el cliente:

| Tipo | Descripción | Carga en cliente | Carga en servidor | Ejemplo |
|---|---|---|---|---|
| **Tipo host** | Toda la carga de procesamiento se realiza en el servidor. El cliente es un terminal que solo se encarga de la entrada y salida de datos. | Mínima | Máxima | Sistemas de tiempo compartido (mainframes, terminales) |
| **Tipo servidor** | El cliente proporciona una interfaz de usuario y el servidor realiza las operaciones de procesamiento. | Interfaz | Mayor parte | Páginas web, bases de datos |
| **Cooperativo** | Tanto el cliente como el servidor realizan parte del procesamiento, repartiendo la carga de forma equilibrada. | Parte de la carga | Parte de la carga | Aplicaciones distribuidas con procesamiento compartido |
| **Basado en cliente** | La mayor parte de la carga de procesamiento se realiza en el cliente. El servidor se utiliza para tareas auxiliares (validación de datos, almacenamiento o servicios en línea). | Máxima | Mínima | Juegos en red |

## Tipos de middleware

| Tipo | Función | Ejemplos |
|---|---|---|
| **Comunicación y mensajería** | Gestiona el intercambio de mensajes entre aplicaciones y nodos, de forma fiable y escalable. | RabbitMQ, Apache Kafka, ActiveMQ, NATS |
| **Acceso a datos** | Proporciona una interfaz uniforme para acceder a datos en diferentes fuentes y sistemas. | JDBC, ODBC, Hibernate (ORM), Redis |
| **Invocación remota** | Permite llamar a funciones y procedimientos en máquinas remotas como si fueran locales. | CORBA, gRPC, Thrift, SOAP |
| **Transacciones** | Gestiona transacciones distribuidas, garantizando la consistencia de los datos. | IBM WebSphere, Oracle Tuxedo, Atomikos, Narayana |
| **Servicios de directorio** | Proporciona servicios de nombres, autenticación y descubrimiento de recursos. | OpenLDAP, Active Directory, Apache ZooKeeper |
| **Aplicaciones y contenedores** | Proporciona un entorno de ejecución para aplicaciones distribuidas, gestionando servicios comunes. | Apache Tomcat, JBoss, Spring, Docker |
