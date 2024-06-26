# 📓 PSeInt Cheatsheet

## Índice
1. [Sintaxis Básica](#sintaxis-básica)
2. [Tipos de Datos](#tipos-de-datos)
3. [Operadores](#operadores)
4. [Estructuras de Control](#estructuras-de-control)
5. [Funciones](#funciones)
6. [Ejemplos Comunes](#ejemplos-comunes)

## Sintaxis Básica

```pseint
Algoritmo HolaMundo
    Escribir "¡Hola, mundo!"
FinAlgoritmo
```

## Tipos de Datos

### Tipos de Datos Básicos

```pseint
Algoritmo TiposDeDatos
    entero: enteroVariable
    real: realVariable
    caracter: caracterVariable
    logico: logicoVariable

    enteroVariable <- 5
    realVariable <- 5.5
    caracterVariable <- 'A'
    logicoVariable <- verdadero

    Escribir enteroVariable
    Escribir realVariable
    Escribir caracterVariable
    Escribir logicoVariable
FinAlgoritmo
```

### Tipos de Datos Derivados

```pseint
Algoritmo TiposDeDatosDerivados
    entero: arreglo[5]
    cadena: cadenaVariable

    arreglo[1] <- 1
    arreglo[2] <- 2
    arreglo[3] <- 3
    arreglo[4] <- 4
    arreglo[5] <- 5

    cadenaVariable <- "Hola"

    Escribir arreglo[1], arreglo[2], arreglo[3], arreglo[4], arreglo[5]
    Escribir cadenaVariable
FinAlgoritmo
```

## Operadores

### Operadores Aritméticos

```pseint
Algoritmo OperadoresAritmeticos
    entero: suma, resta, multiplicacion, division, modulo
    suma <- 5 + 3
    resta <- 5 - 3
    multiplicacion <- 5 * 3
    division <- 5 / 3
    modulo <- 5 % 3

    Escribir suma, resta, multiplicacion, division, modulo
FinAlgoritmo
```

### Operadores Relacionales

```pseint
Algoritmo OperadoresRelacionales
    logico: esIgual, esDiferente, esMayor, esMenor, esMayorIgual, esMenorIgual
    esIgual <- (5 = 3)
    esDiferente <- (5 <> 3)
    esMayor <- (5 > 3)
    esMenor <- (5 < 3)
    esMayorIgual <- (5 >= 3)
    esMenorIgual <- (5 <= 3)

    Escribir esIgual, esDiferente, esMayor, esMenor, esMayorIgual, esMenorIgual
FinAlgoritmo
```

### Operadores Lógicos

```pseint
Algoritmo OperadoresLogicos
    logico: y, o, no
    y <- (verdadero y falso)
    o <- (verdadero o falso)
    no <- no verdadero

    Escribir y, o, no
FinAlgoritmo
```

## Estructuras de Control

### If-Else

```pseint
Algoritmo IfElse
    entero: a
    a <- 5
    Si a > 3 Entonces
        Escribir "a es mayor que 3"
    SiNo
        Escribir "a no es mayor que 3"
    FinSi
FinAlgoritmo
```

### Switch (Seleccionar)

```pseint
Algoritmo Seleccionar
    entero: x
    x <- 2
    Segun x Hacer
        1:
            Escribir "x es 1"
        2:
            Escribir "x es 2"
        DeOtroModo:
            Escribir "x no es 1 ni 2"
    FinSegun
FinAlgoritmo
```

### For Loop

```pseint
Algoritmo ForLoop
    entero: i
    Para i <- 0 Hasta 4 Hacer
        Escribir i
    FinPara
FinAlgoritmo
```

### While Loop

```pseint
Algoritmo WhileLoop
    entero: i
    i <- 0
    Mientras i < 5 Hacer
        Escribir i
        i <- i + 1
    FinMientras
FinAlgoritmo
```

### Do-While Loop

```pseint
Algoritmo DoWhileLoop
    entero: i
    i <- 0
    Repetir
        Escribir i
        i <- i + 1
    Hasta Que i = 5
FinAlgoritmo
```

## Funciones

### Declaración y Definición

```pseint
Funcion suma: entero
    parametros entero: a, b
    suma <- a + b
FinFuncion

Algoritmo FuncionSuma
    entero: resultado
    resultado <- suma(3, 4)
    Escribir "Resultado: ", resultado
FinAlgoritmo
```

### Funciones con Referencias

```pseint
Procedimiento incrementar
    Referencia entero: num
    num <- num + 1
FinProcedimiento

Algoritmo FuncionReferencia
    entero: a
    a <- 5
    incrementar(a)
    Escribir "a incrementado: ", a
FinAlgoritmo
```

## Ejemplos Comunes

### FizzBuzz

```pseint
Algoritmo FizzBuzz
    entero: i
    Para i <- 1 Hasta 100 Hacer
        Si (i % 3 = 0) y (i % 5 = 0) Entonces
            Escribir "FizzBuzz"
        SiNo
            Si (i % 3 = 0) Entonces
                Escribir "Fizz"
            SiNo
                Si (i % 5 = 0) Entonces
                    Escribir "Buzz"
                SiNo
                    Escribir i
                FinSi
            FinSi
        FinSi
    FinPara
FinAlgoritmo
```

### Número Primo

```pseint
Funcion esPrimo: logico
    parametros entero: n
    entero: i
    Si n <= 1 Entonces
        esPrimo <- falso
    SiNo
        esPrimo <- verdadero
        Para i <- 2 Hasta n - 1 Hacer
            Si n % i = 0 Entonces
                esPrimo <- falso
                SalirPara
            FinSi
        FinPara
    FinSi
FinFuncion

Algoritmo NumeroPrimo
    entero: num
    num <- 29
    Si esPrimo(num) Entonces
        Escribir num, " es un número primo"
    SiNo
        Escribir num, " no es un número primo"
    FinSi
FinAlgoritmo
```
