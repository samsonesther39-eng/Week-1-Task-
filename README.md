import random

def get_computer_choice():
    choices = ["rock", "paper", "scissors"]
    return random.choice(choices)  # Fixed: Correctly spelling 'choices'

def determine_winner(user_choice, computer_choice):
    if user_choice == computer_choice:
        return "It's a tie!"
    if (user_choice == "rock" and computer_choice == "scissors") or \
       (user_choice == "scissors" and computer_choice == "paper") or \
       (user_choice == "paper" and computer_choice == "rock"):
        return "You win!"
    return "Computer wins!"

def play_game():
    user_choice = input("Enter your choice (rock, paper, or scissors): ").lower()
    while user_choice not in ["rock", "paper", "scissors"]:
        user_choice = input("Invalid input. Please enter rock, paper, or scissors: ").lower()
    
    computer_choice = get_computer_choice()
    print(f"\nYou chose {user_choice}, computer chose {computer_choice}.\n")
    
    print(determine_winner(user_choice, computer_choice))

play_game()

