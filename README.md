# Combination
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        int num1,num2, factor1,factor2,factor3,combination;

        Scanner input = new Scanner(System.in);
        System.out.println("Lütfen 1.Sayıyı  Giriniz: ");
        num1 = input.nextInt();
        System.out.println("Lütfen 2.Sayıyı  Giriniz: ");
        num2 = input.nextInt();
        factor1 =1;
        factor2=1;
        factor3=1;
       combination=1;

       if(num1-num2>0) {
           for (int i = 1; i <= num1; i++) {
               factor1 = factor1 * i;
           }
           for (int i = 1; i <= num2; i++) {
               factor2 = factor2 * i;
           }
           for (int i = 1; i <= (num1 - num2); i++) {
               factor3 = factor3 * i;
           }
           combination = factor1 / (factor2 * (factor3));
           System.out.println(combination);
       }else{
           System.out.println("Hatalı giriş yaptınız!");
       }

    }
}
