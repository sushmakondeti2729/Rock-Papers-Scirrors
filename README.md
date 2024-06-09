# Rock-Papers-Scirrors
Initialization: The code initializes the game by setting exit to False and initializing the user and computer points to 0.
Game Loop: A while loop runs continuously until exit is set to True.
User and Computer Input: Inside the loop, the user is prompted to input their choice of "rock," "paper," "scissors," or "exit." The computer randomly selects its choice from the same options.
Exit Condition: If the user inputs "exit," the game ends. The total scores for the user and computer are displayed, and exit is set to True to break out of the loop.

import random

exit = False
user_points = 0
computer_points = 0

while exit == False:
    options = ["rock", "paper" , "scissors"]
    user_input = input("Choose rock, paper, scissors or exit: ")
    computer_input = random.choice(options)
    
    if user_input == "exit" :
        print("Game ended")
        print("You won a total score of "+str(user_points)+" and the computer total score is " +str(computer_points))
        exit = True

    if user_input == "rock":
        if computer_input == "rock":
            print("Your input is rock")
            print("computer input is rock")
            print("It is a tie!")
        elif computer_input == "paper":
            print("Your input is rock")
            print("computer input is paper")
            print(" computer wins")
            computer_points += 1
        elif computer_input == "scissors":
            print("Your input is rock")
            print("computer input is scissors")
            print("you win")
            user_points += 1

    elif user_input == "paper":
        if computer_input == "rock":
            print("Your input is paper")
            print("computer input is rock")
            print("you win!")
            user_points += 1
        elif computer_input == "paper":
            print("Your input is paper")
            print("computer input is paper")
            print("it's a tie!")
        elif computer_input == "scissors":
            print("Your input is paper")
            print("computer input is scissors")
            print("computer wins")
            computer_points += 1

    elif user_input == "scissors":
        if computer_input == "rock":
            print("Your input is scissors")
            print("computer input is rock")
            print("computer win!")
            computer_points += 1
        elif computer_input == "paper":
            print("Your input is scissors")
            print("computer input is paper")
            print("you win")
            user_points += 1
        elif computer_input == "scissors":
            print("Your input is scissors")
            print("computer input is scissors")
            print("its a tie")

    elif user_input != " rock" or user_input != "paper" or user_input != "scissors":
        print("Invalid Input")
