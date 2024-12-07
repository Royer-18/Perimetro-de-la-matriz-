package ejer3perimetrodelamatriz;

import java.util.Scanner;

public class Ejer3PerimetrodelaMatriz {

    public static void main(String[] args) {
        
        Scanner teclado = new Scanner (System.in);
        
        System.out.println("ingrese la dimension de la matriz: ");
        int d = teclado.nextInt(); 
        
        int matriz [][] = new int [d][d];
        
        System.out.println("INGRESE LOS ELEMENTOS: ");
        for (int i=0;i<d;i++){
            for (int j=0;j<d;j++){
                matriz[i][j]=teclado.nextInt(); 
            }
        }
       
        //mostrar matriz 
        for (int i=0;i<d;i++){
            for (int j=0;j<d;j++){
                System.out.print("["+ matriz[i][j]+"]");
            }
            System.out.println("");
        }
        
        //suma del perimetro
        int perimetro =0;
        
        for (int j=0;j<d;j++){
                 perimetro = perimetro + matriz[0][j]; 
            }
        
        for (int i=0;i<d;i++){
                 perimetro = perimetro + matriz[i][0]; 
            }
        
        for (int i=0;i<d;i++){
                 perimetro = perimetro + matriz[i][d-1]; 
            }
        
        for (int j=0;j<d;j++){
                 perimetro = perimetro + matriz[d-1][j]; 
            }
        
        int resul = perimetro - matriz[0][0] - matriz[0][d-1] - matriz[d-1][d-1] - matriz[d-1][0]; 
        
        System.out.println("EL PERIMETRO ES: " + resul);
        
    }  
}
