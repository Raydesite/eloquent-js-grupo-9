# grupo de lectura del libro eloquement

## Capitulo 1 - Introduccion

- Un programa es un edificio de pensamiento. No cuesta nada construirlo, no pesa nada, y crece fácilmente bajo el teclear de nuestras manos. Pero sin ningún cuidado, el tamaño de un programa y su complejidad crecerán sin control, confundiendo incluso a la persona que lo creó. Mantener programas bajo control es el problema principal de la programación. Cuando un programa funciona, es hermoso. El arte de la programación es la habilidadde controlar la complejidad. Un gran programa es moderado, hecho simple en su complejidad. La idea de cómo se ve un buen programa se desarrolla con la práctica, no se aprende de una lista de reglas.
- Después de su adopción fuera de Netscape, un documento estándar fue escrito para describir la forma en que debería funcionar el lenguaje JavaScript, para que las diversas piezas de software que decían ser compatibles con JavaScript en realidad estuvieran hablando del mismo lenguaje. Este se llamo el Estándar ECMAScript, por Ecma International que hizo la estandarización. En la práctica, los términos ECMAScript y JavaScript se puede usar indistintamente, son dos nombres para el mismo lenguaje.
- libro, eloquent-javascript.net (pagina 9)
  - Los primeros doce (12) capítulos discuten el lenguaje JavaScript en sí.
  - Los siguientes siete (7) capítulos son acerca de los navegadores web y la forma en la que JavaScript es usado para programarlos.
  - Finalmente, dos (2) capítulos están dedicados a Node.js, otro entorno en donde programar JavaScript.
  - A lo largo del libro, hay cinco capítulos de proyectos, que describen programas de ejemplo más grandes para darte una idea de la programación real.
- La parte del lenguaje del libro comienza
  - con cuatro capítulos para presentar
    - la estructura básica del lenguaje de JavaScript. Estos introducen
    - estructuras de control (como la palabra while que ya viste en esta introducción),
    - funciones (escribir tus propios bloques de construcción),
    - y estructuras de datos. Después de estos, seras capaz de escribir programas simples.
  - Luego, los Capítulos 5 y 6 introducen
    - técnicas para usar funciones y objetos y asi escribir código más abstracto y de manera que puedas mantener la complejidad bajo control.
  - Después de un primer capítulo de proyecto, la primera parte del libro continúa con los capítulos sobre
    - manejo y solución de errores,
    - en expresiones regulares (una herramienta importante para trabajar con texto),
    - en modularidad (otra defensa contra la complejidad),
    - y en programación asincrónica (que se encarga de eventos que toman tiempo). El segundo capítulo de proyecto concluye la primera parte del libro.
- La segunda parte, Capítulos 13 a 19, describe
  - las herramientas a las que el JavaScript en un navegador tiene acceso.
  - Aprenderás a mostrar cosas en la pantalla (Capítulos 14 y 17),
  - responder a entradas de usuario (Capitulo 15), y
  - a comunicarte a través de la red (Capitulo 18).
  - Hay dos capítulos de proyectos en este parte.
    - Después de eso, el Capítulo 20 describe Node.js,
    - y el Capitulo 21 construye un pequeño sistema web usando esta herramienta.
- En orden de aparición, trabajaremos en la construcción de
  - un robot de delivery,
  - un lenguaje de programación,
  - un juego de plataforma,
  - un programa de paint
  - y un sitio web dinámico.
- ejercicios, ve a eloquent-javascript.net/code
  - Muchos ejemplos se mantienen por si mismos y deberían de funcionar en cualquier entorno de JavaScript. Pero código en capítulos más avanzados a menudo se escribe para un entorno específico (el navegador o Node.js) y solo puede ser ejecutado allí. Además, muchos capítulos definen programas más grandes, y las piezas de código que aparecen en ellos dependen de otras piezas o de archivos externos. La caja de arena en el sitio web proporciona enlaces a archivos Zip que contienen todos los scripts y archivos de datos necesarios para ejecutar el código de un capítulo determinado.

## Capitulo 2 - Valores, Tipos, y Operadores

- valores
  - solo podemos representar datos que previamente han sido almacenados en la memoria, a estos los conocemos como valores
  - elementos atómicos de los programas en JavaScript, estos son, los tipos de valores simples y los operadores que actúan en tales valores.
- numeros
  - 32 y 64 bit (2⁶⁴ es igual que un 18 con 18 ceros mas)
  - hay que tener en cuenta los bit del numero negatrivo y de los valores fraciaonarios
  - podemos cargar exponentes para notacion cientifica
  - numeros muy grandes o muy pequeños puyeden no poder expresarse con precision
  - valores que son considerados numeros pero no se representan como tal
    - infinity -infinity
    - NaN
- operadores
  - son los signos en las expresiones matematicas o logicas
  - precedencia de operadores
  - no todos los operadores son simbolos algunos se escriben como palabras los "Operadores unarios"
    - typeof
  - Operadores unarios, son operadores que solo operan un valor
  - Operadores binarios, son operadores que operan dos valores
  - Operadores ternarios, son operadores que operan tres valores
