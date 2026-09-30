# lab7-tecnicas

Bitacora de tecnicas avanzadas de prompting

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo          | Aciertos (de 5) | Formato de la respuesta                             | Todas con el mismo formato (Si/No) |
| :------------ | :-------------: | :-------------------------------------------------- | :--------------------------------: |
| **Zero-shot** |        5        | Tabla detallada con explicaciones y resumen         |                 No                 |
| **One-shot**  |        5        | Listado con flechas y aclaración adicional al final |                 Sí                 |
| **Few-shot**  |        5        | Estricto, línea por línea con texto y etiqueta      |                 Sí                 |

## Ejercicio 3: Chain of Thought

| Pedido          | Respuesta de la IA                           | Muestra los pasos (Si/No) | Correcta (Si/No) |
| :-------------- | :------------------------------------------- | :-----------------------: | :--------------: |
| **Directo**     | 318.6                                        |            No             |        Sí        |
| **Paso a paso** | Desglose completo de cálculos y verificación |            Sí             |        Sí        |

## Ejercicio 4: Role prompting

| Version            | Vocabulario (sencillo/tecnico)                | Usa ejemplos o codigo               | A quien le sirve mas                    |
| :----------------- | :-------------------------------------------- | :---------------------------------- | :-------------------------------------- |
| **A. Sin rol**     | Sencillo y directo                            | Sí (Python básico)                  | Estudiantes o público general           |
| **B. Rol docente** | Muy sencillo con analogías cotidianas (cajas) | Sí (Python explicativo paso a paso) | Principiantes sin experiencia           |
| **C. Rol senior**  | Técnico y profesional (memoria, tipos, scope) | Sí (Código Java y arquitectura)     | Desarrolladores o compañeros de trabajo |

## Ejercicio 5: Descomposicion

- **Qué entregó la IA (paso a paso):** Primero listó los requisitos del sistema, luego estructuró el diseño de las clases con sus atributos y tipos de datos, y finalmente generó el código Java de la clase Producto con sus constructores y validaciones.
- **Comparación (descomposición vs pedido de una sola vez):** Dividir la tarea en pasos ordenados permitió obtener un diseño mucho más limpio, detallado y controlado que si se le hubiera pedido todo de golpe, evitando que la IA omitiera métodos clave o relaciones entre las clases.

## Ejercicio 6: Prompt estructurado y autocritica

### 4. Evaluar

| Qué revisar                                      | Cumple (Sí / No) |
| :----------------------------------------------- | :--------------: |
| ¿Tiene las 4 columnas pedidas?                   |        Sí        |
| ¿Incluye el bloqueo después de 3 intentos?       |        Sí        |
| ¿Incluye casos con campos vacíos?                |        Sí        |
| ¿Indica qué casos agregó en la autocrítica?      |        Sí        |
| ¿Hay algún caso repetido o que no tenga sentido? |        No        |

### 5. Prompt estructurado

```text
Actúa como un analista de QA y experto en testing. Diseña un plan de pruebas completo (casos de prueba) para el módulo de inicio de sesión (login) de un sistema.

El plan debe incluir:
1. Funciones (camino feliz).
2. Credenciales (casos válidos e inválidos).
3. Validación de campos (vacíos, formatos de correo, contraseñas).
4. Seguridad (bloqueo tras 3 intentos fallidos, inyección SQL, etc.).
5. Usabilidad y compatibilidad.

Incluye una sección de autocrítica donde revises tu propio resultado, detectes si faltaron casos importantes (como correos mal formados, campos vacíos específicos o doble clic en botones) y los agregues en una tabla de "Casos agregados".
```

- [Bitacora de tecnicas avanzadas](prompts/README.md)
