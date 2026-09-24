import random

option = ["rock","paper","scissors"]

play_again = True


while play_again:
        
    user_choice = input("\nYour choice: ").lower()  

    if user_choice not in option:
        print(" Invalid choice!   ,  please tray again.")
        continue

    computer_choice = random.choice(option)    
    
    print(f"You chose {user_choice},computer chose {computer_choice}")


    if user_choice == computer_choice:
       print(" It's a tie!")
       play_again = True


    elif (user_choice == "rock" and computer_choice == "scissors") or \
        (user_choice == "paper" and computer_choice == "rock") or \
        (user_choice == "scissors" and computer_choice == "paper"):
        print(" You win!")
        play_again = False

        
    else:
        print("You Lose!")
        play_again = False