- string
  - es una secuencia de numeros (se pueden iterar)
  - valores encerados por comillas
    - Los strings escritos con comillas simples o dobles se comportan casi de la misma manera—La unica diferencia es el tipo de comilla que necesitamos para escapar dentro de ellos.
    - Los strings de comillas inversas, usualmente llamados plantillas literales, pueden realizar algunos trucos más. Mas alla de permitir saltos de lineas, pueden también incrustar otros valores.
  - Los strings no pueden ser divididos, multiplicados, o substraidos, pero el operador + puede ser utilizado en ellos. No los agrega, sino que los concatena (pega) dos strings juntos.
  - valores string tienen un conjunto de funciones (métodos) asociadas, que pueden ser usadas para realizar operaciones en ellos.
  - newline, tab, retorno de carro, etc, solo pueden ser incluidos cuando el string está encapsulado con comillas invertidas y se deben escapar "\"
    - newline
      - \"\\n\"."
      - \\n
  - utiliza el estandar unicode
- Muchas operaciones en el lenguaje que no producen un valor significativo producen undefined simplemente porque tienen que producir algún valor.
- Coercion de tipo

  - Ejemplos de coercion de tipos

    ```
      console.log(8 _ null)
      // → 0
      console.log("5" - 1)
      // → 4
      console.log("5" + 1)
      // → 51
      console.log("cinco" _ 2)
      // → NaN
      console.log(false == 0)
      // → true
      console.log(null == undefined);
      // → true
      console.log(null == 0);
      // → false

    ```

  - El null en la primera expresión se torna 0,
  - y el "5" en la segunda expresión se torna 5 (de string a número).
  - Sin embargo, en la tercera expresión, + intenta realizar una concatenación de string antes que una adición numérica, entonces el 1 es convertido a "1" (de número a string)
  - Cuando algo que no se traduce a un número en una manera obvia (tal como "cinco" o undefined) es convertido a un número, obtenemos el valor NaN. Operaciones aritméticas subsecuentes con NaN, continúan produciendo NaN
  - Cuando se utiliza == para comparar valores del mismo tipo, el resultado sera true, excepto en el caso de NaN.
    - Pero cuando los tipos de datos comparados difieren, JavaScript utiliza una serie de reglas complicadas y confusas para determinar que hacer.
    - En la mayoria de los casos, solo tratara de convertir uno de estos valores al tipo del otro valor.
    - Cuando null o undefined ocurren en cualquiera de los lados del operador, este produce verdadero solo si ambos lados son valores o null o undefined.
    - Cuando queremos probar si un valor tiene un valor real en vez de null o undefined, puedes compararlo con null usando el operador == (o !=).
      - Pero que pasa si queremos probar que algo se refiere precisamente al valor false? Las reglas para convertir strings y números a valores Booleanos, dice que 0, NaN, y el string vació ("") cuentan como false, mientras que todos los otros valores cuentan como true. Debido a esto, expresiones como 0 == false, y "" == false son también verdaderas.
    - Cuando no queremos ninguna conversion de tipo automática, existen otros dos operadores adicionales: === y !==.
      - El primero prueba si un valor es precisamente igual al otro,
      - y el segundo prueba si un valor no es precisamente igual.
      - Entonces "" === false es falso, como es de esperarse.
  - Los operadores lógicos && y ||, manejan valores de diferentes tipos de una forma peculiar.

    - ejempĺo de coercion de tipos con comprovaciones logicas

      ```
      console.log(null || "usuario")
      // → usuario
      console.log("Agnes" || "usuario")
      // → Agnes
      ```

    - Ellos convertirán el valor en su lado izquierdo a un tipo Booleano para decidir que hacer, pero dependiendo del operador y el resultado de la conversión, devolverán o el valor original de la izquierda o el valor de la derecha.
    - El operador ||, por ejemplo, devolverá el valor de su izquierda cuando este puede ser convertido a verdadero y de ser lo contrario devolverá el valor de la derecha. Esto tiene el efecto esperado cuando los valores son Booleanos, pero se comporta de una forma algo análoga con valores de otros tipos.
      - Podemos utilizar esta funcionalidad como una forma de recurrir a un valor por defecto. Si tenemos un valor que puede estar vacío, podemos usar || después de este para remplazarlo con otro valor. Si el valor inicial puede ser convertido a falso, obtendra el reemplazo en su lugar.
    - El operador && funciona de manera similar, pero de forma opuesta. Cuando el valor a su izquierda es algo que se convierte a falso, devuelve ese valor, y de lo contrario, devuelve el valor a su derecha.

  - evaluación de corto circuito
    - Otra propiedad importante de estos dos operadores es que la parte de su derecha solo es evaluada si es necesario.
      - En el caso de que (true || X), no importa que sea X aun si es una pieza del programa que hace algo terrible el resultado será verdadero, y X nunca sera evaluado.
      - Lo mismo sucede con (false && X), que es falso e ignorará X. Esto es llamado evaluación de corto circuito. El operador condicional funciona de manera similar. Del segundo y tercer valor, solo el que es seleccionado es evaluado.

## Citas

- "Cuando la acción deja de servirte, reúne información; cuando la información deja de servirte, duerme." -Ursula K. Le Guin, La Mano Izquierda De La Oscuridad
- “Debajo de la superficie de la máquina, el programa se mueve. Sin esfuerzo, se expande y se contrae. En gran armonía, los electrones se dispersan y se reagrupan. Las figuras en el monitor son tan solo ondas sobre el agua. La esencia se mantiene invisible debajo de la superficie.” —Master Yuan-Ma, The Book of Programming
- “Y mi corazón brilla de un color rojo brillante bajo mi piel transparente y translúcida, y tienen que administrarme 10cc de JavaScript para conseguir que regrese. (respondo bien a las toxinas en la sangre.) Hombre, esa cosa es increible!” —why, Why’s (Poignant) Guide to Ruby
