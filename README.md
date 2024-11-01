# Guessing-letter-
mport random
Computer = '0'
Player   = 'X'

Board = [' '] * 10

def Board(Boox):
    print(f'{Boox[1]} | {Boox[2]} | {Boox[3]}')
    print(f'{Boox[4]} | {Boox[5]} | {Boox[6]}')
    print(f'{Boox[7]} | {Boox[8]} | {Boox[9]}')
    print('-' * 10)
def Lost_or_win():
    if  Boox[1] == Boox[2] == Boox[3] and Boox[1]!=' ':
            return True
    elif Boox[4] == Boox[5] == Boox[6] and Boox[4]!=' ':
            return True
    elif Boox[7] == Boox[8] == Boox[9] and Boox[7]!=' ':
            return True
    elif Boox[1] == Boox[4] == Boox[7] and Boox[1]!=' ':
            return True
    elif Boox[2] == Boox[5] == Boox[8] and Boox[2]!=' ':
            return True
    elif Boox[3] == Boox[6] == Boox[9] and Boox[3]!=' ':
            return True
    elif Boox[1] == Boox[5] == Boox[9] and Boox[1]!=' ':
            return True
    elif Boox[7] == Boox[5] == Boox[3] and Boox[7]!=' ':
        return True
    else :
        return False
    
def Space(pos):
    return True Boox[pos] == ' ' else False

def insert(letter,pos):
    if Space(pos):
        Boox[pos]= letter
        Board(Boox)
        if Lost_or_win():
            if letter == 'X':
                print('Player win')
            else:
                print('Computer win')
                exit()

def Plyr_move(letter):
    pos = int(input("enter the position to inert:"))
    insert(letter,pos)

def Comptr_move(letter):
    pos = random.randint(1,9)
    insert(letter,pos)

while not Lost_or_win():

    Board(Boox)
    Comptr_move(Computer)
    Plyr_move(Player)
