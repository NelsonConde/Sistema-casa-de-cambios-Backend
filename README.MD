# Sistema para Casa de Cambios

## Descripción

Este repositorio contiene el desarrollo de un sistema backend para la gestión operativa de una casa de cambios, construido con **Spring Boot**.

El sistema tiene como objetivo administrar operaciones relacionadas con compra y venta de divisas, clientes, tasas de cambio, usuarios internos, reportes y control de transacciones.

Actualmente el proyecto se encuentra en etapa inicial de planificación y construcción.

## Objetivo del proyecto

Desarrollar una API backend que permita:

* Registrar operaciones de compra y venta de divisas.
* Gestionar clientes.
* Administrar tasas de cambio.
* Controlar usuarios y roles del sistema.
* Consultar historial de transacciones.
* Generar reportes operativos.
* Mantener trazabilidad de las operaciones realizadas.

## Tecnologías previstas

* Java
* Spring Boot
* Spring Web
* Spring Data JPA
* Spring Security
* PostgreSQL o MySQL
* Maven
* Lombok
* JWT para autenticación
* Swagger/OpenAPI para documentación de la API

## Módulos principales previstos

### 1. Autenticación y usuarios

Gestión de usuarios internos del sistema, autenticación, autorización y control de roles.

Roles previstos:

* Administrador
* Cajero
* Supervisor
* Auditor

### 2. Clientes

Registro y administración de clientes que realizan operaciones de cambio.

Información prevista:

* Nombre completo
* Documento de identidad
* Nacionalidad
* Teléfono
* Correo electrónico
* Dirección
* Estado del cliente

### 3. Divisas

Administración de monedas disponibles para operar.

Ejemplos:

* USD
* EUR
* GBP
* COP
* MXN

### 4. Tasas de cambio

Gestión de tasas de compra y venta por divisa.

Información prevista:

* Moneda origen
* Moneda destino
* Tasa de compra
* Tasa de venta
* Fecha de vigencia
* Usuario que registró la tasa

### 5. Operaciones de cambio

Registro de transacciones de compra y venta de divisas.

Información prevista:

* Cliente
* Tipo de operación: compra o venta
* Moneda entregada
* Moneda recibida
* Monto
* Tasa aplicada
* Total calculado
* Fecha y hora
* Usuario responsable
* Estado de la operación

### 6. Reportes

Consultas y reportes sobre:

* Operaciones por fecha
* Operaciones por usuario
* Operaciones por cliente
* Totales por divisa
* Historial de tasas de cambio

## Estructura inicial esperada del proyecto

```bash
src/
 └── main/
     ├── java/
     │   └── com/
     │       └── ejemplo/
     │           └── casacambios/
     │               ├── controller/
     │               ├── service/
     │               ├── repository/
     │               ├── entity/
     │               ├── dto/
     │               ├── config/
     │               ├── security/
     │               └── exception/
     └── resources/
         ├── application.properties
         └── db/
```

## Instalación y ejecución

Cuando el proyecto esté creado, se podrá ejecutar con los siguientes pasos:

### 1. Clonar el repositorio

```bash
git clone <url-del-repositorio>
cd <nombre-del-repositorio>
```

### 2. Configurar la base de datos

Crear una base de datos en PostgreSQL o MySQL y configurar las credenciales en el archivo:

```bash
src/main/resources/application.properties
```

Ejemplo:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/casa_cambios
spring.datasource.username=postgres
spring.datasource.password=admin
spring.jpa.hibernate.ddl-auto=update
```

### 3. Ejecutar la aplicación

```bash
mvn spring-boot:run
```

## Estado del proyecto

Proyecto en fase inicial.

Pendientes:

* Crear estructura base con Spring Boot.
* Definir modelo de datos.
* Crear entidades principales.
* Implementar autenticación.
* Desarrollar endpoints REST.
* Configurar base de datos.
* Agregar documentación con Swagger.
* Crear pruebas unitarias e integrales.

## Buenas prácticas previstas

* Arquitectura por capas.
* Uso de DTOs para entrada y salida de datos.
* Validaciones con Bean Validation.
* Manejo centralizado de excepciones.
* Seguridad basada en JWT.
* Control de roles y permisos.
* Registro de auditoría para operaciones sensibles.
* Pruebas automatizadas.

## Licencia

Este proyecto se encuentra en desarrollo. La licencia será definida posteriormente.
