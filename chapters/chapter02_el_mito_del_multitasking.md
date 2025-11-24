# Capítulo 2: El Mito del Multitasking

Eran las 11 de la mañana y yo era una máquina de productividad. O eso creía.

Tenía abierto el IDE con el código de la nueva feature. En otra pantalla, Slack con tres conversaciones activas. En el teléfono, un email del PM preguntando por el status. Auriculares puestos, música sonando. Y cada 30 segundos, una notificación de algo.

"Estoy haciendo cinco cosas a la vez", pensaba orgulloso. "Soy multitasking."

A las 6 de la tarde revisé lo que había logrado: la feature estaba a medio hacer, había respondido mal dos mensajes en Slack (tuve que pedir disculpas después), el email al PM era confuso, y había introducido un bug que descubrí dos días después.

Había estado ocupado durante 7 horas. Pero no había hecho nada bien.

## La mentira que todos creímos

Hay un mito en la industria tech: la gente exitosa es la que puede hacer varias cosas al mismo tiempo. Los job postings piden "habilidad para gestionar múltiples prioridades". Los managers celebran a la persona que "puede atender diez bolas en el aire".

Multitasking suena a superpoder.

El problema es que no existe.

Sí, leíste bien. El multitasking, como nosotros lo entendemos, no es real. Lo que llamamos multitasking es en realidad algo mucho más costoso: task switching. Y es uno de los asesinos silenciosos de tu productividad.

## El estudio que lo cambió todo

En 2009, investigadores de Stanford liderados por el profesor Clifford Nass hicieron un estudio que sacudió todo lo que creíamos sobre multitasking.

Tomaron dos grupos: personas que hacían multitasking regularmente (chequeaban email mientras programaban, tenían múltiples tabs abiertas, respondían mensajes mientras estaban en meetings) y personas que preferían hacer una cosa a la vez.

¿La hipótesis? Que los multitaskers iban a ser mejores filtrando información irrelevante, cambiando entre tareas, y manejando memoria de trabajo.

¿El resultado? Exactamente lo contrario.

Los multitaskers crónicos fueron PEORES en todo. No podían filtrar información irrelevante. No podían cambiar eficientemente entre tareas. No podían organizar su memoria de trabajo tan bien.

Cliff Nass lo resumió así: "Los multitaskers crónicos son aspirados por cualquier estímulo irrelevante. No pueden mantener nada fuera. Todo les distrae."

En otras palabras: mientras más practicás multitasking, PEOR te volvés en eso.

Es como entrenar para un maratón corriendo en círculos. Estás sudando, estás cansado, pero no estás yendo a ningún lado.

## Los 23 minutos que te están costando tu carrera

Ahora viene la parte que realmente duele.

Gloria Mark es profesora en la Universidad de California, Irvine, y lleva más de 15 años estudiando cómo las personas trabajan con tecnología. Ella y su equipo hicieron un estudio donde siguieron a trabajadores de conocimiento (programadores, analistas, escritores) durante su día laboral.

Midieron cada interrupción. Cada vez que alguien checkeaba email. Cada vez que sonaba Slack. Cada vez que alguien cambiaba de ventana.

¿El hallazgo? Después de una interrupción, una persona tarda en promedio **23 minutos y 15 segundos** en volver completamente a la tarea original.

Veintitrés minutos.

No es que cuando tu compañero te toca el hombro para preguntarte algo "perdés 2 minutos". Es que perdés 23. Porque tu cerebro no puede hacer un switch instantáneo. Necesita tiempo para descargar el contexto de la tarea anterior, cargar el contexto de la nueva tarea, hacer esa tarea, y después volver a cargar TODO el contexto de lo que estabas haciendo.

Hagamos la matemática:

Si te interrumpen 6 veces en un día (y seamos honestos, es mucho más), estás perdiendo 138 minutos solo en recuperar el foco. Eso es más de dos horas. DOS HORAS de tu día laboral simplemente evaporadas en context switching.

