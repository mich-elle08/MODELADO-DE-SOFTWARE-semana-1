**MODELADO DE SOFTWARE**

Un diagrama de casos de uso muestra quién usa el sistema y para qué.



**Un actor: Monitos/muñequitos** es un rol, no una persona concreta. Si ANA es alumna y además encargada cuenta como DOS ACTORES. Los actores se dividen en dos tipos: primario--> inicia el caso de uso porque tiene un objetivo, interactúa directamente con el sistema y se beneficia del resultado

secundario---> Ayuda al primario a lograr su objetivo. No le interesa el resultado en si: cumple una función de apoyo.



**Caso de uso (cómo se nombra un caso de uso???): Óvalos**

|MAL NOMBRADO|PROBLEMA|BIEN NOMBRADO|
|-|-|-|

|Reservas|es un sustantivo, no tiene una accion|solicitar reserva|
|-|-|-|
|Click en guardar|Es un paso de la interfaz|solicitar reserva|
|Validar formulario|Es un paso interno de otro caso|Va dentro del flujo de solicitar reserva|
|Insert en tablas reservas|Es un lenguaje técnico|Solicitar reserva|

FORMULA: verbo en infinitivo+



De negocio o sistema: Un servicio que se ofrece a clientes, socios u otro tipo de sistemas. El usuario lo ve y lo pide

Caso de sistema: Una función interna que nadie ve. un proceso interno del sistema



**Frontera del sistema: Rectángulo que encierra los óvalos**

Un rectángulo con el nombre del sistema. Los casos de uso van dentro; los actores siempre fuera.

\----RELACIÓNES-----

1-Asociación: es una linea continua entre el actor y un caso de uso: el actor participa en este caso.

Solo une al actor con un caso de uso, Normalmente va sin flecha, Puede llevar una etiqueta como "+Procesa". Nunca une un actor con otro actor.



2-Generalización: (herencia) es un caso de uso en una versión más específica de otro. Línea contínua con triangulo vacío que apunta al general (padre).

También implica entre actores: Alumno y Docente heredan de solicitante.

**léelo como: "es un tipo de".** Cancelar reserva es un tipo de Gestionar mis reservas.



3-<<include>>: siempre ocurre

Un caso de uso invoca a otro cada vez que se ejecuta. Flecha punteada del caso base al caso incluido.

Sirve para no repetir un paso que comparten varios casos.

**léelo como: "Usa".** Solicitar reserva usa verificar disponibilidad. Sin el incluido, el base queda incompleto.



4-<<Extend>>: sólo bajo una condición.

Comportamiento Opcional que se agrega a otro caso cuando se cumple una condición. Flecha punteada de la extensión hacia el caso base.



<<include>> frente a <<extend>>

|**Pregunta**|**<<include>>**|**<<extend>>**|
|-|-|-|
|¿cuándo ocurre?|siempre||
||||
||||



5-Dependencia: Un elemento necesita a otro para funcionar bien. Flecha punteada del dependiente hacia el independiente.
A diferencia del include, el otro caso no se ejecuta dentro: solo tiene que haber ocurrido antes.

