# Tarea: Mi prompt profesional

## Funcionalidad elegida
Sistema CRUD (Crear, Leer, Actualizar, Eliminar) para la gestión de productos de una tienda.

## Version 1: prompt básico

```text
Hazme un programa en Java para registrar productos.
```

- **Qué cambié:** Prompt básico sin detalles.
- **Por qué:** Prueba inicial para evaluar la respuesta de la IA.
- **Qué mejoró:** Nada, la respuesta fue genérica y muy simple.

## Version 2

```text
Actúa como desarrollador Java. Crea una clase Producto con atributos id, nombre, precio y stock. Incluye un menú interactivo por consola que permita agregar un producto y listar los productos.
```

- **Qué cambié:** Agregué rol, atributos y menú en consola.
- **Por qué:** Para estructurar la entrada y salida de datos del programa.
- **Qué mejoró:** Creó la clase con getters/setters y un menú funcional.

## Version 3: prompt final

```text
Actúa como un Desarrollador Java Senior. Diseña un sistema de gestión de productos (CRUD) en consola utilizando Java 11.

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
```

- **Qué cambié:** Todos los 5 componentes + restricciones explícitas y manejo de excepciones.
- **Por qué:** Para obtener código listo para producción y robusto ante errores.
- **Qué mejoró:** Generó un CRUD completo estructurado en clases independientes con validaciones.

## Componentes del prompt final

| Componente | Texto de mi prompt |
|------------|--------------------|
| **Rol** | Actúa como un Desarrollador Java Senior. |
| **Instrucción** | Diseña un sistema de gestión de productos (CRUD) en consola utilizando Java 11. |
| **Contexto** | Sistema para gestionar productos con id, nombre, precio y stock. |
| **Ejemplo** | Ejemplo del menú: `1. Registrar producto \| 2. Mostrar productos \| ...` |
| **Formato** | Presenta el resultado organizando el código en clases separadas con comentarios. |

## Evaluación del resultado

| Criterio | Cumple (Sí / No) |
|----------|-------------------|
| ¿Implementa las 4 operaciones del CRUD? | Sí |
| ¿No utiliza librerías externas? | Sí |
| ¿Valida datos numéricos y precios positivos? | Sí |
| ¿Está dividido en clases independientes? | Sí |

## Errores que evité

1. **Ser demasiado general:** En la v1 la IA generó un código plano. Lo evité definiendo cada operación requerida.
2. **No indicar el formato:** La IA solía dar un solo bloque desordenado. Lo evité exigiendo separación explícita de clases (`Producto` y `GestionProductosMain`).