# 🚒 Gestión de Emergencias

Sistema desarrollado en Java con Swing, utilizando el patrón arquitectónico MVC (Modelo - Vista - Controlador) y una base de datos MySQL.  El sistema permite gestionar información relacionada con emergencias, personal, jerarquías, vehículos y tipos de emergencia, manteniendo la información persistida en una base de datos.

## ✨ Funcionalidades

- Registro, edición y eliminación de emergencias.
- Gestión de personal y sus jerarquías.
- Gestión de vehículos, patentes y estados.
- Gestión de tipos de emergencia.
- Asociación de personal y vehículos a cada emergencia.
- Visualización de los recursos asignados a cada intervención.
- Validaciones de datos y formato de patentes.
- Interfaz gráfica con Java Swing.

## 🛠️ Tecnologías

- Java 17
- Java Swing
- MySQL
- JDBC / MySQL Connector
- MVC (Modelo–Vista–Controlador)
- JDatePicker
- IntelliJ IDEA

## 🏗️ Arquitectura

```text
src/
├── modelo/          # Entidades, DAO y conexión a MySQL
├── vista/           # Interfaces gráficas Swing
├── controlador/     # Lógica y eventos de la aplicación
└── util/            # Validaciones y utilidades
```

## 🗃️ Modelo de datos

Las principales entidades utilizadas son:

- `emergencia`
- `tipo_emergencia`
- `personal`
- `jerarquia`
- `vehiculo`
- `emergencia_personal`
- `emergencia_vehiculo`

Las tablas intermedias permiten representar la relación entre una emergencia y los recursos que participaron en ella.

## ⚙️ Configuración

1. Tener instalado Java 17.
2. Tener instalado y ejecutándose MySQL.
3. Crear la base de datos `gestion_emergencias` y sus tablas.
4. Configurar las credenciales en `src/modelo/Conexion.java`.
5. Agregar los JAR de MySQL Connector/J y JDatePicker a las dependencias del módulo en IntelliJ IDEA.
6. Ejecutar la clase `Main`, ubicada en `src/Main.java`.

## 🎯 Objetivo del proyecto

Proyecto académico orientado a aplicar conceptos de programación orientada a objetos, acceso a datos, JDBC, bases de datos relacionales, patrón MVC e interfaces gráficas en un sistema de gestión basado en un caso real.

## 👨‍💻 Autor

**Franco Bazán**

Proyecto desarrollado como parte de la formación en Sistemas de Información.
