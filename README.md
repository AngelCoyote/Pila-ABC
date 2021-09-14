# Pila-ABC
Hacer unas Pila, con el Abecedario 

package pilaabc;

import java.util.Scanner;

/**
 *
 * @author Angel Ulises
 */
public class PilaABC {
    
     int Tope, Max;
    private String Pila[];
    char Car;
    
    public PilaABC(int m){
        Max = m;
        Pila = new String[Max];
        Tope = 0;
        char car = Car; 
    }
    
    // Llenar Automatico 
    private Boolean Llenar(){
        for(Car = 'Z'; Car >='A'; Car--){
             System.out.println(Car);
        }
        return false;
    }

       //Mostrar Pila 
    private void Mostrar(){
        if(!Vacia()){
            for(int a = (Tope-1); a>=0; a--){
                System.out.println(Pila[a]);
            }
        }
        else
            System.out.println("Pila Vacia");
        
    }
    
    
    // Eliminar Dato
    private void Eliminar(){
        if(Tope > 0){
            Car--;
              System.out.println("\nSe ha eliminado el ultimo dato de la pila, quedan: " );
        }else{
             System.out.println("\nLa pila esta vacia!");
        }
    }
    
    // Checar si esta vacia 
    private boolean Vacia(){
        if(Pila == null) return true;
        else return false;
    }
    
    
    public static void main(String[] args) {
        int t, opcion;
        String date;
        Scanner teclado = new Scanner(System.in);
        System.out.println("Pila ABC");
        System.out.println("Tamaño de la Pila");
        t = teclado.nextInt();
        PilaABC pilita = new PilaABC(t);
        do{
            System.out.println("1.  Llenar Pila");
            System.out.println("2. Mostrar Pila");
            System.out.println("3. Eliminar ");
            System.out.println("4. Salir");
            opcion = teclado.nextInt();
            switch(opcion){
                case 1:
                    pilita.Llenar();
                    break;
                    
                case 2:
                    pilita.Mostrar();
                    break;
                    
                case 3:
                    pilita.Eliminar();
                    break;
            }
        }while(opcion !=4);
    }
    
}
