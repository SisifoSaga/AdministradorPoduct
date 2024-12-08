## Proyecto Full Stack con PERN

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
```http
PUT /api/products/1
