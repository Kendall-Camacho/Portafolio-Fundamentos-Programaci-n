# Semana 6

```java
// Clase base
class Vehiculo {
    private String marca;
    private String modelo;
    private int anio;

    public Vehiculo(String marca, String modelo, int anio) {
        this.marca = marca;
        this.modelo = modelo;
        this.anio = anio;
    }

    public void mostrarInfo() {
        System.out.println("Marca: " + marca);
        System.out.println("Modelo: " + modelo);
        System.out.println("Año: " + anio);
    }

    public void arrancar() {
        System.out.println("El vehículo está arrancando...");
    }
}

// Clase derivada
class Coche extends Vehiculo {
    private int numPuertas;

    public Coche(String marca, String modelo, int anio, int numPuertas) {
        super(marca, modelo, anio);
        this.numPuertas = numPuertas;
    }

    @Override
    public void mostrarInfo() {
        super.mostrarInfo();
        System.out.println("Número de puertas: " + numPuertas);
    }

    @Override
    public void arrancar() {
        System.out.println("El coche está arrancando...");
    }
}

// Clase derivada
class Motocicleta extends Vehiculo {
    private boolean tieneSidecar;

    public Motocicleta(String marca, String modelo, int anio, boolean tieneSidecar) {
        super(marca, modelo, anio);
        this.tieneSidecar = tieneSidecar;
    }

    @Override
    public void mostrarInfo() {
        super.mostrarInfo();
        System.out.println("Tiene sidecar: " + (tieneSidecar ? "Sí" : "No"));
    }

    @Override
    public void arrancar() {
        System.out.println("La motocicleta está arrancando...");
    }
}

// Clase principal
public class Main {
    public static void main(String[] args) {
        // Crear instancias de Coche y Motocicleta
        Vehiculo miCoche = new Coche("Toyota", "Corolla", 2020, 4);
        Vehiculo miMoto = new Motocicleta("Harley-Davidson", "Iron 883", 2022, true);

        // Mostrar información y arrancar vehículos
        System.out.println("Información del coche:");
        miCoche.mostrarInfo();
        miCoche.arrancar();

        System.out.println("\nInformación de la motocicleta:");
        miMoto.mostrarInfo();
        miMoto.arrancar();
    }
}
```
