[Inicio](./index.md)

## Sesión 10 

### Polimorfismo en Java - Ejercicios prácticos

## ejercicio 1

### Crea una clase abstracta Vehículo con métodos abstractos acelerar(), frenar() y girar(). Las clases Coche, Moto y Bicicleta heredan de la clase Vehículo y sobreescriben los métodos abstractos para implementar su propio comportamiento.

```java
abstract class Vehiculo {
    public abstract void acelerar();
    public abstract void frenar();
    public abstract void girar();
}

class Coche extends Vehiculo {
    @Override
    public void acelerar() {
        System.out.println("El coche acelera");
    }

    @Override
    public void frenar() {
        System.out.println("El coche frena");
    }

    @Override
    public void girar() {
        System.out.println("El coche gira");
    }
}

class Moto extends Vehiculo {
    @Override
    public void acelerar() {
        System.out.println("La moto acelera");
    }

    @Override
    public void frenar() {
        System.out.println("La moto frena");
    }

    @Override
    public void girar() {
        System.out.println("La moto gira");
    }
}

class Bicicleta extends Vehiculo {
    @Override
    public void acelerar() {
        System.out.println("La bicicleta acelera pedaleando");
    }

    @Override
    public void frenar() {
        System.out.println("La bicicleta frena con los frenos");
    }

    @Override
    public void girar() {
        System.out.println("La bicicleta gira inclinándose");
    }
}

public class Main {
    public static void main(String[] args) {
        Coche coche = new Coche();
        Moto moto = new Moto();
        Bicicleta bicicleta = new Bicicleta();

        coche.acelerar();
        coche.frenar();
        coche.girar();

        moto.acelerar();
        moto.frenar();
        moto.girar();

        bicicleta.acelerar();
        bicicleta.frenar();
        bicicleta.girar();
    }
}
```

## ejercicio 2

### Crea una clase abstracta Producto con métodos abstractos calcularPrecio() y calcularImpuesto(). Las clases Libro, CD y DVD heredan de la clase Producto y sobreescriben los métodos abstractos para implementar su propio cálculo de precio e impuesto.

```java
abstract class Producto {
    public abstract double calcularPrecio();
    public abstract double calcularImpuesto();
}

class Libro extends Producto {
    private double precio;
    
    public Libro(double precio) {
        this.precio = precio;
    }

    @Override
    public double calcularPrecio() {
        return precio;
    }

    @Override
    public double calcularImpuesto() {
        return 0;
    }
}

class CD extends Producto {
    private double precio;
    
    public CD(double precio) {
        this.precio = precio;
    }

    @Override
    public double calcularPrecio() {
        return precio;
    }

    @Override
    public double calcularImpuesto() {
        return precio * 0.10;
    }
}

class DVD extends Producto {
    private double precio;
    
    public DVD(double precio) {
        this.precio = precio;
    }

    @Override
    public double calcularPrecio() {
        return precio;
    }

    @Override
    public double calcularImpuesto() {
        return precio * 0.15;
    }
}

public class Main {
    public static void main(String[] args) {
        Libro libro = new Libro(20.0);
        CD cd = new CD(15.0);
        DVD dvd = new DVD(30.0);

        System.out.println("Libro - Precio: $" + libro.calcularPrecio() + ", Impuesto: $" + libro.calcularImpuesto());
        System.out.println("CD - Precio: $" + cd.calcularPrecio() + ", Impuesto: $" + cd.calcularImpuesto());
        System.out.println("DVD - Precio: $" + dvd.calcularPrecio() + ", Impuesto: $" + dvd.calcularImpuesto());
    }
}

```

## ejercicio 3

### Crea una clase abstracta Cuenta con métodos abstractos depositar(), retirar() y consultarSaldo(). Las clases CuentaCorriente, CuentaAhorro y CuentaPlazoFijo heredan de la clase Cuenta y sobreescriben los métodos abstractos para implementar su propio comportamiento.

```java
abstract class Cuenta {
    private double saldo;

    public Cuenta(double saldoInicial) {
        this.saldo = saldoInicial;
    }

    public abstract void depositar(double monto);

    public abstract void retirar(double monto);

    public double consultarSaldo() {
        return saldo;
    }
}

class CuentaCorriente extends Cuenta {
    public CuentaCorriente(double saldoInicial) {
        super(saldoInicial);
    }

    @Override
    public void depositar(double monto) {
        consultarSaldo();
    }

    @Override
    public void retirar(double monto) {
        consultarSaldo();
    }
}

class CuentaAhorro extends Cuenta {
    public CuentaAhorro(double saldoInicial) {
        super(saldoInicial);
    }

    @Override
    public void depositar(double monto) {
        consultarSaldo();
    }

    @Override
    public void retirar(double monto) {
        consultarSaldo(); 
    }
}

class CuentaPlazoFijo extends Cuenta {
    public CuentaPlazoFijo(double saldoInicial) {
        super(saldoInicial);
    }

    @Override
    public void depositar(double monto) {
        consultarSaldo(); 
    }

    @Override
    public void retirar(double monto) {
        consultarSaldo(); 
    }
}

public class Main {
    public static void main(String[] args) {
        CuentaCorriente cuentaCorriente = new CuentaCorriente(1000);
        CuentaAhorro cuentaAhorro = new CuentaAhorro(2000);
        CuentaPlazoFijo cuentaPlazoFijo = new CuentaPlazoFijo(5000);

        cuentaCorriente.depositar(500);
        cuentaAhorro.retirar(300);
        cuentaPlazoFijo.depositar(1000);

        System.out.println("Saldo en Cuenta Corriente: $" + cuentaCorriente.consultarSaldo());
        System.out.println("Saldo en Cuenta de Ahorro: $" + cuentaAhorro.consultarSaldo());
        System.out.println("Saldo en Cuenta de Plazo Fijo: $" + cuentaPlazoFijo.consultarSaldo());
    }
}

```
