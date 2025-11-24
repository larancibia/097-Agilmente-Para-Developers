# Capítulo 7: El Código Simple Gana

Había pasado tres meses construyendo el sistema de reportes más sofisticado que había hecho en mi vida. Patrones de diseño por todos lados: Factory, Strategy, Observer, Decorator. Abstracciones sobre abstracciones. 47 clases. 10,000 líneas de código. Era hermoso. Era arquitectura pura.

Y era completamente imposible de mantener.

Seis meses después, cuando tuve que agregar una feature simple (un nuevo tipo de reporte), me tomó dos semanas. Dos semanas para algo que debería haber sido dos horas. Porque tenía que navegar por 8 capas de abstracción, entender 15 interfaces, y modificar código en 12 archivos diferentes.

Un developer nuevo en el equipo lo miró y dijo: "No entiendo qué hace esto."

Yo tampoco. Y yo lo había escrito.

Un año después, lo refactorizamos. 10,000 líneas se convirtieron en 500. Las 47 clases se convirtieron en 7. Todas las abstracciones elegantes: eliminadas.

¿El resultado? Hacía exactamente lo mismo. Pero ahora cualquiera podía entenderlo en 20 minutos. Y agregar features tomaba horas, no semanas.

Ahí aprendí una de las lecciones más importantes de mi carrera: simple siempre gana.

## El estudio que destruyó mi ego

Investigadores en la industria de software han estado estudiando complejidad de código durante décadas. Y todos los estudios llegan a la misma conclusión brutal:

**La complejidad del código correlaciona directamente con la cantidad de bugs.**

Un estudio de Microsoft Research analizó miles de módulos en Windows, Office, y otros productos. Midieron la complejidad ciclomática (cuántos caminos de ejecución tiene el código) y correlacionaron con bugs reportados.

La correlación era casi perfecta: a mayor complejidad, exponencialmente más bugs.

No era lineal. Era exponencial. Un módulo dos veces más complejo no tenía el doble de bugs. Tenía cinco veces más bugs.

¿Por qué? Porque los humanos no podemos mantener sistemas complejos en nuestra cabeza. Nuestro working memory tiene límites (acordate del Capítulo 1). Cuando el código excede esos límites, empezamos a cometer errores.

El código complejo no es un signo de inteligencia. Es un signo de no entender los límites de tu propio cerebro.

## Wu Wei: la acción sin esfuerzo

Hay un concepto en el taoísmo chino que me voló la cabeza cuando lo descubrí: Wu Wei (無為).

Se traduce como "no-acción" o "acción sin esfuerzo". Pero no significa no hacer nada. Significa hacer solo lo necesario, de la forma más natural posible, sin forzar.

Es el agua fluyendo alrededor de una piedra en vez de tratar de atravesarla. Es el bambú doblándose con el viento en vez de resistirlo y quebrarse.

Aplicado a código: no agregues complejidad solo porque podés. Agregá solo lo que el problema realmente necesita.

El Tao Te Ching dice: "Para lograr conocimiento, agregá cosas todos los días. Para lograr sabiduría, quitá cosas todos los días."

En código, la sabiduría no es cuántos patrones conocés. Es cuántos podés evitar usar.

## La paradoja de la simplicidad

Acá está lo irónico: escribir código simple es más difícil que escribir código complejo.

Cualquiera puede agregar una abstracción. Toma 10 minutos crear una interface nueva, un factory, una capa de indirección.

Pero escribir código que sea simple, directo, y que resuelva el problema exacto sin más ni menos... eso requiere pensar profundamente.

Blaise Pascal escribió en 1657: "Habría escrito una carta más corta, pero no tenía tiempo." (Es la carta más famosa donde alguien se disculpa por escribir algo largo.)

Lo mismo pasa con el código. Escribir 1000 líneas es fácil. Escribir 100 líneas que hagan lo mismo requiere arte.

## YAGNI: You Ain't Gonna Need It

Uno de los principios más importantes del desarrollo ágil: You Ain't Gonna Need It.

No construyas funcionalidad que "tal vez necesites en el futuro". No crees abstracciones para "cuando escalemos". No implementes features que "algún día alguien podría pedir".