Y ni siquiera contamos el tiempo de la interrupción en sí. Solo el tiempo de volver a concentrarte.

## El residuo de atención

Sophie Leroy, profesora en la Universidad de Minnesota, descubrió algo todavía más fascinante (y aterrador).

Cuando cambiás de una tarea a otra, tu cerebro no hace un corte limpio. Una parte de tu atención se queda "pegada" a la tarea anterior. Ella lo llama "attention residue" (residuo de atención).

Es como cuando estás en una reunión pero tu cerebro sigue pensando en el bug que estabas debuggeando. O cuando estás cenando pero tu mente sigue dándole vueltas al código que escribiste en la tarde.

El attention residue no solo te hace menos eficiente en la nueva tarea. También te agota más rápido.

Imaginate que tu cerebro es tu laptop. Cada vez que abrís una nueva app sin cerrar la anterior, consumís más RAM. Eventualmente todo se pone lento. Necesitás reiniciar.

Eso es tu cerebro en modo multitasking: 47 tabs abiertas, el ventilador a full, la batería muriéndose.

## La ilusión de estar haciendo mucho

Entonces, ¿por qué seguimos haciéndolo?

Porque multitasking se SIENTE productivo.

Cuando respondés un mensaje en Slack mientras debuggeás un issue, sentís que estás aprovechando el tiempo. "Mato dos pájaros de un tiro", pensás.

Pero esa sensación es una ilusión.

Un estudio de la Universidad de Utah encontró que la gente que multitaskea reporta sentirse más productiva, pero cuando miden su output real, es significativamente menor que la gente que hace una cosa a la vez.

Multitasking te da un hit de dopamina (porque estás "haciendo cosas"), pero destruye tu capacidad de hacer trabajo profundo.

Es como comer 10 snacks en vez de una comida completa. Sentís que estás comiendo todo el tiempo, pero al final del día tenés hambre y no tenés energía.

## El costo para tu código

Ahora hablemos del elefante en la habitación: ¿qué le pasa a tu código cuando estás en modo multitasking?

Un estudio de Microsoft Research analizó miles de commits y correlacionó los errores con el contexto en el que fueron escritos. ¿El hallazgo? El código escrito bajo condiciones de multitasking tenía significativamente más bugs.

Tiene sentido. Cuando tu atención está fragmentada:
- No pensás en edge cases
- No considerás el impacto en otras partes del sistema
- Nombrás variables como `temp2` porque no tenés energía mental para pensar un buen nombre
- No escribís tests (o escribís tests mediocres)
- Shippeás código a medio terminar porque "ya lo termino después"

Y después pasás el doble de tiempo debuggeando ese código. O peor: lo debuggea otro y pierde su tiempo por tu multitasking.

El código no es solo el producto de tu trabajo. Es un reflejo del estado de tu mente cuando lo escribiste.

Código escrito en flow: limpio, elegante, simple.
Código escrito en multitasking: confuso, con parches, frágil.

## Pero mi trabajo requiere estar disponible

"Está bien todo eso", me decís, "pero yo trabajo en un equipo. Si no respondo Slack, el equipo se bloquea. Si no estoy en las reuniones, pierdo contexto. Mi trabajo ES estar disponible."

Entiendo. Y es una trampa cultural en la que caímos todos.

Pero acá está la verdad incómoda: si vos estás siempre disponible para los demás, nunca estás disponible para tu trabajo más importante.

El investigador Cal Newport lo explica así: "La cultura de la disponibilidad constante crea la ilusión de productividad mientras destruye la capacidad de producir valor real."

La pregunta no es "¿cómo puedo responder más rápido?" La pregunta es "¿cuál es el trabajo que solo yo puedo hacer, y cómo protejo el tiempo para hacerlo?"

Porque respondiendo mensajes en Slack, cualquiera puede hacerlo. Resolviendo ese problema complejo que está en tu sprint, solo vos (o muy pocas personas) pueden.

