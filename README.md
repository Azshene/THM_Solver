# THM_Solver
Solves a board from the minigame "Treasure Hunter Monolith" from the game "Danganronpa 3: The End of Hope's Peak High". 
The best solution is found by using the alpha-star search algorithm. 
The treasures are completely ignored, and the solver instead attempts to clear as much of the board as possible.

I decided to make this project while I was learning Python in order to help my little brother get the platinum trophy in the game, 
as I couldn't find any good solvers online.

Prerequisites: Python 3 with the Numpy and Pandas libraries installed.

Step 1: Take a picture of the board, pause the game and make a CSV file describing the board using notepad or a similar program. 
        Place it in the "/boards" folder. A few example boards are already present in the folder.
        
Step 2: Execute THM.py from the command prompt using python. 
        Usage: python THM.py [filename (without extension)] [target clearance rate in %] [maximum board state searches] [print_output]
               The following default values to the optional arguments are given:
               target clearance rate = 100
               maximum board state searches = 3000
               print_output = 2 (this prints the solution as a series of images, 1 prints the solution directly into the cmd and 0 doesn't print the solution)
        Example: 
                cd "D:\folder\Treasure Hunter Monolith"
                python THM.py board3 100 3000 2
                
Step 3: Go through the solution step by step as shown in the images in the "/solution" folder.

Step 4: Hopefully enjoy your platinum, this probably still requires a little bit of luck with the positioning of the treasures.

Two additional files are included in the project:

GenerateBoard.py: Generates a random initial board of a specified width and height

                  Usage: Usage: python GenerateBoard.py [height], [width]
      
Stats.py: Returns the mean, standard deviation, coefficient of variance, min and max of the following parameters:
          percentage of board cleared, number of states explored, number of steps for the best solution, 
          boolean of whether max states were exceeded. 
          The parameters are computed for a given amount of samples for a board with a given height and width and 
          given a max amount of states to search
          
          Usage: python Stats.py [height] [width] [maximum board state searches] [samples]
          
Author: Kasper Lindskov Andersen, E-mail: Kasper.LindskovAndersen@gmail.com

License: None, have at it. A mention would be appreciated, however :) 
                
                
