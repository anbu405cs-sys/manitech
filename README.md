Rock, Paper, Scissor – Python Game Application
📌 Project Overview

This is a simple and interactive Rock, Paper, and Scissor game developed using Python.
The user plays against the computer, and the program randomly selects one option each round.
The game determines the winner based on standard rules and allows the user to play multiple rounds.

🎯 Features

User-friendly text-based interface

Computer generates random choices

Displays both user and computer choices

Determines winner instantly

Option to play again

Fully written in simple Python

Beginner-friendly project

🛠️ Technologies Used

Python

Built-in library: random

📂 Project Structure
📁 Rock-Paper-Scissor-Game
│── rock_paper_scissor.py
│── README.md

💻 How to Run the Program

Install Python 3.

Download or clone the repository:

git clone https://github.com/your-username/your-repo-name.git


Open the project folder.

Run the program:

python rock_paper_scissor.py

🧩 Game Rules

Rock beats Scissor

Scissor beats Paper

Paper beats Rock

Same choices → Tie

📜 Source Code
import random

def get_computer_choice():
    choices = ["rock", "paper", "scissor"]
    return random.choice(choices)

def get_user_choice():
    user_input = input("Enter rock, paper or scissor: ").lower()
    return user_input

def determine_winner(user, computer):
    if user == computer:
        return "It's a tie!"
    elif (user == "rock" and computer == "scissor") or \
         (user == "paper" and computer == "rock") or \
         (user == "scissor" and computer == "paper"):
        return "You win!"
    else:
        return "Computer wins!"

while True:
    user_choice = get_user_choice()
    computer_choice = get_computer_choice()

    print(f"You chose: {user_choice}")
    print(f"Computer chose: {computer_choice}")

    result = determine_winner(user_choice, computer_choice)
    print(result)

    play_again = input("Play again? (yes/no): ").lower()
    if play_again != "yes":
        break

print("Thanks for playing!")
