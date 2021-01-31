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

