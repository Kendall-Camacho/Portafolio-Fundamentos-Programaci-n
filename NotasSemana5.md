# Semana 5

## Pratica

```java
import java.util.Scanner;
import java.util.Arrays;
import java.util.ArrayList;
import java.util.Collections;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // 1. Verificar si una cadena contiene un '@' (básicamente verificar si un email es válido)
        System.out.print("Ingrese un email para verificar: ");
        String email = scanner.nextLine();
        if (email.contains("@")) {
            System.out.println("El email es válido.");
        } else {
            System.out.println("El email no es válido.");
        }

        // 2. Ingresar fecha de nacimiento en una estructura matriz y mostrarla
        int[][] fechaNacimiento = new int[3][2]; // Suponiendo formato: [día, mes, año]
        System.out.println("Ingrese su fecha de nacimiento (día, mes, año):");
        for (int i = 0; i < 3; i++) {
            System.out.print("Ingrese " + (i == 0 ? "día" : i == 1 ? "mes" : "año") + ": ");
            fechaNacimiento[i][0] = scanner.nextInt();
        }
        System.out.println("Fecha de nacimiento ingresada:");
        System.out.println("Día: " + fechaNacimiento[0][0]);
        System.out.println("Mes: " + fechaNacimiento[1][0]);
        System.out.println("Año: " + fechaNacimiento[2][0]);

        // 3. Ordenar una lista de números usando el método burbuja
        System.out.print("Ingrese el número de elementos a ordenar (método burbuja): ");
        int n = scanner.nextInt();
        int[] numeros = new int[n];
        System.out.println("Ingrese los números:");
        for (int i = 0; i < n; i++) {
            numeros[i] = scanner.nextInt();
        }
        bubbleSort(numeros);
        System.out.println("Lista ordenada (burbuja): " + Arrays.toString(numeros));

        // Ordenar una lista de números usando heap sort
        System.out.print("Ingrese el número de elementos a ordenar (método heap sort): ");
        n = scanner.nextInt();
        numeros = new int[n];
        System.out.println("Ingrese los números:");
        for (int i = 0; i < n; i++) {
            numeros[i] = scanner.nextInt();
        }
        heapSort(numeros);
        System.out.println("Lista ordenada (heap sort): " + Arrays.toString(numeros));
    }

    // Método de ordenamiento burbuja
    public static void bubbleSort(int[] array) {
        int n = array.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (array[j] > array[j + 1]) {
                    // Intercambiar array[j] y array[j + 1]
                    int temp = array[j];
                    array[j] = array[j + 1];
                    array[j + 1] = temp;
                }
            }
        }
    }

    // Método de ordenamiento heap sort
    public static void heapSort(int[] array) {
        int n = array.length;

        // Construir el heap
        for (int i = n / 2 - 1; i >= 0; i--) {
            heapify(array, n, i);
        }

        // Extraer elementos del heap uno por uno
        for (int i = n - 1; i > 0; i--) {
            // Mover la raíz del heap al final
            int temp = array[0];
            array[0] = array[i];
            array[i] = temp;

            // Llamar heapify en el heap reducido
            heapify(array, i, 0);
        }
    }

    // Función para construir un heap
    public static void heapify(int[] array, int n, int i) {
        int largest = i;
        int left = 2 * i + 1;
        int right = 2 * i + 2;

        if (left < n && array[left] > array[largest]) {
            largest = left;
        }

        if (right < n && array[right] > array[largest]) {
            largest = right;
        }

        if (largest != i) {
            // Intercambiar
            int swap = array[i];
            array[i] = array[largest];
            array[largest] = swap;

            // Recursivamente heapificar el subárbol afectado
            heapify(array, n, largest);
        }
    }
}
```

 
