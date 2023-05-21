# rockpaper
import random

def play_game():
    print("Let's play Rock, Paper, Scissors!")
    print("Enter your choice:")
    print("1. Rock")
    print("2. Paper")
    print("3. Scissors")

    choices = ["Rock", "Paper", "Scissors"]
    user_choice = int(input("Your choice (1-3): "))
    computer_choice = random.randint(1, 3)

    print("You chose:", choices[user_choice - 1])
    print("Computer chose:", choices[computer_choice - 1])

    # Determine the winner
    if user_choice == computer_choice:
        print("It's a tie!")
    elif (
        (user_choice == 1 and computer_choice == 3)
        or (user_choice == 2 and computer_choice == 1)
        or (user_choice == 3 and computer_choice == 2)
    ):
        print("You win!")
    else:
        print("Computer wins!")

    play_again = input("Do you want to play again? (yes/no): ")
    if play_again.lower() == "yes":
        play_game()
    else:
        print("Thanks for playing!")

play_game()
