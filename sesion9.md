[Inicio](./index.md)

## Sesión 9 

### 1- Completar la implementación de la aplicación de convertidor de unidades en Java, siguiendo las instrucciones de la sesión 9.


# Divisas

```java
Divisas

if (unidadOrigen.equals("Dolar") && unidadDestino.equals("Euro")){
            double resultado = cantidad * 0.98;
            return resultado;
        } else if (unidadOrigen.equals("Euro") && unidadDestino.equals("Dolar")) {
            double resultado = cantidad * 1.06;
            return resultado;
        } else if (unidadOrigen.equals("Dólar") && unidadDestino.equals("Peso colombiano")) {
            double resultado = cantidad * 4073.34;
            return resultado;
        } else if (unidadOrigen.equals("Peso colombiano") && unidadDestino.equals("Dólar")) {
            double resultado = cantidad * 0.00025;
            return resultado;
        } else if (unidadOrigen.equals("Euro") && unidadDestino.equals("Peso colombiano")) {
            double resultado = cantidad * 4312.24;
            return resultado;
        } else if (unidadOrigen.equals("Peso colombiano") && unidadDestino.equals("Euro")) {
            double resultado = cantidad * 0.00023;
            return resultado;
        }else {
            throw new IllegalArgumentException("Divisas no compatibles");
        }
```

# Longitudes

```java
if(unidadOrigen.equals("Metros") && unidadDestino.equals("Pies")){
            double resultado = cantidad * 3.28084;
            return resultado;
        } else if (unidadOrigen.equals("Pies") && unidadDestino.equals("Metros")) {
            double resultado = cantidad * 0.3048;
            return resultado;
        } else if (unidadOrigen.equals("Kilometros") && unidadDestino.equals("Millas")) {
            double resultado = cantidad * 0.621371;
            return resultado;
        } else if (unidadOrigen.equals("Millas") && unidadDestino.equals("Kilometros")) {
            double resultado = cantidad * 1.60934;
            return resultado;
        } else if (unidadOrigen.equals("Centimetros") && unidadDestino.equals("Pulgadas")) {
            double resultado = cantidad * 0.393701;
            return resultado;
        } else if (unidadOrigen.equals("Pulgadas") && unidadDestino.equals("Centimetros")) {
            double resultado = cantidad * 2.54;
            return resultado;
        } else if (unidadOrigen.equals("Yardas") && unidadDestino.equals("Metros")) {
            double resultado = cantidad * 0.9144;
            return resultado;
        } else if (unidadOrigen.equals("Metros") && unidadDestino.equals("Yardas")) {
            double resultado = cantidad * 1.09361;
            return resultado;
        } else if (unidadOrigen.equals("Millas Nauticas") && unidadDestino.equals("Kilómetros")) {
            double resultado = cantidad * 1.852;
            return resultado;
        } else if (unidadOrigen.equals("Kilómetros") && unidadDestino.equals("Millas Nauticas")) {
            double resultado = cantidad * 0.539957;
            return resultado;
        } else if (unidadOrigen.equals("Micrometros") && unidadDestino.equals("Milimetros")) {
            double resultado = cantidad * 0.001;
            return resultado;
        } else if (unidadOrigen.equals("Milimetros") && unidadDestino.equals("Micrometros")) {
            double resultado = cantidad * 1000;
            return resultado;
        } else if (unidadOrigen.equals("Decimetros") && unidadDestino.equals("Metros")) {
            double resultado = cantidad * 0.1;
            return resultado;
        } else if (unidadOrigen.equals("Metros") && unidadDestino.equals("Decimetros")) {
            double resultado = cantidad * 10;
            return resultado;
        }else {
            throw new IllegalArgumentException("Longitudes no compatibles");
        }
```

# Peso

