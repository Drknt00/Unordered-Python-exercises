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

# More on OOP:

class Robot:
    pass

Robot.name = "Blyx"
Robot.age = 1

print(Robot.name)
print(Robot.age)

# the keyword "pass" is in this case used as a placeholder, allowing for the code to be executed without an error.

# More on OOP: the __init__ method: the initializer method in classes allows to create attributes for objects, laying the blueprint of is inteded to and avoid repetions. This reduces the lines of code significantly:

# Let's take the following code:

class Employee:
    pass

emp_1 = Employee()
emp_2 = Employee()

emp_1.first = "Hary"
emp_1.last = "Seldon"
emp_1.email = "hary.seldon@trantor.com"
emp_1.pay = 50000

emp_2.first = "Salvor"
emp_2.last = "Hardin"
emp_2.email = "salvor.hardin@trantor.com"
emp_2.pay = 20000

print(emp_1.email)
print(emp_2.email)

# to print the email addresses, using the def __init__ will only require the following:

class Employee:
    def __init__(self, first, last, pay):
        self.first = first
        self.last = last
        self.email = first + "." + last + '@trantor.com'
        self.pay = pay     


emp_1 = Employee("Hary", "Seldon", 50000)
emp_2 = Employee("Salvor", "Hardin", 2000)


print(emp_1.email)
print(emp_2.email)


#9 Python modules: a module is a file containing codes that can be used to program, there are many of them, one popular is the math module, allowind for calculations:

import math

number = 65
result = math.sqrt(number)
print(result)

print(math.pi)

# The output will be as follow:

8.06225774829855
3.14159265358979

the module can also be renamed:

import math as m

number = 65
result = m.sqrt(number)
print(result)
print(m.pi)

# the result come as the same:
8.06225774829855
3.141592653589793


#The math module was imported, (by using the import math), import is the required statement to proceed, when imported, everything inside a module can be used after the dot operator.
In this case, we used .sqrt for square root of number, number being 65.
We then printed the result (square root of 65) and the value of pie (with math.pi), hence the output.

# the from import statement

Importing a modue gives access to everyhting included in it, if we only need to use a specific constant, function...the "from import" statement is useful.

# a simple example would be the follwoing:

from math import sqrt
number = sqrt(25)
print(number)

the output would be 5.0 .

# Another useful module is the random module.

When called , using the the random.randit, it can help index a items in a list:

import random
new_stuff = ["reading", "exercising", "meditating", "sleeping"]
index = random.randint
print(new_stuff[2])


# the dir function: displays all the features inside of a module when called.

import math
print(dir(math))
the output will bring all the associated tasks/features or operations that can be done with the math module.


# custom Modules can also be created in python by creating a file with the .py extension as a name (eg: private.py), and add a few functions inside:

def multiply(a, b):
    return a * b

def add (a + b)
    return a + b
etc... the file itself becomes a module and can be used by imoprting it as follow:

import private
result = private.multipy(5, 3)
print(result) will display 15 as the output.


