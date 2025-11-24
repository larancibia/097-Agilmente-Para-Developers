# Capítulo 6: Programar como un Estoico

Eran las 3 de la mañana. Mi teléfono sonó. Alertas de PagerDuty explotando. Producción caída. Usuarios sin poder acceder. Y yo, medio dormido, con el corazón acelerado, pensando: "Todo es mi culpa."

Me conecté a la laptop. Los logs eran un desastre. El error no tenía sentido. El rollback no funcionaba. El equipo de infraestructura no respondía. Y cada minuto que pasaba, más dinero perdía la empresa.

Pánico. Puro pánico.

Dos horas después resolvimos el issue. No fue mi culpa (era un problema de red en el proveedor de cloud). Pero yo había gastado esas dos horas en un estado de ansiedad total que no me ayudó a resolver nada.

Seis meses después, otra alerta a las 3 AM. Misma situación. Pero esta vez fue diferente.

Esta vez había aprendido a programar como un estoico.

## Marco Aurelio nunca deployó a producción

Marco Aurelio fue emperador de Roma durante 19 años. Lideró guerras, enfrentó plagas, manejó traiciones, y lidió con política corrupta. Y en su tiempo libre, escribió "Meditaciones", un diario personal que hoy es uno de los textos fundamentales del estoicismo.

Spoiler: Marco Aurelio nunca hizo on-call. Nunca debuggeó un memory leak. Nunca vio un pipeline de CI/CD fallar.

Pero sus principios para manejar la adversidad son exactamente lo que necesitás cuando tu código está en llamas.

El estoicismo no es sobre reprimir emociones. Es sobre elegir sabiamente dónde poner tu energía.

## La dicotomía de control

El principio más importante del estoicismo, el que cambió mi vida profesional:

**Hay cosas que controlás, y hay cosas que no controlás. Tu serenidad depende de saber cuál es cuál.**

Epicteto, otro filósofo estoico, lo explicaba así: "Algunas cosas están en nuestro control y otras no. En nuestro control están la opinión, el impulso, el deseo, la aversión, y en una palabra, cualquier cosa que es nuestra propia acción. No están en nuestro control el cuerpo, la propiedad, la reputación, el cargo, y en una palabra, cualquier cosa que NO es nuestra propia acción."

Traducido a developer:

**Cosas que controlás:**
- Tu código
- Cómo reaccionás ante un problema
- Qué aprendés de un error
- Tus hábitos de trabajo
- Tu comunicación
- Cómo te preparás para lo inesperado

**Cosas que NO controlás:**
- Si tu código tiene bugs (todos los tienen)
- Si servicios externos fallan
- Si alguien aprueba tu PR o no
- Si la empresa decide pivotar y tirar tu trabajo de 3 meses
- Si te interrumpen en medio de flow
- Si te dan feedback duro

Cuando gastás energía preocupándote por cosas que no controlás, no cambiás el outcome. Solo te agotás.

## El on-call estoico

Volvamos a esa alerta de las 3 AM.

La primera vez, mi cerebro fue: "¿Por qué me pasa esto a mí? ¿Y si no puedo resolverlo? ¿Y si me echan? ¿Y si el sistema nunca vuelve?". Pánico sobre cosas que no controlaba.

La segunda vez, apliqué la dicotomía de control:

- ¿Puedo controlar que el sistema esté caído? No. Ya está caído.
- ¿Puedo controlar cómo investigo el problema? Sí.
- ¿Puedo controlar si la solución funciona al primer intento? No.
- ¿Puedo controlar qué tan sistemático soy al debuggear? Sí.

Entonces hice lo único que podía hacer: los pasos que estaban bajo mi control. Revisar logs. Hacer hipótesis. Testear. Comunicar al equipo.

El sistema volvió en 40 minutos. La mitad del tiempo que la primera vez. No porque fuera más inteligente, sino porque no desperdicié energía en ansiedad inútil.

## Amor fati: amar el legacy code

Hay otro concepto estoico que es puro oro para developers: amor fati. "Amor por el destino."

No es resignación. Es algo más radical: amar lo que es, incluyendo las cosas difíciles.

