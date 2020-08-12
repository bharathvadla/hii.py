import random
name=input("enter your name:")
print("Goodluck!",name)
words=['cat','green','billa','flying','prabhas','deepika','bharath','baahubali',
       'rana','hulk','thor','ironman','disk','laptop','rose','keyboard','mouse',
       'banana','orange','joker','instagram','lilly','anabelle','anushka','vaccine',
       'doctor','lion','change','elephant','editing','people','america','doraemon','thunderstorm',
       'insomnia','ruler','dustbin']
word=random.choice(words)
print("Guess a character")
guesses=''
turns=10
while(turns>0):
  failed=0
  for char in word:
    if char in guesses:
      print(char)
    else:
      print("_")
      failed+=1
  if failed==0:
    print("You win")
    print("The word is:",word)
    break
  guess=input("Guess a character")
  guesses+=guess
  if guess not in word:
    turns-=1
    print("wrong")
    print("you have",turns,"more guess")
  if turns==0:
    print("you lost the word is:",word)
