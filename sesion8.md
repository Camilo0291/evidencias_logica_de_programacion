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