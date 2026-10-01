# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.
Herramienta de IA usada: (escribe aqui cual usaste)

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo | Aciertos (de 5) | Formato de la respuesta | Todas con el mismo formato (Si/No) |
|------|-----------------|-------------------------|------------------------------------|
| Zero-shot | 5 |Utiliza una tabla |Si |
| One-shot |5 |Numeración |Si |
| Few-shot |5 |Usa comillas y el formato de flecha "->" |Si |

## Ejercicio 3: Chain of Thought

| Pedido | Respuesta de la IA | Muestra los pasos (Si/No) | Correcta (Si/No) |
|--------|--------------------|---------------------------|------------------|
| Directo |318.60 |No |Si |
| Paso a paso |318.60 |Si |Si |

## Ejercicio 4: Role prompting

| Version | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo | A quien le sirve mas |
|---------|-------------------------------|-----------------------|----------------------|
| A. Sin rol |Sencillo|Si|Principiantes sin ningun conocimiento|
| B. Rol docente |Sencillo |Si|Programadores principiantes |
| C. Rol senior |Tecnico |Si|Personas con previos conocimientos |

## Ejercicio 5: Descomposicion

Paso 1: La IA entregó una estructura completa, sugiriendo una base de datos, un diseño del front end y el flujo del sistema.

Paso 2: Hace la estructura mucho mas simple con los 5 requisitos principales.

Paso 3: Entrega una estructura clara de los 5 requisitos con el nombre de los atributos y el tipo de dato.

Paso 4: Entrega el código de Java con los métodos solicitados y la distribución de clases que planteó.

El pedido de una sola vez fue mucho más general y la respuesta se desvió hasta otros temas. En cambio, en el pedido paso por paso, se mantuvo en el hilo de lo solicitado y fue más exacto.

## Ejercicio 6: Prompt estructurado y autocritica
|Qué revisar | Cumple Si/No |
|------------|--------------|
| ¿Tiene las cuatro columnas pedidas? |Si
|¿Incluye el bloqueo después de 3 intentos?|Si
|¿Incluye casos con campos vacíos?|Si
|¿Indica qué casos agregó en la autocrítica?|Si
|¿Hay algún caso repetido o que no tenga sentido?|Si

```text
Prompt Estructurado

Rol: Actua como analista de pruebas de software.
Contexto: Login web con correo y contraseña. La cuenta se bloquea despues de 3 intentos fallidos.
Tarea: Piensa paso a paso que puede fallar y escribe 6 casos de prueba. 
Formato: Tabla con las columnas: ID, escenario, datos de entrada, resultado esperado.

Autocritica: 
Revisa tu tabla: faltan casos limite como campos vacios, correo sin @
o contrasena con espacios? Agrega los que falten e indica cuales agregaste.
```