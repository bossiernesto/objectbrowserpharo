# Introducción #
Cada issue que creamos ó que modificamos, puede tener asociados Tags, que tenemos que setear y actualizar. Éstas son "etiquetas" que nos permiten después ordenar y filtrar los issues para hacer nuestro trabajo más feliz.

A continuación, la descripción de los existentes actualmente:
# Tags #
## Priority ##
Éste tag es importante: me dice qué tan urgente es necesario que se solucione el issue. High es el más alto nivel de urgencia.
```
Priority-High       
Priority-Medium     
Priority-Low  
```
## Dificultad ##
Si sos coder y sabés qué tan fácil / difícil es resolver el issue, entonces seteale una dificultad. Ésto ayuda a que venga alguien atrás (como alguien que no tiene mucha idea) y pueda elegir los fáciles. Ó bien, le permite a alguien saber que va a necesitar dedicar más tiempo/cerebro a resolverlo.
```
Dificultad-MuyDificil
Dificultad-Dificil  
Dificultad-Regular  
Dificultad-Facil    
Dificultad-MuyFacil 
```
## Tema ##
Como algunas de los issues pueden ser tareas (Chores), puede ser que en el issue tracker aparezcan cosas que no requieran cambios de código. Por eso la diferenciación entre Documentación y Codificación.
```
Tema-Doc            
Tema-Code
```
## Tipo ##
Éste es otro tag importante: Define al issue. ¿Qué estoy describiendo?
```
Tipo-Bug``` (Es un error que hay que arreglar)
```
Tipo-Feature``` (Es una mejora / un requerimiento que no existe actualmente y se quiere agregar)
```
Tipo-Chore``` (Tarea general, que no es ni Bug ni Feature)

## Release ##
Por último, el release indica para qué momento el equipo decide poner el issue. En otras palabras, quien crea el issue, salvo que sepa muy bien lo que hace, no debe preocuparse por éste tag (no hace falta ponerlo).
```
Release-Verano2014 
```
# Ejemplos #
## Ejemplo Bug ##
Por ejemplo, tomemos el [issue 199](https://code.google.com/p/objectbrowserpharo/issues/detail?id=199). (Leer la descripción)

Tags:
  * Tipo-Bug -> Porque es algo que no anda en la app y debería andar (debería poder crear tests)
  * Priority-High -> Porque testear es parte importante de la herramienta, y no podemos usarla si esto no anda.
  * Tema-Code -> Porque se requiere codear para arreglarlo
  * Release-Verano2014 -> Porque decidimos que debe estar corregido para el inicio de clases 2014.

## Ejemplo Mejora/Feature ##
Por ejemplo, tomemos el [issue 189](https://code.google.com/p/objectbrowserpharo/issues/detail?id=189). (Leerlo)
  * Tipo-Feature -> Porque en el momento en el que se creó éste feature, no existía la posibilidad de imprimir una lección de manera legible para un humano. Era una sugerencia de algo que podía tener la herramienta.
  * Priority-Medium -> Porque, por un lado, Ozono puede existir sin ésto, pero por el otro, necesitamos ésto para poder corregir más fácilmente.
  * Release-Verano2014 -> Porque se decidió que éste nuevo feature debía estar para el inicio de clases de 2014
  * Tema-Code -> Porque para solucionarlo es necesario codear.

## Ejemplo Chore ##
Un ejemplo de Chore podría ser, por ejemplo, refactorizar una parte del código. Ésto no agrega funcionalidades ni es un error.

Otro ejemplo podría ser escribir cierta documentación, como el [issue 208](https://code.google.com/p/objectbrowserpharo/issues/detail?id=208).

