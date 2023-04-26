# Numbergame
import java.util.Random;
import java.util.Scanner;

public class NumberGuessingGame {
    public static void main(String[] args) {
        Random random = new Random();
        int number = random.nextInt(100) + 1; // Generate a random number between 1 and 100
        int guess;
        int numGuesses = 0;
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("Welcome to the Number Guessing Game!");
        System.out.println("I'm thinking of a number between 1 and 100. Can you guess it?");
        
        do {
            System.out.print("Enter your guess: ");
            guess = scanner.nextInt();
            numGuesses++;
            
            if (guess < number) {
                System.out.println("Too low! Try again.");
            } else if (guess > number) {
                System.out.println("Too high! Try again.");
            }
        } while (guess != number);
        
        System.out.println("Congratulations! You guessed the number in " + numGuesses + " guesses.");
        scanner.close();
    }
}
