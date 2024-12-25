# Dice-Rolling-Simulator
A simple and easy language code for beginner.
import random

def roll_dice(sides=6):
    """Roll a dice with the given number of sides."""
    return random.randint(1, sides)

def main():
    print("Welcome to the Dice Rolling Simulator!")
    while True:
        try:
            sides = int(input("Enter the number of sides on the dice (default is 6): "))
        except ValueError:
            print("Invalid input. Please enter a positive integer.")
            continue
        
        if sides < 1:
            print("The number of sides must be at least 1.")
            continue

        result = roll_dice(sides)
        print(f"You rolled a {result} on a {sides}-sided die.")
        
        again = input("Do you want to roll again? (yes/no): ").strip().lower()
        if again not in ('yes', 'y'):
            print("Thanks for using the Dice Rolling Simulator. Goodbye!")
            break

if __name__ == "__main__":
    main()

