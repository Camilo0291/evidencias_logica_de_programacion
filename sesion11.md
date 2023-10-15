<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 


<!-- Su documentación aquí -->


# Actividad: Ejercicios de Lógica de Programación

1. Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.

2. Desarrollar un algoritmo que realice la conversión de binario a decimal.

# Solución:

1.
```java
package com.mycompany.actividad11;

import java.util.HashSet;

public class Actividad11 {

    public static void main(String[] args) {

        int[] numeros = {1, 2, 3, 4, 5, 2, 4, 6, 7, 8, 8};

        HashSet<Integer> numerosRepetidos = new HashSet<>();

        for (int i = 0; i < numeros.length; i++) {

            for (int j = i + 1; j < numeros.length; j++) {
                if (numeros[i] == numeros[j]) {

                    numerosRepetidos.add(numeros[i]);
                    break;
                }
            }
        }

        if (!numerosRepetidos.isEmpty()) {
            System.out.println("Los números repetidos son:");
            for (int numero : numerosRepetidos) {
                System.out.println(numero);
            }
        } else {

            System.out.println("No hay ningún número repetido");
        }
    }
}
```

2. 

```java
package com.mycompany.actividad11;

import java.util.Scanner;

public class Actividad11 {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        System.out.print("Ingresa un número binario: ");
        String input = scanner.next();

        int decimal = binarioADecimal(input);

        System.out.println("El equivalente decimal es: " + decimal);
    }

    public static int binarioADecimal(String binario) {
        int decimal = 0;
        int longitud = binario.length();

        for (int i = 0; i < longitud; i++) {
            char digito = binario.charAt(i);
            int valor = Character.getNumericValue(digito);

            if (valor != 0 && valor != 1) {
                System.err.println("La entrada no es un número binario válido.");
                System.exit(1);
            }

            int potencia = longitud - i - 1;
            decimal += valor * Math.pow(2, potencia);
        }

        return decimal;
    }
}
```

