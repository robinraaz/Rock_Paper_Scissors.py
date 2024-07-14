# Rock_Paper_Scissors.py
import random
# Function to determine the winner
def determine_winner(player_choice, computer_choice):
    if player_choice == computer_choice:
        return "Draw"
    elif (player_choice == "Rock" and computer_choice == "Scissors") or \
         (player_choice == "Paper" and computer_choice == "Rock"):
        return "Player 1 wins"
    else:
        return "Computer wins"
# Function to get the computer's choice
def get_computer_choice():
    choices = ["Rock", "Paper", "Scissors"]
    return random.choice(choices)
# Main game function
def play_game():
    player_choice = input("Enter your choice (Rock, Paper, Scissors): ").capitalize()
    computer_choice = get_computer_choice()
    print(f"Player 1 choice: {player_choice}")
    print(f"Computer choice: {computer_choice}")
    result = determine_winner(player_choice, computer_choice)
    print(result)
# Play the game
play_game()
