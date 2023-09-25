<!-- No borrar o modificar -->
[Inicio](./index.md)

# Actividad 5: Ejercicios de bucles
Resolver los siguientes ejercicios:

## Ejercicios - while
- Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.
- Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.
### Ejercicios - do while
- Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.
- Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.
### Ejercicios - for
- Imprimir los números impares del 1 al 50.
* Imprimir los números primos del 1 al 100.

## SOLUCIÓN

```java
package actividad5;

import java.util.Scanner;

public class Actividad5 {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // 1. Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.
        System.out.println("1. Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.");

        System.out.print("Ingresa un número: ");
        int numero = sc.nextInt();

        int y = 1;
        while (y <= 10) {
            System.out.println(numero + " X " + y + " = " + (numero * y));
            y++;

        }

        //2. Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son numeros.
        System.out.println("2. Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son numeros.");

        System.out.print("Ingresa una cadena de caracteres: ");
        sc.nextLine();
        String cadena = sc.nextLine();

        int contador = 0;
        int i = 0;
        while (i < cadena.length()) {
            char caracter = cadena.charAt(i);
            if (Character.isDigit(caracter)) {
                contador++;
            }
            i++;
        }
        System.out.println("La cantidad de caracteres numéricos en la cadena es: " + contador);

        //Ejercicios con do-while
        //Imprimier los números del 1 al 100, pero detenerse si el usuario introduce un numero negativo.
        System.out.println("Imprimir los números del 1 al 100, pero detenerse si el usuario introduce un número negativo.");

        int numero2 = 1;

        do {
            System.out.println(numero);
            numero2++;

            System.out.println("Introduce un número negativo para detener:");
            int entradaUsuario = sc.nextInt();

            if (entradaUsuario < 0) {
                System.out.println("Deteniendo el programa...");
                break;
            }
        } while (numero2 <= 100);

        //Pedir al usurario un número entero e imprimir la tabla de multiplicar de ese número, pero detenerse si el usuario introduce el número 0.
        System.out.println("Pedir al usuario un número entero e imprimir la tabla de multiplicar de ese número, pero detenerse si el usuario introduce el número 0.");

        System.out.println("Ingrese un número entero (0 para salir): ");
        int numero3 = sc.nextInt();

        while (numero3 != 0) {
            for (int contador2 = 1; contador2 <= 10; contador2++) {
                System.out.println(numero3 + " x " + contador2 + " = " + (numero3 * contador2));
            }
            System.out.println("Ingrese otro número entero (0 para salir): ");
            numero3 = sc.nextInt();
        }

        //Ejercicios con for
        //Imprimir los números impares del 1 al 50.
        System.out.println("Imprimir los números impares del 1 al 50.");

        for (int contador3 = 1; contador3 <= 50; contador3 += 2) {
            System.out.println(contador3);
        }

        //Imprimir los números primos del 1 al 100.
        System.out.println("imprimir los números primos del 1 al 100.");
        for (int numero4 = 2; numero4 <= 100; numero4++) {
            boolean esPrimo = true;

            for (int contador4 = 2; contador4 <= Math.sqrt(numero4); contador4++) {
                if (numero4 % contador4 == 0) {
                    esPrimo = false;
                    break;
                }
            }

            if (esPrimo) {
                System.out.println(numero4);
            }
        }

    }
}

```




