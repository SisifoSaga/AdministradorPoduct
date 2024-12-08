# Proyecto Full Stack con PERN (Administrador de Productos)

## Versión 0.1.0 - Configuración Inicial

### Descripción
Esta versión incluye la configuración inicial del proyecto y la implementación de la base de datos:
- Configuración del entorno de desarrollo.
- Conexión con PostgreSQL.
- Scripts iniciales para la creación de tablas.

### Archivos clave
- `db.ts`: Configuración de la Base de Datos con PostgresSQL.
- `server.ts`: Archivo con la conexion y comprobación de los servidores.

### Cómo ejecutar
1. Clona este repositorio:
   ```bash
   git clone https://github.com/TuUsuario/PERN_Project.git](https://github.com/SisifoSaga/AdministradorPoduct

## Versión 0.2.0 - Crear Productos

### Descripción
Esta versión permite la creación de productos desde Thunder Client y su almacenamiento en la base de datos.

### Endpoint
- **POST** `https://localhost:4000/api/products`: Permite crear un nuevo producto.

#### Ejemplo de Body:
    "name": "Producto de Ejemplo", VALIDA QUE LA ENTRADA NO SEA NULA
    "price": 50, VALIDA QUE SEA UN NUMERO Y ESTE SEA POSITIVO
    "availability": true, EL VALOR SEA TRUE SI ES QUE NO SE ASIGNA UNO A LA DISPONIBILIDAD


### Versión 0.3.0 - Obtener Productos por ID

#### Descripción
Esta versión agrega la funcionalidad para obtener un producto específico de la base de datos mediante su ID, utilizando el método `GET` en Thunder Client.

#### Endpoint
- **GET** `http://localhost:4000/api/products/"id"`: Obtiene un producto de la base de datos.

#### Validaciones
- El ID debe ser un número entero.
- Si el producto no existe, devuelve un error 404.
- Si el ID no es válido, devuelve un error 400.

#### Ejemplo de Respuesta
**Request:**
GET /products/1

### Versión 0.4.0 - Actualizar y Eliminar Productos

#### Descripción
Esta versión agrega la funcionalidad para actualizar productos completamente o parcialmente y eliminar productos de la base de datos mediante los métodos `PUT`, `PATCH` y `DELETE`.

#### Endpoints
1. **PUT** `http://localhost:4000/api/products/"id"`: Actualiza todos los campos de un producto.
2. **PATCH** `http://localhost:4000/api/products/"id"`: Actualiza un campo específico de un producto.
3. **DELETE** `http://localhost:4000/api/products/"id"`: Elimina un producto de la base de datos.

---

### **1. Actualización Completa**
#### Endpoint
- **PUT** `http://localhost:4000/api/products/"id"`

#### Validaciones
- Todos los campos son obligatorios:
  - `name`: String.
  - `price`: Número.
  - `availability`: Booleano.
- Si el producto no existe, devuelve un error 404.

#### Ejemplo de Request y Respuesta
**Request:**

PUT /api/products/1


## Versión 0.5.0 - Introducción al Testing de API's

### Descripción
Esta versión introduce el testing para los endpoints del proyecto, utilizando herramientas como `Supertest` y `Jest`. Se implementan pruebas completas para validar la funcionalidad y confiabilidad de la API, incluyendo validaciones, manejo de errores y métricas de cobertura de código (Code Coverage).

---

### Pruebas Realizadas

#### 1. Probando una URL con Supertest
- **Descripción:** Validar que la API responde correctamente a una URL específica.
- **Prueba:** Verifica que el servidor responde con un código 200 al acceder a la raíz de la API (`/`).

### 2. Probando el Endpoint de Crear Producto
- **Descripción:** Valida que el endpoint `POST /productos` crea un producto correctamente.
- **Pruebas:**
  - Verifica que un producto válido se almacena en la base de datos.
  - Valida que el campo `price` debe ser mayor a 0.
 
---
    
### 3. Probando el Endpoint de Obtener Producto por ID
- **Descripción:** Valida que el endpoint `GET /productos/:id` responde con el producto correcto.
- **Pruebas:**
  - Valida que el producto existe en la base de datos.
  - Devuelve un error 404 si el producto no existe.

---

### 4. Probando la Actualización de Productos
- **Descripción:** Valida que los endpoints `PUT` y `PATCH` actualizan correctamente los productos.
- **Pruebas:**
  - Valida que se actualicen todos los campos con `PUT`.
  - Valida la actualización parcial con `PATCH`.

---

### 5. Probando la Eliminación de Productos
- **Descripción:** Valida que el endpoint `DELETE /productos/:id` elimina correctamente un producto.
- **Pruebas:**
  - Valida que el producto sea eliminado de la base de datos.
  - Devuelve un error 404 si el producto no existe.

---

### 6. Limpiar la Base de Datos Después de Cada Prueba
- **Descripción:** Se implementa un mecanismo para limpiar los datos de prueba al finalizar cada test para evitar conflictos.

---

### 7. Métricas de Validación - Code Coverage
- **Descripción:** Se incluyen métricas de cobertura de código para evaluar la calidad del testing.
- **Herramienta:** Integración de `jest --coverage` para obtener reportes detallados.
