# THM_Solver
Solves a board from the minigame "Treasure Hunter Monolith" from the game "Danganronpa 3: The End of Hope's Peak High". 
The best solution is found by using the alpha-star search algorithm. 
The treasures are completely ignored, and the solver instead attempts to clear as much of the board as possible.

I decided to make this project while I was learning Python in order to help my little brother get the platinum trophy in the game, 
as I couldn't find any good solvers online.

Prerequisites: Python 3 with the Numpy library installed. The Stats.py and GenerateBoard.py scripts also requires the Pandas library,                  but this is not necessary to use the solver.

Step 1: Take a picture of the board, pause the game and make a CSV file describing the board using notepad or a similar program. 
        Place it in the "/boards" folder. A few example boards are already present in the folder.
        
Step 2: Execute THM.py from the command prompt using python. 

        Usage: python THM.py [filename (without extension)] [target clearance rate in %] [maximum board state searches] [print_output]
               The following default values to the optional arguments are given:
               target clearance rate = 100
               maximum board state searches = 5000
               print_output = 2 (this prints the solution as a series of images, 1 prints the solution directly into the cmd and 0 doesn't print the solution)
               
        Example:
                Type the following into the command prompt:
                
                cd "D:\path\to\scripts\folder"
                python THM.py board3
                
                This will return the best solution found for board3 in the boards folder, attempting to clear 100 % of the board, 
                by searching through a maximum of 5000 different board states. Feel free to allow for a longer search, sometimes this 
                results in a board that's cleared slightly more. The solution is output as a series of .png images
                
Step 3: Go through the solution step by step as shown in the images in the "/solution" folder. 
        Here's an example solution of the 4x4 board, board1.csv: https://imgur.com/a/oArHJZr

Step 4: Hopefully enjoy your platinum. It will probably still require a little bit of luck with the positioning of the treasures.


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
                
                