Construí exactamente lo que necesitás ahora.

¿Por qué? Tres razones:

**1. Probablemente estés equivocado sobre el futuro**

La mayoría de las features que creés "para el futuro" nunca se usan. Gastaste tiempo construyendo algo innecesario. Y peor: ahora ese código está ahí, agregando complejidad que todos tienen que navegar.

**2. Los requerimientos cambian**

Cuando realmente necesites esa funcionalidad, el contexto va a ser diferente. Lo que parecía obvio hoy va a ser irrelevante mañana. Y vas a tener que refactorizar o desechar ese código "preparado para el futuro".

**3. Construir sobre demanda es más barato**

Construir algo cuando lo necesitás, con el contexto real, siempre es más eficiente que construir "por las dudas".

Martin Fowler lo resume: "Es más barato construir software que es fácil de cambiar, que construir software que anticipa todos los cambios futuros."

## El arte de borrar código

El mejor código que escribí el año pasado fue código que borré.

Había un módulo de 800 líneas. Era complicado. Tenía edge cases para edge cases. Tenía configuraciones para situaciones que nunca pasaban. Había sobrevivido cinco refactors.

Un día me detuve y pregunté: "¿Qué problema está resolviendo esto?"

Resulta que el problema original ya no existía. Lo habíamos resuelto de otra forma hace un año. Pero nadie se había dado cuenta. El módulo seguía ahí, siendo mantenido, generando bugs, consumiendo atención.

Lo borré. Entero. 800 líneas a cero.

Los tests pasaron. El sistema funcionó. Nadie notó.

Ese fue el mejor día de ese sprint.

John Carmack (el programador detrás de Doom, Quake, y muchos otros juegos legendarios) dijo: "El mejor código es el código que no existe."

Cada línea de código es deuda. Es algo que alguien tiene que leer. Algo que puede tener bugs. Algo que puede quebrarse con cambios futuros.

Menos código no es pereza. Es responsabilidad.

## Complejidad accidental vs complejidad esencial

Fred Brooks, en su ensayo "No Silver Bullet", hace una distinción crucial:

**Complejidad esencial:** la complejidad inherente al problema que estás resolviendo. Si estás construyendo un sistema de pagos, tiene que manejar distintas monedas, validación de tarjetas, retry logic. Esa complejidad es inevitable.

**Complejidad accidental:** la complejidad que vos agregás por cómo decidiste resolver el problema. Abstracciones innecesarias, patrones mal aplicados, over-engineering.

El problema es que la mayoría del código tiene 10% de complejidad esencial y 90% de complejidad accidental.

Tu trabajo como developer no es eliminar la complejidad esencial (no podés). Es eliminar la complejidad accidental.

Y la forma de hacer eso es preguntándote constantemente: "¿Esto es realmente necesario?"

## Los tres tipos de simplicidad

Cuando digo "código simple", no estoy hablando de código simplista. Hay tres niveles:

### 1. Simplicidad superficial (código ingenuo)

Es el código que escribe alguien que no entiende el problema. No maneja edge cases. No considera performance. No piensa en mantenibilidad.

Ejemplo:
```python
def dividir(a, b):
    return a / b
```

Simple, sí. ¿Pero qué pasa si b es cero? ¿Qué pasa si a o b no son números?

Esto no es sabiduría. Es ingenuidad.

### 2. Simplicidad profunda (código sabio)

Es código que entiende profundamente el problema, maneja todos los casos, pero lo hace de la forma más directa posible.

Ejemplo:
```python
def dividir(a, b):
    if not isinstance(a, (int, float)) or not isinstance(b, (int, float)):
        raise TypeError("Ambos argumentos deben ser números")
    if b == 0:
        raise ValueError("No se puede dividir por cero")
    return a / b
```

Hace todo lo que necesita hacer. Nada más, nada menos.

### 3. Complejidad innecesaria (código que se cree inteligente)

Es código que introduce abstracciones, patrones, e indirecciones que no agregan valor.

