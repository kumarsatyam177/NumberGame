import java.util.Scanner;

public class NumberGame {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int chances = 8;
        int finals = 0;
        boolean playAgain = true;
        System.out.println("Welcome Buddy!");
        System.out.println("Hey buddy, you have about " + chances + " chances to win the game.");

        while (playAgain) {
            int rand = getrandN(1, 100);
            boolean guess = false;

            for (int i = 0; i < chances; i++) {
                System.out.println("Chance " + (i + 1) + ": Enter your guess:");
                int user = sc.nextInt();

                if (user == rand) {
                    guess = true;
                    finals += 1;
                    System.out.println("You won it!");
                    break;
                } else if (user > rand) {
                    System.out.println("Too high");
                } else {
                    System.out.println("Too low");
                }
            }

            if (!guess) {
                System.out.println("Sorry buddy, you lost all your chances. The number was " + rand);
            }

            System.out.println("Do you want to play again (y/n)?");
            String pA = sc.next();
            playAgain = pA.equalsIgnoreCase("y");
        }

        System.out.println("That's it buddy, hope you enjoyed it.");
        System.out.println("Here is your score: " + finals);
    }

    public static int getrandN(int min, int max) {
        return (int) (Math.random() * (max - min + 1) + min);
    }
}
