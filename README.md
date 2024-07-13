 import random

def guess_the_number():
    print("Welcome to Guess the Number Game!")
    print("I'm thinking of a number between 1 and 100.")
    secret_number = random.randint(1, 100)
    attempts = 0
    
    while True:
        guess = input("Enter your guess (between 1 and 100): ")
        try:
            guess = int(guess)
            attempts += 1
            
            if guess < 1 or guess > 100:
                print("Please enter a number between 1 and 100.")
                continue
            
            if guess < secret_number:
                print("Too low! Try guessing higher.")
            elif guess > secret_number:
                print("Too high! Try guessing lower.")
            else:
                print(f"Congratulations! You've guessed the number {secret_number} correctly!")
                print(f"It took you {attempts} attempts.")
                break
        
        except ValueError:
            print("Invalid input! Please enter a valid number.")

# play game

if __ppgame__ == "__play game__":
    guess_the_number()
