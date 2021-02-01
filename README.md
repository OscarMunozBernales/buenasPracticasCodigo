# Curso de buenas Practicas para escritura de código


# 1. Introducción

## 1.1. ¿A quién beneficia contar con código bien escrito?
El código bien escrito beneficia a todos los involucrados en el proyecto.

- **A tí**: Cuando retomemos un proyecto después de un largo tiempo nos beneficiará ya que sabremos cómo está ordenado y cómo está escrito todo.
- **A cualquiera**: Cualquier persona que deba modificar el código después de tí.
- **A tu cliente**: Aunque nunca lo sabrá, su negocio estará mejor atendido.

## 1.2. Ejes que hacen a la calidad del código

Los siguientes elementos dotan de calidad al código:
- **Legibilidad**: qué tan fácil es interpretar lo que el código dice.
- **Mantenibilidad**: cuánto esfuerzo supondrá adaptar el código a nuevos requerimientos.
- **Testeabilidad**: cuánto esfuerzo supondrá realizar pruebas sobre este código.

# 2. Aprender a escribir código legible

## 2.1. Código prolijo

El código fuente lo escribimos para personas como tú y yo, para las computadoras tenemos las versiones compiladas.

Debemos seguir un estándar de codificación, el cual nos ayuda a:

- Generar código claro y consistente.
- Evitar perder tiempo en decisiones triviales.
### Tips para mejorar la legibilidad de nuestro código:
- **Define un estándar**: Piénsalo una vez y déjalo por escrito.
- **Respétalo**: Haz un esfuerzo por adherir al estándar durante tu día a día.
- **Apóyate en algún linter**: Esta sencilla herramienta te ayudará a incorporar buenas prácticas.

## 2.2. Identificadores mnemotécnicos, específicos y precisos

Los identificadores son variables, funciones, clases, módulos, componentes, etc. Elementos a los que nosotros debamos crearles un nombre propio.
Ejemplo sin un identificador mnemotécnico una función se vería así:
```php
function f( int $b, int $a ) : float {
        return ( $b * $a ) / 2;
}
```
Al leer este código no sabemos para qué funciona y hasta podríamos borrarlo por equivocación.
Ahora utilizando un identificador mnemotécnico se vería así:
```
function areaRectangulo( int $base, int $altura ) : float {
        return ( $base * $altura ) / 2;
}
```
Ahora gracias a que el código es más legible sabemos para qué funciona esta función.
**Atención a los identificadores que estableces**.

# 3. Aprende a escribir código mantenible
## 3.1. Código modular
El código modular son pedazos de códigos divididos que pueden ser utilizados en cualquier lugar para evitar tener un solo archivo con un bloque de código gigante.

## 3.2. Código reutilizable
Escribir código reutilizable nos va a ayudar a que en lugar de copiar y pegar una misma línea de código pero con diferentes parámetros lo hagamos a través de una función que retorne los valores que necesitamos y luego la podremos llamar en cualquier lugar del código que necesitemos pasándole los parámetros que deseamos.

Acá algunos tips:
- Mantén tu código DRY (O SECO, en español). Es decir “Don’t Repeat Yourself” (O “No te repitas”)
- Haz métodos o funciones que hagan solamente una cosa.
- Haz pruebas unitarias para tus métodos y que sean fáciles de testear
- Trata de pensar de forma abstracta, usa interfaces o clases abstractas
- Escribe código que se pueda extender fácilmente en un futuro (Básicamente que modificarlo no signifique prenderle fuego a medio código)
- No escribas código innecesario o que no hace falta en el momento.
- Reduce el acoplamiento (Acoplamiento hace referencia a que, el comportamiento de una función depende enteramente de lo que retorne otra función, y esta de otra, y otra, y otra…)
- Usa más código modular.
- Escribe tu código como si fuera una API externa (Que se pueda importar de otro código y sirva completamente)

## 3.3. Código organizado
El código organizado se refiere a cómo tenemos distribuido nuestros archivos en la raíz (root) del proyecto. A mayor organización, mayor entendimiento del código.

# 4. Escribir código libre de vicios

## 4.1. Evitar el hardCoding
El hardcoding es la práctica de escribir valores literales en lugar de identificadores. **No debe de usarse**, ya que si el día de mañana debemos cambiar los valores eso significa que debemos cambiar el código en los lugares que esté ese valor estático por completo y luego mandar a producción, cuándo podríamos hacer el cambio más orgánico en una variable que afecte a todos los lugares que es llamada.

## 4.2. Evitar efectos colaterales.
Debemos analizar muy bien nuestro código para evitar efectos colaterales y evitar que nuestro código deje de funcionar. Un consejo de nuestro profesor en esta clase: **No uses variables globales**.

# 5. Conocer los principios SOLID
## 5.1. Principios SOLID: Single Responsibility Principle
**SOLID** son cinco principios básicos de la programación orientada a objetos que ayudan a crear software mantenible en el tiempo.

SOLID significa:
- S: Single Reponsibility Principle (Principio de responsabilidad unica)
- O: Open/Closed Principle (Principio de abierto o cerrado)
- L: Liskov Substitution Principle (Principio de sustitución de Liskov)
- I: Interface Segregation Principle (Principio de segracion de interfaces)
- D: Dependency Inversion Principle (Principio de inverción de dependencia)

La S se trata de una clase que debe tener sólo una razón para cambiar.

## 5.1. Single Reponsibility Principle (Principio de responsabilidad unica)
El principio de responsabilidad única (también conocido como “la lata cohesión”) nos dice que una clase debería tener un único objetivo, muy claro, muy conciso y muy acotado.

## 5.2. Open/Closed Principle (Principio de abierto o cerrado)
Open/Closed Principle establece que una entidad de software debe quedarse abierta para su extensión, pero cerrada para su modificación.

## 5.3. Liskov Substitution Principle (Principio de sustitución de Liskov)
El Liskov Substitution Principle establece que cada clase que hereda de otra puede usarse como su padre sin necesidad de conocer las diferencias entre ellas. Para que pueda darse este principio debe cumplir con dos puntos:

- El cliente debe usar métodos de la clase padre únicamente.
- La clase hija no debe alterar el comportamiento de los métodos de la clase padre.

## 5.4. Interface Segregation Principle (Principio de segracion de interfaces)
El Interface Segregation Principle establece que los clientes de un programa sólo deberían conocer de éste los métodos que realmente usan.

## 5.5. Dependency Inversion Principle (Principio de inverción de dependencia)
Dependency Inversion Principle detalla que los módulos de alto nivel no deben depender de los de bajo nivel, ambos deben depender de abstracciones.
Las abstracciones no deben depender de los detalles, los detalles deben depender de las abstracciones.

