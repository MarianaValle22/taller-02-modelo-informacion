# 📄 Informe Técnico del Taller

## 🔖 Nombre del Taller
_Taller 2 - [Modelo de Información y Diagrama de Contexto]_

## 👥 Integrantes del equipo
| Nombre | Correo Electrónico |
|---|---|
| Valentina Alejandra López Romero | valentinalopro@unisabana.edu.co |
| Mariana Valle Moreno | marianavamo@unisabana.edu.co |
| Laura Camila Rodriguez León | laurarodleo@unisabana.edu.co |

## 🧠 Descripción general del trabajo
El objetivo del taller fue modelar el flujo de información y las entidades involucradas en el proceso de autoevaluación institucional por programas, gestionado desde el área de Experiencia y Servicio de Desarrollo Estratégico, explícitamente, Logística de Aplicación.

La actividad se desarrolló mediante la identificación de actores, entidades clave y sistemas que intervienen en la planeación, logística y aplicación de la encuesta de acreditación de programas en la Universidad de La Sabana. Se construyó un modelo entidad–relación (ERD) que representa la estructura de información requerida y un diagrama de contexto que evidencia los flujos entre facultades, proveedores, estudiantes aplicadores (PAT) y el equipo coordinador.

## 🔧 Proceso de desarrollo
Se analizó cómo se gestiona actualmente la encuesta:

- Envío de correos a directores de programa.
- Recolección de información en archivos Excel.
- Consolidación manual de datos.
- Programación logística.
- Envío de información al proveedor externo.
- Recepción de informes generales e institucionales.

Y se identificaron puntos críticos como:

- Información incompleta o inconsistente.
- Multiplicidad de formatos.
- Repetición de datos entre programas.
- Dificultad para consolidar docentes que pertenecen a varios programas.
- Sobrecarga operativa centralizada en una sola persona.

## 🧩 Análisis del modelo propuesto
Se tomaron las siguientes decisiones:

Definir entidades principales como:

- Programa
- Docente
- Asignatura
- Semestre
- Encuesta
- Aplicación de Encuesta
- PAT (Estudiante aplicador de encuestas)
- Proveedor
- Cronograma
Además, se incorporaron entidades débiles tales como:
- DocentePrograma (para representar la pertenencia de un docente a múltiples programas y posibles roles como director).
- DetalleCronograma (para desagregar el cronograma en bloques específicos de aplicación).

Modelar relaciones que permitan:

El modelo permite representar que:

- Un docente puede pertenecer a varios programas.
- Un programa ofrece múltiples asignaturas.
- Cada asignatura pertenece a un semestre específico.
- Cada programa genera su propio cronograma.
- Un cronograma contiene múltiples bloques de aplicación (DetalleCronograma).
- Cada bloque de aplicación se concreta en una Aplicación de Encuesta.
- Un PAT puede aplicar múltiples encuestas según su disponibilidad.
- El proveedor recibe la información consolidada y genera informes institucionales y por programa.
- Considerar la Aplicación de Encuesta como entidad articuladora del modelo logístico.

## 📈 Diagrama final entregado
![ModeloEntidad (3)](https://github.com/user-attachments/assets/76dcbc4e-4598-477e-8cc5-ea23b8298ca5)

## 📋 Tabla de actores, entidades o componentes (si aplica)


| Nombre del elemento    | Tipo              | Descripción                                                          | Responsable            |
| ---------------------- | ----------------- | -------------------------------------------------------------------- | ---------------------- |
| Programa               | Entidad           | Unidad académica que gestiona su proceso de autoevaluación           | Facultad               |
| Docente                | Entidad           | Profesor que dicta asignaturas y puede pertenecer a varios programas | Programa               |
| PAT                    | Actor / Entidad   | Estudiante encargado de aplicar la encuesta en aula                  | Coordinación logística |
| Cronograma             | Entidad           | Documento formal diligenciado por decanos con Plan A y Plan B        | Decanos                |
| Aplicación de Encuesta | Proceso / Entidad | Ejecución específica de una encuesta en una clase determinada        | Coordinación logística |
| Proveedor              | Actor externo     | Tercero encargado de generar los enlaces y los informes consolidados | Proveedor externo      |


## 🔍 Investigación complementaria
### Tema investigado:
Modelo Entidad–Relación (ERD) y su aplicación en el diseño y gestión de bases de datos.

### Resumen:
El modelo entidad–relación (ERD), propuesto por Peter Chen en la década de 1970, es una herramienta utilizada en la fase conceptual del diseño de bases de datos. Su propósito es representar gráficamente cómo se estructuran los datos dentro de un sistema, mostrando entidades, atributos, relaciones y cardinalidades antes de su implementación en un sistema gestor de bases de datos.

De acuerdo con IBM [1], los ERD permiten a analistas de negocio e ingenieros de datos modelar información, evaluar el alcance de una base de datos y planificar su arquitectura. En el enfoque de tres esquemas de la ingeniería de software, el ERD corresponde al nivel conceptual, ya que define la estructura lógica sin entrar aún en detalles físicos de implementación. Además, son útiles en procesos de integración de datos y reingeniería de procesos empresariales (BPR), porque ofrecen una visión global del sistema de información y facilitan la identificación de redundancias o errores estructurales.

Un ERD se compone de cuatro elementos fundamentales:

- Entidades, que pueden ser fuertes (independientes) o débiles (dependientes de otra entidad).
- Atributos, que describen las características de cada entidad y pueden ser simples, compuestos, derivados o clave.
- Relaciones, que representan la interacción entre entidades.
- Cardinalidades, que indican cuántas instancias de una entidad se relacionan con otra (1:1, 1:N, N:M).

Asimismo, el modelo entidad–relación puede desarrollarse en tres niveles: conceptual, lógico y físico. El modelo conceptual presenta una visión general; el lógico detalla atributos y estructuras; y el físico incorpora claves primarias y foráneas listas para implementación en un SGBD [2].

En el contexto del taller, el ERD permitió estructurar formalmente el proceso de autoevaluación institucional, identificando entidades principales y sus relaciones. Esta representación conceptual facilita la transición desde un manejo manual de datos hacia una arquitectura organizada, coherente y alineada con principios de diseño de bases de datos.

## 📚 Referencias
- [1] IBM. What is an Entity Relationship Diagram (ERD)? s.f. https://www.ibm.com/es-es/think/topics/entity-relationship-diagram
- [2] ILERNA. Modelo entidad–relación en bases de datos. s.f. https://www.ilerna.es/blog/modelo-entidad-relacion-base-datos

---

_Este documento hace parte de la entrega del taller 2 del curso AREM (Arquitectura Empresarial) - Universidad de La Sabana._
