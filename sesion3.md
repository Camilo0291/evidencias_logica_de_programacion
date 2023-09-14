<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 3 


<!-- Su documentación aquí -->

# Actividad 3: Ejercicios de operaciones básicas en Java.

- Suma y multiplicación: Escribe un programa que solicite al usuario dos números enteros y luego imprima la suma y multiplicación de esos números.

- Resta y división: Escribe un programa que tome dos números enteros ingresados por el usuario y calcule la resta y división de esos números.

- Operaciones combinadas: Escribe un programa que solicite al usuario tres números enteros y realice las siguientes operaciones: suma de los tres números, multiplicación del primer número por el segundo y división del resultado entre el tercer número.

- Operaciones con decimales: Escribe un programa que solicite al usuario dos números decimales y realice las siguientes operaciones: suma, resta, multiplicación y división.

- Incremento y decremento: Escribe un programa que declare una variable entera y la inicialice con un valor. Luego, incrementa su valor en 1 y muestra el resultado. Después, decrementa su valor en 1 y muestra el resultado nuevamente.

- Operador de asignación compuesta: Escribe un programa que declare una variable entera y la inicialice con un valor. Utiliza el operador de asignación compuesta para sumar 5 a la variable y luego mostrar su valor.

- Operadores lógicos: Escribe un programa que tome dos valores booleanos ingresados por el usuario y muestre el resultado de las operaciones lógicas AND, OR y NOT entre esos valores.

- Operador ternario: Escribe un programa que tome un número entero ingresado por el usuario y utilice el operador ternario para determinar si el número es positivo o negativo. Luego, muestra el resultado en la salida.

# Solución:

1.
```java
package com.mycompany.ejercicioo1;

import java.util.Scanner;

public class Ejercicioo1 {

    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        System.out.println("Ingrese el primer número: ");
        int numero1 = entrada.nextInt();
        System.out.println("Ingrese be el segundo número: ");
        int numero2 = entrada.nextInt();

        int suma = numero1 + numero2;
        System.out.println("El resultado de la suma: " + suma);

        int multiplicación = numero1 * numero2;
        System.out.println("El resultado de la multiplicación: " + multiplicación);
        
    }
}
```

2.
```java
package com.mycompany.ejercicioo1;

import java.util.Scanner;

public class Ejercicioo1 {

    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        System.out.println("Ingrese el primer número: ");
        int numero1 = entrada.nextInt();
        System.out.println("Ingrese be el segundo número: ");
        int numero2 = entrada.nextInt();

        int suma = numero1 + numero2;
        System.out.println("El resultado de la suma: " + suma);

        int multiplicación = numero1 * numero2;
        System.out.println("El resultado de la multiplicación: " + multiplicación);
        
    }
}
```

3.
```java
package com.mycompany.ejercicioo3;

import java.util.Scanner;

public class Ejercicioo3 {

    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        System.out.println("Ingrese el primer número: ");
        int numero1 = entrada.nextInt();
        System.out.println("Ingrese el segundo número: ");
        int numero2 = entrada.nextInt();
        System.out.println("Ingrese el tercer número: ");
        int numero3 = entrada.nextInt();

        int suma = numero1 + numero2 + numero3;
        int multiplicación = numero1 * numero2;

        System.out.println("El resultado de la suma: " + suma);
        System.out.println("El resultado de la multiplicación: " + multiplicación);
        System.out.println("El resultado de la división es: " + numero3);

    }
}
```

4.
```java
package com.mycompany.ejercicioo4;

import java.util.Scanner;

public class Ejercicioo4 {

    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        System.out.println("Ingrese el primer número decimal: ");
        double numero1 = entrada.nextDouble();
        System.out.println("Ingrese el segundo número decimal");
        double numero2 = entrada.nextDouble();

        double suma = numero1 + numero2;
        double resta = numero1 - numero2;
        double multiplicación = numero1 * numero2;
        double división = numero1 / numero2;
        
        System.out.println("El resultado: "+ suma);
        System.out.println("El resultado: "+ resta);
        System.out.println("El resultado: "+ multiplicación);
        System.out.println("El resultado: "+ división);
        
        

    }
}
```

5.
```java
package com.mycompany.ejercicioo5;

public class Ejercicioo5 {

    public static void main(String[] args) {
        
        int numero = 10;
        
        numero++;
        System.out.println("El valor después del incremento es: "+ numero);
        
        numero--;
        System.out.println("El valor después del decremento es: "+numero);
    }
}     
```

6.
```java
package com.mycompany.ejercicioo6;

public class Ejercicioo6 {

    public static void main(String[] args) {
       int numero = 10;
       numero +=5;
        System.out.println("El valor de la variable es: "+numero);
       
    }
}      
```

7.
```java
package com.mycompany.ejercicioo7;

import java.util.Scanner;

public class Ejercicioo7 {

    public static void main(String[] args) {

        Scanner entrada = new Scanner(System.in);
        
        System.out.println("Ingrese el primer valor booleano (true o false): ");
        boolean valor1 = entrada.nextBoolean();
        System.out.println("Ingrese el segundo valor booleano (true o false): ");
        boolean valor2 = entrada.nextBoolean();

        boolean resultadoAnd = valor1 && valor2;
        boolean resultadoOr = valor1 || valor2;
        boolean resultadoNot1 = !valor1;
        boolean resultadoNot2 = !valor2;
        
        System.out.println("Resultado de la operación AND: "+resultadoAnd);
        System.out.println("Resultado de la operación OR: "+resultadoOr);
        System.out.println("Resultado de la operación NOT: "+resultadoNot1);
        System.out.println("Resultado de la operación NOT: "+resultadoNot2);
        
        
        
    }
}
```

8.
```java
package com.mycompany.ejercicioo8;

import java.util.Scanner;

public class Ejercicioo8 {

    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        System.out.println("Escribe un número:");
        double numero = entrada.nextDouble();

        if (numero == 0) {

        } else if (numero < 0) {
            System.out.println("El número es negativo");
        } else {
            System.out.println("El número es positivo");
        }

    }
}
```






