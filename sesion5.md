<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 


<!-- Su documentación aquí -->

# Actividad 5: Ejercicios de bucles

Resolver los siguientes ejercicios:

## Ejercicios - while
- Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.
- Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.

## Ejercicios - do while
- Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.
- Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.

## Ejercicios - for
- Imprimir los números impares del 1 al 50.
- Imprimir los números primos del 1 al 100.

# Solución:

### while
1.
```java
package com.mycompany.ejercicioo1;

import java.util.Scanner;

public class Ejercicioo1 {

    public static void main(String[] args) {

        System.out.println("----------------------------------");
        System.out.println("Ejercicio 1 while");

        Scanner scanner = new Scanner(System.in);

        System.out.println("Ingrese un numero: ");
        int numero = scanner.nextInt();

        for (int i = 1; i <= 10; i++) {
            int resultado = numero * i;
            System.out.println(numero + "x" + i + "=" + resultado);
        }
    }
}
```

2.
``` Java
package com.mycompany.ejercicioo1;

import java.util.Scanner;

public class Ejercicioo1 {

    public static void main(String[] args) {

        System.out.println("----------------------------------");
        System.out.println("Ejercicio 2 while");

        Scanner sr = new Scanner(System.in);

        System.out.print("Ingrese una cadena de caracteres: ");
        String cadena = sr.nextLine();

        int contadorCaracteres = 0;
        for (int i = 0; i < cadena.length(); i++) {
            if (Character.isDigit(cadena.charAt(i))) {
                contadorCaracteres++;
                System.out.println("La cantidad de caracteres que son numeros son: " + contadorCaracteres);

            }
        }
    }
}
```

### do while
1.
``` Java
package com.mycompany.ejercicioo2;

import java.util.Scanner;

public class Ejercicioo2 {

    public static void main(String[] args) {

        System.out.println("-------------------------------------");
        System.out.println("Ejercicio 1 do-while");

        Scanner scanner = new Scanner(System.in);

        int numero = 0;
        do {
            System.out.print("Ingrese un número: ");
            numero = scanner.nextInt();

            if (numero >= 0) {
                for (int i = 1; i <= 100; i++) {
                    System.out.println(i);
                }
            }
        } while (numero >= 0);

        System.out.println("Ha ingresado un número negativo. El programa se ha detenido.");
    }
}
```


2.
``` Java
package com.mycompany.ejercicioo2;

import java.util.Scanner;

public class Ejercicioo2 {

    public static void main(String[] args) {

        System.out.println("---------------------------------");
        System.out.println("Ejercicio 2 do-while");

        int número;

        do {
            System.out.println("Ingrese un número entero (0 para salir): ");
            numero = scanner.nextInt();

            if (numero != 0) {
                System.out.println("Tabla de multiplicar del numero " + numero + ":");
                for (int i = 1; i <= 10; i++) {
                    System.out.println(numero + "X" + i + "=" + (numero * i));
                }
                System.out.println();
            }
        } while (numero != 0);
        System.out.println("El programa se ha detenido. Ha ingresado el número 0.");

    }
}
```

### for
1.
``` Java
package com.mycompany.ejercicioo3;

import java.util.Scanner;

public class Ejercicioo3 {

    public static void main(String[] args) {

        System.out.println("-------------------------------------");
        System.out.println("Ejercicio 1 for");

        for (int i = 1; i <= 50; i++) {
            if (i % 2 != 0) {
                System.out.println(i + "");
            }
        }
    }
}
```

2.
``` Java
package com.mycompany.ejercicioo3;

import java.util.Scanner;

public class Ejercicioo3 {

     System.out.println("-----------------------------------------");
        System.out.println("Ejercicio 2 for");

        for (int i = 2; i <= 100; i++) {
            int raiz = (int) Math.sqrt(i);
            int contador = 0;
            for (int j = raiz; j > 1; j--) {
                if (i % j == 0) {
                    contador++;
                }
            }
            if (contador < 1) {
                System.out.println(i);
            }
        }

    }
```






