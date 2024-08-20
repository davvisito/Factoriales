# Factorial de un Numero

## ¿Que es la funcion factorial?

La función factorial se representa con un signo de exclamación “!” detrás de un número. Esta exclamación quiere decir que hay que multiplicar todos los números enteros positivos que hay entre ese número y el 1.

### Ejemplo:

6! = 1 x 2 3 x 4 x 5 x 6 = 720


en este caso, el numero factorial es 6, generalmente "6 factorial"

```

fun main() {
    // Número fijo para calcular el factorial
    val numero = 6
    
    // Calculamos el factorial usando la función recursiva
    val resultado = factorial(numero)
    
    // Imprimimos el resultado
    println("El factorial de $numero es $resultado")
}

// Función recursiva para calcular el factorial
fun factorial(n: Int): Int {
    return if (n <= 1) 1 else n * factorial(n - 1)
}

```



## Estructura de la funcion funcional:

```
fun factorial(n: Int): Int {
    return if (n <= 1) 1 else n * factorial(n - 1)
}
```

**Explicación del Código**:

Caso Base:

if (n <= 1) 1: Esto cubre los casos base de la recursión.
El factorial de 0 y 1 es 1, por lo que la función retorna 1 cuando n es 0 o 1.
El caso base es crucial para evitar la recursión infinita y para proporcionar un valor que pueda combinarse con los resultados de las llamadas recursivas.

Función principal main:

* Define un número fijo (numero = 6) cuyo factorial se quiere calcular.
* Llama a la función factorial para calcular el factorial de ese número.
* Imprime el resultado en la consola.

Función recursiva factorial:

* Calcula el factorial de un número entero n.
* Si n es menor o igual a 1, devuelve 1 (caso base de la recursión).
* Si n es mayor que 1, multiplica n por el resultado de la función factorial(n - 1), llamándose a sí misma con n - 1.

  Al ejecutar saldra por pantalla:

  ```
  El factorial de 6 es 720
  
  ```


## Errores Comunes

* **Número Negativo**: La función no maneja números negativos, lo que podría llevar a una recursión infinita o un resultado incorrecto si no se valida la entrada adecuadamente.
* **Desbordamiento de Pila**: Para números muy grandes, el uso de recursión puede causar un desbordamiento de pila.
