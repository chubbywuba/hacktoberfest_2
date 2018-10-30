# hacktoberfest_2
#Guess a number game
# import random
import random
# create and initialize variables 
# have user input lower end of range
lower = raw_input ("I want the number between")
intLower = int(lower)

# have user input upper end of range
upper = raw_input ("and ")
intUpper = int(upper)
turns = 4
turnsCount = 0
win_flag = False
# generate the mystery number
MysteryNumber = random.randint(intLower,intUpper)

# have user input the number of turns and range
print "You will have ",turns," turns to guess a number between ", lower, " and ", upper

while (turns > 0):
  turnsCount +=1
  # have user input a guess
  guess = raw_input("Guess a number:")
  intGuess = int(guess)
 
  # provide feedback	
  if (intGuess == MysteryNumber):
    win_flag = True
    break
	
  elif ( intGuess > MysteryNumber):
    # print guess lower message
    print "guess lower"
    
  else:
    # print guess higher message
    print "guess higher"
  
  turns -=1

  if (intGuess < lower): 
   print 'stay between', intLower, 'and',intUpper,
  
  if (intGuess > upper):
    print 'stay between', intLower, 'and' ,intUpper,
  
else:
    print "Guess a number:"


if win_flag:
  # print – message and number of turns
  print "You Win!"
  print "You guessed the mystery number in ", turnsCount, " turns"
  
else:
  # print – message and mystery number
  print "You lose"
  print "The mystery number was", MysteryNumber
   
