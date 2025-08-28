# Trabajo-
.
import java.util.Scanner;

public class PagoTrabajador {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Horas trabajadas: ");
        double horas = scanner.nextDouble();
        System.out.print("Valor por hora: ");
        double valorHora = scanner.nextDouble();
        
        double pagoTotal = (horas > 40) 
            ? (40 * valorHora + (horas - 40) * valorHora * 2) 
            : (horas * valorHora);
        
        double pagoFinal = pagoTotal * 0.92; // Descuento del 8%
        
        System.out.printf("Pago final: %.2f\n", pagoFinal);
        scanner.close();
    }
}
