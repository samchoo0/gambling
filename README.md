this is for fun only no sue
import random

def rolldice():
    # Rolls a dice (random number between 1 and 6)
    return random.randint(1, 6)

def gamblinggame():
    print("Welcome to the Dice Gambling Game!")

Initialize balance
    balance = 100  # Starting balance

    while balance > 0:
        print(f"\nYour current balance: ${balance}")
        betamount = int(input("Enter your bet amount (or type 0 to exit): $"))

Exit the game if bet amount is 0
        if betamount == 0:
            print("Thanks for playing! Goodbye!")
            break

        # Check if the bet amount is valid
        if bet_amount > balance:
            print("You do not have enough balance to make that bet. Try a smaller amount.")
            continue

Choose the number to bet on (1 to 6)
        bet_number = int(input("Choose a number to bet on (1-6): "))

Check if the bet number is valid
        if bet_number < 1 or bet_number > 6:
            print("Invalid number. Please choose a number between 1 and 6.")
            continue

        # Roll the dice
        rolled_number = roll_dice()
        print(f"The dice rolled: {rolled_number}")

Check if the player wins or loses
        if rolled_number == bet_number:
            print(f"Congratulations! You win ${bet_amount * 5}!")
            balance += bet_amount * 5  # Player wins 5x their bet amount
        else:
            print(f"Sorry! You lose ${bet_amount}.")
            balance -= bet_amount  # Player loses their bet amount

Check if the player is out of money
        if balance <= 0:
            print("You have run out of money. Game over!")
            break

if __name == "__main":
    gambling_game()
