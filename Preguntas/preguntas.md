# PREGUNTAS
## CLASE-1
### Que esperas del curso?
El último cuatrimestre estuve estudiando fundamentos de estadística por mi cuenta, intentando construir una base sólida sobre el tema que me permitiera trasladar esos conocimientos a problemas reales. Por este motivo, espero que esta materia pueda brindarme herramientas prácticas para poner a prueba lo aprendido. Me gustaría aprender aplicaciones concretas en contextos reales, abordando mecanismos y problemáticas más complejos que los ejercicios que suelen resolverse usando simplemente lapiz y hoja. También considero que esta cursada representa una buena oportunidad para repasar y consolidar los conocimientos que adquirí, dado que, en el contexto del paro que atravesamos, tuve que estudiar gran parte de los contenidos de forma autodidacta. Desde que cursé PLP, comencé a interesarme por distintos paradigmas de programación. Por eso, creo que este curso es una oportunidad para ampliar y profundizar ese conocimiento. Habiendo leído los primeros capítulos del libro que guiará la cursada, considero que podrian ser muy utiles
### Qué fue lo que más te llamó la atención del material?
Me resulta interesante y extraña esta forma de pensar los problemas. Creo que la comparación con el análisis de captchas refleja bien esta idea. Para resolver el problema dentro de este paradigma ya no es necesario contar con un gran conjunto previo de captchas etiquetados; el propio lenguaje permite generar la información necesaria y realizar la inferencia sobre la distribución subyacente.
Siento que esta propuesta tiene ciertas similitudes con Prolog. La idea de automatizar la inferencia bayesiana me recuerda a cómo Prolog realizaba deducciones lógicas a través de árboles de derivación para encontrar una respuesta. En ambos casos, el programador describe el problema y delega gran parte del proceso de inferencia al sistema. Creo que el verdadero poder de esta rama se encuentra justamente ahí, en la posibilidad de abstraernos de los mecanismos de inferencia y concentrarnos en la descripción del modelo o del problema que queremos resolver
### Qué fue lo que menos entendiste del material?
Dudas:
- No me termina de quedar clara la idea de iterar un modelo, significa probarlo con distintas observaciones?
- Tampoco termino de entender la idea de que el resultado de un programa probabilístico sea una distribución. Quizas me acostumbre a que la salida de un programa sea un valor único y no una distribución de probabilidades. No logro visualizar cómo se refleja esto en la práctica como resultado del programa
- una de las ideas de estos lenguajes es poder construir el modelo de forma declarativa o estática, a diferencia de los lenguajes de programación más convencionales? Esta duda surge especialmente a partir del último párrafo citado en la página 24
- Cómo hace el evaluador para mantener la información de los pesos, asociada a la probabilidad de X, y a su vez modifica las probabilidades a medida que se observan nuevos valores de Y?
- Qué ocurre cuando realizamos una gran cantidad de observaciones? Cómo impacta eso en el proceso de inferencia y en el uso de memoria?
### Qué te gustaría aprender hoy?
Poder ver en ejecucion ejemplos practicas, capaz una regresion lineal siempre es le mejor caso para analizar con respecto a a lenguajes por fuera de este paradigma. Tambien seria interesante poder ver mas sobre el mecanismo de inferencia oculto durante la ejecucion de este tipo de programas, me gustraia poder etender si el usuario puede manipular la forma en la que se realiza la inferencia.
Tambien me llama la atencion que no define un sistema de tipos, pese a que repite que ciertas expresiones deben ser de determinada forma, sino la expresion no tiene sentido durante la ejecucion.

## CLASE-2
### Qué fue lo que más te llamó la atención del material?
La forma de explicar la sintaxis es en cierta forma similar a como se suele abordar a los lenguajes funcionales, esto me parecio practico. Me parece curioso el hecho de limitar la recursion, teniendo en cuenta que estamos construyendo modelo sobre fenomenos probabilistioc, las posibilidades son infinitas, por lo tanto es entendible querer limitar la cantidad de pasos de ejecucion que se realizan.
Siento tambien que el algoritmo de evaluacion, para el metodo de likehodd, termina siendo relativamente sencillo para la implicacion y el poder que tiene en el paradigma.

### Qué fue lo que menos entendiste del material?
Creo que la seccion 4.1.1 es confusa, no termino de entender si me perdi algun formalismo importante en la demostracion dada, tal que al final termina derivando el metodo de likehood de manera muy sencilla. No se si solo hay que pensar que el metodo de likehood wighting solo es un caso de lo demostrado antes.
Con respecto el metodo de likehood, se habla que cuando se ejecuta se genera el likehood. Frente a multiples ejecuciones de lo mismo esto cambia? se guarda el registro de pesos de ejecuciones pasadas?
Si bien entiendo el proceso de actualizacion de pesos, no me termina de quedar claro que representa σ(log W), no nos importa el likehood por separado de cada valor sino lo que obtenemos de todos?

### Qué te gustaría aprender hoy?
Seria interesante poder entender la funcion de sample, en que se basa para tomar una muestra de un a distrbucion?
Por otro lado estaria bueno ver, con un programa sencillo, esta actualizacion de likehood durante la ejecucion de un programa.

## CLASE-3
### Qué fue lo que más te llamó la atención del material?
Me parece util e interesante la representacion grafica. Entiendo que es algo que no subre y el libro lo utiliza dado que un momento esa idea fue el pilar para esta reama, pero me fue practico para entender los conceptos de la seccion 3.2. No se si es para esta seccion, pero me llama la atencion como coexisten estos metodos tan sofisticados (likhood wrighting y MH) en el mismo ecosistema del lenguaje. Hasta la seccion anterior creo que entendia mejor como se podian resolver los problemas, la incorporacion de MH me lleva tener mas interes en lo que hay debajo de estos sistemas. 
Me parece, a su vez, una buena forma de optimizar, la reutilizacion de la funcion EVAL para ambos metodos

### Qué fue lo que menos entendiste del material?
En la ecuacion 3.11, por que en P(Y|X) no se hace referencia a las variables X? Debido a que estamos en el caso de todo lo observado?
En la ecucion 3.13, Al no tener data observdada, la expresion por la que se reemplaza es solo.
La funcion factor premite introducir el reemplaza de la funcion de likehood por una funcion arbitraria ante la falta de datos observados?
No se si termino de entenderlo lo propuesto en la unidad 4.2, en comparacion con metropolis hasting: Ambos metodos tienen el mismo objetivo pero ya no utiliza muestras del prior? A su vez en este metodo se toma tanto la densidad de del sample como de la observacion?

### Qué te gustaría aprender hoy?
Seria interesante pode introducir ejemplo de estas distrbuciones donde no se utiliza datos observados. Tambien considero importante incluir algun ejemplo sobre MH