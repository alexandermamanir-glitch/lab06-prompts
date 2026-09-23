# Bitacora de prompts
 
Laboratorio 06: Fundamentos de Ingenieria de Prompts.
 
Herramienta de IA usada: ChatGPT
 
## Ejercicio 2: Tokens y ventana de contexto

| Texto | Caracteres | Tokens |
|---|---|---|
| Los estudiantes programan en Java. | 35 | 7 |
| The students program in Java. | 29 | 6 |
| desafortunadamente | 17 | 5 |
 
## Ejercicio 3: Temperatura

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|---|---|---|
| 0 | 100.0% | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 | 65.2% | BiblioTec, LibroYa, BiblioTec, BiblioTec, PrestaLibro |
| 1 | 45.8% | BiblioTec, LibroYa, PrestaLibro, BiblioTec, LectoGo |
| 1.8 | 32.8% | BiblioTec, LibroYa, PrestaLibro, BiblioTec, LectoGo |

Al subir la temperatura, los porcentajes se distribuyen entre más opciones y los nombres elegidos en los 5 intentos varían en cada ejecución. El simulador nunca inventa un nombre nuevo porque la temperatura solo cambia la probabilidad de elección entre las opciones existentes, pero no agrega conocimiento ni datos nuevos al modelo.
 
## Ejercicio 4: Prompt vago vs estructurado

### Comparativa de Prompts:

| Criterio | Prompt vago | Prompt estructurado |
|---|---|---|
| Menciona el objetivo del sistema | No | Sí |
| Menciona a los usuarios principales | No | Sí |
| Tiene exactamente 3 funcionalidades | No | Sí |
| Esta en 3 párrafos | No | Sí |
| Lo usaría en un informe real | No | Sí |
 
## Ejercicio 5: Anatomia de un prompt

| Componente | Texto de mi prompt |
|---|---|
| Rol | Actúa como un Arquitecto de Software Senior especializado en desarrollo web. |
| Instrucción | Diseña la arquitectura de un sistema de reservas de libros para una biblioteca. |
| Contexto | El sistema debe atender a más de 5,000 estudiantes simultáneamente durante periodos de exámenes. |
| Ejemplo | Muestra componentes clave como Auth Service -> DB Relacional. |
| Formato | Devuelve la respuesta organizada en una lista numerada con viñetas para las tecnologías. |

### Cambios por nivel:
- **Nivel 1:** Genera una respuesta básica y genérica sin estructura clara.
- **Nivel 2:** Al añadir el Rol, adapta el tono a un nivel técnico especializado.
- **Nivel 3:** La Instrucción directa delimita el objetivo exacto del sistema.
- **Nivel 4:** El Contexto permite que la IA considere la alta carga de usuarios simultáneos.
- **Nivel 5:** El Formato y Ejemplo aseguran que la respuesta sea limpia y legible al primer intento.
 
## Ejercicio 6: Del prompt basico al profesional

PROMPT PROFESIONAL INICIAL:
Actúa como un desarrollador Java Senior. Diseña una interfaz gráfica con Java Swing para un sistema de inicio de sesión (Login) de TiendaTec. Incluye campos para correo y contraseña, y un botón para ingresar.

PROMPT DE MEJORA (ITERACIÓN):
Mejora el código anterior con estas restricciones: no uses librerías externas, valida que el correo contenga @ y que la contraseña tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.