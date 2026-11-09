# 📖 Glosario — Introducción a la Programación

`🔵 Materia: Introducción a la Programación` &nbsp;·&nbsp; `📅 Actualizado: Semana 2 (con adelanto de la Unidad 2)`

> Definiciones construidas a partir del material de cada semana. Los términos están agrupados por semana y, dentro de cada una, en orden alfabético.

---

## Semana 1 — Conceptos fundamentales de programación

### ASCII
Código estándar que asigna un número a cada letra, dígito, signo y carácter de control. Usa 7 bits (128 posiciones) y se transmite en un byte con el bit más alto en 0. Ejemplo: la letra k es 107 = 01101011 = 0x6B.

### Base (de un sistema de numeración)
Cantidad de símbolos diferentes que usa un sistema numérico: 10 en el decimal, 2 en el binario, 8 en el octal y 16 en el hexadecimal.

### Binario (sistema de numeración)
Sistema de base 2 que usa solo 0 y 1 (apagado y encendido); es la base del funcionamiento de las computadoras. Ejemplo: 1010 = 10 en decimal.

### Bit
Cada dígito del sistema binario.

### Byte
Grupo de 8 bits. Su valor máximo es 11111111 en binario, que equivale a FF en hexadecimal y a 255 en decimal.

### Comandos
Instrucciones que permiten interactuar con el sistema operativo sin interfaz gráfica; ofrecen rapidez, precisión y automatización. Ejemplos: `ls`, `cd`, `mkdir`, `rm`, `cp` y `mv`.

### Comodín (`*`)
Símbolo que en la terminal representa cualquier secuencia de caracteres. Ejemplo: `mv *0xFF* cuarentena/` mueve todos los archivos cuyo nombre contiene `0xFF`.

### Conversión de decimal a binario
Procedimiento de divisiones sucesivas entre 2: se anotan los residuos y se leen en orden contrario al que se obtuvieron. Ejemplo: 200 (decimal) = 11001000 (binario).

### Directorio
Carpeta del sistema de archivos que agrupa archivos y otras carpetas. Con comandos se crea (`mkdir`), se cambia de uno a otro (`cd`) y se lista su contenido (`ls`).

### Hexadecimal (sistema de numeración)
Sistema de base 16 con los símbolos 0–9 y A–F (A = 10 … F = 15) que representa grandes cantidades binarias de forma compacta. Ejemplo: FF = 255 en decimal. Se usa en direcciones de memoria, colores HTML y CSS, depuración e identificadores de hardware.

### Prefijo `0x`
Marca que indica que el número que sigue está escrito en hexadecimal. Ejemplo: `0x6B` = 107 en decimal.

### Sistema aditivo
Sistema de numeración en el que se suman los valores de los símbolos y la posición no importa. Ejemplos: el egipcio y el romano (XVI = 10 + 5 + 1 = 16).

### Sistema de numeración
Conjunto de reglas y símbolos que define cómo se representan los números; los más usados en computación son el decimal (base 10), el binario (base 2) y el hexadecimal (base 16).

### Sistema posicional
Sistema de numeración en el que el valor de un símbolo depende del lugar que ocupa y de la base del sistema. Ejemplos: decimal, binario, octal y hexadecimal.

---

## Adelanto de la Unidad 2 — Lenguaje de programación C

### Compilado
Característica de C: el código fuente se traduce a un programa ejecutable antes de correr.

### Constante
Valor que no cambia durante la ejecución de un programa. Ejemplo: `const float PI = 3.1416;`

### Dev-C++
Entorno en el que, según la presentación, debe ejecutarse correctamente el programa del desafío de la calculadora.

### `printf()` y `scanf()`
Funciones de C para interactuar con el usuario: `printf()` muestra una salida y `scanf()` recibe una entrada.

### Variable
Espacio que almacena datos que pueden cambiar y que debe declararse con un tipo de dato. Ejemplo: `int contador;`
