<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 


<!-- Su documentación aquí -->

# Actividad: Ejecicios Array - ArrayList
## 1. En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.

#### Actividad realizada con el compañero Nelson Fonnegra

### Ejemplo Array
```java
import java.util.Arrays;

public class EjercicioArray {

    public static void main(String[] args) {
        // Crear un array de números enteros
        int[] numeros = {5, 2, 10, 7, 1};

        // Imprimir el array original
        System.out.println("Array original: " + Arrays.toString(numeros));

        // Calcular la suma de los elementos del array
        int suma = 0;
        for (int i = 0; i < numeros.length; i++) {
            suma += numeros[i];
        }
        System.out.println("La suma de los elementos es: " + suma);

        // Encontrar el número más grande en el array
        int maximo = numeros[0];
        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);

        // Ordenar el array en orden ascendente
        Arrays.sort(numeros);
        System.out.println("Array ordenado: " + Arrays.toString(numeros));
    }
}
```

### Ejemplo Array list
```java
import java.util.ArrayList; 
import java.util.Scanner;

public class AppNotas {

  public static void main(String[] args) {

    ArrayList<String> notas = new ArrayList<>();
    
    Scanner scan = new Scanner(System.in);

    while(true) {

      System.out.println("1. Agregar nota");  
      System.out.println("2. Mostrar notas");
      System.out.println("3. Salir");

      int opcion = scan.nextInt();

      if (opcion == 1) {
        agregarNota(notas, scan);  
      } else if (opcion == 2) {
        mostrarNotas(notas);
      } else {
        break;
      }

    }

  }

  public static void agregarNota(ArrayList<String> notas, Scanner scan) {
    
    System.out.println("Ingrese el titulo de la nota:");
    String titulo = scan.nextLine();
    
    System.out.println("Ingrese el contenido de la nota:");
    String contenido = scan.nextLine();
    
    notas.add(titulo + " - " + contenido);

  }

  public static void mostrarNotas(ArrayList<String> notas) {

    for(String n : notas) {
      System.out.println(n);
    }

  }

}
```

## 2. Crear un ejemplo de Array y otro de ArrayList para visualizar sus diferencias.


### Array

```java
package com.mycompany.mavenproject3;

import java.util.Arrays;

public class Mavenproject3 {

    public static void main(String[] args) {

        // Crear un array de palabras
        String[] palabras = {"manzana", "banana", "pera", "maracuya" "naranja", "kiwi"};

        // Imprimir el array original
        System.out.println("Array original: " + Arrays.toString(palabras));

        // Concatenar todas las palabras en una sola cadena
        String concatenacion = "";
        for (int i = 0; i < palabras.length; i++) {
            concatenacion += palabras[i];
        }
        System.out.println("Concatenación de palabras: " + concatenacion);

        // Encontrar la palabra más larga en el array
        String palabraMasLarga = palabras[0];
        for (int i = 1; i < palabras.length; i++) {
            if (palabras[i].length() > palabraMasLarga.length()) {
                palabraMasLarga = palabras[i];
            }
        }
        System.out.println("La palabra más larga es: " + palabraMasLarga);

        // Ordenar el array en orden alfabético
        Arrays.sort(palabras);
        System.out.println("Array ordenado: " + Arrays.toString(palabras));
    }
}
```





