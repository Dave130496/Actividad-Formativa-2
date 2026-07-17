import java.util.Scanner;

// Clase principal
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Entrada de datos
        System.out.println("Ingresa el precio del producto a importar:");
        double precio = sc.nextDouble();

        // Instanciación de objeto Producto
        Producto producto = new Producto(precio);

        // Uso de método para calcular el total
        double total = producto.calcularTotal();

        // Mostrar resultado
        System.out.println("El total del producto importado es de $" + total);

        sc.close();
    }
}

// Clase Producto
class Producto {
    // Atributo
    private double precio;

    // Constructor
    public Producto(double precio) {
        this.precio = precio;
    }

    // Método para calcular el total con incremento
    public double calcularTotal() {
        if (precio < 1500) {
            return precio * 1.11;
        } else {
            return precio * 1.08;
        }
    }
}

