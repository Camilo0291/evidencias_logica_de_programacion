<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


<!-- Su documentación aquí -->

# Actividad: Ejecicios de métodos en Java
Implementar los siguientes métodos:

- Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

# Solución:

1. 
```java

package com.mycompany.numeromayor;

public class Numeromayor {

    public static void main(String[] args) {
        int num1 = 8;
        int num2 = 5;

        int mayor = obtenerMayor(num1, num2);

        System.out.println("El mayor número es: " + mayor);
    }

    public static int obtenerMayor(int num1, int num2) {
        if (num1 > num2) {
            return num1;
        } else {
            return num2;
        }
    }
}
```

2.
```java

package com.mycompany.cadenavocales;

public class Cadenavocales {

    public static int contarVocales(String texto) {
        int contador = 0;

        texto = texto.toLowerCase();

        for (int i = 0; i < texto.length(); i++) {
            char letra = texto.charAt(i);

            if (letra == 'a' || letra == 'e' || letra == 'i' || letra == 'o' || letra == 'u') {
                contador++;
            }
        }

        return contador;
    }

    public static void main(String[] args) {
        String texto = "Hola mundo";
        int numeroVocales = contarVocales(texto);

        System.out.println("Número de vocales: " + numeroVocales);
    }
}
```

3.
```java

package com.mycompany.cadenaordenalfabetico;

public class Cadenaordenalfabetico {

    public static String convertirMayusculasMinisculas(String cadena) {
        StringBuilder nuevaCadena = new StringBuilder();

        for (int i = 0; i < cadena.length(); i++) {
            char caracter = cadena.charAt(i);

            if (Character.isUpperCase(caracter)) {

                nuevaCadena.append(Character.toLowerCase(caracter));
            } else if (Character.isLowerCase(caracter)) {

                nuevaCadena.append(Character.toUpperCase(caracter));
            } else {
                nuevaCadena.append(caracter);
            }
        }

        return nuevaCadena.toString();
    }

    public static void main(String[] args) {
        String cadena = "Hola Mundo!";
        String nuevaCadena = convertirMayusculasMinisculas(cadena);
        System.out.println("Cadena original: " + cadena);
        System.out.println("Cadena convertida: " + nuevaCadena);
    }
}
```

4.
```java

package com.mycompany.numeropalabras;

public class Numeropalabras {

    public static int contarPalabras(String texto) {
        if (texto == null || texto.isEmpty()) {
            return 0;
        }
        String[] palabras = texto.split("\s+");
        return palabras.length;
    }

    public static void main(String[] args) {
        String texto = "Esto es una cadena de texto.";
        int numeroPalabras = contarPalabras(texto);
        System.out.println("Numero de palabras: " + numeroPalabras);
    }
}
```

5.
```java

package com.mycompany.cadenapalabras;

import java.util.Arrays;

public class Cadenapalabras {

    public static void main(String[] args) {
        String texto = "Hola mundo, este es un ejemplo";
        String resultado = ordenarPalabras(texto);
        System.out.println(resultado);
    }

    public static String ordenarPalabras(String texto) {

        String[] palabras = texto.split(" ");

        Arrays.sort(palabras);

        String resultado = String.join(" ", palabras);

        return resultado;

    }
}
```



