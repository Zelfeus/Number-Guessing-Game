import random

def hint1(n):
    print("Hint:")
    if n%2==0:
        print("The number is even")
    else:
        print("the number is odd")

def hint2(n):
    print("Hint:")
    if n<(upper+lower)/2:
        print("the number is less than ",int((upper+lower)/2))
    else: 
        print("the number is greater than ",int((upper+lower)/2))

def hint3(n,g):
    print("Hint:")
    if g >= n-5 and g <= n+5:
        print("Hotter!!!")
    else:
        print("Colder")
        
upper = int(input("Enter the upper limit: \n"))
lower = int(input("Enter the lower limit  \n"))
n = random.randint(upper,lower)

C=10

while C>0:
    g=int(input("Guess an integer between "+str(upper)+ " to "+str(lower)+ ":\n"))
    if g == n:
        print("Correct")
        print("Total points =",C)
        break
    else:
        C=C-1
        print("Wrong!!! Total points = ",C)
    hint = random.randint(1,3)
    if hint == 1:
        hint1(n)
    elif hint ==2:
        hint2(n)
    else:
        hint3(n,g)
