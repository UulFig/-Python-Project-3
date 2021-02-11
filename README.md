# -Python-Project-3
#3 Do you can drive ? 

def age_inputNumber(message):
  while True:
    try:
       userInput = int(input(message))
    except ValueError:
       print("Please, put an valid age.\n")
       continue
    else:
       return userInput
       break

def license_inputNumber(question):
    userInput = str(input(question)).lower()
    if userInput == "yes":
        return 1
    elif userInput == "no":
        return 0
    else:
        return license_inputNumber("Please, use 'yes' or 'no'.\n")

age = age_inputNumber("How old are you?\n")

if (age>=18):
    print("You are old enough to drive.\n")
else:
    print("You will be able to drive in " + str(18-age) + " year(s).\n")


license = license_inputNumber("Do you have a license to drive?\n")

if (license == 1):
    print("You can drive!")
elif (license == 0):
    print("You can not drive!")
