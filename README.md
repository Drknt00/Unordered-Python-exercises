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

    
