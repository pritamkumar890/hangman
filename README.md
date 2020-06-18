# hangman
#it is an good hangman game
import random
name=input("Enter your name dear")
print(f"welcome {name} to hangman game! lets play it ")
print("==========")
print("    |   |  ")
print("    o___| ")
print("   /|\     ")
print("    |      ")
print("   / \     ")

print("In this game one word will be choosen from computer from 10 words that you have given")
print("And then you have guess the letters of the choosen words ")

words=["apple","ball","cat","dog","elephant","fish",]
picked= random.choice(words)
turn=10
Right=["_"]*len(picked)
while True:
    user_input = input("enter your choice")
    if user_input in picked:
        index=0
        for i in picked:
            if i==user_input:
                Right[index]=user_input
            index+=1
        print(Right)
        if "_" not in Right:
            print("hurrey ! you win the game😘😘😘😘")
            break



    if user_input not in picked:
        turn=turn-1
        if turn==9:
            print(f"you have 9 chances left ")
            print("you have guessed wrong letter")
            print("==========")
        elif turn==8:
            print(f"you have 8 chances left")
            print("you have guessed wrong letter")
            print("==========")
            print("    |      ")
        elif turn==7:
            print(f"you have 7 chances left")
            print("you have guessed wrong letter")
            print("==========")
            print("    |      ")
            print("    o      ")
        elif turn== 6:
            print(f"you have 6 chances left")
            print("you have guessed wrong letter")
            print("==========")
            print("    |      ")
            print("    o      ")
            print("    |      ")
            print("    |      ")
        elif turn==5:
            print(f"you have 5 chances left")
            print("you have guessed wrong letter")
            print("==========")
            print("    |      ")
            print("    o      ")
            print("    |      ")
            print("    |      ")
            print("   / \     ")
        elif turn==4:
            print(f"you have 4 chances left")
            print("you have guessed wrong letter")
            print("==========")
            print("    |      ")
            print("    o      ")
            print("   /|\     ")
            print("    |      ")
            print("   / \     ")
        elif turn==3:
            print(f"you have 3 chances left")
            print("you have guessed wrong letter")
            print("==========")
            print("    |   |  ")
            print("    o      ")
            print("   /|\     ")
            print("    |      ")
            print("   / \     ")
        elif turn==2:
            print(f"you have 2 chances left")
            print("you have guessed wrong letter")
            print("==========")
            print("    |   |  ")
            print("    o   |  ")
            print("   /|\     ")
            print("    |      ")
            print("   / \     ")
        elif turn==1:
            print("you have guessed wrong letter")
            print("==========")
            print("    |   |  ")
            print("    o  _| ")
            print("   /|\     ")
            print("    |      ")
            print("   / \     ")
        else:
            print(f"you have lost chances,let kind man die")
            print("you have guessed wrong letter")
            print("==========")
            print("    |   |  ")
            print("    o___| ")
            print("   /|\     ")
            print("    |      ")
            print("   / \     ")
        if turn== 0:
            break
