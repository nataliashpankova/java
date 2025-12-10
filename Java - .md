# java

Scrivi un metodo statico isPrime() che restituisca true se l'argomento è un numero primo e false in caso contrario.
Un numero primo è un numero intero positivo che non ha divisori diversi da uno e se stesso.

import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        for (int i = 0; i < 5; i++) {
            int number = scan.nextInt();
            System.out.print(isPrime(number) + " ");
        }
    }
    // put your code here
    public static boolean isPrime(int number) {
        if (number <= 1) {
            return false;
        }
        for (int i = 2; i <= (int) (number / 2); i++) {
            if (number % i == 0) {
                return false;
            }
        }
        return true;
    }
}
