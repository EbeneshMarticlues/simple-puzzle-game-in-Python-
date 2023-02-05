# simple-puzzle-game-in-Python-

This game generates a random number between 1 and 100 and then repeatedly prompts the player to guess the number. After each guess, the game informs the player whether the guess was too high or too low. The game continues until the player correctly guesses the number, and then it reports the number of attempts it took.

you can add more features to make the game more challenging and interactive. For example, you can:

Keep track of the player's previous guesses and display them to the player.
Limit the number of attempts the player has to guess the number.
Add difficulty levels (e.g. guess a number between 1 and 1000).
Provide hints to the player (e.g. whether the number is even or odd).
Keep score and allow the player to play multiple rounds.

import random

def puzzle_game():
    print("Welcome to the Puzzle Game!")
    print("The objective is to guess a number between 1 and 100.")
    number = random.randint(1, 100)
    guess = None
    attempts = 0
    previous_guesses = []
    while guess != number and attempts < 10:
        guess = int(input("Enter your guess: "))
        if guess < number:
            print("Too low.")
        elif guess > number:
            print("Too high.")
        attempts += 1
        previous_guesses.append(guess)
        print(f"Previous guesses: {previous_guesses}")
    if guess == number:
        print(f"You got it in {attempts} attempts!")
    else:
        print(f"You have reached the maximum number of attempts. The number was {number}.")

if __name__ == "__main__":
    puzzle_game()


