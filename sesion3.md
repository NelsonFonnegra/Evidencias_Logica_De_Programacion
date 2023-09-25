<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 3 


<!-- Su documentación aquí -->


# Actividad 3: Ejercicios de operaciones básicas en Java.

Suma y multiplicación: Escribe un programa que solicite al usuario dos números enteros y luego imprima la suma y multiplicación de esos números.

Resta y división: Escribe un programa que tome dos números enteros ingresados por el usuario y calcule la resta y división de esos números.

Operaciones combinadas: Escribe un programa que solicite al usuario tres números enteros y realice las siguientes operaciones: suma de los tres números, multiplicación del primer número por el segundo y división del resultado entre el tercer número.

Operaciones con decimales: Escribe un programa que solicite al usuario dos números decimales y realice las siguientes operaciones: suma, resta, multiplicación y división.

Incremento y decremento: Escribe un programa que declare una variable entera y la inicialice con un valor. Luego, incrementa su valor en 1 y muestra el resultado. Después, decrementa su valor en 1 y muestra el resultado nuevamente.

Operador de asignación compuesta: Escribe un programa que declare una variable entera y la inicialice con un valor. Utiliza el operador de asignación compuesta para sumar 5 a la variable y luego mostrar su valor.

Operadores lógicos: Escribe un programa que tome dos valores booleanos ingresados por el usuario y muestre el resultado de las operaciones lógicas AND, OR y NOT entre esos valores.

Operador ternario: Escribe un programa que tome un número entero ingresado por el usuario y utilice el operador ternario para determinar si el número es positivo o negativo. Luego, muestra el resultado en la salida.

### SOLUCIÓN
```JAVA

package com.mycompany.actividad3;


import java.util.Scanner;

public class Actividad3 {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        //Escribe un programa que solicite al usuario dos números enteros y luego imprima la suma y multiplicación de esos números.
        System.out.println("1. Suma y multiplicación ");
        
        System.out.print("Ingrese el primer número: ");
        int numero1 = (int) scanner.nextInt();

        System.out.print("Ingrese el segundo número: ");
        int numero2 = (int) scanner.nextInt();

        int suma = numero1 + numero2;

        System.out.println("El resultado de la suma es: " + suma);

        int multiplicacion = numero1 * numero2;

        System.out.println("El resultado de la multiplicación es: " + multiplicacion);

        //Escribe un programa que tome dos números enteros ingresados por el usuario y calcule la resta y división de esos números.
        System.out.println("2. Resta y división ");
        System.out.print("Ingrese el primer número: ");
        int numero3 = (int) scanner.nextInt();

        System.out.print("Ingrese el segundo número: ");
        int numero4 = (int) scanner.nextInt();

        int resta = numero3 - numero4;

        System.out.println("El resultado de la resta es: " + resta);

        int division = numero3 / numero4;

        System.out.println("El resultado de la división es: " + division);

        //Escribe un programa que solicite al usuario tres números enteros y realice las siguientes operaciones: suma de los tres números, multiplicación del primer número por el segundo y división del resultado entre el tercer número.
        System.out.println("3. Operaciones combinadas ");
        
        System.out.print("Ingrese el primer número: ");
        int numero5 = (int) scanner.nextInt();

        System.out.print("Ingrese el segundo número: ");
        int numero6 = (int) scanner.nextInt();

        System.out.print("Ingrese el tercer número: ");
        int numero7 = (int) scanner.nextInt();

        int sumatotal = numero5 + numero6 + numero7;

        System.out.println("El resultado de la suma es: " + sumatotal);

        int multiplicacionnum5pornum6 = numero5 * numero6;

        System.out.println("El resultado de la multiplicación es: " + multiplicacionnum5pornum6);

        double resultadodivision = multiplicacionnum5pornum6 / numero7;

        System.out.println("El resultado de la división es: " + resultadodivision);

        //Escribe un programa que solicite al usuario dos números decimales y realice las siguientes operaciones: suma, resta, multiplicación y división.
        System.out.println("4. Operaciones con decimales ");
        
        System.out.print("Ingrese el primer número decimal: ");
        double numero8 = (double) scanner.nextDouble();
        
        System.out.print("Ingrese el segundo número decimal: ");
        double numero9 = (double) scanner.nextDouble();
        
        double sumadecimal = numero8 + numero9;
        System.out.println("El resultado de la suma es: " + sumadecimal);
        
        double restadecimal = numero8 - numero9;
        System.out.println("El resultado de la resta es: " + restadecimal);
        
        double multiplicaciondecimal = numero8 * numero9;
        System.out.println("El resultado de la multiplicación es: " + multiplicaciondecimal);
        
        double divisiondecimal = numero8 / numero9;
        System.out.println("El resultado de la división es: " + divisiondecimal);
        
//Escribe un programa que declare una variable entera y la inicialice con un valor. Luego, incrementa su valor en 1 y muestra el resultado. Después, decrementa su valor en 1 y muestra el resultado nuevamente.
        
        System.out.println("5. Incremento y decremento ");
        
        System.out.print("Ingrese un valor: ");
        int valor = (int) scanner.nextInt();
        
        
        valor = valor + 1;
        System.out.println("el valor después del incremento es: " + valor);
        
        valor = valor - 1;
        System.out.println("el valor después del decremento es: " + valor);
        
        //Escribe un programa que declare una variable entera y la inicialice con un valor. Utiliza el operador de asignación compuesta para sumar 5 a la variable y luego mostrar su valor.
        System.out.println("6. Operador de asignación compuesta: ");
        
        System.out.print("Ingrese un valor: ");
        int valor2 = (int) scanner.nextInt();
        
        valor2 += 5;
        System.out.println("El valor de la variable después de sumar 5 es: " + valor2);
        
        
//Escribe un programa que tome dos valores booleanos ingresados por el usuario y muestre el resultado de las operaciones lógicas AND, OR y NOT entre esos valores.
  System.out.println("7. Operadores lógicos: ");

System.out.print("Ingresa el primer valor booleano (true/false): ");
        boolean valor3 = scanner.nextBoolean();

        System.out.print("Ingresa el segundo valor booleano (true/false): ");
        boolean valor4 = scanner.nextBoolean();

        boolean resultadoAnd = valor3 && valor4;
        boolean resultadoOr = valor3 || valor4;
        boolean resultadoNot1 = !valor3;
        boolean resultadoNot2 = !valor4;

        System.out.println("Resultado de AND: " + resultadoAnd);
        System.out.println("Resultado de OR: " + resultadoOr);
        System.out.println("Resultado de NOT para el primer valor: " + resultadoNot1);
        System.out.println("Resultado de NOT para el segundo valor: " + resultadoNot2);
          
//Escribe un programa que tome un número entero ingresado por el usuario y utilice el operador ternario para determinar si el número es positivo o negativo. Luego, muestra el resultado en la salida.

System.out.println("8. Operador ternario: ");

System.out.print("Ingresa un número entero : ");
int numeroentero = scanner.nextInt();

       String resultado = (numeroentero > 0) ? "positivo" : "negativo o cero";
       System.out.println("El número es " + resultado);

    }
}
```



