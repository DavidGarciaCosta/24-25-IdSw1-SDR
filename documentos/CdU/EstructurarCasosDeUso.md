# 📝 Estructurar el Modelo de Casos de Uso

| [⬅️ Prototipar Casos de Uso](PrototiparCasosDeUso.md) | Generar Diagramas UML ➡️ |
|:--|--:|


## 🎯 **Objetivo**
El objetivo de este paso es **estructurar el modelo de casos de uso**, organizando las clases necesarias y estableciendo las relaciones entre ellas, según el diagrama conceptual previamente definido.

## 📋 **Clases y Relaciones en el Modelo**  

| **#** | **Clase**                     | **Descripción**                                                                                                                                                                                                                                   | **Imagen**                                                                                                                                                     |  
|-------|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| 1     | 🏫 **Sin_Asignacion**         | Representa el estado inicial del proceso, en el que no hay carga asignada. <br> - Esta clase solo tiene un atributo que indica el estado actual del flujo.                                                                                      | [Imagen]()                                                                                                                                                    |  
| 2     | 📜 **Propuesta_Carga**        | Encapsula la lógica para crear una propuesta inicial de carga docente basada en docencia, gestión e investigación. <br> - Atributos: <br> -- Profesor. <br> -- Materias. <br> -- Horas planificadas.                                             | [Imagen]()                                                                                                                                                    |  
| 3     | 📋 **Asignacion_Inicial**     | Valida y registra la asignación inicial. <br> - Se asegura de que la propuesta inicial cumpla con los requisitos del contrato y del programa académico. <br> - Depende de la clase **Verificar_Contrato** para continuar el flujo.               | [Imagen]()                                                                                                                                                    |  
| 4     | ⚖️ **Verificar_Contrato**    | Verifica la compatibilidad del contrato del profesor con la carga propuesta. <br> - Atributos clave: <br> -- Tipo de contrato. <br> -- Estado de compatibilidad.                                                                                | [Imagen]()                                                                                                                                                    |  
| 5     | 🔍 **Revisión_EQ_TC**         | Compara la EQ TC (Equivalencia de Tiempo Completo) real con la registrada en el contrato para verificar si se respetan los límites.                                                                                                              | [Imagen]()                                                                                                                                                    |  
| 6     | 📊 **Revisión_Carga**         | Revisa la proporción de carga docente asignada en docencia, gestión e investigación, validando que cumpla con las proporciones definidas.                                                                                                        | [Imagen]()                                                                                                                                                    |  
| 7     | ✔️ **Verificar_Memoria**      | Confirma si la carga asignada es compatible con la memoria académica aprobada del programa. <br> - Si hay desbalances, envía el flujo a **Ajuste_Carga**.                                                                                       | [Imagen]()                                                                                                                                                    |  
| 8     | 🛠️ **Ajuste_Carga**           | Permite realizar modificaciones a la carga docente según las necesidades del programa y las restricciones legales.                                                                                                                               | [Imagen]()                                                                                                                                                    |  
| 9     | ✅ **Asignada**                | Representa el estado final en el que la carga ha sido aprobada y asignada. <br> - Incluye detalles finales del contrato y la proporción de carga asignada en cada actividad.                                                                     | [Imagen]()                                                                                                                                                    |  
| 10    | 🏛️ **Cumplimiento_Legal**     | Opcionalmente, valida la conformidad legal de la asignación final con las normativas vigentes. <br> - Si no cumple, retorna el flujo a **Ajuste_Carga** para realizar las modificaciones necesarias.                                              | [Imagen]()                                                                                                                                                    |  

### ✏️ **Notas**
- Cada clase en este modelo representa un estado o proceso específico dentro del flujo de asignación de carga docente.
- Las relaciones entre clases están diseñadas para garantizar un proceso coherente y verificable.
- Las imágenes de los diagramas pueden incluir bocetos UML o tablas de atributos de cada clase.
