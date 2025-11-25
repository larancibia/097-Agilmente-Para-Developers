# Capítulo 1: El Bug en Tu Cerebro

Era martes. Las 3 de la tarde. Llevaba seis horas sentado frente a la pantalla y no había avanzado nada. NADA. Tenía que implementar una feature que había estimado en dos días, y ya iba por el tercero. El cursor parpadeaba en la línea 247 del archivo. Mis ojos miraban el código, pero mi cerebro estaba en otro planeta.

Abrí Stack Overflow. Cerré Stack Overflow. Abrí Slack. Respondí tres mensajes que podían esperar. Volví al código. Leí la misma función cuatro veces sin entender qué hacía. Me serví más café. Volví a la pantalla.

"¿Qué me pasa?", pensé. "Antes era bueno en esto."

Resulta que no era el único. Y no era porque me estuviera volviendo peor programador. Era porque nadie me había explicado cómo funciona realmente el cerebro cuando programas.

## El descubrimiento que cambió todo

Dos años después de esa tarde horrible, leí un paper que me voló la cabeza. Una investigadora alemana llamada Dra. Janet Siegmund hizo algo que nadie había hecho antes: metió programadores dentro de una máquina de resonancia magnética funcional (fMRI) y les pidió que hicieran code review mientras escaneaba sus cerebros.

El estudio, publicado en 2014 en la conferencia ICSE (International Conference on Software Engineering), fue revolucionario. Por primera vez teníamos evidencia empírica de qué áreas del cerebro se activan cuando programamos.

¿Qué descubrió? Que cuando programas, se encienden CINCO áreas diferentes de tu cerebro simultáneamente:

1. La corteza frontal medial (la que procesa lenguaje natural)
2. La corteza prefrontal dorsolateral (memoria de trabajo)
3. La corteza parietal superior (atención)
4. El área de Broca (comprensión de sintaxis)
5. El córtex temporal (procesamiento semántico)

Para que te hagas una idea: cuando lees un libro, se activan dos o tres áreas. Cuando resuelves ecuaciones matemáticas, tres o cuatro. Cuando programas, CINCO. Al mismo tiempo.

Programar no es solo "pensar". Es ejecutar una sinfonía cognitiva con cinco secciones diferentes de tu orquesta neuronal, todas tocando al mismo tiempo, sin partitura.

No es de extrañar que a las 3 de la tarde mi cerebro dijera "hasta acá llegué, amigo".

## La historia de John Carmack y el poder del cerebro descansado

John Carmack, el legendario programador detrás de Doom, Quake, y revoluciones técnicas en gráficos 3D, tiene una filosofía interesante sobre la programación. En una entrevista de 2013, explicó cómo trabaja en problemas complejos.

"No intento forzar soluciones", dijo. "Cuando estoy atascado en un problema realmente difícil, me voy. Literalmente dejo la oficina. Camino, juego con mis hijos, hago cualquier cosa menos pensar en el problema. Y casi siempre, la solución aparece cuando no la estoy buscando."

Carmack entendió intuitivamente algo que la neurociencia confirma: tu cerebro hace su mejor trabajo cuando no lo estás forzando.

En su época en id Software, Carmack era conocido por trabajar en "sprints" intensos de concentración total, seguidos de períodos de desconexión completa. No intentaba mantener 12 horas continuas de programación. Sabía que su cerebro tenía límites.

Y este es el tipo que escribió motores gráficos que cambiaron la industria de los videojuegos.

Si Carmack respeta los límites de su cerebro, tal vez nosotros también deberíamos.

## Tu cerebro no es una computadora

Durante años me comparé con mi laptop. Ella podía trabajar 24/7. Yo no. Ella no se cansaba después de seis horas de debugging. Yo sí. Ella podía mantener 47 tabs abiertas sin inmutarse. Yo perdía el hilo con tres.

"Tengo que mejorar mi rendimiento", pensaba, como si fuera un procesador que necesita más GHz.

Pero acá está el problema: tu cerebro NO es una computadora.

Una computadora ejecuta instrucciones de manera determinista. Tu cerebro es un órgano biológico que necesita glucosa, oxígeno, y descanso. Una computadora no tiene emociones. Tu cerebro está constantemente procesando señales de estrés, hambre, aburrimiento, entusiasmo. Una computadora puede hacer context switching en nanosegundos. Tu cerebro necesita 23 minutos para recuperar el foco después de una interrupción (pero eso lo vemos en el siguiente capítulo).

