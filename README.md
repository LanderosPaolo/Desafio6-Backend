# Desafío 6: Autenticación y Autorización de usuarios con JWT

Este proyecto es un servidor Express que maneja consultas a una base de datos PostgreSQL y utiliza JSON Web Tokens (JWT) para autenticación. Proporciona las siguientes funcionalidades:

- Registro de usuarios
- Inicio de sesión de usuarios
- Obtención de información de usuarios

## Requisitos previos

Antes de ejecutar este proyecto, asegúrate de tener lo siguiente instalado:

- Node.js
- PostgreSQL

Crea un archivo .env en el directorio raíz del proyecto y proporciona los siguientes valores:

    DB_HOST=nombre_del_host
    DB_USER=nombre_de_usuario
    DB_PASSWORD=contraseña
    DB_NAME=nombre_de_la_base_de_datos
    JWT_SECRET=clave_secreta_para_generar_tokens
    PORT=puerto_donde_operará

Uso

    Inicia el servidor:

    npm run start

    o

    npm run dev

    Accede a la API a través de http://localhost:3000.

Endpoints

    POST /usuarios: Crea un nuevo usuario. Requiere los siguientes campos en el cuerpo de la solicitud: 
     - email, 
     - password, 
     - rol 
     - lenguage.

    POST /login: Inicia sesión de usuario. Requiere los campos en el cuerpo de la solicitud:
      - email,
      - password

    GET /usuarios: Obtiene la información del usuario autenticado. Requiere el encabezado Authorization con un token JWT válido.

Estructura del proyecto

El proyecto sigue la siguiente estructura de archivos:

    index.js: Archivo principal que configura el servidor Express y define las rutas.
    consultas.js: Archivo que contiene las consultas a la base de datos.
    middleware.js: Archivo que contiene los middlewares para validar las solicitudes.