```java
if(unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Libras")){
            double resultado = cantidad * 2.20462;
            return resultado;
        }else if (unidadOrigen.equals("Libras") && unidadDestino.equals("Kilogramos")){
            double resultado = cantidad * 0.453592;
            return resultado;
        }else if (unidadOrigen.equals("Gramos") && unidadDestino.equals("Libras")){
            double resultado = cantidad * 0.00220462;
            return resultado;
        }else if (unidadOrigen.equals("Libras") && unidadDestino.equals("Gramos")){
            double resultado = cantidad * 453.592;
            return resultado;
        }else if (unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Gramos")){
            double resultado = cantidad * 1000;
            return resultado;
        }else if (unidadOrigen.equals("Gramos") && unidadDestino.equals("Kilogramos")){
            double resultado = cantidad * 0.001;
            return resultado;
        }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Kilogramos")){
            double resultado = cantidad * 1000;
            return resultado;
        }else if (unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Toneladas")){
            double resultado = cantidad * 0.001;
            return resultado;
        }else if (unidadOrigen.equals("Libras") && unidadDestino.equals("Onzas")){
            double resultado = cantidad * 16;
            return resultado;
        }else if (unidadOrigen.equals("Onzas") && unidadDestino.equals("Libras")){
            double resultado = cantidad * 0.0625;
            return resultado;
        }else if (unidadOrigen.equals("Gramos ") && unidadDestino.equals("Onzas")){
            double resultado = cantidad * 0.035274;
            return resultado;
        }else if (unidadOrigen.equals("Onzas") && unidadDestino.equals("Gramos")){
            double resultado = cantidad * 28.3495;
            return resultado;
        }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Libras")){
            double resultado = cantidad * 2204.62;
            return resultado;
        }else if (unidadOrigen.equals("Libras") && unidadDestino.equals("Toneladas")){
            double resultado = cantidad * 0.000453592;
            return resultado;
        }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Gramos")){
            double resultado = cantidad * 1000000;
            return resultado;
        }else if (unidadOrigen.equals("Gramos") && unidadDestino.equals("Toneladas")){
            double resultado = cantidad * 0.000001;
            return resultado;
        }else if (unidadOrigen.equals("Toneladas") && unidadDestino.equals("Miligramos")){
            double resultado = cantidad * 1000000000;
            return resultado;
        }else if (unidadOrigen.equals("Miligramos") && unidadDestino.equals("Toneladas")){
            double resultado = cantidad * 0.000000001;
            return resultado;
        }else if (unidadOrigen.equals("Kilogramos") && unidadDestino.equals("Miligramos")){
            double resultado = cantidad * 1000000;
            return resultado;
        }else if (unidadOrigen.equals("Miligramos") && unidadDestino.equals("Kilogramos")){
            double resultado = cantidad * 0.000001;
            return resultado;
        }else{
            throw new IllegalArgumentException("Pesos no compatibles");
        }
```

### 2- Agregar la subclase programador que contenga siguientes conversiones:
#### Decimal a Binario
#### Decimal a Hexadecimal
#### Binario a Decimal
#### Hexadecimal a Binario

```java
import java.util.Scanner;

public class CalculadoraConversiones {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        while (true) {
            System.out.println("Seleccione una opción:");
            System.out.println("1. Decimal a Binario");
            System.out.println("2. Decimal a Hexadecimal");
            System.out.println("3. Binario a Decimal");
            System.out.println("4. Hexadecimal a Binario");
            System.out.println("5. Salir");

            int opcion = scanner.nextInt();
            scanner.nextLine();

            switch (opcion) {
                case 1:
                    System.out.print("Ingrese un número decimal: ");
                    int decimalNumero = scanner.nextInt();
                    String binario = decimalABinario(decimalNumero);
                    System.out.println("El número en binario es: " + binario);
                    break;
                case 2:
                    System.out.print("Ingrese un número decimal: ");
                    int decimalNum = scanner.nextInt();
                    String hexadecimal = decimalAHexadecimal(decimalNum);
                    System.out.println("El número en hexadecimal es: " + hexadecimal);
                    break;
                case 3:
                    System.out.print("Ingrese un número binario: ");
                    String binarioNum = scanner.nextLine();
                    int decimal = binarioADecimal(binarioNum);
                    System.out.println("El número en decimal es: " + decimal);
                    break;
                case 4:
                    System.out.print("Ingrese un número hexadecimal: ");
                    String hexadecimalNum = scanner.nextLine();
                    String binarioHex = hexadecimalABinario(hexadecimalNum);
                    System.out.println("El número en binario es: " + binarioHex);
                    break;
                case 5:
                    System.out.println("¡Hasta luego!");
                    System.exit(0);
                default:
                    System.out.println("Opción no válida. Por favor, seleccione una opción válida.");
            }
        }
    }

    public static String decimalABinario(int decimal) {
        return Integer.toBinaryString(decimal);
    }

    public static String decimalAHexadecimal(int decimal) {
        return Integer.toHexString(decimal);
    }

    public static int binarioADecimal(String binario) {
        return Integer.parseInt(binario, 2);
    }

    public static String hexadecimalABinario(String hexadecimal) {
        int decimal = Integer.parseInt(hexadecimal, 16);
        return Integer.toBinaryString(decimal);
    }
}
```