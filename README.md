[![Run on Repl.it](https://repl.it/badge/github/maya5768/mayaD)](https://repl.it/github/maya5768/mayaD)
# mayaD
# # Question #1:
# def func():
#     question = 'Enter number between 1 - 10000: '
#     while True:
#         try:
#             a = int(input(question))
#             if a > 10000 or a < 1:
#                 question = 'Only between 1 - 10000: '
#             else:
#                 print(a)
#                 break
#         except ValueError:
#             question = 'Only a number: '
# func()

# # Question #2:
# print('a' > 'b')  # False
# print('a' > 'B')  # True
# print(f'The ASCII Value of c is {ord("c")}')  # ASCII Value of c
# print(f'The char value of 99 is {chr(99)}')  # Chr value of 99

# # Question #3:
# while True:
#     try:
#         string = list(input('Enter string: '))
#         choice = int(input('Enter choice (1 = Lower, 2 = Upper): '))
#         break
#     except ValueError:
#         print('Error, Try again')

# if choice == 1:
#     for i in range(len(string)):
#         if ord(string[i]) in range(65, 90):
#             string[i] = chr(ord(string[i]) + 32)

# elif choice == 2:
#     for i in range(len(string)):
#         if ord(string[i]) in range(97, 122):
#             string[i] = chr(ord(string[i]) - 32)

# print(''.join(string))

# # Question #4:
# for index, value in enumerate([1, 2, 6, 9]):
#     print(index, value)

# # Question #5:
# class Cat:
#     color = 'black'

#     def __init__(self, name):
#         self.name = name

#     def say(self):
#         print(self.name, ' say meow')

#     def eat(self):
#         print(self.name, 'I am eating')


# mizi = Cat('mizi')
# shimon = Cat('shimon')

# mizi.say()
# shimon.say()

# mizi.color = 'white'

# # Question #6:
# Question #1:
from user import User

def register():
    while True:
        check = input('Enter Password: ')
        if len(check) > 8 and check[0].isupper():
            break
        print('Password must be longer than 8 and start with upper letter!')
    return check


print('REGISTER')
user = User(
    input('Enter Username: '), register(), input('Enter Code: '))

while True:
    print('\n', 'LOGIN')
    user.login(input('Enter Username: '), input('Enter password: '))

