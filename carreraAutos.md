// clase dado

package clasemath;

/**
 *
 * @author AdanSutro
 */
public class Dado {
       
  public int genera_num()
     {int numero= (int)(Math.random()*6+1);   
      return numero;
     }
}

//clase automovil

package clasemath;

/**
 *
 * @author AdanSutro
 */
public class Vehiculo {
    private String color;
    private int posicion;
    
    //metodo contructor 
    public Vehiculo (String colours)
    {color=colours;
     posicion=0;
    }
    //metodos
    public void set_posicion(int valor){
    posicion=posicion+valor;
    }
    public int get_posicion() {
        return posicion;
    }
    public String mostrar_pos(){
    return ("Color "+color+"  "+posicion );
    }  
}

// clase principal 

package clasemath;
import javax.swing.JOptionPane;

/**
 *
 * @author AdanSutro
 */
public class ProgramaPrincipal {
    
    public static void main (String args[]){
       Vehiculo auto1=new Vehiculo("Rojo");
       Vehiculo auto2=new Vehiculo("Azul");
    
       Dado dado=new Dado();
    
    String menu= "1.- Acelerar auto 1\n"+
                 "2.- Acelerar auto 2\n"+"3.- Salir\n";
     
    int opcion;
    
    do{
        String posiciones=("INDYCARS\n\n")+"Posicion Auto 1:"+auto1.mostrar_pos()+"\n"+
                "Posicion Auto 2: " + auto2.mostrar_pos() + "\n\n\n" + menu;        
        String valor=JOptionPane.showInputDialog(posiciones);
        opcion=Integer.parseInt(valor);
        switch(opcion){
             case 1:auto1.set_posicion(dado.genera_num());
              if (auto1.get_posicion() >= 21) {
                JOptionPane.showMessageDialog(null, "¡Auto 1 (Rojo) ha ganado!");
                opcion = 3; // Para salir del bucle
                }
                break;
             case 2:auto2.set_posicion(dado.genera_num());
             if (auto2.get_posicion() >= 21) {
             JOptionPane.showMessageDialog(null, "¡Auto 2 (Azul) ha ganado!");
             opcion = 3; // Para salir del bucle
             }
            break;
  
            case 3: JOptionPane.showMessageDialog(null, "Salir de la Aplicacion");break;
            default :JOptionPane.showMessageDialog(null,"Opcion no valida");break;
        }
    }while (opcion !=3);
    }//fin main
}// fin class