Ejemplo:
```python
class DivisionStrategy:
    def execute(self, a, b):
        raise NotImplementedError

class StandardDivisionStrategy(DivisionStrategy):
    def execute(self, a, b):
        return a / b

class DivisionContext:
    def __init__(self, strategy):
        self.strategy = strategy

    def divide(self, a, b):
        validator = NumberValidator()
        validator.validate(a)
        validator.validate(b)
        return self.strategy.execute(a, b)

# Usar:
context = DivisionContext(StandardDivisionStrategy())
result = context.divide(10, 2)
```

Para hacer una división. EN SERIO.

Esto no es profesionalismo. Es ego.

## Cuando la complejidad SÍ es necesaria

Ahora, no todo puede ser simple. A veces la complejidad es inevitable.

¿Cuándo está justificada?

**1. Cuando reduce complejidad a largo plazo**

A veces agregar una abstracción HOY hace que agregar 50 features futuras sea trivial. Ahí la complejidad se paga sola.

Pero esto requiere estar seguro de que esas 50 features van a existir. No suposiciones. Certeza.

**2. Cuando el dominio es inherentemente complejo**

Si estás implementando un algoritmo de criptografía, va a ser complejo. Si estás manejando transacciones distribuidas, va a ser complejo.

No simplificás la solución. Simplificás todo lo que está ALREDEDOR de la solución.

**3. Cuando el costo de bugs es extremo**

Si tu código maneja dinero, vidas humanas, o datos críticos, está bien agregar complejidad (validaciones extra, tipos más estrictos, tests exhaustivos) para minimizar errores.

Pero incluso ahí: hacelo tan simple como SEA POSIBLE dentro de esas restricciones.

## Las reglas de la simplicidad

Después de años escribiendo y revisando código, estos son mis criterios para código simple:

**1. Podés explicarlo en una oración**
Si necesitás tres párrafos para explicar qué hace una función, está haciendo demasiado.

**2. Cabe en tu cabeza**
Si no podés mantener toda la lógica de un módulo en tu working memory, es demasiado complejo.

**3. No hay sorpresas**
El código hace exactamente lo que esperás que haga leyendo su nombre. No hay side effects ocultos. No hay magia.

**4. Borrás algo y se rompe**
Si podés borrar una línea o una función y todo sigue funcionando, es que no era necesario. Borrar código que no se usa es mantenimiento esencial.

## Tres prácticas para esta semana

**1. La regla de las 15 líneas**

Esta semana, cada función que escribas: intentá que tenga 15 líneas o menos. Si pasa de 15, pregúntate: ¿Puedo extraer una sub-función? ¿Estoy haciendo demasiadas cosas?

No es una regla absoluta. Pero es un buen ejercicio para forzarte a pensar en simplicidad.

**2. El desafío de borrar**

Elegí un archivo que no has tocado en meses. Leelo. ¿Hay funciones que nunca se llaman? ¿Imports que no se usan? ¿Comentarios obsoletos? ¿Código comentado "por las dudas"?

Borralo. TODO. Vas a sentir ansiedad ("¿y si lo necesito?"). Hacelo igual. Tenés git. Si realmente lo necesitás (spoiler: no lo vas a necesitar), lo recuperás.

**3. El test de explicación**

Antes de hacer commit de código complejo, intentá explicárselo a alguien (o a un rubber duck). Si no podés explicarlo claramente en menos de 2 minutos, es demasiado complejo. Simplificá hasta que puedas.

---

Hay una frase atribuida a Antoine de Saint-Exupéry: "La perfección no se alcanza cuando no hay nada más que agregar, sino cuando no hay nada más que quitar."

Ese es el código perfecto.

No es el código con todos los patrones. Es el código sin nada innecesario.

No es el código que demuestra cuánto sabés. Es el código que resuelve el problema y se va.

No es el código que impresiona. Es el código que funciona, y que cuando lo leés en seis meses todavía entendés qué hace.

La simplicidad no es simplismo. Es sabiduría destilada.

Y cuando lográs escribir código simple que resuelve problemas complejos, eso sí es arte.

Porque cualquiera puede hacer algo complicado lucir complicado.

Pero hacer algo complicado lucir simple...

Eso requiere maestría.
