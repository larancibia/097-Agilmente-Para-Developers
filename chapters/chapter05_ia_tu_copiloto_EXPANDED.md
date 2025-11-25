# Capítulo 5: IA: Tu Copiloto, No Tu Piloto

La primera vez que GitHub Copilot completó una función entera por mí, sentí dos cosas simultáneamente: fascinación y terror.

Fascinación porque acababa de escribir un comentario explicando qué necesitaba, y la IA generó 20 líneas de código perfectamente válido. Código que me hubiera tomado 15 minutos escribir apareció en 2 segundos.

Terror porque pensé: "¿Acabo de volverme obsoleto?"

Dos años después, la respuesta es clara: no. Pero mi forma de trabajar cambió completamente.

## El estudio que nadie puede ignorar

En 2022, GitHub publicó un estudio con datos de millones de desarrolladores usando Copilot. El hallazgo central: los developers que usaban Copilot completaban tareas **55% más rápido** que los que no lo usaban.

Cincuenta y cinco por ciento.

No era un estudio pequeño. No era una demo controlada. Era data real, de gente real, haciendo trabajo real.

Pero acá está la parte interesante: la velocidad no era uniforme. Algunos developers eran 80% más rápidos. Otros apenas 20%. ¿La diferencia?

Los que mejor aprovechaban la IA no eran los que aceptaban cada sugerencia ciegamente. Eran los que sabían cuándo usarla y cuándo ignorarla.

Profundizando en los datos, GitHub encontró algo más: los developers más experimentados (10+ años) se beneficiaban MÁS de Copilot que los juniors. Lo opuesto a lo que muchos esperaban.

¿Por qué? Porque los seniors sabían exactamente qué estaban buscando. Podían evaluar rápidamente si una sugerencia era correcta. Y podían modificarla inteligentemente para que se adaptara a su contexto.

Los juniors, por otro lado, a veces aceptaban código que no entendían. Y eso creaba problemas a futuro.

## La IA no reemplaza pensar

Investigadores de Stanford (Peng et al., 2023) hicieron un estudio fascinante: midieron la calidad del código escrito con asistencia de IA versus sin ella.

¿El resultado? El código escrito con IA era igual de funcional. Pasaba los mismos tests. Pero cuando analizaron la seguridad, encontraron algo preocupante: los developers que usaban IA tendían a escribir código menos seguro.

¿Por qué? Porque confiaban demasiado. La IA sugería algo que se veía correcto, y ellos lo aceptaban sin pensarlo dos veces. No validaban inputs. No manejaban edge cases. No consideraban vectores de ataque.

La IA puede escribir código. Pero no puede (todavía) pensar en todas las implicaciones de ese código.

Esa sigue siendo tu responsabilidad.

El estudio fue más allá: pidieron a developers que explicaran el código que habían escrito con asistencia de IA. Los que aceptaron sugerencias ciegamente tenían dificultad explicando su propio código. Los que usaron IA como punto de partida pero lo modificaron conscientemente podían explicar cada línea.

La diferencia no es trivial. En seis meses, cuando ese código tiene un bug, ¿quién va a poder debuggearlo?

## Cuándo la IA es brillante

Después de dos años usando IA intensivamente, descubrí que hay categorías de tareas donde la IA es increíblemente útil:

### 1. Boilerplate

Todo ese código repetitivo que tenés que escribir pero que no requiere creatividad: getters/setters, constructores, mappers, DTOs.

Ahí la IA es oro. ¿Para qué perder 10 minutos escribiendo un mapper cuando la IA lo puede generar en 10 segundos?

Pero incluso acá: revisá el resultado. A veces la IA genera mappers que copian referencias en vez de clonar objetos. O que no manejan nulls. Son detalles, pero importan.

### 2. Patrones conocidos

Cuando necesitás implementar algo que es un patrón estándar: autenticación JWT, validación de formularios, manejo de errores básico.

La IA vio miles de implementaciones de esos patrones. Puede darte una implementación sólida en segundos.

Descubrí algo útil: en vez de pedirle "implementa autenticación JWT", soy más específico: "implementa autenticación JWT con refresh tokens, usando bcrypt para passwords, y validando el token en cada request". Más contexto = mejor resultado.

### 3. Traducción entre lenguajes/frameworks

"Necesito esta función de Python en JavaScript". "Quiero hacer esto que hacía en React pero en Vue".

