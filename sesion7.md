<!-- No borrar o modificar -->
[Inicio](./index.md)

# Actividad: Ejecicios Array - ArrayList
1. En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.

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

2. Crear un ejemplo de Array y otro de ArrayList para visualizar sus diferencias.

### Array

```java
package com.mycompany.para_practicar;

public class Para_practicar {

    public static void main(String[] args) {
       
       // Crear un array para almacenar las calificaciones de los estudiantes
        double[] calificaciones = new double[5]; // Suponemos 5 estudiantes

        // Agregar calificaciones
        calificaciones[0] = 4.5;
        calificaciones[1] = 5.0;
        calificaciones[2] = 4.4;
        calificaciones[3] = 3.8;
        calificaciones[4] = 4.5;

        // Mostrar las calificaciones de los estudiantes
        System.out.println("Calificaciones de los estudiantes:");
        for (int i = 0; i < calificaciones.length; i++) {
            System.out.println("Estudiante " + (i + 1) + ": " + calificaciones[i]);
        }

        // Calcular el promedio de calificaciones
        double suma = 0;
        for (double calificacion : calificaciones) {
            suma += calificacion;
        }
        double promedio = suma / calificaciones.length;

        System.out.println("Promedio de calificaciones: " + promedio);
    }
}
```
### ArrayList

```java
import java.util.ArrayList;

public class GestionCalificacionesArrayList {
    public static void main(String[] args) {
        // Crear un ArrayList para almacenar las calificaciones de los estudiantes
        ArrayList<Double> calificaciones = new ArrayList<>();

        // Agregar calificaciones
        calificaciones.add(90.5);
        calificaciones.add(85.0);
        calificaciones.add(78.5);
        calificaciones.add(92.0);
        calificaciones.add(88.5);

        // Mostrar las calificaciones de los estudiantes
        System.out.println("Calificaciones de los estudiantes:");
        for (int i = 0; i < calificaciones.size(); i++) {
            System.out.println("Estudiante " + (i + 1) + ": " + calificaciones.get(i));
        }

        // Calcular el promedio de calificaciones
        double suma = 0;
        for (double calificacion : calificaciones) {
            suma += calificacion;
        }
        double promedio = suma / calificaciones.size();

        System.out.println("Promedio de calificaciones: " + promedio);
    }
}
```





