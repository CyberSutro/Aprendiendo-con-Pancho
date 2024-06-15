package Promedio;
import java.util.Scanner;

/**
 *
 * @author AdanSutro
 */
public class Prom {
    
    public static void main(String []args){
        
     Scanner scanner = new Scanner(System.in);

     System.out.println("ingrese la nota de matematicas");
        int matematicas= scanner.nextInt();
      
     System.out.println("ingrese la nota de biologia");
        int biologia= scanner.nextInt();  
        
     System.out.println("ingrese la nota de quimica");
        int quimica= scanner.nextInt();
    
        int promedio=0;
        
        promedio=(matematicas+biologia+quimica)/3;
        
        if (promedio>=6){
            System.out.println("el alumno Aprobo "+promedio);
        } 
        else {
         System.out.println("el alumno reprobo "+promedio);
        }
    } 
    
}
