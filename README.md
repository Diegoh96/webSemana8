# webSemana8
realizamos lo solicitado y lo pendiente 
Cambios realizados en el proyecto

1. Implementación de Node.js y Express

Se configuró un servidor backend utilizando Express para gestionar las solicitudes HTTP del sistema.

Cambios realizados:

- Creación del archivo `server.js`
- Configuración del puerto 3000
- Implementación de rutas GET y POST
- Configuración de middlewares

---

2. Integración con MySQL

Se conectó el proyecto con MySQL mediante XAMPP utilizando la librería `mysql2`.

Cambios realizados:

- Creación de la base de datos `formularioDB`
- Creación de tabla `contactos`
- Configuración de conexión MySQL
- Inserción de datos desde el formulario

---

3. Arquitectura de 3 capas

El proyecto fue reorganizado utilizando separación de responsabilidades.

Estructura implementada

```text
routes/
controllers/
services/
middlewares/
presentation/
```

---

4. Implementación de rutas

Se agregaron rutas para manejar solicitudes del cliente.

GET /

Permite verificar el funcionamiento del servidor.

POST /enviar

Permite enviar y guardar información en MySQL.

---

5. Implementación de controladores

Se separó la lógica de las rutas utilizando controladores.

Funciones implementadas:

- Inicio del servidor
- Guardado de contactos
- Manejo de respuestas HTTP

---

6. Implementación de servicios

Se creó una capa de servicios para manejar la conexión a la base de datos.

Archivo implementado:

```text
services/db.js
```

---

7. Implementación de middleware

Se creó un middleware de validación de datos.

Función:

- Verificar campos vacíos
- Evitar inserciones incorrectas
- Controlar errores HTTP

Código utilizado:

```javascript
if (!nombre || !email || !mensaje)
```

---

8. Implementación de cookies y sesiones

Se integró manejo de sesiones utilizando:

- cookie-parser
- express-session

Objetivo:

- Manejar sesiones de usuario
- Guardar información temporal

---

9. Manejo de errores HTTP

Se implementó control de errores utilizando códigos HTTP.

Códigos utilizados

- 200 → Solicitud correcta
- 400 → Campos incompletos
- 500 → Error del servidor

---

10. Mejoras realizadas al frontend

Se conectó el formulario HTML con el backend mediante `fetch()`.

Mejoras:

- Envío dinámico de datos
- Comunicación frontend-backend
- Validaciones básicas

---

11. Organización del código

Se reorganizó el proyecto para mejorar:

- Mantenimiento
- Escalabilidad
- Orden del backend
- Separación de responsabilidades

---

12. Corrección de errores

Problema detectado

```text
Cannot find module 'server.js'
```

Solución aplicada

- Verificación de ubicación del archivo
- Creación correcta de `server.js`
- Ejecución desde la carpeta correcta

---

13. Resultado final

El proyecto quedó funcionando correctamente con:

- Node.js
- Express
- MySQL
- XAMPP
- Arquitectura 3 capas
- Middleware
- Cookies y sesiones
- Rutas GET y POST
- Persistencia de datos
- Validaciones
- Manejo de errores
