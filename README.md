# RockPaperScissors
This is simple code  for game


using System;

class Program
{
    static void Main()
    {
        Random rand = new Random();
        int computerChoice = rand.Next(1, 4);
        int playerChoice;

        Console.WriteLine("Enter 1 for Rock, 2 for Paper, or 3 for Scissors:");

        while (true)
        {
            if (int.TryParse(Console.ReadLine(), out playerChoice) && playerChoice >= 1 && playerChoice <= 3)
            {
                break;
            }
            else
            {
                Console.WriteLine("Invalid input. Enter 1 for Rock, 2 for Paper, or 3 for Scissors:");
            }
        }   

        Console.Write("Computer chose: ");
        switch (computerChoice)
        {
            case 1:
                Console.WriteLine("Rock");
                break;
            case 2:
                Console.WriteLine("Paper");
                break;
            case 3:
                Console.WriteLine("Scissors");
                break;
        }

        if (computerChoice == playerChoice)
        {
            Console.WriteLine("The game was a draw!");
        }
        else if (computerChoice == 1 && playerChoice == 3 ||
            computerChoice == 2 && playerChoice == 1 ||
            computerChoice == 3 && playerChoice == 2)
        {
            Console.WriteLine("Computer wins!");
        }
        else
        {
            Console.WriteLine("You win!");
           
        }
        Console.ReadLine();
        
        
    }
}
