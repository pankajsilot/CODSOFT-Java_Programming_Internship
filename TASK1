package CODSOFT;

import java.io.IOException;
import java.util.Random;
import java.util.Scanner;

public class TASK1 {

    public static void main(String[] args) throws IOException {
        Scanner inputScanner = new Scanner(System.in);
        Random randomGenerator = new Random();

        System.out.println("\nWelcome to the Ultimate Guessing Game!\nThe game will generate a mystery number between 1 and 100.");
        System.out.println("Your mission, should you choose to accept it, is to guess that elusive number.");
        System.out.println("Your score will be the number of attempts it takes you to crack the code.\n");

        System.out.print("How many rounds do you dare to play? (Choose between 1 and 5): ");
        int totalRounds = inputScanner.nextInt();

        for (int currentRound = 1; currentRound <= totalRounds; currentRound++) {
            System.out.println();
            System.out.println("Round " + currentRound + " - Let the mind games begin!\n");

            System.out.println("Select your difficulty level:\n1 --> Easy [Unlimited attempts]\n2 --> Hard [Limited attempts]");
            int difficultyChoice = inputScanner.nextInt();

            switch (difficultyChoice) {
                case 1: {
                    System.out.println("Easy mode activated - No limits on attempts.\n");

                    int mysteryNumber = 1 + randomGenerator.nextInt(100);
                    System.out.println("Mystery number generated...");

                    int attemptCount = 1;
                    while (true) {
                        System.out.print("Take a shot! Enter your guess #" + attemptCount + ": ");
                        int userGuess = inputScanner.nextInt();

                        if (userGuess > mysteryNumber) {
                            System.out.println("The number " + userGuess + " is HIGHER than the Mystery Number. Keep guessing...");
                        } else if (userGuess < mysteryNumber) {
                            System.out.println("The number " + userGuess + " is LOWER than the Mystery Number. Keep guessing...");
                        } else {
                            System.out.println(
                                    "Congratulations! You cracked the code with " + attemptCount + " attempts. The Mystery Number was " + mysteryNumber + ".");
                            break;
                        }
                        attemptCount++;
                    }
                    break;
                }
                case 2: {
                    System.out.println("Hard mode initiated - Limited attempts, just 5 to be precise.\n");

                    int mysteryNumber = 1 + randomGenerator.nextInt(100);
                    System.out.println("Mystery number generated...");

                    int attemptCount = 1;
                    while (attemptCount <= 5) {
                        System.out.println("\nAttempts remaining: " + (6 - attemptCount) + " ...\n");
                        System.out.print("Take a shot! Enter your guess #" + attemptCount + ": ");
                        int userGuess = inputScanner.nextInt();

                        if (userGuess > mysteryNumber) {
                            System.out.println("The number " + userGuess + " is HIGHER than the Mystery Number. Keep guessing...");
                        } else if (userGuess < mysteryNumber) {
                            System.out.println("The number " + userGuess + " is LOWER than the Mystery Number. Keep guessing...");
                        } else {
                            System.out.println(
                                    "Congratulations! You cracked the code with " + attemptCount + " attempts. The Mystery Number was " + mysteryNumber + ".");
                            break;
                        }
                        attemptCount++;
                    }

                    if (attemptCount > 5) {
                        System.out.println("Uh-oh! You couldn't guess the number in 5 attempts. The Mystery Number was " + mysteryNumber + ". Better luck next time!\n");
                    }
                    break;
                }
                default: {
                    System.out.println("--- INVALID INPUT ---\n Oops! This round has been wasted. Choose a valid difficulty next time.");
                    break;
                }
            }

            System.out.println("Round " + currentRound + " is officially over.");
        }
        System.out.println("\nAll rounds completed.\nThanks for playing the Ultimate Guessing Game. Hope you had a blast!");
        inputScanner.close();
    }
}