La IA es excelente traduciendo lógica de un contexto a otro.

Pero cuidado: los idioms de un lenguaje no siempre se traducen bien a otro. La IA puede darte código JavaScript que es literalmente Python traducido, en vez de código JavaScript idiomático.

### 4. Tests

Escribir tests puede ser tedioso. La IA puede generar casos de test basándose en tu código, incluyendo edge cases que quizás no habías considerado.

Obviamente tenés que revisarlos. Pero como punto de partida, es excelente.

Un patrón que me funciona: escribo el primer test yo (para establecer el estilo y estructura). Después le pido a la IA que genere variaciones. Reviso cada una, las ajusto, las dejo.

### 5. Documentación

Pedirle a la IA que genere docstrings, comentarios, o README basándose en tu código. No va a ser perfecto, pero te da un 80% del trabajo hecho.

Y acá hay un bonus inesperado: si la IA no puede explicar claramente qué hace tu código, probablemente tu código es demasiado complejo. Es un test indirecto de claridad.

### 6. Refactoring mecánico

Cambiar nombres de variables consistentemente. Extraer funciones. Reorganizar imports. Tareas que son mecánicas pero tediosas.

La IA es excelente para esto. Es como tener un intern muy rápido haciendo el trabajo tedioso.

## Cuándo la IA es peligrosa

Pero también hay categorías donde la IA es activamente dañina:

### 1. Arquitectura y diseño

La IA no entiende tu sistema completo. No conoce las decisiones de diseño que tomaste hace 6 meses. No entiende las limitaciones de tu infraestructura.

Pedirle a la IA que "diseñe la arquitectura" es una receta para desastre. Puede darte algo que suena razonable pero que no encaja con tu contexto.

La arquitectura requiere entender tradeoffs. La IA puede enumerar opciones, pero no puede decidir qué es mejor para TU situación específica.

### 2. Debugging complejo

La IA puede sugerir fixes, pero sin entender realmente la causa raíz. Podés terminar aplicando un parche sobre un parche sobre un parche.

Debugging requiere entendimiento profundo del sistema. Eso todavía es 100% humano.

Experimento que hice: le mostré a ChatGPT un bug complejo. Me dio 5 sugerencias. Probé las 5. Ninguna funcionó. Porque todas atacaban síntomas, no la causa raíz. Tuve que debuggear yo, entender el sistema, encontrar el problema real.

### 3. Decisiones de performance

La IA puede escribir código que funciona. Pero ¿es eficiente? ¿Escala? ¿Tiene memory leaks?

Esas consideraciones requieren profiling, medición, entendimiento del runtime. La IA no hace eso.

Un ejemplo real: la IA me generó una función que funcionaba perfecto... con 10 elementos. Con 10,000 elementos era O(n²) y mataba el sistema. Porque no estaba pensando en performance, solo en corrección.

### 4. Lógica de negocio crítica

Si estás implementando algo que impacta dinero, seguridad, o datos sensibles, NO confíes ciegamente en la IA.

Cada línea que la IA sugiere en esos contextos necesita ser scrutinizada como si la hubiera escrito un junior con dos días de experiencia.

Porque eso es lo que es: código probabilístico basado en patterns. No hay garantías.

### 5. Contexto específico de tu dominio

La IA fue entrenada con código público de internet. Conoce patrones generales. No conoce las reglas específicas de tu industria, tu empresa, tu equipo.

Si tenés convenciones de naming específicas, arquitecturas custom, o restricciones particulares, la IA no las va a seguir automáticamente. Tenés que revisarlo todo.

## El riesgo del deskilling

Acá está el peligro más sutil: si usás la IA para TODO, dejás de aprender.

Un estudio de investigadores en MIT encontró que cuando las personas usan asistentes de IA constantemente, su propia habilidad para resolver esos problemas sin IA se deteriora.

Lo llaman "deskilling" (pérdida de habilidades).

Es como usar GPS todo el tiempo: eventualmente perdés la habilidad de navegar sin él. Y el día que se cae el GPS, estás perdido.

No estoy diciendo "no uses IA". Estoy diciendo: no la uses para TODO.

De vez en cuando, implementá algo completamente a mano. Resolvé un problema sin autocompletado. Escribí tests desde cero. Debuggeá sin pedirle ayuda a ChatGPT.

Mantené tus skills afilados.

