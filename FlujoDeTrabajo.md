# Introducción #

Ésto explica qué hay que tener en cuenta al ser desarrollador del proyecto. Es de cumplimiento necesario.

# Status de los Issues #

Un issue es la "unidad mínima de trabajo". Ó sea, una tarea. Cada cosa que haya que hacer para el proyecto (sea codificar ó hacer otra cosa) tendrá un issue asociado. Para ver los tipos de issues, leer [TagsEnIssues](TagsEnIssues.md)

## Mientras están "Vivos" (opened) ##
Al manejar issues, es necesario saber los posibles estados en los que puede vivir:
|New                  | Ningun developer vio el Issue (puede ser que haya que cerrarlo -> ver "Para matarlos"). Si está todo bien, alguien debería pasarlo a Accepted |
|:--------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
|Accepted             | El Issue lo revisó un developer. En el caso de un Bug, pasa a accepted cuando pudo ser reproducido el error |
|Started              | Estamos trabajando para su satisfacción. Al terminar de trabajar, puedo pasarlo a ReviewRequested ó a MergeNeeded (en caso de ser código) ó puede pasarse a Done (en caso de ser documentación) |
|ReviewRequested      | Cambios terminados, se necesita PeerReview. O sea, me gustaría que vean mi código porque no confío mucho en lo que hice, por más que ande |
|MergeNeeded          | DEPRECADO NO USAR. Todavía nadie lo pasó a la versión estable. En cuanto se pase, el estado debe cambiar a Done |

## Para matarlos (closed) ##
|Invalid              | This was not a valid issue report |
|:--------------------|:----------------------------------|
|Duplicate            | This report duplicates an existing issue |
|WontFix              | We decided to not take action on this issue |
|Done                 | Task completed |
|Verified             | DEPRECADO NO USAR |

# Flujo de Trabajo #
## Elegir un issue ##
  * En ésta página: https://code.google.com/p/objectbrowserpharo/issues/list
  * TODA tarea que se haga del proyecto, debe estar respaldada por un issue. Si no existe, crearlo, teniendo en cuenta esto: [TagsEnIssues](TagsEnIssues.md).
  * Se debe elegir los issues que estén en estado "Accepted".
  * Además, está bueno resolver issues que tengan una prioridad alta, ó pertenezcan al release actual (ver [TagsEnIssues](TagsEnIssues.md)).
  * Si se es principiante, está bueno elegir los issues con menor dificultad.
## Ponerse como Owner del Issue, y pasarlo a Started ##
  * En la página del issue, hacer click en "Add a comment or make changes". En "Owner" poner el usuario, y en "Status" poner "Started".
  * Esto me permite avisar al resto que alguien está trabajando en el issue, y quién lo está haciendo.
## Resolver el Issue ##
Si el issue es una tarea que no tiene que ver con codificación, sólo se resuelve ésta tarea y listo.
Ahora, si el issue es de codificación:
#### Descargarse el código ####
  * Hay que tener descargada la última versión de Ozono.
```
Gofer it
 smalltalkhubUser: 'Uqbar' project: 'Ozono';
 configurationOf: 'ObjectBrowser';
 loadVersion: #bleedingEdge
```
#### Leer Documentación ####
  * Para conocer el modelo interno del Object Browser, por ahora la documentación está [acá](https://sites.google.com/site/objectbrowsertool/documentacin-de-desarrollo)
#### Testear ####
  * Necesitamos mantener un test coverage interesante, así que el primer paso para desarrollar debería ser:
    * En un Bug, la máxima de Leo Gassman: "Si hay un Bug y sin embargo los tests están verdes, debemos hacer un test que pruebe que esto está fallando (que dé rojo) para que cuando lo arreglemos, dé verde"
    * En un Feature, no hace falta hacer TDD (aunque se puede). Pero sí hay que asegurarse de tener la nueva funcionalidad cubierta por tests.
#### Commitear los cambios ####
  * Una vez que se hacen las modificaciones correspondientes, hay que utilizar Monticello para cargarlas al repo: [Tutorial de Monticello](https://docs.google.com/document/d/1LLrTr17R5irLp947i8Zlc7HOa7PtX_tFvu9m5vNjvlE/edit)
    * Cuidado, para commitear en el proyecto Ozono hay que tener un usuario en SmalltalkHub, en el team "Uqbar"
  * Al commitear no olvidar poner en el comentario **el número de issue que se está resolviendo**.
## Cerrar el Issue ##
  * Cuando se pudo resolver un issue por completo, hay que ponerlo en status "ReviewRequested". La idea es que siempre haya otro que le pegue un vistazo a tu código antes de darlo por cerrado.
  * Una vez que la versión estable se actualice, y se haya hecho peer review, ya puede pasarse el issue a Done (esto hará que desaparezca de la lista de "Open").

# Otros Flujos #
## Revisar Issues en New ##
  * Pasar a Accepted
TODO
  * Pasar a los otros....
TODO