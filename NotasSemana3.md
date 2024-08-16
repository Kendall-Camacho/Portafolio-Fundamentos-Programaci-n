# Semana 3

### Notas Importantes


# Operadores en Java

```java
int a = 10;
int b = 5;
boolean x = true;
boolean y = false;

// Operadores Aritméticos

// Suma
int suma = a + b;
System.out.println("La suma es: " + suma); // Resultado: 15

// Resta
int resta = a - b;
System.out.println("La resta es: " + resta); // Resultado: 5

// Multiplicación
int multiplicacion = a * b;
System.out.println("La multiplicación es: " + multiplicacion); // Resultado: 50

// División
int division = a / b;
System.out.println("La división es: " + division); // Resultado: 2

// Módulo
int modulo = a % b;
System.out.println("El módulo es: " + modulo); // Resultado: 1

// Incremento
a++;
System.out.println("El valor incrementado es: " + a); // Resultado: 11

// Decremento
a--;
System.out.println("El valor decrementado es: " + a); // Resultado: 9

// Operadores Lógicos

// AND lógico
boolean andResultado = x && y;
System.out.println("AND lógico: " + andResultado); // Resultado: false

// OR lógico
boolean orResultado = x || y;
System.out.println("OR lógico: " + orResultado); // Resultado: true

// NOT lógico
boolean notResultado = !x;
System.out.println("NOT lógico: " + notResultado); // Resultado: false

// Operadores Booleanos de Comparación

// Igualdad
boolean esIgual = a == b;
System.out.println("Igualdad: " + esIgual); // Resultado: false

// Desigualdad
boolean esDesigual = a != b;
System.out.println("Desigualdad: " + esDesigual); // Resultado: true

// Mayor que
boolean mayorQue = a > b;
System.out.println("Mayor que: " + mayorQue); // Resultado: true

// Menor que
boolean menorQue = a < b;
System.out.println("Menor que: " + menorQue); // Resultado: false

// Mayor o igual que
boolean mayorOIgual = a >= b;
System.out.println("Mayor o igual que: " + mayorOIgual); // Resultado: true

// Menor o igual que
boolean menorOIgual = a <= b;
System.out.println("Menor o igual que: " + menorOIgual); // Resultado: false

# Flujos de Control en Java

```java
int a = 10;
int b = 5;
int c = 7;
boolean condition = true;

// Estructura if-else
if (a > b) {
    System.out.println("a es mayor que b");
} else {
    System.out.println("b es mayor o igual que a");
}

// Estructura if-else if-else
if (a > b && a > c) {
    System.out.println("a es el mayor");
} else if (b > c) {
    System.out.println("b es el mayor");
} else {
    System.out.println("c es el mayor");
}

// Estructura switch
int day = 3;
switch (day) {
    case 1:
        System.out.println("Es lunes");
        break;
    case 2:
        System.out.println("Es martes");
        break;
    case 3:
        System.out.println("Es miércoles");
        break;
    default:
        System.out.println("Es otro día");
        break;
}

// Estructura while
int i = 0;
while (i < 5) {
    System.out.println("Valor de i en while: " + i);
    i++;
}

// Estructura do-while
i = 0;
do {
    System.out.println("Valor de i en do-while: " + i);
    i++;
} while (i < 5);

// Estructura for
for (int j = 0; j < 5; j++) {
    System.out.println("Valor de j en for: " + j);
}

// Estructura for-each
int[] numbers = {1, 2, 3, 4, 5};
for (int number : numbers) {
    System.out.println("Número: " + number);
}

// Estructura break y continue

// Uso de break
for (int j = 0; j < 5; j++) {
    if (j == 3) {
        break; // Sale del bucle cuando j es 3
    }
    System.out.println("Valor de j antes del break: " + j);
}

// Uso de continue
for (int j = 0; j < 5; j++) {
    if (j == 3) {
        continue; // Salta la iteración cuando j es 3
    }
    System.out.println("Valor de j con continue: " + j);
}