Porque la IA es una herramienta increíble cuando la sabés usar. Pero si dependés completamente de ella, sos frágil.

Pienso en esto como ir al gimnasio. Podés usar máquinas (IA) para hacer ejercicio más eficiente. Pero si SOLO usás máquinas y nunca hacés nada sin asistencia, tus músculos estabilizadores se atrofian. Necesitás balance.

## El efecto Dunning-Kruger con IA

Hay un fenómeno que estoy viendo cada vez más: developers juniors que usan IA intensivamente y creen que saben más de lo que realmente saben.

El efecto Dunning-Kruger es cuando personas incompetentes sobreestiman su competencia. Con IA, esto se amplifica.

Un junior puede "escribir" código complejo con IA sin entenderlo realmente. El código funciona (a veces). Pasa los tests (algunos). Se ve profesional.

Pero cuando algo sale mal, o cuando necesitan modificar ese código, están perdidos. Porque nunca desarrollaron el modelo mental subyacente.

Es la diferencia entre saber usar un framework y entender programación. La IA te puede hacer productivo con un framework en días. Pero no te puede dar años de experiencia entendiendo conceptos fundamentales.

## La regla de oro

Después de mucha experimentación, llegué a esta regla simple:

**La IA sugiere. Yo decido.**

Nunca acepto una sugerencia de IA sin leerla y entenderla completamente. Si no entiendo qué hace una línea de código, no la uso. No importa que funcione.

Porque en 3 meses, cuando ese código tenga un bug, voy a tener que entenderlo. Y si nunca lo entendí desde el principio, voy a perder 10x el tiempo que "ahorré" al dejarlo que la IA lo escribiera.

La IA acelera la escritura. Pero no puede reemplazar el entendimiento.

Y agregué una regla adicional: si la IA genera algo que me sorprende (en el buen sentido), me detengo. Investigo por qué lo hizo así. Aprendo algo nuevo.

La IA puede ser tu profesor si prestás atención.

## Cómo uso IA efectivamente

Mi workflow actual:

### Para features nuevas

1. Pienso la arquitectura yo (papel y lápiz)
2. Escribo los tests principales yo (para forzarme a pensar en edge cases)
3. Dejo que la IA genere implementaciones boilerplate
4. Reviso cada línea, refactorizo lo que no me gusta
5. Los tests complejos o críticos los escribo yo

Este orden importa. Si dejo que la IA escriba la arquitectura primero, voy a estar sesgado por su solución. Prefiero pensar independientemente primero.

### Para debugging

1. Trato de resolver el problema yo durante 20-30 minutos
2. Si me trabo, le explico el problema a la IA (rubber ducking++)
3. Considero sus sugerencias, pero verifico cada una
4. Una vez que entiendo la causa raíz, implemento el fix yo

El tiempo que paso solo (20-30 min) es crítico. Es donde realmente aprendo. La IA es el backup, no el primer recurso.

### Para learning

1. Cuando aprendo algo nuevo, NO uso IA en las primeras implementaciones
2. Lucho con el problema, leo la documentación, cometo errores
3. Una vez que lo entiendo, AHORA uso IA para ir más rápido
4. Pero ya tengo el modelo mental

Esta es mi regla más importante. Aprender con IA desde el inicio es como usar calculadora para aprender aritmética. Podés hacer las operaciones, pero nunca desarrollás la intuición.

### Para code reviews

Algo que empecé a hacer: pasarle código a la IA y pedirle que lo critique. No para aceptar su crítica ciegamente, sino para ver perspectivas que quizás me perdí.

A veces encuentra cosas que yo no vi. A veces encuentra "problemas" que no son problemas en mi contexto. El punto es: una perspectiva adicional, para considerar.

## El futuro no es IA vs Humanos

Hay una narrativa popular: "La IA va a reemplazar a los programadores."

Es falsa. O al menos, incompleta.

Lo que va a pasar es: los programadores que usan IA efectivamente van a reemplazar a los que no.

Porque un desarrollador senior con IA puede hacer el trabajo de 3 desarrolladores senior sin IA. Pero un developer que solo sabe usar IA y no entiende lo que está haciendo no va a sobrevivir al primer bug complejo.

La IA amplifica tu habilidad. Si sos bueno, te hace excelente. Si sos mediocre y dependiente, te hace obsoleto.