## Los tres hábitos para proteger tu atención

Esto no es sobre volverse un ermitaño que no responde mensajes. Es sobre ser estratégico con el recurso más valioso que tenés: tu atención.

### 1. Bloques de tiempo protegido

Todos los días, sin excepción, bloqueá 2 horas en tu calendario para trabajo profundo. Puede ser de 9 a 11, de 14 a 16, la franja que sea. Pero que sea sagrada.

Durante esas 2 horas:
- Slack en "No molestar"
- Email cerrado
- Teléfono en modo avión o en otra habitación
- Auriculares puestos (con o sin música)

Y acá está el truco: avisale a tu equipo. "De 9 a 11 estoy en modo focus. A las 11 reviso mensajes." Al principio va a sentirse raro. A las dos semanas, tu equipo se adapta. Y tu productividad se dispara.

### 2. Batch processing para comunicación

En vez de responder mensajes a medida que llegan (que es la receta perfecta para vivir interrumpido), definí momentos específicos para comunicación.

Por ejemplo:
- 11:00 - 20 minutos de Slack
- 14:00 - 20 minutos de email
- 17:00 - últimos mensajes del día

Tres momentos. Una hora total. Es SUFICIENTE. Y tu equipo va a aprender que no respondés en tiempo real, pero que respondés de manera confiable.

La clave es: cuando estás en esos 20 minutos, estás 100% en comunicación. Respondés todo, con contexto, con atención. No mandás mensajes a medias mientras estás pensando en otra cosa.

### 3. El ritual de transición

Cuando NECESITES cambiar de tarea (porque a veces es inevitable), no lo hagas bruscamente.

Tomá 2 minutos entre tareas:
1. Escribí en un papel: "¿Qué estaba haciendo? ¿Qué sigue?"
2. Cerrá los ojos, tres respiraciones profundas
3. Abrí los ojos, leé lo que escribiste de la nueva tarea

Suena tonto. Funciona increíblemente bien. Porque le estás dando a tu cerebro permiso explícito para soltar el attention residue y cargar el nuevo contexto.

Es como hacer `git commit` antes de cambiar de branch. Guardás el estado, limpiás el working directory, y arrancás limpio.

## La verdad simple

No existe tal cosa como multitasking eficiente. Existe priorizar bien y trabajar con foco. Existe comunicar claramente cuándo estás disponible. Existe respetar tu atención como el recurso finito que es.

Cada vez que abrís Slack mientras estás debuggeando, le estás prendiendo fuego a 23 minutos de tu día.

Cada vez que "rápido chequeo este email" mientras estás en flow, estás reseteando el timer.

Cada vez que decís "solo atiendo esta meeting mientras termino este código", estás garantizando que ambas cosas salgan mal.

Tu cerebro no es un procesador multi-core. Es un procesador single-thread increíblemente poderoso.

Tratalo como tal.

## Tres acciones para esta semana

**1. El experimento de las 2 horas**

Elegí un día. Bloqueá 2 horas. Desconectate completamente. Hacé UNA tarea. Anotá cuánto lograste. Compará con tu día normal. La diferencia va a ser brutal.

**2. Medí tus interrupciones**

Durante un día, cada vez que te interrumpen (o vos mismo te interrumpís chequeando algo), hacé una marca en un papel. Al final del día, contá. Vas a sorprenderte. Y ese número es tu punto de partida para mejorar.

**3. Renegociá disponibilidad con tu equipo**

Hablá con tu team lead o con tu equipo: "Quiero hacer un experimento. De 9 a 11 voy a estar en modo focus total. Si hay algo urgente, me llaman. Si no, a las 11 estoy disponible." La mayoría de las veces van a decir que sí. Porque ellos también lo necesitan.

---

El multitasking no es un skill. Es un bug.

Y como todo bug, la solución es simple una vez que lo identificás.

Stop trying to do everything at once. Start doing one thing completely.

Tu cerebro te lo va a agradecer. Y tu código también.
