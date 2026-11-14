# Tarea: Mi prompt avanzado

## Tarea elegida

Generar casos de prueba para un sistema de registro de usuarios.

---

## Version 1: prompt basico

```text
Genera casos de prueba para un formulario de registro de usuarios que solicite nombre, correo electrónico y contraseña.
```

### Técnica agregada
Ninguna (prompt básico).

### ¿Por qué?
Sirve como punto de partida para comparar resultados.

### ¿Qué mejoró?
Se obtiene una respuesta funcional, pero suele ser breve y poco estructurada.

---

## Version 2


```text
Actúa como Analista QA especializado en pruebas de aplicaciones web.

Genera casos de prueba para un formulario de registro de usuarios que solicite nombre, correo electrónico y contraseña.

Presenta el resultado en una tabla con:
- ID
- Caso de prueba
- Datos de entrada
- Resultado esperado
```

### Técnica agregada
Role Prompting + Prompt Estructurado.

### ¿Por qué?
El rol orienta a la IA hacia el contexto de pruebas de software y el formato definido mejora la organización.

### ¿Qué mejoró?
Los casos son más profesionales y aparecen organizados en una tabla.

---

## Version 3: prompt final

```text
Actúa como Analista QA especializado en pruebas de aplicaciones web.

Tarea:
Generar casos de prueba para un formulario de registro de usuarios.

Sigue este proceso:

1. Identifica los campos del formulario.
2. Determina validaciones posibles para cada campo.
3. Genera casos positivos y negativos.
4. Revisa tu resultado y verifica que no existan casos duplicados ni validaciones faltantes.

Ejemplo del formato esperado:

Caso:
Entrada: correo válido, contraseña válida
Resultado esperado: registro exitoso

Caso:
Entrada: correo sin formato válido
Resultado esperado: mensaje de error

Entrega la respuesta en una tabla con:
- ID
- Caso de prueba
- Datos de entrada
- Resultado esperado
- Tipo (Positivo/Negativo)
```

### Técnica agregada
- Role Prompting
- Few-Shot
- Descomposición
- Autocrítica

### ¿Por qué?
Permiten obtener respuestas más completas, organizadas y revisadas.

### ¿Qué mejoró?
Se generan más casos de prueba, se reduce la omisión de validaciones y el formato es consistente.

---

## Tecnicas usadas en el prompt final

| Parte del prompt | Técnica |
|------------------|----------|
| Actúa como Analista QA especializado | Role Prompting |
| Ejemplo del formato esperado | Few-Shot |
| Pasos 1, 2 y 3 | Descomposición |
| Paso 4: revisa tu resultado | Autocrítica |
| Entrega la respuesta en una tabla | Prompt Estructurado |

---

## Evaluacion del resultado

| Criterio | Sí/No |
|----------|--------|
| Los casos de prueba están organizados en tabla | Sí |
| Incluye casos positivos y negativos | Sí |
| Sigue el formato solicitado | Sí |
| Evita duplicados después de la revisión | Sí |
| Aplica el rol definido | Sí |

---

## Por que elegi estas tecnicas

Elegí Role Prompting porque permite orientar a la IA hacia el trabajo de un Analista QA, obteniendo respuestas más cercanas a un entorno profesional. Utilicé Descomposición para guiar el razonamiento en etapas y asegurar que se cubrieran todas las validaciones importantes. Incorporé Few-Shot para fijar el formato esperado de las respuestas y mantener la consistencia. Finalmente, añadí Autocrítica para que la IA revise sus propios resultados y reduzca errores u omisiones. Estas técnicas fueron seleccionadas porque mejoran directamente la calidad de los casos de prueba generados, mientras que otras técnicas aportaban menos valor para esta tarea específica.