El neurocientífico Daniel Levitin, autor de "The Organized Mind", lo explica así: "Tu cerebro consume el 20% de toda la energía de tu cuerpo, a pesar de representar solo el 2% de tu peso. Y cuando estás haciendo trabajo cognitivo intenso, ese consumo aumenta todavía más."

Cada vez que te sientas a programar, estás encendiendo el componente más costoso energéticamente de todo tu cuerpo. No es que seas débil. Es que estás haciendo triatlón cognitivo.

## El estudio de Microsoft Research sobre carga cognitiva

En 2018, investigadores de Microsoft Research publicaron un estudio fascinante: analizaron la actividad cerebral de desarrolladores mientras trabajaban en tareas de programación de diferente complejidad.

Usaron EEG (electroencefalografía) para medir la "carga cognitiva" - básicamente, qué tan duro está trabajando tu cerebro en un momento dado.

Los hallazgos fueron reveladores:

1. **La carga cognitiva variaba enormemente según la tarea**: Leer código familiar tenía una carga baja. Entender código nuevo y complejo disparaba la carga a niveles máximos.

2. **La fatiga se acumula rápidamente**: Después de 2 horas de trabajo cognitivo intenso, la capacidad del cerebro para procesar nueva información disminuía significativamente.

3. **El context switching es devastador**: Cada vez que un desarrollador cambiaba de tarea (de código a email, de debugging a una reunión), había un pico masivo de carga cognitiva solo en el proceso de cambio.

Este estudio confirmó lo que muchos desarrolladores sienten pero no pueden articular: no todas las horas de trabajo son iguales. Una hora de deep work en código complejo consume mucha más energía mental que tres horas de tareas administrativas.

## Las cinco tareas simultáneas del programador

Volvamos al estudio de Siegmund. ¿Por qué se activan tantas áreas del cerebro cuando programas?

Porque estás haciendo cinco cosas a la vez:

### 1. Comprender sintaxis (como aprender un idioma extranjero)

Cuando lees `const users = await db.query('SELECT * FROM users')`, tu cerebro está parseando un lenguaje artificial. El área de Broca, la misma que usas para entender gramática, está trabajando full. Es como leer francés si tu lengua nativa es español: posible, pero requiere esfuerzo consciente.

Un estudio de 2017 de investigadores en MIT (Ivanova et al.) escaneó cerebros de programadores leyendo código en Python y encontró algo fascinante: el código NO activa las áreas del lenguaje de la misma forma que el lenguaje natural. En vez, activa una red de áreas asociadas con lógica y razonamiento matemático, ADEMÁS de algunas áreas de lenguaje.

Es como si tu cerebro tuviera que hacer malabares con dos sistemas diferentes simultáneamente: el sistema de lenguaje (para entender los nombres de variables, los comentarios, la estructura) y el sistema lógico-matemático (para entender qué hace realmente el código).

Por eso leer código es más agotador que leer un artículo de noticias, incluso si el artículo es más largo.

### 2. Mantener el contexto en memoria de trabajo

Tu memoria de trabajo (working memory) puede mantener entre 4 y 7 "chunks" de información simultáneamente. Este número, descubierto por el psicólogo George Miller en 1956 y confirmado por décadas de investigación posterior, es un límite fundamental del cerebro humano.

Pero cuando programas, necesitas mantener en mente: qué hace esta función, qué hace la función que la llamó, qué estructura tiene el objeto que recibe, qué retorna, qué side effects puede tener, y qué esperan las funciones downstream.

Eso es fácilmente 10-15 chunks. Estás constantemente haciendo malabares con más bolas de las que tu cerebro puede sostener.

Investigadores en Carnegie Mellon University (Pane & Myers, 1996) encontraron que los programadores pasan aproximadamente 60% de su tiempo simplemente tratando de entender qué hace el código existente. No escribiendo código nuevo. No diseñando arquitecturas. Solo intentando mantener el modelo mental de lo que ya existe.

Y cada vez que pierdes ese modelo mental (una interrupción, una distracción, un cambio de contexto), tienes que reconstruirlo desde cero. Eso puede tomar 10-15 minutos de relectura y reconexión de piezas.

### 3. Construir modelos mentales

