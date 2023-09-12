<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


<!-- Su documentación aquí -->

# Actividad 4: Ejercicios de control de flujo con expresiones compuestas

```Java
// Variables de tipo String
String nombre = "Juan Pérez";
String apellido = "González";
String identificación = "1000000001";
String correo = "juan.perez@ejemplo.com";
String carrera = "Desarrollo de Software";
String universidad = "Cesde";
// Variable de tipo int
int edad = 20;
// Variable de tipo boolean
boolean esActivo = true;
boolean becado = false;
// Variable de tipo char
char género = 'M';
// Variable de tipo double
double promedio = 4.5;
// Variable de tipo int
int semestre = 2;
```

Con la información anterior, implementa los siguientes ejercicios:

1. Determinar si el estudiante es mayor de edad y tiene un estado activo.
2. Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.
3. Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.
4. Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.
5. Mostrar toda la información del estudiante si está matriculado en el Cesde.
6. Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.
7. Determinar la cantidad de beca que recibe el estudiante según su promedio:
- 0.0 - 3.4: El estudiante no recibe beca.
- 3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
- 4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
- 4.5 - 5.0: El estudiante recibe una beca completa.


# Solución:

```Java
package com.mycompany.actividad4;

import java.util.Scanner;

public class Actividad4 {

    public static void main(String[] args) {
        // Variables de tipo String
        String nombre = "Juan";
        String apellido = "Pérez González";
        String identificación = "1000000001";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
// Variable de tipo int
        int edad = 20;
// Variable de tipo boolean
        boolean esActivo = true;
        boolean becado = false;
// Variable de tipo char
        char género = 'M';
// Variable de tipo double
        double promedio = 4.5;
// Variable de tipo int
        int semestre = 2;

        System.out.println("----------------------------------");
        System.out.println("Ejercicio 1");

        if (edad >= 18 && esActivo) {
            System.out.println("Es mayor de edad y esta activo");
        }

        System.out.println("----------------------------------");
        System.out.println("Ejercicio 2");

        if (becado || carrera.equals("Desarrollo de Software")) {
            System.out.println("El estudiante tiene una beca o estudia desarrollo de software");
        }

        System.out.println("----------------------------------");
        System.out.println("Ejercicio 3");

        if (semestre == 2 && esActivo) {
            System.out.println("El estudiante está en el último semestre de su carrera y esta activo.");
        }

        System.out.println("----------------------------------");
        System.out.println("Ejercicio 4");

        if (carrera.equals("Desarrollo de Software") && promedio > 4.0) {
            System.out.println("El estudiante cumple con los requisitos");
        } else {
            System.out.println("El estudiante no cumple con los requisitos");
        }

        System.out.println("----------------------------------");
        System.out.println("Ejercicio 5");

        if (universidad == "Cesde") {
            System.out.println("Información del estudiante");
            System.out.println(nombre);
            System.out.println(apellido);
            System.out.println(identificación);
            System.out.println(correo);
            System.out.println(carrera);
            System.out.println(universidad);
            System.out.println(edad);
            System.out.println(esActivo);
            System.out.println(becado);
            System.out.println(género);
            System.out.println(promedio);
            System.out.println(semestre);
        }

        System.out.println("----------------------------------");
        System.out.println("Ejercicio 6");

        if ("Cesde".equals(universidad) && promedio >= 4.1 && esActivo) {
            System.out.println("Tienes una beca del 50%");
        }

        System.out.println("----------------------------------");
        System.out.println("Ejercicio 7");

        if (promedio >= 4.5) {
            System.out.println("Tienes una beca completa para estudiar tu carrera de desarrollo");
        }

        System.out.println("----------------------------------");
        System.out.println("Ejercicio 8");

        String mensaje = (género == 'M') ? "El estudiante es hombre" : (género == 'F') ? "El estudiante es mujer" : "El género del estudiante es desconocido";
        System.out.println(mensaje);

        System.out.println("----------------------------------");
        System.out.println("Ejercicio 9");

        switch (semestre) {
            case 1:
                System.out.println("El estudiante está en el primer semestre");
                break;
            case 2:
                System.out.println("El estudiante está en el segundo semestre");
                break;
            case 3:
                System.out.println("El estudiante está en el tercer semestre");
                break;
            default:
                System.out.println("El estudiante está en un semestre posterior al tercero");
                break;
        }

        System.out.println("----------------------------------");
        System.out.println("Ejercicio 10");

        if (promedio >= 4.0) {
            System.out.println("El estudiante tiene un promedio mayor o igual a 4.0");
        } else if (promedio >= 3.5) {
            System.out.println("El estudiante tiene un promedio mayor o igual a 3.5");
        } else {
            System.out.println("El estudiante tiene un promedio menor a 3.5");
        }

    }
}
```







