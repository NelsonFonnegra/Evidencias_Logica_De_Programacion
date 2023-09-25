<!-- No borrar o modificar -->
[Inicio](./index.md)

# Actividad 4: Ejercicios de control de flujo con expresiones compuestas

```java
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
Mostrar toda la información del estudiante si está matriculado en el Cesde.
5. Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.
Determinar la cantidad de beca que recibe el estudiante según su promedio:
- 0.0 - 3.4: El estudiante no recibe beca.
- 3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
- 4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
- 4.5 - 5.0: El estudiante recibe una beca completa.

```java
package com.mycompany.actividad4;


public class Actividad4 {

    public static void main(String[] args) {
        String nombre = "Juan Pérez";
        String apellido = "González";
        String identificación = "1000000001";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
        int edad = 20;
        boolean esActivo = true;
        boolean becado = false;
        char género = 'M';
        double promedio = 4.5;
        int semestre = 2;

        // Determinar si el estudiante es mayor de edad y tiene un estado activo.
        if (edad >= 18 && esActivo) {
            System.out.println("El estudiante es mayor de edad y tiene un estado activo.");
        }

        // Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.
        if (becado || carrera.equals("Desarrollo de Software")) {
            System.out.println("El estudiante tiene una beca o una carrera relacionada con el desarrollo de software.");
        }

        // Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.
        if (semestre == 10 && esActivo) {
            System.out.println("El estudiante está en el último semestre de su carrera y tiene un estado activo.");
        }

        // Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.
        if (carrera.equals("Desarrollo de Software") && promedio > 4.0) {
            System.out.println("El estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.");
        }

        // Mostrar toda la información del estudiante si está matriculado en el Cesde.
        if (universidad.equals("Cesde")) {
            System.out.println("Información del estudiante:");
            System.out.println("Nombre: " + nombre);
            System.out.println("Apellido: " + apellido);
            System.out.println("Identificación: " + identificación);
            System.out.println("Correo: " + correo);
            System.out.println("Carrera: " + carrera);
            System.out.println("Universidad: " + universidad);
            System.out.println("Edad: " + edad);
            System.out.println("Es activo: " + esActivo);
            System.out.println("Becado: " + becado);
            System.out.println("Género: " + género);
            System.out.println("Promedio: " + promedio);
            System.out.println("Semestre: " + semestre);
        }

        // Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.
        if (universidad.equals("Cesde") && promedio > 4.0 && esActivo) {
            becado = true;
            System.out.println("Se ha asignado una beca del 50% al estudiante.");
        }

        // Determinar la cantidad de beca que recibe el estudiante según su promedio.
        if (promedio >= 0.0 && promedio <= 3.4) {
            System.out.println("El estudiante no recibe beca.");
        } else if (promedio >= 3.5 && promedio <= 3.9) {
            System.out.println("El estudiante recibe una beca parcial del 25%.");
        } else if (promedio >= 4.0 && promedio <= 4.4) {
            System.out.println("El estudiante recibe una beca parcial del 50%.");
        } else if (promedio >= 4.5 && promedio <= 5.0) {
            System.out.println("El estudiante recibe una beca completa.");
        }

        //si el estudiante tiene genero M escribir el estudiante es género masculino si no escribir el estudiante es género femenino
        {
            if (género == 'M') {
                System.out.println("El estudiante es hombre.");
            } else {
                System.out.println("El estudiante es mujer.");
            }

            //si el estudiante tiene semestre menor que 2 escribir el estudiante es nuevo, de 2 a 5 el estudiante está en proceso de adaptación, si el estudiante está en el semestre 6 a 9 está en etapa final, si está en el semestre 10 el estudiante está en proceso de graduación.
            switch (semestre) {
                case 1:
                    System.out.println("El estudiante es nuevo.");
                    break;
                case 2:
                case 3:
                case 4:
                case 5:
                    System.out.println("El estudiante está en proceso de adaptación.");
                    break;
                case 6:
                case 7:
                case 8:
                case 9:
                    System.out.println("El estudiante está en etapa final.");
                    break;
                case 10:
                    System.out.println("El estudiante está en proceso de graduación.");
                    break;
                default:
                    System.out.println("El semestre ingresado no es válido.");
                    break;
            }
            if (semestre != 10) {
                System.out.println("el estudiante no está realizando trabajo de grado");
            }
        }
    }
}

```