Para entender un sistema, no alcanza con leer el código línea por línea. Necesitas construir un modelo mental: una representación abstracta de cómo funciona todo. "Este servicio llama a la API, que actualiza la base de datos, que dispara un webhook, que..."

Esto activa tu corteza parietal. Es la misma área que usas para navegación espacial. Literalmente estás "navegando" por un espacio abstracto de relaciones entre componentes.

Neurocientíficos como Barbara Tversky en Stanford han demostrado que cuando pensamos en sistemas abstractos, nuestro cerebro usa metáforas espaciales. Por eso los buenos diagramas ayudan tanto: estás externalizando un modelo mental espacial que tu cerebro está tratando de construir internamente.

He visto desarrolladores senior que pueden "caminar" mentalmente a través de un codebase como si fuera un edificio físico. "El módulo de autenticación está 'arriba' en el stack, conecta 'hacia abajo' con la base de datos..." Estas no son metáforas casuales. Es literal mente cómo tu cerebro representa la arquitectura.

### 4. Resolver problemas (la parte de puzzle)

"¿Por qué este test falla?" "¿Cómo implemento esta lógica sin romper el resto?" Esto es resolución de problemas pura, y activa tu corteza prefrontal dorsolateral. La misma área que se ilumina cuando juegas ajedrez.

Un estudio de 2014 (Sherin et al.) en UC Berkeley analizó a programadores resolviendo bugs y encontró algo interesante: los mejores debuggers no eran los que tenían más conocimiento técnico. Eran los que tenían mejor capacidad para formar y testear hipótesis sistemáticamente.

Es casi científico: observas un comportamiento, formas una hipótesis sobre la causa, diseñas un experimento (un cambio en el código o un log adicional) para testear la hipótesis, observas el resultado, y refinás tu modelo.

Los programadores excepcionales hacen esto instintivamente. Los promedio saltan de solución en solución sin un modelo claro de qué están testeando.

Y hacer este proceso científico, mentalmente, mientras mantienes todo el contexto del sistema, mientras comprendes sintaxis, mientras navegas la arquitectura... es AGOTADOR.

### 5. Planificar y ejecutar (la función ejecutiva)

Y encima de todo eso, tu cerebro está constantemente preguntándose: "¿Qué hago ahora? ¿Esto es prioritario? ¿Debería refactorizar esto o seguir adelante? ¿Cuánto tiempo me queda?"

Tu corteza prefrontal está haciendo de project manager mientras el resto de tu cerebro está en producción.

Esta es la "función ejecutiva" del cerebro, y es particularmente vulnerable a la fatiga. Cuando estás cansado, tu capacidad de planificar, priorizar, y mantener disciplina se derrumba primero.

Por eso al final de un día largo, es más probable que:
- Tomes atajos que sabés que no deberías tomar
- Saltes tests "para ir más rápido"
- Hagas commits de código a medio terminar
- Digas "ya lo arreglo después"

No es falta de profesionalismo. Es que la parte de tu cerebro responsable de decisiones a largo plazo está exhausta.

## La revelación de Linus Torvalds

Linus Torvalds, el creador de Linux, tiene una filosofía interesante sobre productividad. En una conversación pública en 2016, alguien le preguntó cuántas horas al día programaba.

Su respuesta: "Si estoy programando más de 4-5 horas al día, algo está mal."

Espera, ¿qué? El tipo que mantiene el kernel de Linux, usado en billones de dispositivos, ¿trabaja solo 4-5 horas al día?

Torvalds explicó: "La programación real, el trabajo duro de diseño y pensamiento, no puedo hacerlo más de unas pocas horas. El resto del tiempo estoy leyendo código, respondiendo emails, revisando patches. Eso es importante, pero no es el trabajo cognitivo pesado."

Él distingue entre "trabajo duro" (deep work, diseño, arquitectura, resolver problemas complejos) y "trabajo necesario" (comunicación, review, mantenimiento). El primero tiene un límite diario estricto. El segundo puede extenderse.

Esta distinción es crucial. No todas las horas de trabajo son cognitivamente equivalentes.

## La revelación

Cuando entendí esto, todo cambió.

No era que yo fuera mal programador. No era que "me faltara disciplina". No era que "antes era más inteligente".

Era que estaba pidiendo a mi cerebro que hiciera una de las tareas cognitivas más demandantes que existen, durante 8 horas seguidas, 5 días a la semana, sin darle las condiciones óptimas.

