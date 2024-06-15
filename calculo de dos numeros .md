package Operacion;
import java.util.Scanner;

/**
 *
 * @author AdanSutro
 */
public class Opera1 {
     public static void main(String[] args) {
    
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("Ingresa el primer número:");
        int num_1 = scanner.nextInt();
        
        System.out.println("Ingresa el segundo número:");
        int num_2 = scanner.nextInt();
        
        System.out.println("Selecciona la operación a realizar:");
        System.out.println("1. Suma");
        System.out.println("2. Resta");
        System.out.println("3. Multiplicación");
        System.out.println("4. División");
        int operacion = scanner.nextInt();
        
        int resultado = 0;
    
        switch (operacion) {
            case 1:
                resultado = num_1 + num_2;
                System.out.println("El resultado de la suma es: " + resultado);
                break;
            case 2:
                resultado = num_1 - num_2;
                System.out.println("El resultado de la resta es: " + resultado);
                break;
            case 3:
                resultado = num_1 * num_2;
                System.out.println("El resultado de la multiplicación es: " + resultado);
                break;
            case 4:
                if (num_2 != 0) {
                    resultado = num_1 / num_2;
                    System.out.println("El resultado de la división es: " + resultado);
                } else {
                    System.out.println("Error: No se puede dividir entre cero.");
                }
                break;
            default:
                System.out.println("Operación no válida.");
                break;
        }
        
        scanner.close();
    }
}
