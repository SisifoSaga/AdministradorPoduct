# Proyecto Full Stack con PERN

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

