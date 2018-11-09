# Hello_World
Just another repository
from tkinter import *

root = Tk()

Label(root, text='attempts').grid(row=0, column=0)
aEntry = Entry(root)
aEntry.grid(row=0, column=1)
Label(root, text='completions').grid(row=1, column=0)
bEntry = Entry(root)
bEntry.grid(row=1, column=1)
Label(root, text='yards').grid(row=2, column=0)
cEntry = Entry(root)
cEntry.grid(row=2, column=1)
Label(root, text='touchdowns').grid(row=3, column=0)
dEntry = Entry(root)
dEntry.grid(row=3, column=1)
Label(root, text='interceptions').grid(row=4, column=0)
eEntry = Entry(root)
eEntry.grid(row=4, column=1)
"""
Label(root, text='QB name').grid(row=5, column=0)
fEntry = Entry(root)
fEntry.grid(row=5, column=1)
"""
threeEntry = Entry(root)
threeEntry.grid(row=6, column=1)


def a():
    num1 = aEntry.get()
    num2 = bEntry.get()
    A = ((num2 / num1) - .03) * 5
    if A > 2.375:
        A = 2.375
    if A < 0:
        A = 0
    return A


def b():
    num1 = aEntry.get()
    num3 = cEntry.get()
    B = ((num3 / num1) - 3) * 0.25
    if B > 2.375:
        B = 2.375
    if B < 0:
        B = 0
    return B


def c():
    num1 = aEntry.get()
    num4 = dEntry.get()
    C = (num4 / num1) * 20
    if C > 2.375:
        C = 2.375
    if C < 0:
        C = 0
    return C


def d():
    num1 = aEntry.get()
    num5 = eEntry.get()
    D = 2.375 - ((num5 / num1) * 25)
    if D > 2.375:
        D = 2.375
    if D < 0:
        D = 0
    return D


def r():
    threeEntry.delete(0, 'end')
    jesus = a
    pizza = b
    pie = c
    mary = d

    rate = ((float(jesus) + float(pizza) + float(pie) + float(mary)) / 6) * 100
    print(rate)
    threeEntry.insert(0, int(rate))


Button = Button(root, text='Calculate', command=r).grid(row=6, column=0)


root.mainloop()

