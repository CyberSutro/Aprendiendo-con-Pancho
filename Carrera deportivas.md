package maraton;
import java.util.Vector;
import javax.swing.JOptionPane;


/**
 *
 * @author AdanSutro
 */
public class Maraton {
    public static void main(String [] args ){
    Vector corredor=new Vector(15,5);
    JOptionPane JO=new JOptionPane();
    int opcion;
    String menu="Meta\n"+"1.-Ingreso N° Corredor\n"+
                "2.- Ver Podio\n"+"3.- Ver Llegada Corredores\n"+"4.-Salir\n";
do{
    opcion=Integer.parseInt(JO.showInputDialog(menu));
    switch(opcion)
    {case 1:int numero= Integer.parseInt(JO.showInputDialog("ingrese N° corredor"));
               corredor.add(numero);break;
               
   case 2:
    if (corredor.size() >= 3) {
        JO.showMessageDialog(null, "PODIO\n" +
            "1° Lugar: " + corredor.elementAt(0) + "\n" +
            "2° Lugar: " + corredor.elementAt(1) + "\n" +
            "3° Lugar: " + corredor.elementAt(2));
    } else {
        JO.showMessageDialog(null, "No hay suficientes corredores para el podio.");
    }
    break;
    
    case 3:String llegada="llegada corredores \n";
         for (int indice=0; indice<corredor.size (); indice++){
              llegada+=corredor.elementAt(indice)+ " ";
         }//fin for 
         JO.showMessageDialog(null, llegada); break;
         
    case 4:JO.showMessageDialog(null, "salir");break;
    
    default:JO.showMessageDialog(null,"Opcion No valida "); break;
            
    }// fin switch 
}while(opcion!=4);
 }
}  
    
