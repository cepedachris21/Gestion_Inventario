
# Gestion de Inventario - Chris Cepeda

Preuba de Programacion avanzada, sistema de gestion de inventario.

# 📦- Sistema de Inventario

[![.NET 8](https://img.shields.io/badge/.NET-8.0-blueviolet?logo=dotnet)](https://dotnet.microsoft.com/)
[![Razor Pages](https://img.shields.io/badge/Razor%20Pages-ASP.NET%20Core-blue?logo=razor)](https://learn.microsoft.com/aspnet/core/razor-pages)
[![SQL Server](https://img.shields.io/badge/SQL%20Server-2017%2B-red?logo=microsoftsqlserver)](https://www.microsoft.com/sql-server)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **MyApp** es una aplicación web moderna para la gestión de inventario, préstamos y auditoría, desarrollada con una arquitectura N-Capas en .NET 8 y Razor Pages. Permite controlar artículos, usuarios, roles y reportes avanzados en PDF y Excel.

---

## 📑 Tabla de Contenidos

- [Características](#características)
- [Tecnologías](#tecnologías)
- [Arquitectura](#arquitectura)
- [Patrones de Diseño](#patrones-de-diseño)
- [Despliegue](#despliegue)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Capturas de Pantalla](#capturas-de-pantalla)

---

## ✨ Características

- **Gestión de Usuarios y Roles**  
  Autenticación segura, roles de Administrador y Operador, activación/desactivación de cuentas.

- **Inventario de Artículos**  
  CRUD completo, categorías, estados, ubicación y búsqueda avanzada.

- **Préstamos de Artículos**  
  Flujo de solicitud, aprobación, entrega, devolución y rechazo.

- **Auditoría y Seguridad**  
  Registro de acciones, cambios, login, IP y usuario. Hash de contraseñas con BCrypt.

- **Panel de Control (Dashboard)**  
  Estadísticas clave: artículos, préstamos activos, pendientes y vencidos.

- **Reportes Profesionales**  
  - PDF: Listado de artículos, estado general del inventario.
  - Excel: Historial de préstamos, actividad de usuarios.

- **UI Moderna y Responsive**  
  Basada en Bootstrap 5, con experiencia de usuario mejorada y notificaciones.

---

## 🛠️ Tecnologías

- **Backend:** .NET 8, C#
- **Web:** ASP.NET Core Razor Pages
- **ORM:** Entity Framework Core 8
- **Base de Datos:** SQL Server 2017+
- **Logging:** Serilog
- **PDF:** QuestPDF
- **Excel:** ClosedXML
- **Seguridad:** BCrypt.Net-Next, Anti-CSRF
- **Frontend:** HTML, CSS, Bootstrap 5, JavaScript

---

## 🏗️ Arquitectura

El proyecto sigue una **arquitectura N-Capas** para máxima mantenibilidad y escalabilidad:

- **Entities:** Modelos de dominio (User, Item, Loan, etc.)
- **DataAccess:** Repositorios, Unit of Work, contexto EF Core, configuraciones.
- **Business:** Servicios de negocio, DTOs, lógica de validación y orquestación.
- **Presentation:** Razor Pages, controladores, modelos de vista y recursos estáticos.


---

## 🧩 Patrones de Diseño

- **Repository Pattern:**  
  Abstracción de acceso a datos, desacoplando la lógica de negocio de EF Core.

- **Unit of Work Pattern:**  
  Gestión de transacciones atómicas y consistencia de datos.

- **DTOs y ViewModels:**  
  Separación de modelos de dominio y presentación.

---

## 🚀 Despliegue

### 1. Prerrequisitos

- [.NET 8 SDK](https://dotnet.microsoft.com/download)
- SQL Server 2017+ (Express o superior)
- Visual Studio 2022 (recomendado) o VS Code

### 2. Clonar el Repositorio

(* Repositorio actual *)

### 3. Configurar la Cadena de Conexión

Edita `MyApp.Presentation/appsettings.json`:



### 4. Restaurar y Migrar la Base de Datos

dotnet restore cd MyApp.Presentation dotnet ef database update

### 5. Ejecutar la Aplicación

dotnet run
