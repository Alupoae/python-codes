# python-codes
Some learning pythons Codes
# tuples
t = ('a', 'b', 'c')
print(t.index('b'))
print(type(t))
print(len(t))
# sets
myset = set()
print(myset)
myset.add(1)
print(myset)
myset.add(2)
print(myset)
# Booleans
print(1 == 1)
print(1 < 2)
print(1 != 1)
# List Comprehensions

my_string = 'hello' # first way to represent
my_list = []
for letter in my_string:
    my_list.append(letter)
print(my_list)

my_list = [letter for letter in my_string] # second way to represent
print(my_list)

my_numbers = [x for x in range(0, 10)]
print(my_numbers)

celcius = [0, 20, 23, 38]
fahrenhit =[((9/5)*temp+32) for temp in celcius] # using append function
print(fahrenhit)

fahrenhit = []  # using append function in second way
for temp in celcius:
    fahrenhit.append((9/5)*temp+32)
print(fahrenhit)
# **2 poower of
# x%2 == 0 is used for even numbers

my_set = []
for x in [2, 4, 5]:
    for y in [1, 10, 100]:
        my_set.append(x*y)
print(my_set)
# Methods
my_list1 = [1, 2, 3]
my_list1.append(4)
print(my_list1)
# Functions
# 1 def Keywords
def say_hello():
    print("hello")
    print('are you ok?')
print(say_hello())

def say_hello(name):
    print(f'Hello {name}')
print(say_hello('Jose'))

def add_num(num1, num2):
    return num1 + num2
print(add_num(12, 20))

def add_num(num1, num2):
    return num1 + num2
result = add_num(10, 20)
print(result)

def print_result(a, b):
    print(a+b)
print(print_result(10, 20))

def myfunc(a, b):
    print(a+b)
    return a+b
result = myfunc(20, 80)
print(result)

# Function with logic
def even_check(number):
    sum = number % 2 == 0
    return sum
print(even_check(20))

# function that return true if any number is even inside the list
def check_even_list(num_list):
    for number in num_list:
        if number % 2 == 0:
            return True
        else:
            return False
print(check_even_list([1, 3, 5]))
print(check_even_list([2, 1, 4, 7]))
def even_list(numbers):
    new_list =[]
    for num in numbers:
        if num % 2 == 0:
            new_list.append(num)
    else:
        pass
    return new_list
print(even_list([1, 2, 3, 6]))
print(even_list([1, 3, 5]))

# function and tuple unpacking
work_hours = [('Dani', 100), ('Maria', 300), ('Jane', 400)]
def empolyee_check(work_hours):
    current_max = 0
    employee_winner = ''
    for employee, hour in work_hours:
        if hour > current_max:
            current_max = hour
            employee_winner = employee
        else:
            pass
    return (employee_winner, current_max)
print(empolyee_check(work_hours))

# Interaction Between Function
example = [1, 2, 3, 4, 5, 6]
from random import shuffle
result1 = shuffle(example)
print(result1)
def shuffle_list(mygame):
    shuffle(mygame)
    return mygame
result1 =shuffle_list(example)
print(result1)
my_game = ['', '0', '']

def player_guess():
    guess = ''
    while guess not in ['0', '1', '2']:
        guess = input('Pick up a number:0,1,2 = ')
    return int(guess)
print(player_guess())

def check_guess(mygame,guess):
    if mygame[guess] == '0':
        print('Correct')
    else:
        print("Wrong Guess")
        print(mygame)
# Initial List
mygame = ['', '0', '']
# Shuffle List
mixedup_list = shuffle_list(mygame)
# User Guess
guess = player_guess()
# Check Guess
check_guess(mixedup_list, guess)
