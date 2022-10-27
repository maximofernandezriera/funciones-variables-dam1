## Teoría de funciones, variables y parámetros en pseudocódigo

Partimos del siguiente ejemplo. Un programa principal y una función que calcula el máximo entre dos números:

### La función se llama CalcularMaximo y retorna max

    Funcion max <- CalcularMaximo(num1,num2)
    Definir max Como Entero
    Si num1>num2 Entonces
        max <- num1
       SiNo
        max <- num2
    FinSi
    FinFuncion

### Maximo es el programa principal

    Proceso Maximo
    Definir numero1,numero2,num_maximo Como Entero
    Escribir "Dime el número1:"
    Leer numero1
    Escribir "Dime el número2:"
    Leer numero2
    num_maximo <- CalcularMaximo(numero1,numero2)
    Escribir "El máximo es ",num_maximo
    FinProceso

## Ámbito de variables
Las variables definidas en la función no existen en otras funciones o el programa principal. Igualmente las variables del programa principal no existen en la función.

Por ejemplo la variable max definida en la función no existe en el programa principalmente. Igualmente la variable numero1 definida en el programa principal no existe en la función.

## Parámetros formales y argumentos (reales o argumentos son palabras sinónimas)

- Parámetros formales: Son las variables que recibe la función, se crean al definir la función. Su contenido lo recibe al realizar la llamada a la función de los parámetro reales. Los parámetros formales son variables locales dentro de la función.

- Parámetros reales o argumentos: Son la expresiones que se utilizan en la llamada de la función, sus valores se copiarán en los parámetros formales.

## Paso de parámetros por valor y por referencia

- Paso por valor: El valor de los parámetros reales se copian en los parámetros formales, por lo tanto una modificación de algún parámetro formal no modifica el parámetro real.
- Paso por referencia: Cuando se pasa un parámetro por referencia implica que si modificamos el parámetro formal se modificará el parámetro real.

Por de defecto, los arrays se pasan por referencia, las demás estructuras de datos: por valor.
Si queremos indicar explícitamente como se pasan los parámetros podemos usar las palabras claves Por Valor o Por Referencia.
