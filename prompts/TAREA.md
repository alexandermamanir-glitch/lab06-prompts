# Tarea: Mi prompt profesional

## Funcionalidad elegida
Sistema CRUD (Crear, Leer, Actualizar, Eliminar) para la gestión de productos de una tienda[cite: 3].

## Version 1: prompt básico

```text
Hazme un programa en Java para registrar productos.
Actúa como desarrollador Java. Crea una clase Producto con atributos id, nombre, precio y stock. Incluye un menú interactivo por consola que permita agregar un producto y listar los productos.
çActúa como un Desarrollador Java Senior. Diseña un sistema de gestión de productos (CRUD) en consola utilizando Java 11.

El programa debe permitir al usuario:
1. Agregar un nuevo producto (id, nombre, precio, stock).
2. Listar todos los productos.
3. Actualizar el precio o stock por ID.
4. Eliminar un producto por ID.

Restricciones y reglas de negocio:
- No uses librerías externas (solo clases nativas ArrayList y Scanner).
- Valida que el precio sea mayor a 0 y stock no negativo.
- Maneja excepciones si ingresan texto en lugar de números.

Ejemplo de salida del menú:
1. Registrar producto | 2. Mostrar productos | 3. Editar | 4. Eliminar | 5. Salir

Presenta el resultado organizando el código en clases separadas (Producto y GestionProductosMain) con comentarios explicativos.