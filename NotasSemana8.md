# Semana 8

## Notas importantes:

`Polimorfismo`: Principio de sustitución, se puede utilizar un objeto de la subclase siempre que el programa espere un objeto de la superclase. En pocas palabras, un objeto se puede comportar de forma diferente según el contexto. Un ejemplo sencillo, se tiene la clase `Animal` la cual tiene el método abstracto `MakeSound()` que se implementa de forma distinta en las subclases `Gato` y `Perro` debido a que ambos reproducen un sonido, sin embargo es distinto en cada caso.

Ejemplo:
```java
// Clase base
abstract class Animal {
    // Método abstracto
    abstract void makeSound();
}

// Clase derivada
class Cat extends Animal {
    void makeSound() {
        System.out.println("Meow");
    }
}

// Clase derivada
class Dog extends Animal {
    void makeSound() {
        System.out.println("Woof");
    }
}

// Clase principal
public class Main {
    public static void main(String[] args) {
        // Crear instancias de Cat y Dog
        Animal myCat = new Cat();
        Animal myDog = new Dog();

        // Llamar al método makeSound() usando polimorfismo
        myCat.makeSound(); // Imprime "Meow"
        myDog.makeSound(); // Imprime "Woof"
    }
}
```

## Clases abstractas POO:
Son clases base para otras clases llamadas "clases concretas". Consiste en ocultar lo complicado de nuestro código y servir funciones de alto nivel. Una clase abstracta es una clase común que posee atributos y métodos, tiene cómo minimo un método abstracto. 

```java
// Clase abstracta
abstract class Forma {
    // Método abstracto
    abstract double calcularArea();
}

// Clase derivada
class Circulo extends Forma {
    private double radio;

    public Circulo(double radio) {
        this.radio = radio;
    }

    double calcularArea() {
        return Math.PI * radio * radio;
    }
}

// Clase derivada
class Rectangulo extends Forma {
    private double ancho;
    private double alto;

    public Rectangulo(double ancho, double alto) {
        this.ancho = ancho;
        this.alto = alto;
    }

    double calcularArea() {
        return ancho * alto;
    }
}

// Clase principal
public class Main {
    public static void main(String[] args) {
        // Crear instancias de Circulo y Rectangulo
        Forma miCirculo = new Circulo(5.0);
        Forma miRectangulo = new Rectangulo(4.0, 6.0);

        // Calcular y mostrar áreas
        System.out.println("Área del círculo: " + miCirculo.calcularArea());
        System.out.println("Área del rectángulo: " + miRectangulo.calcularArea());
    }
}
```
# Tipos enumerados Java:
```java
// Definición de la enumeración
enum Talla {
    PEQUEÑA, MEDIANA, GRANDE, EXTRA_GRANDE
}

// Clase principal
public class Main {
    public static void main(String[] args) {
        // Crear una variable de tipo Talla
        Talla miTalla = Talla.MEDIANA;

        // Mostrar la talla seleccionada
        System.out.println("La talla seleccionada es: " + miTalla);

        // Usar la enumeración en una estructura de control
        switch (miTalla) {
            case PEQUEÑA:
                System.out.println("Talla pequeña seleccionada.");
                break;
            case MEDIANA:
                System.out.println("Talla mediana seleccionada.");
                break;
            case GRANDE:
                System.out.println("Talla grande seleccionada.");
                break;
            case EXTRA_GRANDE:
                System.out.println("Talla extra grande seleccionada.");
                break;
        }
    }
}
```

