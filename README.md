## Versión 0.2.0 - Crear Productos

### Descripción
Esta versión permite la creación de productos desde Thunder Client y su almacenamiento en la base de datos.

### Endpoint
- **POST** `https://localhost:4000/api/products`: Permite crear un nuevo producto.

#### Ejemplo de Body:
```json
{
    "name": "Producto de Ejemplo", VALIDA QUE LA ENTRADA NO SEA NULA
    "price": 50, VALIDA QUE SEA UN NUMERO Y ESTE SEA POSITIVO
    "availability": true, EL VALOR SEA TRUE SI ES QUE NO SE ASIGNA UNO A LA DISPONIBILIDAD
}
