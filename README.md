import java.util.Scanner;

public class NumberManipulations {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter the number:");
        int number = scanner.nextInt();

        int result;
        if (number > 50) {
            int tens = number / 10;
            int ones = number % 10;
            result = tens - ones;
        } else {
            // Reverse the number manually
            int reversed = reverseNumber(number);
            int tens = reversed / 10;
            int ones = reversed % 10;
            result = tens - ones;
        }

        System.out.println("Result: " + result);

        scanner.close();
    }

    // Function to manually reverse a number
    public static int reverseNumber(int number) {
        int reversed = 0;
        while (number != 0) {
            int digit = number % 10;
            reversed = reversed * 10 + digit;
            number /= 10;
        }
        return reversed;
    }
}
