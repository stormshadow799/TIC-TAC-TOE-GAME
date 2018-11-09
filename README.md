# TIC-TAC-TOE-GAME
# I have created this game in python in just 50 lines of Code.
# I hope that u will like this. Enjoy!!!!!!!!!!

import sys
def show(lists):
    print("--------|-------------|-----------")
    print(lists[0])
    print("--------|-------------|-----------")
    print(lists[1])
    print("--------|-------------|-----------")
    print(lists[2])
    print("--------|-------------|-----------")
def win(lists,x):
    if "  x     |     x       |    x       " in lists:
        return True
    if lists[0][2] == 'x'  and lists[1][2] == 'x' and lists[2][2] == 'x':
        return True
    if lists[0][14] == 'x' and lists[1][14] == 'x' and lists[2][14] == 'x':
        return True
    if lists[0][27] == 'x' and lists[1][27] == 'x' and lists[2][27] == 'x':
        return True
    if lists[0][2] == 'x' and lists[1][14] == 'x' and lists[2][27] == 'x':
        return True
    if lists[0][27] == 'x' and lists[1][14] == 'x' and lists[2][2] == 'x':
        return True
lists = ["  1     |     2       |    3       ","  4     |     5       |    6        ","  7     |     8       |    9        "]
print("--------|-------------|-----------")
print(lists[0])
print("--------|-------------|-----------")
print(lists[1])
print("--------|-------------|-----------")
print(lists[2])
print("--------|-------------|-----------")
a=0
while a<5:
    x = str(input("Enter Your Choice Player One"))
    for i in lists:
        for j in i.split():
            if x == j:
                lists = [i.replace(j, "x") for i in lists]
            if win(lists,"x"):
                print("First Player Wins")
                sys.exit()
            show(lists)
 x = str(input("Enter Your Choice Player Two"))
    for i in lists:
        for j in i.split():
            if x == j:
                lists = [i.replace(j, "0") for i in lists]
            if win(lists, "0"):
                print("Second Player Wins")
                sys.exit()
            show(lists)
    a = a + 1
