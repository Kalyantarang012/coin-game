# coin-game
#code for simple python random coin game
import random

heads_orTails = input("heads or talis: ")

total_random_side = 0
num_flips = 10
wins = 0
losses = 0

for _ in range(num_flips):
    coin = "  "

    random_side = random.randint(1, 2)
    if random_side == 1:
        coin = "heads"
    else:
        coin = "tails"

    total_random_side += random_side

    if coin == heads_orTails:
      print("you win")
      wins += 1
    else:
      print("you lose")
      losses += 1


    print(random_side)

average_random_side = total_random_side / num_flips
print(f"\nThe average random number is: {round(average_random_side)}")
print(f"Wins: {wins}")
print(f"Losses: {losses}")
