# infa_2020_maltsev

from graph import *
from random import *


windowSize(1000, 800)

def krug(a, x, y, r):
    brushColor(a)
    circle(x, y, r)

def kvad(c1, c2, c3, x1, y1, x2, y2):
    penColor(c1, c2, c3)
    brushColor(c1, c2, c3)
    rectangle(x1, y1, x2, y2)

kvad(0, 250, 100, 0, 0, 1000, 800/6)
kvad(230, 230, 230, 0, 800/6, 1000, 800)

x1Cord = 0
y1Cord = 0
x2Cord = 0
y2Cord = 0
for i in range(4):
    x1Cord = randint(250*i, 250 + 250*i)
    y1Cord = randint(2000 // 6, 2000)
    x2Cord = x1Cord + 100*random()
    kvad(230, 230, 0, x1Cord, y1Cord, x2Cord, y2Cord)
    print(x1Cord)


run()