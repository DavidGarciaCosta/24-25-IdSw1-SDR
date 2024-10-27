# 📊 Modelo de Dominio

En esta sección se describen en detalle los tres diagramas principales que componen el modelo de dominio del proyecto: el diagrama de clases, el diagrama de objetos y el diagrama de estados. Para cada diagrama, se muestra una tabla con la representación en formato SVG y un enlace al código fuente en formato `.puml`.

---

## 1. Diagrama de Clases

El diagrama de clases describe la estructura del sistema en términos de entidades principales (como `Profesor`, `Asignatura`, `Titulacion`, etc.) y las relaciones entre ellas. Este diagrama proporciona una visión general de cómo se conectan las diferentes clases en el dominio de la gestión de datos académicos de UNEATLANTICO.

| Diagrama | Código Fuente |
|----------|---------------|
| ![Diagrama de Clases](/images/modelosUML/MdD/diagramaDeClases.svg) | [Ver código](/modelosUML/diagramaDeClases.puml) |

### Descripción:

El Profesor es una entidad que tiene la responsabilidad de impartir Asignaturas y elaborar la MemoriaAcadémica correspondiente. Esta MemoriaAcadémica reporta información acerca de las Asignaturas que el profesor enseña. Las Asignaturas, están relacionadas tanto con una Titulación y como con un PlanEstudios. Finalmente, tanto el PlanEstudios como la Titulación se ofrecen en un Departamento académico. 

---

## 2. Diagrama de Objetos

El diagrama de objetos representa instancias específicas de las clases descritas anteriormente, mostrando un escenario concreto del sistema en acción. Este diagrama visualiza cómo los objetos (instancias de las clases) interactúan en un contexto particular, basado en la gestión de asignaturas, profesores y memorias académicas.

| Diagrama | Código Fuente |
|----------|---------------|
| ![Diagrama de Objetos](/images/modelosUML/MdD/diagramaDeObjetos.svg) | [Ver código](/modelosUML/diagramaDeObjetos.puml) |

### Descripción:

En este diagrama, se observa un sistema educativo en el que el profesor "Juan Pérez", imparte "Programación". Además de impartirla, el profesor elabora la memoria1, con fecha de "2024-10-21". Esta memoria reporta sobre la misma asignatura1 que Juan Pérez enseña. "Programación" pertenece a  "Ingeniería Informática", y además forma parte del "Plan 2024". Tanto la "Ingeniería Informática" como el "Plan 2024" se ofrecen en "Departamento de Ingeniería Informática".

---

## 3. Diagrama de Estados

El diagrama de estados detalla los diferentes estados por los que pasan las entidades clave del sistema, en este caso `Asignatura` y `Profesor`, a lo largo de su ciclo de vida. Esto es fundamental para gestionar el flujo de trabajo, desde la creación de una asignatura hasta la generación de la memoria académica.

| Diagrama | Código Fuente |
|----------|---------------|
| ![Diagrama de Estados](/images/modelosUML/MdD/diagramaDeEstados.svg) | [Ver código](/modelosUML/diagramaDeEstados.puml) |

### Descripción:
 ...   aqui como se va a cambiar el diagrama ya se hace la descripcion