Pienso en la IA como pensaba en Stack Overflow cuando apareció. Al principio, algunos dijeron "ahora cualquiera puede programar, los developers van a ser obsoletos". No pasó. Lo que pasó es que todos usamos Stack Overflow y nos volvimos más productivos.

La IA es Stack Overflow con esteroides. Un tool poderoso. Pero sigue siendo un tool.

## La IA y el flujo

Una cosa que descubrí: la IA puede ayudar con el flow o romperlo, dependiendo de cómo la uses.

**Ayuda con flow cuando:**
- Elimina tareas repetitivas que te sacan del flow
- Te da un scaffolding rápido para empezar (combate el blank canvas)
- Sugiere sintaxis que no recordás exactamente (elimina fricciones)

**Rompe flow cuando:**
- Constantemente estás evaluando si la sugerencia es correcta (te saca de la tarea)
- Generó código que no entendés y tenés que investigar qué hace
- Te hizo confiar en algo que estaba mal y ahora tenés que revertir

La clave es: usá IA para eliminar fricciones, no para reemplazar pensamiento.

Ajusté mi setup: Copilot sugiere, pero lo tengo configurado para que no sea demasiado agresivo. No quiero que autocomplete todo. Quiero que sugiera cuando le pido, no constantemente.

Esto mantiene mi cerebro en el driver's seat.

## Las preguntas que cambiarán tu uso de IA

Después de observar cómo diferentes developers usan IA, noté patrones. Los que la usan bien se hacen estas preguntas constantemente:

1. **"¿Entiendo qué hace este código?"**
   Si la respuesta es no, no avanzas hasta que entiendas.

2. **"¿Podría explicar esto en una code review?"**
   Si no podés defender el código en una discusión, no lo uses.

3. **"¿Esto es mejor que lo que yo hubiera escrito?"**
   A veces la IA genera algo peor. No aceptes sugerencias solo porque son automáticas.

4. **"¿Qué estoy aprendiendo de esto?"**
   Si no aprendés nada, estás perdiendo una oportunidad.

5. **"¿Podría hacer esto sin IA si necesitara?"**
   Si la respuesta es no, estás desarrollando dependencia peligrosa.

## Tres prácticas para esta semana

**1. El test de entendimiento**

Esta semana, cada vez que aceptés una sugerencia de IA, preguntate: "¿Puedo explicar línea por línea qué hace este código?". Si la respuesta es no, no lo uses. Tomá el tiempo de entenderlo o escribilo vos.

Llevá un contador. ¿Cuántas sugerencias aceptaste? ¿Cuántas rechazaste? ¿Cuántas modificaste? Esto te da awareness de cómo estás usando la herramienta.

**2. El día sin IA**

Elegí un día. Apagá Copilot, no uses ChatGPT, hacé todo manualmente. Va a ser más lento. Vas a recordar por qué la IA es útil. Pero también vas a recordar que podés funcionar sin ella.

Y vas a notar algo: algunas cosas que pensabas que necesitaban IA, en realidad no las necesitan. Estabas usando IA por default, no por necesidad.

**3. El audit de calidad**

Revisá código que escribiste con asistencia de IA hace un mes. ¿Está bien? ¿Tiene bugs que no tenía el código que escribiste manualmente? ¿Lo entendés ahora? Eso te va a dar feedback sobre cómo estás usando la IA.

Si encontrás que el código asistido por IA es consistentemente peor, estás usándola mal. Si es consistentemente mejor, estás usándola bien. Si es igual, quizás no la necesitás tanto como pensás.

---

La IA no es el enemigo. Pero tampoco es mágica.

Es una herramienta. Increíblemente poderosa, pero herramienta al fin.

Como toda herramienta, podés usarla bien o mal. Podés dejar que te amplifique o que te atrofie.

La diferencia está en una palabra: criterio.

La IA puede escribir código más rápido que vos. Pero no puede (todavía) tener el criterio de cuándo ese código es apropiado, cuándo es peligroso, cuándo hay un approach mejor.

Ese criterio es tuyo. Es lo que te hace valioso. Y es lo que ninguna IA puede reemplazar.

Usá la IA. Aprendé a usarla bien. Pero nunca dejes que piense por vos.

Porque en el mundo del futuro, el desarrollador más valioso no va a ser el que escribe código más rápido.

Va a ser el que toma las mejores decisiones.

Y esa sigue siendo una habilidad 100% humana.

Por ahora.
