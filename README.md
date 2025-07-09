import random

cards = ["A", "2", "3", "4", "5", "6", "7", "8", "9", "10", "J", "Q", "K"]

card_values = {
    "A": 11 or 1,
    "2": 2,
    "3": 3,
    "4": 4,
    "5": 5,
    "6": 6,
    "7": 7,
    "8": 8,
    "9": 9,
    "10": 10,
    "J": 10,
    "Q": 10,
    "K": 10
}


user_input = input("Would you like to play BlackJack? (Yes/No): ")

if user_input == "Yes":
    first_card = random.choice(cards)
    second_card = random.choice(cards)
    print(first_card, second_card)

    dealer_first_card = random.choice(cards)
    dealer_second_card = random.choice(cards)
    print("Dealer", dealer_first_card)

    hitorstand_input = input("Would you like to hit or stand (Hit/Stand): ")
    if hitorstand_input == "Hit":
        hit_random = random.choice(cards)
        print(hit_random)

            

    if first_card + second_card + hit_random > 21:
        print("You lose")
        
    else:
        second_hitorstand_input = input("Would you like to hit or stand (Hit/Stand): ")
        if second_hitorstand_input == "Hit":
            secondhit_random = random.choice(cards)
            print(secondhit_random)

        if first_card + second_card + hit_random + second_hitorstand_input > 21:
            print("You lose")

        

