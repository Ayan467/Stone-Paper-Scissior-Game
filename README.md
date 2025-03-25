# Stone-Paper-Scissior-Game
Author-Ayan Samanta



import java.util.*; 
import java.util.Random; 
import java.util.Scanner; 
 
public class Main { 
    public static void main(String[] args) { 
        Scanner scanner = new Scanner(System.in); 
        Random random = new Random(); 
         
        String[] choices = {"Rock", "Paper", "Scissors"}; 
         
        while (true) { 
            System.out.print("Enter Rock, Paper, or Scissors (or Quit to exit): "); 
            String userInput = scanner.nextLine(); 
             
            if (userInput.equalsIgnoreCase("Quit")) { 
                System.out.println("Thanks for playing!"); 
                break; 
            } 
             
            int computerChoiceIndex = random.nextInt(3); 
            String computerChoice = choices[computerChoiceIndex]; 
             
            System.out.println("Computer chose: " + computerChoice); 
             
            if (userInput.equalsIgnoreCase(computerChoice)) { 
                System.out.println("It's a tie!"); 
            } else if ((userInput.equalsIgnoreCase("Rock") && computerChoice.equals("Scissors")) 
|| 
                       (userInput.equalsIgnoreCase("Paper") && computerChoice.equals("Rock")) || 
                       (userInput.equalsIgnoreCase("Scissors") && computerChoice.equals("Paper"))) 
{ 
                System.out.println("You win!"); 
            } else { 
                System.out.println("You lose!"); 
            } 
        } 
         
        scanner.close(); 
    } 
} 
