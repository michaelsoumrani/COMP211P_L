# COMP211P_L

//we have to add comments

// we have to do something in case the user inputs a non caps letter 

//This program prompts the user to make a selection in the main menu of the game

import java.util.scanner
public class MainMenu
{
 public static void main(String[] args)
 {
  Scanner scan = new Scanner(System.in);
  String aChoice = scan.nextLine();
  Menu theMenu = new Menu(aChoice);
  
  // Now we ask the user to choose an option and organize the responses in different methods
  
  char selection = 'L';
  while ((selection != 'Q') || (selection != 'P') || (selection != 'B'))
  {
    System.out.println("Welcome to the Word Game")
    System.out.println("\t" + "Login (L)");
    System.out.println("\t" + "Register (R)");
    System.out.println("\t" + "About (A)");
    System.out.println("\t" + "Play the Game (P)");
    System.out.println("\t" + "Show the Leader Board (B)");
    System.out.println("\t" + "Quit (Q)");
    System.out.println();
    System.out.print("\t" + "Please choose an option: ");
    selection = scan.next().charAt(0);
    switch (selection)
  {
      case 'L':
        theMenu.login();
        break;
      case 'R':
        theMenu.register();
        break;
      case 'A':
      // Or we could directly system out print the info about the game
        theMenu.about();
        break;
      case 'P':
        theMenu.play();
        break;
      case 'B':
        theMenu.leaderboard();
        break;
     // No need for case Q as it will automatically end the game
      }
        }
        System.out.println("\tPROGRAM ENDED\n");
    }
}
     
     
  

  
  
