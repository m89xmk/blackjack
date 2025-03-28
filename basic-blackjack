import random
# from art import logo

def deal_card():
    decks = [2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10,11]
    card = random.choice(decks)
    return card

def cal_score(decks):
    if sum(decks) == 21 and len(decks) == 2:
        return 0

    if 11 in decks and sum(decks) > 21:
        decks.remove(11)
        decks.append(1)

    return sum(decks)

def compare(user_hand, dealer_hand):
    if user_hand == dealer_hand:
        return "Draw"
    elif user_hand == 0:
        return "User Win"
    elif dealer_hand == 0:
        return "Dealer Win"
    elif user_hand > 21:
        return "Dealer Win"
    elif dealer_hand > 21:
        return  "User Win"
    elif user_hand > dealer_hand:
        return "User Win"
    elif user_hand < dealer_hand:
        return "Dealer Win"

def play():
    print(logo)
    user_hand = []
    dealer_hand = []

    for i in range(2):
        user_hand.append(deal_card())
        dealer_hand.append(deal_card())

    while True:
        user_score = cal_score(user_hand)
        dealer_score = cal_score(dealer_hand)
        print(f"Your cards: {user_hand}, current score: {user_score}")
        print(f"Computer's first card: {dealer_hand[0]}")

        if dealer_score == 0 or  user_score == 0 or user_score > 21:
            break
        else:
            should_deal = input("'y' plus deck 'n' end : ")
            if  should_deal == 'y':
                 user_hand.append(deal_card())
            else:
                break


    while dealer_score!=0 and dealer_score < 17:
        dealer_hand.append(deal_card())
        dealer_score = cal_score(dealer_hand)

    print(f"Your final hand: {user_hand}, final score: {user_score}")
    print(f"Computer's final hand: {dealer_hand}, final score: {dealer_score}")
    print(compare(user_score, dealer_score))

while input("Do you want to play a game of Blackjack? Type 'y' or 'n': ") == "y":
    play()