Es como pedirle a un maratonista que corra los 42 kilómetros sin tomar agua y después decirle "¿por qué tardaste tanto?".

El investigador Felienne Hermans, de la Universidad de Leiden, lo resume perfectamente: "Programar no es escribir código. Programar es pensar intensivamente sobre problemas abstractos y expresar esas soluciones en un lenguaje formal artificial. Es una de las actividades cognitivas más complejas que realizamos."

En su libro "The Programmer's Brain" (2021), Hermans profundiza en esta idea. Documenta estudios donde programadores novatos y expertos resuelven el mismo problema, y analiza qué pasa en sus cerebros.

La diferencia no es que los expertos sean "más inteligentes". Es que tienen mejores "chunks" mentales - patrones que reconocen instantáneamente. Cuando un experto ve un patrón familiar (un loop, un patrón de diseño, una estructura de datos común), lo procesa como una unidad. Un novato tiene que procesar cada línea individualmente.

Es como leer. Un lector experto ve la palabra "programación" y la reconoce instantáneamente. Un niño aprendiendo a leer tiene que decodificar cada letra: p-r-o-g-r-a-m-a-c-i-ó-n.

Pero incluso para los expertos, código nuevo y complejo requiere procesamiento línea por línea. Y eso agota la capacidad cognitiva rápidamente.

## El mito del "rockstar developer"

Hay una narrativa tóxica en la industria tech: el "10x developer" que programa 12 horas al día, vive en la oficina, duerme poco, y produce código brillante constantemente.

Esta narrativa es dañina por dos razones:

1. **Es mayormente falsa**: Los estudios sobre productividad de desarrolladores (como el de Laurent Bossavit en "The Leprechauns of Software Engineering") muestran que la variación en productividad raramente es 10x, y cuando lo es, NO se debe a trabajar más horas.

2. **Ignora la sostenibilidad**: Conozco varios "rockstar developers" de hace 10 años. La mitad dejó la programación por burnout. La otra mitad ahora trabaja horarios normales y es mucho más productiva.

Bill Gates, en su época en Microsoft, tenía una política curiosa: se tomaba dos "Think Weeks" al año. Una semana completa, dos veces al año, donde se aislaba en una cabaña sin distracciones, solo para leer y pensar.

Nada de código. Nada de emails. Solo pensamiento profundo.

Muchas de las decisiones estratégicas más importantes de Microsoft salieron de esas Think Weeks.

Si Gates, conocido por su ética de trabajo brutal, reconocía el valor de parar y pensar... tal vez hay algo ahí.

## ¿Y ahora qué?

La buena noticia es que una vez que entiendes cómo funciona tu hardware, puedes optimizar tu software.

Si sabes que tu cerebro consume energía como un motor V8, puedes:
- Darle el combustible correcto (no, RedBull no cuenta)
- Respetar los tiempos de descanso (sí, son necesarios)
- Diseñar tu ambiente para minimizar el gasto cognitivo innecesario

Si sabes que tu memoria de trabajo tiene límites, puedes:
- Escribir funciones pequeñas que quepan en tu cabeza
- Hacer diagramas antes de codear
- Usar tests para externalizar el "estado" en vez de mantenerlo todo en tu mente

Si sabes que el context switching te cuesta caro, puedes:
- Proteger bloques de tiempo profundo
- Apagar notificaciones
- Decir "no" a más reuniones

No se trata de ser un programador 10x. Se trata de entender que tu cerebro es tu herramienta más valiosa, y que como toda herramienta, tiene un manual de uso.

Ese manual existe. Se llama neurociencia.

Y en los próximos capítulos vamos a leerlo juntos.

## La historia de DHH y los límites conscientes

David Heinemeier Hansson (DHH), creador de Ruby on Rails y fundador de Basecamp, es vocal sobre trabajar menos horas.

En su libro "It Doesn't Have to Be Crazy at Work" (co-escrito con Jason Fried), documenta cómo Basecamp tiene una política de 40 horas semanales. No 50. No "40 pero en realidad 60". Cuarenta.

Y durante el verano, trabajan 32 horas (4 días a la semana).

¿El resultado? Basecamp es rentable, tiene millones de usuarios, y sus empleados tienen vidas fuera del trabajo.

