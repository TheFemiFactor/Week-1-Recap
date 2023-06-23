import random

# Variables
x = 5
y = "Femi" # 'Femi', """"Femi""" '''Femi'''

# Casting
a = str(3)   #"3"
b = int(3)   # 3: whole number
c = float(3) # 3.0: decimal

# Type
print(type(a))
print(type(b))
print(type(c))

C = "three"

print(c)
print(C)

# Variables
d, e, f = "Detriot", "Eureka!", "Fayetteville"
print(d)
print(e)
print(f)

g = h = i = "France"
print(g)
print(h)
print(i)

cars = ["Mercedes", "Lamborghini", "Ferrari"]
j, k, l = cars

# Output
print(b, l)

# Escape characters
# We are currently in class and here is a "quote"
print("We are currently in class and here is a \"quote\"")

# Create list of cities represented in this class
# Create a variable and get input of city from person on the street
# if input is in city, print "your city is represented"
# if input is not in city (else), print "your city is not represented"
# Freestyle Python
repCities = ["Charlotte", "Salisbury", "Greenville", "Seattle", "Atlanta", "Hampton", "Tashkent", "East Orange"]
userCity = input("What city do you represent?: ")
if userCity in repCities:
  print("Your city is represented.")
else: 
  print("Your city ain't on the list")

# List
city = ["St Paul", "Brooklyn", "Charlotte", "Portland", "Brooklyn"]
        #0             1            2            3       4 Queens
#print(city[2])
#print(city[1:3])
#print(city[:3])

#if "Portland" in city:
  #print("Yes, the city is in the list")

city[4] = "Queens"
#print(city[4])
#city = ["St Paul", "Brooklyn", "Charlotte", "Portland", "Queens"]


city.insert(3, "Tashkent")
#city = ["St Paul", "Brooklyn", "Charlotte", "Tashkent", "Portland", "Queens"]

city[4:5] = ["Oakland"]
#city = ["St Paul", "Brooklyn", "Charlotte", "Tashkent", "Oakland", "Queens"]
#          0             1          2             3          4          5

city.remove("St Paul") # Removes by value
#city = ["Brooklyn", "Charlotte", "Tashkent", "Oakland", "Queens"]
#            0            1           2           3          4
city.pop(3) # Removes by index
#city = ["Brooklyn", "Charlotte", "Tashkent", "Queens"]

city.clear()
print(city)


# Sorting Lists
repCities = ["Charlotte", "Salisbury", "Greenville", "Seattle", "Atlanta", "Hampton", "Tashkent", "East Orange", "a"]

repCities.sort(key = str.lower)

numberList = [1, 2, 3, 4, 10, 20, 45, 99]
numberList.sort(reverse = True)

repCities2 = repCities.copy()

repCityNum = repCities + numberList
repCities.extend(numberList)
print(repCities)


'''
List methods/functions
append()	Adds an element at the end of the list
clear()	Removes all the elements from the list
copy()	Returns a copy of the list
count()	Returns the number of elements with the specified value
extend()	Add the elements of a list (or any iterable), to the end of the current list
index()	Returns the index of the first element with the specified value
insert()	Adds an element at the specified position
pop()	Removes the element at the specified position
remove()	Removes the item with the specified value
reverse()	Reverses the order of the list
sort()	Sorts the list
'''


# Create variables for letters, digits and special chars
# Keep generating till it meets the condition of at least 2 special chars/digits
# Create loop that will generate password
# Continue generating if enter, stop program if esc

import secrets
import string

# Create a function
def create_password(password_length=8): # setting the length of the password
  # Gather pool of alphanumeric characters for password, separately so that validate that we have digits and special characters
  letters = string.ascii_letters
  digits = string.digits
  specialChars = string.punctuation

  # Combo of letters, digits and special characters 
  alphabet = letters + digits + specialChars
  password = ''
  passwordStrong = False # Enables us to keep generating password till security conditions are met

  while not passwordStrong:
    password = ''
    # For the length of the password you want, loop through and pick a random/secret value from the alphabet 
    for x in range(password_length):
      password += ''.join(secrets.choice(alphabet))

    # If any special characters are in password, if the sum of digits in the password >= 2 then agree that the password is strong
    if (any(char in specialChars for char in password) and sum(char in digits for char in password) >= 2):
      passwordStrong = True
    # If password is strong, return what you got, if not keep trying
  return password


loop = True
while (loop):
  cont = input("Press Enter to continue or Esc to exit: ").lower()
  #enter, Enter, eNter, enTer, entEr, enteR, eNTeR
  if cont == "enter":
    print(create_password())
  elif cont == "esc":
    print("Thanks for using our app!")
    loop = False
  else:
    print("Please stick to the script. Kthanksbye, try again.")
