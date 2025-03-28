Clase 1
================

## Tipos de datos en R

### Datos básicos

Los tipos de datos básicos que tenemos en R son:

- ‘logical’: las posibles valores son `TRUE` o `FALSE`. **Importante:**
  R es sensible a mayusculas.
- ‘character’: una secuencia de caracteres (puede ser solo uno), se
  escribe entre comillas simples o dobles `"Hola mundo"`.
- ‘numeric’: un numero con decimeales. Es importante que utilicemos el
  punto como separador `3.1415`.
- ‘integer’: un número entero.
- ‘complex’: un número complejo `3-2i`.
- ‘raw’: es una sequencia de bits.

Los ultimos tipos de datos no los vamos a utilizar.

## Including Code

#### Asignaciones de variables

Para asignar el valor a una variable, se utiliza el símbolo el operador
de asignación (‘\<-’), apuntando hacia el objeto que recibe el valor.
Por ejemplo, le asignamos a la variable x el valor 2.

``` r
x <- 2
```

**Importante:** Si en una instancia posterior del código realizamos otra
asignación hacia la variable x, perderemos el valor 2 asignado
previamente.

R trabaja sobre estructuras de datos. La estructura más simple es un
vector numérico, que consiste en un conjunto ordenado de números. Cuando
asignamos un valor a una variable, estamos creando un vector de
dimensión 1.

Para crear vectores de dimensión mayor se utiliza el comando `c()`. Por
ejemplo, para asignarle a la variable y un vector que contenga los
valores 3, 6 y 2 haremos

``` r
y <- c(3,6,2)
```

Para saber qué valores tiene la variable y, la imprimimos.

``` r
print(y)
```

    ## [1] 3 6 2

Si bien el comando `<-` es el más utilizado, existen otras formas de
asignación de variables. Podemos utilizar el comando
`assign("variable", valor)`.

``` r
assign("x", c(1.3, 2.5, 4.2, 9.7, 8.1))
print(x)
```

    ## [1] 1.3 2.5 4.2 9.7 8.1

Notar que ahora x ya no vale 2.

La asignación también se puede realizar utilizando el comando `<-` en la
otra dirección

``` r
c(1, 2, 3) -> x
print(x)
```

    ## [1] 1 2 3

Si no se utiliza ninguna de las tres formas de asignación, el valor se
mostrará por pantalla pero no se guardará en ninguna variable.

``` r
c(3, 5, 6)
```

    ## [1] 3 5 6

## Aritmética vectorial

Los vectores pueden usarse en expresiones aritméticas, donde las
operaciones se realizan elemento a elemento.

``` r
v1 <- c(3, 5, 6)
v2 <- c(5, 7, 13)
v3 <- v1 + v2

print(v3)
```

    ## [1]  8 12 19

Dos vectores que se utilizan en la misma expresión no tienen por qué ser
de la misma longitud.

Si no lo son, el resultado será un vector de la longitud del más largo,
y el más corto será reciclado, repitiéndolo tantas veces como sea
necesario (puede que no un número exacto de veces) hasta que coincida
con el más largo. Lo mismo sucede cuando a un vector le sumamos un
escalar.

R suele advertirnos de este problema.

``` r
v1 <- c(3, 5, 6)
v2 <- c(5, 7, 13, 6, 19)
v3 <- v1 + v2
```

    ## Warning in v1 + v2: longitud de objeto mayor no es múltiplo de la longitud de
    ## uno menor

``` r
print(v3)
```

    ## [1]  8 12 19  9 24

``` r
v4 <- v1/v2
```

    ## Warning in v1/v2: longitud de objeto mayor no es múltiplo de la longitud de uno
    ## menor

``` r
print(v4)
```

    ## [1] 0.6000000 0.7142857 0.4615385 0.5000000 0.2631579

Algunas funciones importantes para trabajar con vectores son: `sum(v1)`,
`length(v1)`, `mean(v1)`, `cumsum(v1)`, `var(v1)`, `sort(v1)`, etc

## Including Plots

Acá mejor no incluir gráficos.

You can also embed plots, for example:

![](Clase1_files/figure-gfm/pressure-1.png)<!-- -->

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.

En el mismo lugar, como digjo el Torta!!!

### ESTO SE VA A ROMPER

Si estamos escribiendo en el mismo lugar, no deberia saber en que orden
poner las cosas.
