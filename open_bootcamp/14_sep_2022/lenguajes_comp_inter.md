# Lenguajes Compilados e Interpretados

Un **compilador** se puede pensar como un traductor, toma un lenguaje de entrada y lo convierte a uno de salida.

De estos existen dos tipo basicamente, uno convierte a codigo maquina y el otro a lenguaje intermedio, uno lo usan los lenguajes compilados y el otro los lenguajes interpretados.

## Compilador

El flujo de trabajo vendria a hacer lo siguiente:

- **Analisis Lexico**

    - Se pasa el codigo fuente a un comprobador lexico, `parser`. Su funcion es generar un string de tokens.
    - Cada vez que se convierte a tokens, se busca por palabras reservadas, operadores e identificadores.


- **Analisis Sintactico**

    - Analiza si lo que esta escrito tiene sentido, leyendo los tokens, si no lanza errores
    - Si esta correcto pasa a la siguiente fase


- **Generar codigo intermedio**

    - Simplifica el lenguaje humano a uno que manipule mejor el compilador.
    - Esto lo genera en una estructura de datos en un abstract syntax tree.


- **Optimizacion del codigo intermedio**

    - Elimina codigo redundante, limpia y optimiza el codigo fuente
    - Se puede hacer un unroll loops, si el costo computacional de un loop es mayor a escribirlo llanamente


- **Generacion de codigo**

    - Genera o codigo maquina o genera codigo interpretado
    - Codigo listo para ser ejecutado, codigo listo para ser interpretado

