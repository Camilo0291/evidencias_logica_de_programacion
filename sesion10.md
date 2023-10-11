<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


<!-- Su documentación aquí -->

# Actividad: Prueba, ejecución y explicación de ejercicios de lógica de programación.
Selecciona dos ejercicios de la sesión 10, impleméntalos, ejecútalos y proporciona una explicación detallada de cada uno

```java
import java.util.Scanner;

public class MRU {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double velocidad, tiempo, distancia;
      
      // Solicita la velocidad y el tiempo
      System.out.print("Ingrese la velocidad en metros por segundo: ");
      velocidad = input.nextDouble();
      System.out.print("Ingrese el tiempo en segundos: ");
      tiempo = input.nextDouble();

      // Calcula la distancia recorrida
      distancia = velocidad * tiempo;

      // Muestra el resultado en la consola
      System.out.printf("La distancia recorrida es de %.2f metros.", distancia);
   }
}
```
### Explicación:

1. import java.util.Scanner;: esta línea importa la clase Scanner del paquete java.util, que se utiliza para recuperar datos de entrada del usuario.
2. public class MRU {: Aquí se declara una clase denominada MRU. Esta es la clase principal del programa, incluido el método principal, que es el punto de entrada del programa Java.
3. public static void main(String[] args) {: Este es el método principal del programa. Cuando se ejecuta el programa, Java comienza a ejecutar el código en el método. Los argumentos pasados ​​al programa se reciben como matrices de cadenas (String[] args), aunque no se utilizan en este ejemplo. Entrada del escáner = nuevo escáner (System.in);: crea un objeto de escáner llamado entrada que se utiliza para leer la entrada del usuario desde la consola.
4. doble velocidad, tiempo, distancia;: declara tres variables de tipo doble para contener velocidad, tiempo y distancia. 5. Estas variables se utilizarán para realizar los cálculos.
6. System.out.print("Ingrese la velocidad en metros por segundo:");: se mostrará un mensaje en la consola solicitando al usuario que ingrese la velocidad en metros por segundo. speed = input.nextDouble();: el objeto escáner se utiliza para leer el valor decimal ingresado por el usuario (doble precisión) almacenado en la variable de velocidad.
7. System.out.print("Ingrese el tiempo en segundos:");: Se mostrará un mensaje en la consola solicitando al usuario que ingrese el tiempo en segundos. time = input.nextDouble();: utiliza nuevamente el objeto escáner para leer el valor decimal (doble) ingresado por el usuario y almacenado en la variable tiempo.
8. Distancia = velocidad * tiempo;: La distancia recorrida se calcula multiplicando la velocidad por el tiempo. Este cálculo se realiza según la fórmula MRU: distancia = velocidad * tiempo.
9. System.out.printf("La distancia recorrida es %.2f metros.", distancia);: los resultados se muestran en la consola usando System.out.printf. El resultado tiene el formato de dos decimales (%.2f) y se muestra en el mensaje.


```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.Scanner;

public class AsignacionEjercicios {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      ArrayList<String> personas = new ArrayList<String>();

      // Solicitar lista de personas
      System.out.print("Ingrese la lista de personas separadas por coma: ");
      String inputPersonas = input.nextLine();
      String[] personasArray = inputPersonas.split(",");
      for (String persona : personasArray) {
         personas.add(persona.trim());
      }

      // Obtener cantidad de ejercicios
      int cantidadEjercicios = personas.size();

      // Generar lista de ejercicios aleatorios sin repetir
      ArrayList<Integer> numerosEjercicios = new ArrayList<Integer>();
      for (int i = 1; i <= cantidadEjercicios; i++) {
         numerosEjercicios.add(i);
      }
      Collections.shuffle(numerosEjercicios); // mezclar la lista de números de ejercicios para asignarlos aleatoriamente
      ArrayList<String> ejercicios = new ArrayList<String>();
      for (int i = 0; i < cantidadEjercicios; i++) {
         ejercicios.add("Ejercicio " + numerosEjercicios.get(i));
      }

      // Asignar ejercicios a personas
      Collections.shuffle(personas); // mezclar la lista de personas para asignarles ejercicios aleatorios
      for (int i = 0; i < cantidadEjercicios; i++) {
         System.out.printf("%s: %s%n", personas.get(i), ejercicios.get(i));
      }
   }
}
```

### Explicación:

1. Se importan las clases necesarias:

- java.util.ArrayList: Para trabajar con listas dinámicas.
- java.util.Collections: Para realizar operaciones de mezcla (shuffle) en listas.
- java.util.Scanner: Para obtener la entrada del usuario.
- Se declara una variable input de tipo Scanner para capturar la entrada del usuario.

2. Se crea una lista personas de tipo ArrayList`<String>` para almacenar los nombres de las personas.

3. El programa solicita al usuario que ingrese una lista de nombres de personas separados por comas. La entrada se lee como una cadena (inputPersonas).

4. Se utiliza el método split(",") para dividir la cadena ingresada en un arreglo de cadenas personasArray, separadas por comas.

5. Se recorre el arreglo personasArray, se eliminan los espacios en blanco alrededor de cada nombre utilizando trim(), y se agregan los nombres limpios a la lista personas.

6. Se obtiene la cantidad de ejercicios a asignar, que es igual a la cantidad de personas en la lista.

7. Se crea una lista numerosEjercicios de tipo ArrayList`<Integer>` para representar los números de ejercicios disponibles. Esta lista contiene números del 1 al número de personas, inicialmente en orden.

8. Se utiliza Collections.shuffle(numerosEjercicios) para mezclar aleatoriamente los números de ejercicios en la lista numerosEjercicios. Esto asegura que los ejercicios se asignen aleatoriamente a las personas.

9. Se crea una lista ejercicios de tipo ArrayList`<String>` para almacenar los ejercicios asignados. Se asigna a cada ejercicio un nombre "Ejercicio X", donde X es el número de ejercicio obtenido de la lista mezclada numerosEjercicios.

10. Se mezcla aleatoriamente la lista personas utilizando Collections.shuffle(personas). Esto garantiza que los ejercicios se asignen aleatoriamente a las personas.

11. Se recorren las listas personas y ejercicios y se muestra en la consola la asignación de ejercicio para cada persona.

