# AokTugasKonversi
import java.util.Scanner;

public class AokTugasKonversi {
    public static void main(String[] args) {
        Scanner inp = new Scanner(System.in);
        
        //Declare
        boolean running = true;
        String biner = "";
        String hexadesimal = "";
        int desimal = 0;


        //menu awal
        while (running){
            System.out.println("Menu");
            System.out.println("1. Biner ke desimal");
            System.out.println("2. Desimal ke biner");
            System.out.println("3. Biner ke hexadesimal");
            System.out.println("4. Hexadesimal ke biner");
            System.out.println("5. Desimal ke hexadesimal");
            System.out.println("6. Hexadesimal ke desimal");
            System.out.println("0. keluar");
        
            int Menu = inp.nextInt();
             inp.nextLine();
            
            //switch case menu
            switch (Menu) {
                case 1: 
                System.out.println("Masukkan bilangan biner: ");
                biner = inp.nextLine();
                desimal = Integer.parseInt(biner, 2);
                System.out.println("hasilnya adalah: " + desimal);
                break;

                case 2:
                System.out.println("Masukkan bilangan desimal: ");
                desimal = inp.nextInt();
                biner = Integer.toBinaryString(desimal);
                System.out.println("hasilnya adalah: " + biner);
                break;

                case 3:
                System.out.println("Masukkan bilangan biner: ");
                biner = inp.nextLine();
                hexadesimal = Integer.toString(Integer.parseInt(biner, 2), 16);
                System.out.println("Hasilnya adalah: " + hexadesimal);
                break;

                case 4:
                System.out.println("Masukkan bilangan hexadesimal: ");
                hexadesimal = inp.nextLine();
                biner = Integer.toString(Integer.parseInt(hexadesimal, 16), 2);
                System.out.println("Hasilnya adalah: " + biner);
                break;

                case 5:
                System.out.println("Masukkan bilangan desimal: ");
                desimal = inp.nextInt();
                hexadesimal = Integer.toHexString(desimal);
                System.out.println("Hasilnya adalah: " + hexadesimal);
                break;

                case 6:
                System.out.println("Masukkan bilangan hexadesimal: ");
                hexadesimal = inp.nextLine();
                desimal = Integer.parseInt(hexadesimal,16);
                System.out.println("Hasilnya adalah: "+ desimal);
                break;
            
                case 0:
                running = false;
                System.out.println("Anda sudah keluar");
                default:
            }
    }
}
}

