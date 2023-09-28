[Inicio](./index.md)

## Sesión 4

### Actividad: Creación de una clase de producto con modificadores de acceso y getters y setters

```java
Public class Producto {
Public String nombre;
Private double precio;
Protected int cantidad;
Final String fabricante;
Static String marca;
String categoria; 


Public Producto(String nombre, double precio, int cantidad, String fabricante, String marca, String categoria) }
	this.nombre = nombre;
	this.precio = precio;
	this.cantidad = cantidad;
	this.fabricante = fabricante;
	Producto.marca = marca;
	This.categoria = categoría;
}


public double getPrecio() {
	Return precio;
}

public void setPrecio(double precio){
	this.precio = precio;
}


Public int getCantidad () {
	Return cantirar;
}

Public void setCantidad(int cantidad) {
	This.cantidad = cantidad;
}


Public String getNombre() {
	Return nombre;
}


Public String getFabricante() {
	Return fabricante;
}


Public static String getMarca () {
	Return marca;
}


Public String getCategoria () {
	Return categoria;
}
Public void setCategoria(String categoria) {
	This.categoria = categoria;
}
Public void imprimirInformacion() {
System.out.printIn(“Nombre: ” + nombre);
System.out.printIn(“Precio: ” + precio);
System.out.printIn(“Cantidad: ” + cantidad);
System.out.printIn(“Fabricante: ” + fabricante);
System.out.printIn(“Marca: ” + marca);
System.out.printIn(“Categoria: ” categoria);
}

Public static void main(String[ ] args) {
Producto product = new Producto(“Producto1”, 29.99, 100, “Fabricante1”, “Marca1”, “Categoria1”);

Producto.imprimirInformacion();
Producto.setPrecio(39.99);
System.out.printIn(“Precio actualizado: ” + producto.getPrecio());
}
}
```