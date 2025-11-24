# Capítulo 1: El Bug en Tu Cerebro

Era martes. Las 3 de la tarde. Llevaba seis horas sentado frente a la pantalla y no había avanzado nada. NADA. Tenía que implementar una feature que había estimado en dos días, y ya iba por el tercero. El cursor parpadeaba en la línea 247 del archivo. Mis ojos miraban el código, pero mi cerebro estaba en otro planeta.

Abrí Stack Overflow. Cerré Stack Overflow. Abrí Slack. Respondí tres mensajes que podían esperar. Volví al código. Leí la misma función cuatro veces sin entender qué hacía. Me serví más café. Volví a la pantalla.

"¿Qué me pasa?", pensé. "Antes era bueno en esto."

Resulta que no era el único. Y no era porque me estuviera volviendo peor programador. Era porque nadie me había explicado cómo funciona realmente el cerebro cuando programas.

## El descubrimiento que cambió todo

Dos años después de esa tarde horrible, leí un paper que me voló la cabeza. Un investigador alemán llamado Dr. Janet Siegmund hizo algo que nadie había hecho antes: metió programadores dentro de una máquina de resonancia magnética funcional (fMRI) y les pidió que hicieran code review mientras escaneaba sus cerebros.

¿Qué descubrió? Que cuando programas, se encienden CINCO áreas diferentes de tu cerebro simultáneamente:

1. La corteza frontal medial (la que procesa lenguaje natural)
2. La corteza prefrontal dorsolateral (memoria de trabajo)
3. La corteza parietal superior (atención)
4. El área de Broca (comprensión de sintaxis)
5. El córtex temporal (procesamiento semántico)

Para que te hagas una idea: cuando lees un libro, se activan dos o tres áreas. Cuando resuelves ecuaciones matemáticas, tres o cuatro. Cuando programas, CINCO. Al mismo tiempo.

Programar no es solo "pensar". Es ejecutar una sinfonía cognitiva con cinco secciones diferentes de tu orquesta neuronal, todas tocando al mismo tiempo, sin partitura.

No es de extrañar que a las 3 de la tarde mi cerebro dijera "hasta acá llegué, amigo".

## Tu cerebro no es una computadora

Durante años me comparé con mi laptop. Ella podía trabajar 24/7. Yo no. Ella no se cansaba después de seis horas de debugging. Yo sí. Ella podía mantener 47 tabs abiertas sin inmutarse. Yo perdía el hilo con tres.

"Tengo que mejorar mi rendimiento", pensaba, como si fuera un procesador que necesita más GHz.

Pero acá está el problema: tu cerebro NO es una computadora.

Una computadora ejecuta instrucciones de manera determinista. Tu cerebro es un órgano biológico que necesita glucosa, oxígeno, y descanso. Una computadora no tiene emociones. Tu cerebro está constantemente procesando señales de estrés, hambre, aburrimiento, entusiasmo. Una computadora puede hacer context switching en nanosegundos. Tu cerebro necesita 23 minutos para recuperar el foco después de una interrupción (pero eso lo vemos en el siguiente capítulo).

El neurocientífico Daniel Levitin lo explica así: "Tu cerebro consume el 20% de toda la energía de tu cuerpo, a pesar de representar solo el 2% de tu peso. Y cuando estás haciendo trabajo cognitivo intenso, ese consumo aumenta todavía más."

Cada vez que te sientas a programar, estás encendiendo el componente más costoso energéticamente de todo tu cuerpo. No es que seas débil. Es que estás haciendo triatlón cognitivo.

## Las cinco tareas simultáneas del programador

Volvamos al estudio de Siegmund. ¿Por qué se activan tantas áreas del cerebro cuando programas?

Porque estás haciendo cinco cosas a la vez:

**1. Comprender sintaxis (como aprender un idioma extranjero)**

Cuando lees `const users = await db.query('SELECT * FROM users')`, tu cerebro está parseando un lenguaje artificial. El área de Broca, la misma que usas para entender gramática, está trabajando full. Es como leer francés si tu lengua nativa es español: posible, pero requiere esfuerzo consciente.

**2. Mantener el contexto en memoria de trabajo**

Tu memoria de trabajo (working memory) puede mantener entre 4 y 7 "chunks" de información simultáneamente. Pero cuando programas, necesitas mantener en mente: qué hace esta función, qué hace la función que la llamó, qué estructura tiene el objeto que recibe, qué retorna, qué side effects puede tener, y qué esperan las funciones downstream.

Eso es fácilmente 10-15 chunks. Estás constantemente haciendo malabares con más bolas de las que tu cerebro puede sostener.

**3. Construir modelos mentales**

Para entender un sistema, no alcanza con leer el código línea por línea. Necesitas construir un modelo mental: una representación abstracta de cómo funciona todo. "Este servicio llama a la API, que actualiza la base de datos, que dispara un webhook, que..."

Esto activa tu corteza parietal. Es la misma área que usas para navegación espacial. Literalmente estás "navegando" por un espacio abstracto de relaciones entre componentes.

**4. Resolver problemas (la parte de puzzle)**

"¿Por qué este test falla?" "¿Cómo implemento esta lógica sin romper el resto?" Esto es resolución de problemas pura, y activa tu corteza prefrontal dorsolateral. La misma área que se ilumina cuando juegas ajedrez.

**5. Planificar y ejecutar (la función ejecutiva)**

Y encima de todo eso, tu cerebro está constantemente preguntándose: "¿Qué hago ahora? ¿Esto es prioritario? ¿Debería refactorizar esto o seguir adelante? ¿Cuánto tiempo me queda?"

Tu corteza prefrontal está haciendo de project manager mientras el resto de tu cerebro está en producción.

## La revelación

Cuando entendí esto, todo cambió.

No era que yo fuera mal programador. No era que "me faltara disciplina". No era que "antes era más inteligente".

Era que estaba pidiendo a mi cerebro que hiciera una de las tareas cognitivas más demandantes que existen, durante 8 horas seguidas, 5 días a la semana, sin darle las condiciones óptimas.

Es como pedirle a un maratonista que corra los 42 kilómetros sin tomar agua y después decirle "¿por qué tardaste tanto?".

El investigador Felienne Hermans, de la Universidad de Leiden, lo resume perfectamente: "Programar no es escribir código. Programar es pensar intensivamente sobre problemas abstractos y expresar esas soluciones en un lenguaje formal artificial. Es una de las actividades cognitivas más complejas que realizamos."

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

## Tres cosas que puedes hacer hoy

**1. Mide tu energía cognitiva**

Durante una semana, cada dos horas pregúntate: "Del 1 al 10, ¿cuánta energía mental tengo?". Anótalo. Al final de la semana vas a ver un patrón. Ahí están tus horas de oro. Úsalas para las tareas que requieren pensar, no para contestar emails.

**2. Respeta el límite de 90 minutos**

Tu cerebro trabaja en ciclos ultradianos de 90-120 minutos. Después de ese tiempo, la capacidad de concentración cae en picada. Programa un timer. A los 90 minutos: pará, levántate, caminá 5 minutos. No es negociable.

**3. Externaliza tu memoria de trabajo**

Antes de abrir el IDE, tomá un papel y escribí: "¿Qué voy a hacer? ¿Qué necesito recordar?". Puede ser una lista, un diagrama, lo que sea. El simple acto de escribirlo libera espacio en tu RAM mental.

---

Tu cerebro no es el problema. El problema es que nunca te enseñaron a usarlo.

Ahora ya lo sabés.