Nietzsche (que no era estoico pero adoptó esta idea) lo resumió: "Mi fórmula para la grandeza en un ser humano es amor fati: no querer nada diferente, ni hacia adelante, ni hacia atrás, ni en toda la eternidad."

En el contexto de programación: amar el legacy code.

Ya sé, ya sé. Suena imposible. Pero escuchame.

Ese sistema legacy de 10 años, sin tests, con nombres de variables como `temp2`, con lógica de negocio en los controllers, con 5 frameworks obsoletos...

Podés pasarte 8 horas al día maldiciendo al developer que lo escribió (probablemente renunció hace años y está en una playa). Podés quejarte en cada standup. Podés sentir resentimiento cada vez que lo ves.

O podés aceptar: "Este es el código que existe. Este es mi contexto. ¿Qué puedo hacer con esto?"

No estoy diciendo que no lo refactorices. Refactorizar es amor fati en acción: aceptás el estado actual y trabajás para mejorarlo incremental mente.

Lo que NO es amor fati: resentimiento perpetuo que te agota y no cambia nada.

## La práctica del premortem estoico

Los estoicos tenían una práctica llamada "premeditatio malorum": visualizar anticipadamente las cosas que pueden salir mal.

Suena negativo, pero es lo opuesto. Cuando mentalmente ensayás las adversidades, cuando vienen (y van a venir), no te toman por sorpresa.

Los Navy SEALs usan una versión de esto en su entrenamiento de resiliencia. Lo llaman "mental rehearsal": antes de una misión, visualizan todo lo que puede salir mal y cómo van a responder.

Como developer, podés hacer lo mismo:

**Antes de un deploy:**
"¿Qué puede salir mal? El deploy falla. Okay, ¿qué hago? Rollback. ¿Y si el rollback falla? Tengo el runbook. ¿Y si nada funciona? Escalo con el team lead."

**Antes de un code review:**
"¿Qué puede pasar? Puede que pidan cambios. Okay, es parte del proceso. ¿Y si me piden rehacer todo? Aprendí algo importante. ¿Y si soy demasiado sensible al feedback? Respiro, lo leo objetivamente."

**Antes de una demo:**
"¿Qué puede salir mal? La demo puede fallar. Okay, tengo un video de respaldo. ¿Y si hacen preguntas que no puedo responder? Digo 'buena pregunta, lo investigo y te respondo'."

No estás esperando que salga mal. Estás eliminando el miedo a que salga mal.

## Las tres disciplinas estoicas del desarrollo

Epicteto organizaba el estoicismo en tres disciplinas. Acá está mi versión para developers:

### 1. La disciplina del deseo (qué querés)

No desees cosas fuera de tu control. Suena obvio, pero cuántos de nosotros deseamos:
- "Que este bug no exista" (ya existe)
- "Que este proyecto no sea tan complejo" (ya lo es)
- "Que me aprueben este PR sin cambios" (no controlás eso)

En vez, desea cosas en tu control:
- "Voy a entender este bug profundamente"
- "Voy a encontrar la parte del proyecto donde puedo simplificar"
- "Voy a escribir este PR tan claramente que sea fácil de revisar"

Cambiar tu deseo cambia tu experiencia.

### 2. La disciplina de la acción (qué hacés)

Actuá virtuosamente: con excelencia, con justicia, con templanza, con coraje.

En código:
- Excelencia: escribir el mejor código que podés, no "lo suficiente para que pase"
- Justicia: tratar al próximo developer que lea tu código (que puede ser tu yo futuro) con respeto
- Templanza: no over-engineer, no hacer el refactor gigante cuando no es el momento
- Coraje: hacer el refactor difícil cuando SÍ es el momento, aunque sea intimidante

Cada línea de código es una acción. Cada acción refleja tu carácter.

### 3. La disciplina del juicio (cómo pensás)

Tus pensamientos sobre una situación determinan tu experiencia más que la situación misma.

Un test que falla no es una catástrofe. Es información.
Un bug en producción no es tu fracaso como persona. Es un evento que requiere respuesta.
Feedback duro en un PR no es un ataque. Es alguien invirtiendo tiempo en hacerte mejor.

Marco Aurelio escribió: "Si te duele algo externo, no es eso lo que te molesta, sino tu juicio sobre ello. Y eso está en tu poder borrarlo."

