# Programacion-Avanzada
Sistema de Gestión de Eventos Académicos

Desarrollar una aplicación web completa en ASP.NET Core MVC (.NET 10) que permita gestionar eventos académicos (conferencias, talleres,etc), usando SQL Express como motor de base de datos y Entity Framework Core (Code First) como ORM.

## Requisitos Previos

Antes de comenzar, asegúrate de tener instalado lo siguiente en tu equipo:
* [SDK de .NET](https://dotnet.microsoft.com/download) (Versión 9.0 u 10.0 ).
* [SQL Server Management Studio 22](https://www.microsoft.com/es-mx/sql-server/sql-server-downloads).
* [Visual Studio 2022](https://visualstudio.microsoft.com/es/).

---

## Instrucciones de Configuración y Despliegue.

  1. Restaurar Paquetes de NuGet:
    En *Herramientas* > *Administrador de paquetes NuGet* > *Consola*
    ingresa: dotnet restore
    ejecuta.

  2. Configurar la Cadena de Conexión (Connection String)
    En el archivo *aappsettings.json* en la raiz del proyecto.

      "ConnectionStrings": {
          "cadenaSQL": " *Nombre del servidor* \\SQLEXPRESS;Database=EventosAcadémicos;Integrated Security=True;TrustServerCertificate=True;"
        }

  3. Aplicar las Migraciones y Crear la Base de Datos
    Para generar la base de datos de manera automática con las tablas de Eventos, Participantes e Inscripciones mediante Entity Framework Code First se usa el siguiente comando.
      En *Herramientas* > *Administrador de paquetes NuGet* > *Consola*
      ingresa: Update-Database
      ejecuta.
     
  4. Ejecutar la Aplicación
     Una vez creada la base de datos, compila y levanta el servidor web local.
     
