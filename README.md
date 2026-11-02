# 💻 Introducción a la Programación

`🔵 Materia: Introducción a la Programación` &nbsp;·&nbsp; `🔵 Bimestre: 2/18` &nbsp;·&nbsp; `🟢 Modalidad: Actividades colaborativas`

> Documentación de mi avance en la materia: resumen temático por semana (`README.md`), definiciones (`glosario.md`), bitácora de trabajo (`notas.md`) y reglas de entrega (`formato_entrega.md`). Forma parte de mi carrera en [licenciatura-ids](https://github.com/Nerfe5/licenciatura-ids).

---

## 🎯 Objetivo general

Comprender los comandos básicos de la programación a través del uso del lenguaje C, que permitirá analizar programas, manejar y gestionar la información del ordenador.

**Pregunta guía del curso:** ¿De qué manera se aplica la programación en la resolución de problemas básicos?

## 🗓️ Calendario (bimestre 2)

| Semana | Fechas |
|---|---|
| 1 | 26 de octubre – 2 de noviembre |
| 2 | 2 – 9 de noviembre |
| 3 | 9 – 16 de noviembre |
| 4 | 16 – 23 de noviembre |
| 5 | 23 – 30 de noviembre |
| 6 | 30 de noviembre – 7 de diciembre |
| 7 | 7 – 14 de diciembre |

## 📚 Temario

1. **Conceptos fundamentales de programación:** sistemas de numeración (binario y hexadecimal) y administración de archivos y carpetas a través de comandos.
2. **Lenguaje de programación C:** función `main`, entrada y salida de datos, variables y constantes, tipos de datos (`char`, `int`, `float`, `double`), expresiones y sentencias.
3. **Estructuras de control:** secuencial, selectivas (`if`, `else`, `switch`) y repetitivas (`for`, `while`, `do while`).
4. **Funciones:** estructura de una función, variables locales y globales, clases de almacenamiento (`static`, `extern`, `auto`, `register`), estructura general de un programa en C, macros y el preprocesador de C.

---

## 🧭 Semana 1 — Conceptos fundamentales de programación

> Resumen elaborado a partir de la presentación de la semana "U1. Conceptos fundamentales de programación" (presentación de la semana, 2026), impartida el 26 de octubre de 2026.

### 🎯 Resultados de aprendizaje

- [ ] Explicar cómo se representa la información en una computadora.
- [ ] Diferenciar entre los sistemas de numeración decimal, binario y hexadecimal.
- [ ] Convertir valores básicos entre binario y hexadecimal.
- [ ] Utilizar comandos esenciales para gestionar archivos y carpetas.

### 🧩 Conceptos fundamentales de programación

Todo programa, sin importar el lenguaje, se apoya en cinco conceptos: **datos**, **variables**, **instrucciones**, **lógica** y **representación de la información**.

### 🔢 Sistemas de numeración

Un **sistema de numeración** define cómo se representan los números con un conjunto específico de símbolos. Las computadoras usan sistemas distintos al decimal porque trabajan con **señales eléctricas** (encendido/apagado).

| Sistema | Base | Símbolos | Ejemplo |
|---|---|---|---|
| **Decimal** | 10 | 0–9 | 10 |
| **Binario** | 2 | 0 y 1 (0 = apagado, 1 = encendido); cada dígito es un **bit** | 1010 (binario) = 10 (decimal) |
| **Hexadecimal** | 16 | 0–9 y A–F (A = 10, B = 11, C = 12, D = 13, E = 14, F = 15) | FF (hexadecimal) = 255 (decimal) |

- **Binario:** base del funcionamiento de las computadoras; permite representar datos, instrucciones y direcciones de memoria.
- **Hexadecimal:** representa grandes cantidades binarias de forma más compacta; se usa en direcciones de memoria, códigos de color (HTML y CSS), depuración de programas e identificadores de hardware, y facilita leer y analizar el binario.

#### Sistemas aditivos y posicionales

| | Aditivos | Posicionales |
|---|---|---|
| **Cómo se obtiene el valor** | Se suman los valores de los símbolos | El valor depende del símbolo, de su posición y de la base |
| **¿Importa la posición?** | No | Sí |
| **Ejemplos** | Egipcio, romano | Decimal, binario, octal, hexadecimal (y el maya, de base 20) |
| **Limitación o ventaja** | Impracticables para cantidades muy grandes o muy pequeñas | Permiten escribir cantidades grandes con pocos símbolos; necesitan el cero |

*(Jiménez Murillo, 2009, pp. 4-5.)*

#### Conversión de decimal a binario (divisiones sucesivas)

Se divide el número y cada cociente entre 2, anotando el residuo, hasta llegar a 0; los residuos se leen en orden contrario al que se obtuvieron. Ejemplo con 200:

| División | Residuo |
|---|---|
| 200 ÷ 2 = 100 | 0 |
| 100 ÷ 2 = 50 | 0 |
| 50 ÷ 2 = 25 | 0 |
| 25 ÷ 2 = 12 | 1 |
| 12 ÷ 2 = 6 | 0 |
| 6 ÷ 2 = 3 | 0 |
| 3 ÷ 2 = 1 | 1 |
| 1 ÷ 2 = 0 | 1 |

Leyendo los residuos de abajo hacia arriba: **200 (decimal) = 11001000 (binario)** = C8 (hexadecimal). Comprobación: 128 + 64 + 8 = 200.

Otro método (restas de potencias de 2, de mayor a menor): se va comparando el número con 128, 64, 32, 16, 8, 4, 2 y 1; si cabe se anota 1 y se resta, y si no cabe se anota 0.

#### Caso de la válvula `0x1F`

El prefijo `0x` indica que el número es hexadecimal. `1F` = 1 × 16¹ + 15 × 16⁰ = 16 + 15 = **31**, y el registro binario `00011111` lo confirma (16 + 8 + 4 + 2 + 1 = 31). Como el protocolo del caso exige activar la electrobomba de recirculación cuando el caudal supera 30 L/s, 31 L/s obliga a activarla. Saber calcular el dato permite verificarlo y no depender solo de lo que muestre una pantalla.

### 💻 Administración de archivos y carpetas con comandos

Los comandos permiten interactuar con el sistema operativo sin interfaz gráfica, con ventajas de **rapidez, precisión, automatización** y uso profesional en servidores y programación.

| Comando | Función |
|---|---|
| `ls` | Listar archivos |
| `cd` | Cambiar de directorio |
| `mkdir` | Crear carpeta |
| `rm` | Eliminar archivos |
| `cp` | Copiar |
| `mv` | Mover o renombrar |

### 📝 Actividades de la semana

- **Foro 1 (sistemas de numeración, 27 de octubre al 9 de noviembre):** importancia de los sistemas de numeración en la programación y cómo el binario permite procesar la información, y conversión de 200 a binario con procedimiento; además, comentar las publicaciones de compañeros.
- **Ruta hacia el éxito profesional (foro):** ¿por qué aprender sistemas de numeración y comandos ayuda en la formación profesional? y ¿por qué las computadoras usan binario y no decimal?
- **Espacio colaborativo (video):** discusión sobre por qué los procesadores usan interruptores binarios y no símbolos sumados como los números romanos, el caso de la válvula `0x1F`, y comentar la aportación de un compañero.
- **Desafío en clase (práctica):** mapa comparativo visual de binario, hexadecimal, conversiones, uso real del hexadecimal, comandos y su relación con la programación.
- **Otras actividades:** actividad entregable, examen y actividad de la semana 2 con el asistente virtual.

### 🔑 Palabras clave de la semana

`Sistema de numeración` · `Sistema posicional` · `Sistema aditivo` · `Base` · `Binario` · `Bit` · `Hexadecimal` · `Conversión` · `Comandos` · `Directorio`

---

## 🧭 Semana 2 — Conceptos fundamentales de programación (continuación de la Unidad 1)

> Actividad colaborativa de la semana (inicia el 2 de noviembre de 2026), con apoyo del asesor académico virtual. Se entrega en el formato institucional, en Word o PDF.

### 📝 Qué pide la actividad

1. **Investigación teórica:** diferencias entre los sistemas decimal, binario y hexadecimal y cómo se usa la base en cada uno.
2. **Conversión práctica:** lógica y procedimiento de decimal a binario y viceversa, con el ejemplo completo del número 50.
3. **Codificación de caracteres:** qué es ASCII y cómo se relaciona con el binario y el hexadecimal.
4. **Justificación:** un ejemplo práctico en que la conversión de decimal a binario sea crucial (un transistor, un semáforo simple).
5. **Situación práctica:** plantear un escenario propio o resolver el caso de una empresa de microcontroladores que migra los registros de sus logs de binario de 8 bits a hexadecimal (valor ASCII 107: binario, hexadecimal, eficiencia y reflexión de al menos 5 líneas).

*(Pendientes por confirmar: rúbrica, fecha límite, límite de cuartillas, si el membrete cuenta como imagen y si hay que evidenciar el uso del asesor virtual.)*

---

## 🔭 Adelanto de la Unidad 2 — Lenguaje de programación C (inicia en la Semana 3, 9 de noviembre)

> Resumen elaborado a partir del video y la presentación "U2. Lenguaje de programación C", revisados el 2 de noviembre de 2026, antes de que inicie la Unidad 2. Cubre lo que muestran las diapositivas; no incluye lo que se explica solo de forma oral.

### 🧪 Elementos básicos del lenguaje C

- **Características de C:** estructurado, compilado, de propósito general y muy cercano al hardware.
- **Usos:** programación de microcontroladores, sistemas de control, creación de firmware y bases de sistemas operativos.
- **Entrada y salida de datos:** `printf()` para salida y `scanf()` para entrada. Ejemplo: `int edad; printf("Ingresa tu edad: "); scanf("%d", &edad);`
- **Variables:** almacenan datos que pueden cambiar y deben declararse con un tipo de dato. Ejemplo: `int contador;`
- **Constantes:** valores que no cambian durante la ejecución. Ejemplo: `const float PI = 3.1416;`

### 🤔 Preguntas para reflexionar (situación práctica)

- ¿Por qué el lenguaje C es ampliamente utilizado en el desarrollo de sistemas embebidos y de bajo nivel?
- ¿Qué problemas pueden presentarse en un programa si no se comprenden correctamente los tipos de datos y las variables?

### 📝 Desafío planteado en el video

- Desarrollar una calculadora básica en C que realice suma, resta, multiplicación y división entre dos números, y que se ejecute correctamente en Dev-C++. *(Por confirmar cuándo se pide y si es entregable.)*

### 🔑 Palabras clave del adelanto

`Lenguaje C` · `Compilado` · `printf()` · `scanf()` · `Variable` · `Constante` · `Dev-C++`

---

## 📝 Seguimiento de entregas (modalidad colaborativa)

- [x] Semana 1 — espacio colaborativo: respuestas publicadas en la publicación del video (caso `0x1F` y binario frente a números romanos)
- [x] Semana 1 — Foro 1: participación publicada (sistemas de numeración y conversión de 200 a binario, con cita y referencia)
- [x] Semana 1 — Foro 1: comentario a la publicación de un compañero; foro cerrado de mi lado el 2 de noviembre
- [ ] Semana 2 — actividad colaborativa de la Unidad 1 (sistemas de numeración y ASCII)
- [ ] Semana 3 — *(por definir)*
- [ ] Semana 4 — *(por definir)*
- [ ] Semana 5 — *(por definir)*
- [ ] Semana 6 — *(por definir)*
- [ ] Semana 7 — *(por definir)*

---

## 📚 Fuentes del material de la semana

**Semana 1**

- *U1. Conceptos fundamentales de programación* [Diapositivas del curso, Semana 1]. (2026).
- Jiménez Murillo, J. A. (2009). *Matemáticas para la computación*. Alfaomega.

**Adelanto de la Unidad 2.** *U2. Lenguaje de programación C* [Video y diapositivas del curso]. (2026). Referencias que cita la presentación:

- Kernighan, B. W., y Ritchie, D. M. (1988). *The C programming language* (2.ª ed.). Prentice Hall.
- Deitel, P., y Deitel, H. (2016). *C how to program* (8.ª ed.). Pearson.
- ISO/IEC. (2018). *ISO/IEC 9899:2018 — Programming languages — C*.
- GeeksforGeeks. (2024). *C programming language*.