Tu código tiene bugs. Eso no puede cambiar (bugs son inevitables). Pero tu relación con esos bugs, eso SÍ podés elegir.

## Resiliencia en el sprint

Un sprint típico está lleno de estoicismo aplicado:

**Lunes:** Te asignan una tarea que estimaste en 2 días. Descubrís que es mucho más compleja. Tu PM no está contento.

Respuesta estoica: La complejidad ya existe. El enojo del PM ya existe. ¿Qué está en tu control? Comunicar claramente por qué es más complejo, renegociar el deadline o el scope, empezar a trabajar sistemáticamente en la solución.

**Miércoles:** Tu PR está en review hace dos días. Nadie lo revisa. Te estás bloqueando.

Respuesta estoica: No controlás cuándo otros tienen tiempo. Controlás tu comunicación. "Hey, estoy bloqueado, ¿alguien puede revisar esto hoy?". Si no, moverte a otra tarea mientras tanto.

**Viernes:** Hiciste una demo. Funcionó perfectamente. Alguien dijo "¿y por qué no hiciste [esta cosa obvio en retrospectiva]?"

Respuesta estoica: No controlás si otros van a cuestionar tus decisiones. Controlás cómo respondés: "Buen punto, no lo había considerado. Lo agrego al backlog" o "Lo consideré, descarté por X razón".

## La práctica del journaling técnico

Marco Aurelio escribió Meditaciones para sí mismo. Era su forma de procesar eventos, recordar principios, mantenerse centrado.

Hacé lo mismo con tu código.

Al final de cada día, 5 minutos, escribí:
- ¿Qué salió bien hoy?
- ¿Qué salió mal?
- ¿Qué estuvo en mi control?
- ¿Qué NO estuvo en mi control pero igual me frustró? (para reconocerlo y soltarlo)
- ¿Qué aprendí?

No tiene que ser elaborado. Bullet points son suficientes.

Pero ese acto de reflexión hace dos cosas:
1. Te ayuda a soltar el estrés del día
2. Te hace consciente de patrones (si todos los días te frustra lo mismo, tal vez hay algo que PODÉS cambiar)

## Tres prácticas para esta semana

**1. El ejercicio de la dicotomía**

La próxima vez que algo salga mal (y va a pasar), antes de reaccionar, tomá 30 segundos. Dividí un papel en dos columnas: "En mi control" y "Fuera de mi control". Escribí todo lo relacionado al problema.

Después, ponés tu energía 100% en la columna izquierda. La columna derecha: la aceptás.

**2. El amor fati de 5 minutos**

Elegí la parte del código que más odiás. Podés ser legacy, puede ser algo que escribiste vos hace 6 meses. Miralo por 5 minutos y preguntate: "¿Qué tiene de interesante este código? ¿Qué problema estaba resolviendo? ¿Qué puedo aprender de esto?"

No tenés que arreglarlo. Solo mirarlo sin juicio.

**3. El premortem del deploy**

Antes de tu próximo deploy (o PR, o demo), escribí: "¿Qué puede salir mal? ¿Cómo voy a responder?". Tres escenarios. Dos minutos.

Cuando algo salga mal (puede que no, pero si), vas a estar mentalmente preparado.

---

El estoicismo no te hace inmune al estrés. Te hace capaz de funcionar a pesar de él.

No elimina los problemas. Te enseña dónde poner tu energía para resolverlos.

No hace que el código sea perfecto. Te ayuda a aceptar que nunca lo será, y a mejorarlo igual.

Hace 2000 años, Marco Aurelio escribió: "Tenés poder sobre tu mente, no sobre los eventos externos. Reconocé esto, y encontrarás fuerza."

Hoy, deployando a producción, debuggeando a las 3 AM, o navegando legacy code, el principio es el mismo:

No podés controlar el código legacy que te tocó mantener. Pero podés controlar cómo lo mejorás.

No podés controlar si producción se cae. Pero podés controlar cómo respondés.

No podés controlar si tu carrera tiene obstáculos. Pero podés controlar si esos obstáculos te destruyen o te fortalecen.

Esa es la programación estoica.

Y una vez que la practicás, nunca más te sentís impotente frente al código.
