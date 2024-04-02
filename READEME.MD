It's just a game of guessing the number from 1 to 100, made in Python and very simple
```
import random

print("Welcome to the Guess")

random_number = random.randint(1, 100)
attempts = 10
response = 0
while int(response) != random_number:
    response = input("Guess a number between 1 and 100: ")
    if int(response) ==random_number:
        print("Correct!")
    elif int(response) > random_number:
        attempts -= 1
        print("you you missed, the number is smaller. You still have {}".format(attempts))
    elif int(response) < random_number:
        attempts -= 1
        print("you you missed, the number is bigger. You still have {}".format(attempts))

print("Thank you for playing!")
