package TercerEjer;
import java.util.Scanner;

/**
 *
 * @author AdanSutro
 */
public class Coca_cola {
    
    public static void main (String[]args){
    Scanner entrada = new Scanner(System.in);
    
    String nombre="";
    int clave=0, antiguedad =0;
    
   System.out.println("********************************************** ");
   System.out.println("*Bienvenido al Sistema de vacaciones de coca cola* ");
   System.out.println("********************************************** ");
   System.out.println(" ");
   System.out.println(" ");
   
   System.out.println("¿CUAL ES EL NOMBRE DEL TRABAJADOR?: ");
   nombre=entrada.nextLine();
   System.out.println("");
   
   System.out.println("¿cuanto tiempo de servicio tiene el trabajador?: ");
   antiguedad=entrada.nextInt();
   System.out.println("");
    
   System.out.print("¿cual es la clave del trabajador: ");
   clave=entrada.nextInt();
   System.out.println("");
   
   if (clave==1)
   { 
       if (antiguedad==1)
       { System.out.println("el trabajador" + nombre + "tiene derecho a 6 dias de vacaciones ");
       } else if (antiguedad >= 2 && antiguedad <= 6) 
       { System.out.println("el trabajador " + nombre + "tiene derecho a 14 dias de vacaciones ");
       } else if (antiguedad >= 7)
       { System.out.println("el trabajador " + nombre + "tiene derecho a 20 dias de vacaciones ");
       }
       
   }else if (clave==2)
   {
       if (antiguedad==1)
       { System.out.println("el trabajador" + nombre + "tiene derecho a 7 dias de vacaciones ");
       } else if (antiguedad >= 2 && antiguedad <= 6) 
       { System.out.println("el trabajador " + nombre + "tiene derecho a 15 dias de vacaciones ");
       } else if (antiguedad >= 7)
       { System.out.println("el trabajador " + nombre + "tiene derecho a 22 dias de vacaciones ");
       }
       
   }else if (clave==3)
   {
       if (antiguedad==1)
       { System.out.println("el trabajador" + nombre + "tiene derecho a 10 dias de vacaciones ");
       } else if (antiguedad >= 2 && antiguedad <= 6) 
       { System.out.println("el trabajador " + nombre + "tiene derecho a 20 dias de vacaciones ");
       } else if (antiguedad >= 7)
       { System.out.println("el trabajador " + nombre + "tiene derecho a 30 dias de vacaciones ");
       }
       
   }else 
   { System.out.println("ERROR, CLAVE DE DEPARTAMENTO INCORRECTO ");
   }
   
    }    
}
