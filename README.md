# Palindromo


package palindromo;
import java.util.Scanner;

public class Palindromo {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("DIGITE UMA PALAVRA:");
        String palavra = scanner.nextLine();
        if (verificarPalindromo(palavra)) {
            System.out.println(palavra + " é um palíndromo."); 
        } else {
            System.out.println(palavra + " não é um palíndromo.");
        }
        // fecha Scanner
        scanner.close();
    }

    public static boolean verificarPalindromo(String palavra) {
        palavra = palavra.toLowerCase();
        // converte a palavra para minúsculas para evitar problemas de comparação de maiúsculas/minúsculas
        int comprimento = palavra.length();
        for (int i = 0; i < comprimento / 2; i++) {
            if (palavra.charAt(i) != palavra.charAt(comprimento - i - 1)) {
                return false;
            }
        }
        return true;
    }
}
