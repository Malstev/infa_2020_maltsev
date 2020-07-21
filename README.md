from graph import *



def igolka(x1, y1, a, b):
    penColor('black')
    brushColor(10, 10, 10)
    polygon([(x1, y1), ((x1 + 10) - a, (y1 - 40) - b), (x1 + 20, y1 - b), (x1, y1)])
    polygon([(x1 + 20, y1), ((x1 + 30) - a, (y1 - 40) - b), (x1 + 40, y1 - b), (x1, y1)])


def telo_ega():
    penColor(220, 220, 220)
    brushColor(40, 40, 40)
    oval(300, 530, 400, 470)
    #tulovische

    oval(319 - 6, 523 - 3, 319 + 6, 523 + 3)
    #noga 2-ya sleva

    oval(307 - 6, 515 - 3, 307 + 6, 515 + 3)
    #samaya levaya noga

    oval(394 - 6, 514 - 3, 394 + 6, 514 + 3)
    #samaya pravaya noga

    oval(383 - 6, 522 - 3, 383 + 6, 522 + 3)
    #vtoraya sprava noga

    oval(382, 490, 418, 513)
    #golova

    circle(418, (490+513)/2, 2)
    #nos

    brushColor(0, 0, 0)
    circle(395, (490 + 513) / 2 - 3, 2)
    circle(403, (490 + 513) / 2 - 5, 2)
    #glaza



def kvad(c1, c2, c3, x1, y1, x2, y2):
    penColor(c1, c2, c3)
    brushColor(c1, c2, c3)
    rectangle(x1, y1, x2, y2)


kvad(0, 250, 100, 0, 0, 500, 400)
kvad(100, 100, 100, 0, 400, 500, 600)


# risuet zemluy i nebo
#zemlya imeet koordinati x(0-500), y(400-600)
#nebo imeet koordinati x(0-500), y(0-400)
def derevo(x1, y1, x2):
    c1 = 250
    c2 = 250
    c3 = 0
    y2 = 0
    kvad(c1, c2, c3, x1, y1, x2, y2)


derevo(0, 430, 40)
derevo(60, 580, 150)
derevo(380, 430, 410)
derevo(470, 500, 495)
telo_ega()




run()
