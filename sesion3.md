[Inicio](./index.md)

## Sesión 3 


# Análisis de la Clase 'Jugadores' en Java"

### Los atributos son instancias que almacenan cierta informacion, en este caso en la clase "**jugadores**"

### En este las variables son

1. Edad con variable int
1. Nombre con variable String
1. Posicion con variable String
1. El numero de la camiseta con int
1. El nombre del equipo con String

### Constructor

El constructor, es un metodo **publico** especial el cual permite inicializar atributos de una clase, los cuales se le impone a un objeto

#### Aqui un ejemplo de su utilizacion en la clase

```java
public  Jugadores(String nombre, int edad, String posicion, int numero_camiseta, String equipo)
 {
this.nombre = nombre;
this.edad = edad;
this.posicion = posicion;
this.numero_camiseta = numero_camiseta;
this.equipo = equipo;
}

```

### Getter
La función de esta es permitir el obtener el valor de una propiedad de la clase y así poder utilizar este valor en diferentes métodos

#### Aqui un ejemplo de su utilizacion en la clase

```java
public String getNombre() {
return nombre;
}

public int getEdad() {
return edad;
}

public String getPosicion() {
return posicion;
}

public int getNumero_camiseta() {
return numero_camiseta;
}

public String getEquipo() {
return equipo;
}
```

### Setter

La funcion de este es modificar los valores de los atributos de una clase

#### Aqui un ejemplo de su utilizacion en la clase

```java
public void setNombre(String nombre) {
this.nombre = nombre;
}

public void setEdad(int edad) {
this.edad = edad;
}

public void setPosicion(String posicion) {
this.posicion = posicion;
}
public void setNumero_camiseta(int numero_camiseta) {
this.numero_camiseta = numero_camiseta;
}

public void setEquipo(String equipo) {
this.equipo = equipo;
}
```

### ToString

Este sirve para representar y manipular una secuencia de caracteres. En el caso de la clase se utiliza para hacer un resumen de la cadena y devolver algunas caracteristicas **(atributos)** del jugador

#### Aqui un ejemplo de su utilizacion en la clase

```java
public String toString() {
return "Jugadores{" +
"nombre='" + nombre + '\'' +
", edad=" + edad +
", posicion='" + posicion + '\'' +
", numero_camiseta=" + numero_camiseta +
", equipo='" + equipo + '\'' +
'}';
}
```