DHH argumenta que los límites te fuerzan a priorizar. Cuando sabes que solo tienes 8 horas, no las desperdicias en meetings innecesarias o features que nadie pidió. Haces lo que realmente importa.

Es la Ley de Parkinson invertida: "El trabajo se expande para llenar el tiempo disponible." Si te das 60 horas para algo, te va a tomar 60 horas. Si te das 40, encontrarás la forma de hacerlo en 40.

El secreto no es trabajar más. Es eliminar todo lo que no es esencial.

## Tres cosas que puedes hacer hoy

### 1. Mide tu energía cognitiva

Durante una semana, cada dos horas pregúntate: "Del 1 al 10, ¿cuánta energía mental tengo?". Anótalo. Al final de la semana vas a ver un patrón. Ahí están tus horas de oro. Úsalas para las tareas que requieren pensar, no para contestar emails.

Vas a descubrir algo interesante: tu energía mental no es constante. Tiene picos y valles. Y esos picos son diferentes para cada persona.

Algunos tienen pico de energía de 9 AM a 11 AM. Otros de 9 PM a 11 PM. No hay correcto o incorrecto. Solo TU patrón.

Una vez que lo conoces, protégelo con tu vida. Esas horas son oro puro.

### 2. Respeta el límite de 90 minutos

Tu cerebro trabaja en ciclos ultradianos de 90-120 minutos. Este ritmo fue descubierto por el investigador Nathan Kleitman en los años 1960s, y ha sido confirmado por décadas de investigación en cronobiología.

Después de 90 minutos de trabajo cognitivo intenso, la capacidad de concentración cae en picada. No es falta de voluntad. Es biología.

Programa un timer. A los 90 minutos: para, levántate, camina 5 minutos. No es negociable.

Vas a sentir que "estoy en un buen momento, no quiero parar". Pará igual. Porque si empujas más allá de ese límite, las próximas horas van a ser significativamente menos productivas.

Dos sesiones de 90 minutos con descanso intermedio son mucho más productivas que una sesión de 3 horas continua.

### 3. Externaliza tu memoria de trabajo

Antes de abrir el IDE, toma un papel y escribí: "¿Qué voy a hacer? ¿Qué necesito recordar?". Puede ser una lista, un diagrama, lo que sea. El simple acto de escribirlo libera espacio en tu RAM mental.

Esto se llama "carga cognitiva externa" y hay estudios que muestran su efectividad. Cuando externalizas información (a papel, a un diagrama, a un test), tu cerebro ya no tiene que mantenerla activamente en memoria de trabajo.

Es como hacer swap en tu computadora: mueves datos de la RAM limitada a almacenamiento externo.

Los mejores programadores que conozco todos tienen libretas llenas de diagramas, listas, y garabatos. No es porque no puedan recordar las cosas. Es porque entienden que su memoria de trabajo es limitada, y prefieren usarla para pensar, no para recordar.

---

Tu cerebro no es el problema. El problema es que nunca te enseñaron a usarlo.

Ahora ya lo sabés.

El siguiente capítulo es sobre el mito del multitasking. Porque una vez que entendés cómo funciona tu cerebro, el siguiente paso es entender por qué intentar hacer varias cosas a la vez es la forma más eficiente de destruir tu productividad.

Pero por ahora, solo recor dá esto:

Tu cerebro es la máquina más sofisticada del universo conocido. 86 mil millones de neuronas. 100 billones de conexiones sinápticas. Capaz de creatividad, abstracción, y resolución de problemas que ninguna computadora puede replicar.

Pero tiene límites. Físicos, biológicos, innegables.

Respetá esos límites, y tu cerebro va a hacer cosas increíbles.

Ignoralos, y vas a pasar tardes enteras mirando la línea 247 de un archivo, preguntándote qué te pasa.

La diferencia entre un programador que lucha constantemente y uno que fluye no es talento.

Es entendimiento.

Y ahora vos entendés.


## Apéndice Capítulo 1: Herramientas Prácticas para Gestionar Tu Working Memory

Ahora que entendés los límites de tu working memory, acá están las herramientas específicas que uso para trabajar con (no contra) esas limitaciones:

**1. El Stack de Contexto en Papel**

Cuando estoy debuggeando algo complejo o diseñando una arquitectura:
- Uso un papel (sí, papel físico)
- Dibujo el stack de lo que estoy pensando
- Cada "nivel" es una abstracción
- Cuando llego a 5-7 niveles, sé que necesito simplificar

