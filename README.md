Configuración y Ejecución del Proyecto Backend con Entity Framework Core y SQL Server

git clone https://github.com/CristhoferDaniel/Product-backend.git
cd Product-backend


Instalación de Dependencias
Asegúrate de tener instalado Visual Studio 2022 y los siguientes paquetes NuGet:

Entity Framework Core
Entity Framework Core Tools (para las migraciones)
Microsoft.EntityFrameworkCore.SqlServer
Estos paquetes pueden ser instalados a través de NuGet Package Manager en Visual Studio.


Configuración de la Base de Datos
SQL Server
Configuración del Connection String:

Asegúrate de reemplazar tu Connection String en appsettings.json o appsettings.Development.json:
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=nombre_servidor;Database=nombre_base_datos;Trusted_Connection=True;MultipleActiveResultSets=true"
  }
}
Reemplaza nombre_servidor y nombre_base_datos con tu configuración específica de SQL Server.

Trusted_Connection=True hara la conexion automatica con las credenciales

abre la consola de administrador de paquetes en administrador de paquetes Nuget 
escribir add-Migration Initial

guardar cambios y poner en la consola update-database
se creara la base de datos segun el modelo

ejecutar el proyecto 
![image](https://github.com/user-attachments/assets/76157a94-f680-4244-809c-f38df97f0c51)


El proyecto sigue una estructura organizada que incluye los siguientes directorios:

Context: Contiene la clase de contexto de Entity Framework Core (DbContext) donde se define la configuración de las entidades y las relaciones.

Controllers: Contiene controladores de API REST para manejar las solicitudes HTTP y las respuestas relacionadas con los recursos del proyecto.

Models: Contiene las clases de modelos que representan las entidades de la base de datos.

Migrations: Contiene las migraciones de base de datos generadas por Entity Framework Core para actualizar el esquema de la base de datos según los cambios en el modelo.



