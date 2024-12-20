'''exampl output:-Welcome to the Dice Roller!
Press Enter to roll the dice...
You rolled a 4!
Do you want to roll again? (y/n): y
Press Enter to roll the dice...
You rolled a 2!
Do you want to roll again? (y/n): n
Thanks for playing!
'''
# simple-dice-roller
import random

def roll_dice():
    # Generate a random number between 1 and 6
    return random.randint(1, 6)

def dice_roller():
    print("Welcome to the Dice Roller!")
    
    while True:
        input("Press Enter to roll the dice...")
        roll = roll_dice()
        print(f"You rolled a {roll}!")
        
        # Ask the user if they want to roll again
        again = input("Do you want to roll again? (y/n): ").lower()
        if again != 'y':
            print("Thanks for playing!")
            break

# Start the dice roller game
if __name__ == "__main__":
    dice_roller()
