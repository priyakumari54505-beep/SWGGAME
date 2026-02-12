# SWGGAME
snake water and gun game in which computer and you play tha game between two.
import random
'''
1 for snake
-1 for water
0 for gun
'''

computer = random.choice([-1,0,1])
youstr = input("Enter your choice:")
youDict = {"S":1,"W":-1,"G":0}
reverseDict = {1:"Snake",-1:"Water",0:"Gun"}

you = youDict[youstr]

#by now we have 2 numbers(variables),you and computer

print(f"you chose{reverseDict[you]}\ncomputer chose {reverseDict[computer]}")

if(computer == you):
    print("Its a draw")
else:
    if(computer == -1 and you == 1):
        print("you win!")
    elif(computer == -1 and you == 0):
        print("you lose!")
    elif(computer == 1 and you == -1):
        print("you lose!")
    elif(computer == 1 and you == 0):
        print("you win!")
    elif(computer == 0 and you == -1):
        print("you win!")
    elif(computer == 0 and you == 1):
        print("you lose!")
    else:
        print("something went wrong!")
        
