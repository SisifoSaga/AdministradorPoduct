## Proyecto Full Stack con PERN

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
```http
GET /productos/1
