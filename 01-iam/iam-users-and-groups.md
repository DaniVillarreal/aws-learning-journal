# IAM: Creación de Usuario y Grupo (Consola AWS)

## Objetivo
Crear un usuario IAM y asignarlo a un grupo con permisos administrativos,
evitando el uso del usuario root.

## Contexto
IAM (Identity and Access Management) es un servicio global de AWS que permite
gestionar identidades y permisos dentro de una cuenta.

## Pasos realizados en la consola

1. Accedí a la consola de AWS usando el usuario root.
2. Busqué el servicio **IAM**.
3. Entré a la sección **Usuarios**.
4. Creé un nuevo usuario con las siguientes características:
   - Nombre de usuario: `daniel`
   - Acceso a la consola de administración: habilitado
   - Contraseña: generada automáticamente
   - Cambio de contraseña en el primer inicio de sesión: habilitado

![Creación de usuario IAM](images/iam-create-user.png)

## Creación del grupo

1. Desde IAM, creé un grupo llamado `Admin`.
2. Asigné la política:
   - `AdministratorAccess`
3. Añadí el usuario `daniel` al grupo `Admin`.

![Creación de usuario IAM](images/iam-create-group.png)


## Configuración clave
- Usuario root solo se utilizó para la creación inicial.
- Los permisos se asignaron mediante grupo, no directamente al usuario.

## Resultado
El usuario `daniel` puede iniciar sesión en la consola de AWS y administrar
los servicios según los permisos definidos por el grupo `Admin`.

## Buenas prácticas aplicadas
- No usar el usuario root para tareas diarias.
- Uso de grupos para gestionar permisos.
- Principio de organización y escalabilidad.

## Aprendizajes
- IAM es un servicio global (no depende de regiones).
- Los grupos simplifican la administración de permisos.
- Los permisos determinan qué acciones puede realizar un usuario.
