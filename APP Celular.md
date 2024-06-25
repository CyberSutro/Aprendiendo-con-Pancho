//programa principal del celular
package cargarcelu;
import javax.swing.JOptionPane;

/**
 *
 * @author Luis Salinas Vera, estudiante de ingenieria en ciberseguridad UDLA
 * 
 */
public class PrincipalCelular {
    
  public static void main(String[] args) {
    celular miCelular = new celular();
    String opcion;

    do {
        opcion = JOptionPane.showInputDialog(null, 
             "MENU CELULAR\n" +
             "1.- Llamada telefónica\n" +
             "2.- Cargar Dinero al Celular\n" +
             "3.- Cargar Batería al Celular\n" +
             "4.- Mostrar Estadística\n" +
             "5.- Salir\n" +
             "Elija una opción:", 
             "Catedra de Programacion ", JOptionPane.QUESTION_MESSAGE);

    switch(opcion) {
        case "1":
        miCelular.llamadaTelefonica();
        break;
        
        case "2":
        String monto2 = JOptionPane.showInputDialog("Ingrese el monto a cargar:");
        //convertir a numero
        double monto = Double.parseDouble(monto2);
        miCelular.cargarDinero(monto);
        JOptionPane.showMessageDialog(null, "Dinero cargado "); 
        break;
                
        case "3":
        miCelular.cargarBateria();
        JOptionPane.showMessageDialog(null, "Batería cargada ");
        break;
        
        case "4":
        String estadistica = miCelular.mostrarEstadistica();
        JOptionPane.showMessageDialog(null, estadistica);
        break;
                
        case "5":
        JOptionPane.showMessageDialog(null, "Saliendo de la aplicación.");
        break;
        
        default:
        JOptionPane.showMessageDialog(null, "Opción no válida.");
        }
    //mientras no sea 5, el bucle se repetira
    } while (!opcion.equals("5"));
 }
}

// clase del celular
package cargarcelu;
import javax.swing.JOptionPane;

/**
 *
 * @author AdanSutro
 */
public class celular {
    //saldo en $
    private double saldoDinero;
    //bateria en miliamperios (mAh)
    private int cargaBateria;
    //cantidad de dinero acumulado al celular
    private double dineroAcumulado;
    //cantidad de veces que se ha cargado el celular
    private int vecesCargadaBateria;

// Constructor
public celular() {
   saldoDinero = 5000;
   cargaBateria = 500;
   dineroAcumulado = 0;
   vecesCargadaBateria = 0;
}

// Método llamada telefónica
public void llamadaTelefonica() {
    if (saldoDinero >= 150 && cargaBateria >= 50) {
        saldoDinero -= 150;
        cargaBateria -= 50;
        JOptionPane.showMessageDialog(null, "Llamada realizada exitosamente ");
    } else {
        JOptionPane.showMessageDialog(null, "Saldo o batería baja para realizar la llamada ");
        }
}

// Método cargar dinero
public void cargarDinero(double monto) {
    saldoDinero += monto;
    acumularDineroCargado(monto);
    }

// Método cargar batería 
public void cargarBateria() {
    cargaBateria += 300;
    acumularVecesCargadaBateria();
    }

 // Método para acumular dinero cargado al celular
private void acumularDineroCargado(double monto) {
    dineroAcumulado += monto;
    }

// Método acumular veces que se ha cargado la batería
private void acumularVecesCargadaBateria() {
    vecesCargadaBateria++;
    }

// Método estadísticas
public String mostrarEstadistica() {
    return "Saldo en dinero: $" + saldoDinero +
           "\nCarga de batería: " + cargaBateria + " mAh" +
           "\nDinero acumulado cargado: $" + dineroAcumulado +
           "\nVeces que se ha cargado la batería: " + vecesCargadaBateria;
    }
}
