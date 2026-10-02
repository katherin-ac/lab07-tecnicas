# Tarea: Mi prompt avanzado

## Tarea elegida

## Version 1: prompt basico

```
genera clases de un sistema de notas para estudiantes
```

## Version 2

### Usamos Role Prompting

```
Actúa como un profesor de programación Java que esta enseñando diseño de clases a estudiantes principiantes. Diseña las clases necesarias para un sistema de notas de estudiantes en Java.
```

## Version 3: prompt final

### Usamos Role Prompting, Prompt Estructurado y Autocrítica

```
<rol>Actúa como un profesor de programación Java que enseña diseño de clases a estudiantes principiantes. </rol>
<contexto> Necesito diseñar un sistema de notas para estudiantes en Java.
El sistema debe permitir representar estudiantes, cursos y notas. </contexto>
 <tarea> Diseña las clases necesarias. Para cada clase indica sus atributos y métodos principales. Revisa tu propuesta y verifica si falta alguna clase, atributo o método importante. Si encuentras algo que falte, corrígelo.</tarea>
<formato> Presenta la respuesta en una tabla con las columnas:
Clase | Atributos | Métodos | Propósito
 Después de la tabla, muestra las correcciones realizadas durante la revisión. </formato>
```

## Tecnicas usadas en el prompt final

| Técnica             | Parte del prompt                               |
| ------------------- | ---------------------------------------------- |
| Role prompting      | Actúa como un profesor de programación Java... |
| Prompt estructurado | uso de <\rol> <\contexto> <\tarea> <\formato>  |
| Autocritica         | Revisa tu propuesta y verifica...              |

## Evaluacion del resultado

| Criterio                                                 | Cumple |
| -------------------------------------------------------- | ------ |
| Rol específico                                           | Sí     |
| Clases necesarias para el sistema                        | Sí     |
| Incluye atributos y métodos para cada clase              | Sí     |
| ¿Respeta el formato de tabla solicitado?                 | Sí     |
| ¿Incluye una revisión del diseño?                        | Sí     |
| ¿Indica las correcciones realizadas durante la revisión? | Sí     |

## Por que elegi estas tecnicas

Estas técnicas son sencillas y permiten mejorar progresivamente el prompt hasta llegar al resultado que queremos. No se usó few-shot porque esta tarea no necesitaba ejemplos previos para establecer un formato, ni chain of thought porque el objetivo era obtener un diseño organizado y revisarlo, no mostrar un razonamiento paso a paso. Tampoco descomposición porque la tarea podía resolverse en una sola solicitud y luego revisarlas mediante autocrítica.
