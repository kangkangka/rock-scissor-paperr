# rock-scissor-paper
import random


play = True

while play :

    
    player = input("Enter your choice (rock/paper/scissor): ")
    player = player.lower()
    while (player != "rock" and player != "paper" and player != "scissor"):
        player = input("Enter your choice (rock/paper/scissor): ")
        player = player.lower()

    
    computer = random.randint(1,3)
    if (computer == 1):
        computer = "rock"
    elif (computer == 2):
        computer = "paper"
    elif (computer == 3):
        computer = "scissor"
    else:
        print ("Error. Enter your choice from rock,paper, scissor.")

    
    if (player == computer):
        print ("we are same!")
    elif (player == "rock"):
        if (computer == "paper"):
            print ("you win.");
        if (computer == "scissor"):
            print ("you loose.");
    elif (player == "paper"):
        if (computer == "rock"):
            print ("you win.");
        if (computer == "scissor"):
            print ("you loose.");
    elif (player == "scissor"):
        if (computer == "rock"):
            print ("you loose.");
        if (computer == "paper"):
            print ("you loose.");

    
    userInput = input("Do you want to stop game? Yes or No: ")
    userInput = userInput.lower()
    if (userInput == "yes"):
        play = False
        print ("See you next time")
    else:
        play = True

