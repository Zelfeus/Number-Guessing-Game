# Number-Guessing-Game
A game where the system would generate a random number and you'll be given the task of guessing what the number is, 
your starting points would be 10 and as you keep on guessing the number your points would keep reducing while you receive help through hints.
Good Luck!!


import random
#define hint1, whether the number is even or odd
def hint1(n):
    print("Hint:")
    if n%2==0:
        print("The number is even")
    else:
        print("the number is odd")
#define hint2, whether the number is lesser or greater than the midpoint of the range entered
def hint2(n):
    print("Hint:")
    if n<(upper+lower)/2:
        print("the number is less than ",int((upper+lower)/2))
    else: 
        print("the number is greater than ",int((upper+lower)/2))

#define hint3, whether the number guessed is around a difference of 5 from the generated number
def hint3(n,g):
    print("Hint:")
    if g >= n-5 and g <= n+5:
        print("Hotter!!!")
    else:
        print("Colder")
        
#Ask user to enter the upper limit
upper = int(input("Enter the upper limit: \n"))

#Ask user to enter the lower limit
lower = int(input("Enter the lower limit  \n"))

#Generate the random number
n = random.randint(upper,lower)

#set a counter for the number of points 
C=10

#Create a loop set for exiting when points equal to 0
while C>0:
    g=int(input("Guess an integer between "+str(upper)+ " to "+str(lower)+ ":\n"))
    if g == n:
        print("Correct")
        print("Total points =",C)
        #break loop and print the number of points attained 
        break
    else: #if wrong then decrement the points by 1
        C=C-1
        print("Wrong!!! Total points = ",C)
    #Create a variable randomly generating numbers 1-3 which would denote the hint to be generated
    hint = random.randint(1,3)
    if hint == 1: 
        hint1(n) #call hint1
    elif hint ==2:
        hint2(n) #call hint2
    else:
        hint3(n,g) #call hint3
