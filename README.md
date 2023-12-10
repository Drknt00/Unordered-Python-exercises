# Unordered-Python-exercises
A few exercises of basic python fundamentals
# 1 - Conditional statements

number = float(input("Enter a number: "))
if number < 0:
    print("the number is negative.")
elif number == 0:
    print("the number is equal to 0.")
else:
    print("The number is positive.")



#2 Basic while loop

#The following is a basic exampple of a while loop
#while loops runs in a way that will keep on repeating a block of code, as long as the conditioan is met

count = 0

while count < 3:
    print("This is a basic loop")
    print("Looping is fundamental concept in all programming languages.")
    
# the above code will keep on running (infinite loop or recursive loop, the below is the corrected way:

count = 0

while count < 3:
    print("This is a basic loop")
    print("Looping is fundamental concept in all programming languages.")
    count = count +1

#in the above example, the section count + 1 will add one from the initial cound 0, it will keep on running to 1, 2, 3 and 4, the condition is met at 4, the loop stops .


# 3 - Basic multiplication table with while loops:

# basic multiplication table

number = int(input("Enter a number: "))

count = 1

while count <= 10:
    product = number * count
    print(product)
    count = count + 1


# 4 - For loops

# basic for loop

words = ["her", "there", "up", "down"]
for word in words:
    print(word)

# the above example shows how for loops work in python, it itirates through items in a given list.

 # using the range() built-in funchtion
# this functions is similar to the while loop but in a for loop:

for count in range(1, 13):
    print(count)

# the code value 13 is excluded in the output, as it stops to 1 item prior to it.



# 5- the "break" statement

# Using break allows to stop a code from continuing when a certain required is met

for item in range(1, 11):
    if item == 9:
        break
    print(item)

# in the above, given that the condition is set to 9, the code will break (stop) a digit before it, at 8 .


# 6- The "continue statement
# as the name indicates, it allows a code to run even after a condition is met

for i in range(7):
    digit = int(input("enter a digit: "))
    if digit > 12:
        continue
    print(digit)

# in the above example, the code will keep on running, the user will be prompted to input a digit until the range 6 (one less that the 7) is met.


7- #Functions
# a function is basically a collective statements that can be used when called upon:

def message():
    print("Warning!")
    print("Computation error, self-destroy in 3 min!")

message()

# in the above example, the function message, when called (since it was defined with the two statments above it), will be displayed.

# Functions can be used in a variety of ways, greeting someone, doing a specific task, etc.

def elevate(task):
    print("I will elevate", task)

elevate("programing")

# the output of the above code, when the func is elave() is called would be "I will elevate programing"


#another example of using functions to make calculations:

def multiply_digits(d1, d2):
    result = d1 * d2
    print("the result is", result)

d1 = 3
d2 = 4
multiply_digits(d1, d2)


#8 - Object oriented programming : classes - __init__ method, and self:

class User:
    def __init__(self, full_name, birthday):
        self.name = full_name
        self.birthday = birthday #yyymmdd

        # Extract first and last names
        name_pieces = full_name.split(" ")
        self.first_name = name_pieces[0]
        self.last_name = name_pieces[-1]

user = User("Roronoa Zorro", "19950512")
print(user.name)
print(user.first_name)
print(user.last_name)
print(user.birthday)

