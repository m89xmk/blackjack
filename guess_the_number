import random

def play():
    print("Welcome to the number guessing game!")
    print("I'm thinking of a number between 1 ~ 100.")

    secret_number = random.randint(1, 100)
    difficulties = {'easy': 10, 'hard': 5}
    print(secret_number)

    difficulty = input("Choose a difficulty. Type 'easy ' or 'hard': ")
    life = difficulties.get(difficulty, 0)

    if difficulty == 'easy':
        print(f"You have a {life} attempts remaining to guess the number")

    elif difficulty == 'hard':
        print(f"You have a {life} attempts remaining to guess the number")

    while life > 0:

        user_input = int(input("Make a guess: "))

        if life == 0:
            print(f"You've run out of guess. The answer was {secret_number} ")

        elif user_input == secret_number:
            print(f"You've got it! The answer was {secret_number}")
            break

        if user_input > secret_number:
            life -= 1
            print("Too high")
            print("Guess again")
            print(f"You have a {life} attempts remaining to guess the number")

        elif user_input < secret_number:
            life -= 1
            print("Too low")
            print("Guess again")
            print(f"You have a {life} attempts remaining to guess the number")

play()
