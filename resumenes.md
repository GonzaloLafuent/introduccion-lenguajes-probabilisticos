# RESUMEN
## CLASE-1
La defincion se define como lenguajes de progamacion en si mas la oprtunidad de incorporar samples de un modelo mas las observaciones. la idea con esto es poder modelar un fenomeno porbabilistico y a arptir de eso poder inferir resultado de lo que se denomina variables latentes, variables que no podemos observar del modelo.

el simbolo mulito implica un sample, uan varibales era un sample de una determinada distrbucion. En el modelo de la calidad de escuela, esta variable no exite, pero asumimos que esta. Este problema se resuelve con python, generando un monton de informacion aleatoria. En este caso vamos  atener una aproximacion de la respuesta que buscamos.

Entonces por que este tipo de paradigma? que pasa si tengo una observacion mas, si en vez de ver la nota mayor a 120 tengo uno que sea exactamente 125. No voy a poder. Van a permitir resolver modelos mas complejos.

p(y|X) = funcion de verosimilitud. la probabilida de y obersevado X. Se puede conseguir informacion de X, donde se le puede asignar una distrbicuion. Bayes nos da una probabilida dde la variables latente dado y observado. En la practica nos imporata calcula esperanza, no nos importa la distribucion, pero esto es imposible. La idea es aproximar esas esperanzas. 

## CLASE-2
Teorema importante, ley de los grandes numeros (haces que ML funcione): supongamos que teneos varibales aleatorias X,..X_n, IID, donde la varianza y la esperanza es finita, entonces el limte de la sumatoria i= a n de x_i  sobre N, tiende a la esperanza de X, donde esa sumatoria es tambien X, una varible aletoria. 

Relacionado a esto tenemos: si tenemos de veulta la sumatoria de i=1 a n de x_i sobre N, si a esto el resto la esperanza de x_i.  esto es una forma de ver el error, yo se que esto va a dar 0. En ir a cero se puede pensar como que la compeljida de un algoritmo tiende a infitio, para poder ve esto se lo divida porx, de esta forma sabes que tu algirtmo es lineal. aca hacemos algo pareciod, como eso da 0 no se deivide por algo que da infito, sino que se multiplca por algo que da ingito.
Si multiplico eso por la raiz cuadra de N, lo caul va infito de forma mas lenta, eso tiene a N(0,varianza), tiende a una distribucion normal. Esto es el teorema central del limite. Por eso decidimo que si queremos reducir el error tenemos que aumentar la muenstras, cuanto? de forma cuadratica. 

nostros nos vamos a trbajar con una sola ejeuccion, sino que vamos a tener distrbuciones de ejecuciones de programas. Modelo grafico: se usaba mucho en otra epoca del machine learning.

las observadas son y son observadas, tenemos datos. la x es sobre la cula consulto. joint es la porbabilidad de las dos cosas, como logica tambien es una interseccion o un y logico. la evidencia es la integral, se inetgra sobre los que no esatn del lado de y. la probailida de Y, es la esperanza, donde X se distrbuye como p(X), de p(y|x). posteriror predictive se determina como, la probalidad de poder predicr valores de y habiendo observado y.

pregunta 3) respuesta b, nos falta la likehood, es super importante, nos falta ver dada lo que genremos si se parece a lo que observamos, es gran parte del trabajo. Lo que se uso en el ejemplo de los captchas es una gaussiana.una cosas imporatnte es que miimzs los errores cuadraticos, puede tener una interepretaciones probabilsiitica, y con eso podes tener un modelo bayesiano. 

cuando ejeuctamos la distrbicuion de X, cambia. estamos buscanod poder aproximar esperanzas. vamos a internear genrar samples, que se parezca a la sitrbucion a posteriori. 

modelo continuo: en un modelo cotniuo, no se puede evaluar un valor exacto. desde el punta de vista computacionla podes encontrar esot, pero si trabajdmos con reales de verad no encontramos esto. si nuestra varribale tiene distrbucion continua no puedo consultar por igual. Esto nos lleva a tener que usar otro modelo.

la idea de este lengauje es que el sample genra valores y el observe dice que un valor lo vi. si usamos un random como entras varibales tenemos un simulador hacia adlenta, pero si usamos observe tenemos que tener otro tipo de  interpretacion. 

para poder genra esto cada vez que vemos un sample genra una muestra, el observe no genre valores pero actualiza un score que se va a tener, este va ser un score del programa. la densidad es la funcion de de densidad de una distribucion evaluada. 

FOPL: tiene variables aletorias, pero antes de ejecutralo le deamos una cuota finita de variables aleatorias. 
HOPL: este no tiene un limite sobre las variables aleatorias.

los que poseen limites son los que mas se usan, por lo general los otros no tanto. El hechho de limitar varias cosas se da tal que ayudan a hacer mejor inferencia. 

pregunta 2 de la segunda parte, X e Y son variables aleatorias, el tema es que X se samplea, Y es la observacion. Tenemos mu y 3 observaciones de Y, Y es una vaibrale aletoria que tiene esa determinada dsitrbucion. Tecnciamnte son 4 pero 3 vimos el valor, sabemos que paso con ellas. 
Lo que lo hace una varibale aletoria es que viene de una dsitrbucion. 

notacion se menatica, dada un ambeinte global ro, una ambiente local l elestado de ifnerecia sigma y una xpresion e, esto se vellua a un valor v y a un nuevo estado de inferencia sigma prima. Define un ambientes global, todas las cosas dad por el sistema como funciones, en el local estan el resultado de los let. 
cuandos e hace un observe, a los sigma se os auemnta con el log density. 

en la regla, observe deveulve la suma de todos los le, hacemos un oberve de una ditrbucion del valor, calculaos la porbailiad de la densidad y lo devolvemos. en ese grafico cada uno de los posiles acciones puede tener un observe, por lo tanto siempre tiene la posibilidad de devolver un likehodd. lsuma de losg es la usma de los loafitmos de los liklyhodds. 