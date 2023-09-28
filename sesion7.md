[Inicio](./index.md)

## Sesión 7 


### Crea una clase llamada Producto que representará productos en una tienda en línea

```java
public class Producto {
    private String nombre;
    private double precio;
    private int cantidad;

    public void actualizarPrecio(double nuevoPrecio) {
        precio = nuevoPrecio;
    }

    public void actualizarPrecioEnPesos(double nuevoPrecioEnPesos) {
        precio = nuevoPrecioEnPesos / 4000.0;
    }

    public static void main(String[] args) {
        
        Producto camisa = new Producto("Camisa", 29.99, 50);
        Producto pantalon = new Producto("Pantalón", 49.99, 30);

        System.out.println("Información inicial de la camisa:");
        camisa.mostrarInformacion();
        System.out.println("\nInformación inicial del pantalón:");
        pantalon.mostrarInformacion();

        camisa.actualizarPrecio(34.99);

        pantalon.actualizarPrecioEnPesos(150000.0);

        System.out.println("\nInformación actualizada de la camisa:");
        camisa.mostrarInformacion();
        System.out.println("\nInformación actualizada del pantalón:");
        pantalon.mostrarInformacion();
    }
}

```