Ejemplo debuggeando un bug:
1. Usuario reporta error X
2. Error viene del endpoint Y
3. Endpoint llama servicio Z
4. Servicio consulta DB con query Q
5. Query asume constraint C
6. Constraint violado por data D

Siete niveles. Puedo mantenerlo en papel. No puedo mantenerlo solo en mi cabeza.

**2. La Técnica del "Rubber Duck Debugging" Mejorada**

El rubber duck tradicional: explicar tu código a un patito de goma.

Mi versión: escribir la explicación. Por qué escribir > hablar:
- Fuerza más claridad (writing is thinking)
- Queda registro (para próxima vez que olvidás)
- Identificás gaps más fácil

Cuando estoy trabado en un problema por >30 minutos, escribo:
"El problema es: [descripción]
Lo que ya probé: [lista]
Lo que estoy asumiendo: [lista]
Lo que no entiendo todavía: [lista]"

El 70% de las veces, writing the problem clarifies the solution.

**3. El Working Memory Checkpoint**

Cada 90 minutos de trabajo profundo, hago un checkpoint:
1. Escribo en 2-3 oraciones: ¿en qué estaba trabajando?
2. ¿Qué decisiones tomé y por qué?
3. ¿Qué está pending para próxima sesión?

Takes 2 minutos. Pero cuando vuelvo (después del break o al día siguiente), no gasto 20 minutos "reloading context".

Es como hacer commit no solo del código sino del estado mental.

**4. La Regla del "Offload Everything"**

Si no necesito recordarlo, no lo recuerdo. Lo escribo.

- Ideas que aparecen mid-work: a un inbox (not ahora, después)
- TODOs: en un task manager, not en mi cabeza
- Datos que necesito referencia: en docs, not en memoria
- Decisiones: en decision logs

Mi cerebro es para pensar, no para storage. Storage es para disk.

**5. El Patrón de Zoom Levels**

Cuando trabajo en algo complejo, alterno entre 3 niveles de zoom:

Zoom Out (Big Picture): ¿Qué problema estoy resolviendo? ¿Por qué importa?
Zoom Medium (Architecture): ¿Cómo se conectan las piezas?
Zoom In (Implementation): ¿Cómo implemento esta pieza específica?

Work en un nivel durante 15-30 min. Después, zoom out or zoom in.

Por qué funciona: working memory se satura trabajando en un solo nivel demasiado tiempo. Cambiar niveles "refresca" tu capacidad cognitiva.

**6. La Técnica del "Think in Chunks"**

En vez de pensar en todos los pasos de una task, pienso en chunks lógicos.

No: "necesito hacer paso 1, después paso 2, después 3, 4, 5, 6, 7..."
Sí: "necesito hacer setup, después implementation, después testing, después deployment"

4 chunks > 7 pasos individuales para working memory.

Después, cuando estoy en "implementation chunk", subdivido: "backend, frontend, integration".

Pero nunca mantengo más de 5-7 cosas a la vez.

**7. El "Context Switch Tax" Log**

Durante una semana, cada vez que te interrumpen o switcheás contexto, anotá:
- Hora
- De qué a qué switche taste
- Cuánto tiempo te tomó volver a estar productivo

Al final de la semana, suma el context switch tax total.

Typical resultado: 8-12 horas perdidas por semana solo en context switches.

Ese awareness es devastador. Y motivador. Porque ahora sabés exactamente cuánto te cuesta cada "solo una pregunta rápida".

**8. La Matrix de Complejidad Cognitiva**

No todas las tareas consumen igual working memory. Aprendé a categorizar:

Low WM (working memory):
- Code reviews simples
- Documentation
- Tests straightforward
- Refactors mecánicos

Medium WM:
- Feature implementations standard
- Bug fixing moderate
- Code reviews complex
- System integration

High WM:
- Architecture design
- Debugging obscure issues
- Performance optimization
- System refactors

Hacé high WM tasks cuando tu cerebro está fresh (primer bloque de deep work).
Medium WM en segundo bloque.
Low WM cuando estás cansado o después de context switches.

No desperdicies tu cerebro fresh en low WM tasks. Es mal use de recursos.

Estos no son hacks. Son respeto por cómo tu cerebro funciona. Working memory es tu recurso más limitado como developer. Tratalo como tal.
