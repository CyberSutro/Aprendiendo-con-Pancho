// clase Automovil

package automovil.constructor;


/**
 *
 * @author AdanSutro
 */
public class Automovil {
    
    String color;
    int velocidad=0;
    
    //metodo contructor 
public Automovil (String colour){
color=colour;}

public void acelerar (int cantidad){
velocidad=velocidad + cantidad;}

public void frenar (int cantidad){
velocidad= velocidad - cantidad;}

public int velocimetro (){
return velocidad;
}
}

// programa principal 

package automovil.constructor;
import javax.swing.JOptionPane;

/**
 *
 * @author AdanSutro
 */
public class principal {
    
 public static void main (String args []){
 
 Automovil auto=new Automovil("rojo");
         
 String panel= "(1) Acelerar\n"+" (2) Frenar\n"+" (3) Salir\n"+
                "Elegir una opcion\n";
 
 int opcion;
 
 do{
 opcion=Integer.parseInt(JOptionPane.showInputDialog("VELOCIDAD [  "+
                         auto.velocimetro()+"  ]\n\n"+panel));
 
 switch (opcion)
 {case 1: auto.acelerar(50);break;
  case 2: auto.frenar(20);break;
  case 3: JOptionPane.showMessageDialog(null," Salir");break;
  default: JOptionPane.showMessageDialog(null, "valor no corresponde ");break;
 }// fin switch
 }while (opcion!=3);
 }
 }
    
    

