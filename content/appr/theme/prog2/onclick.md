# Cliquer - `onclick`

Dans ce chapitre nous explorons comment un programme peux détecter un clic de souris et y réagir.
Cliquer (ou toucher) est la méthode principale pour interagir avec un smartphone : on touche avec le doigt une certaine position de l'écran et le programme y réagit. Nous allons voir que

- la méthode `onclick(f)` permet de définir une fonction de rappel,
- la fonction de rappel `f(x, y)` est appelée lors d'un clic de souris,
- la méthode `listen()` met en marche les événements interactifs.

## Fonction de rappel

En informatique, une fonction de rappel (**callback** en anglais) ou fonction de post-traitement est une fonction qui est passée en argument à une autre fonction. Cette dernière peut alors faire usage de cette fonction de rappel comme de n'importe quelle autre fonction, alors qu'elle ne la connaît pas par avance.

## Fonction `onclick`

La méthode `onclick(f)` permet de définir une fonction `f` qui est alors appelé à chaque fois quand on clique avec la souris dans le canevas. A ce moment la fonction `f` est appelé avec les coordonnés `(x, y)` de la souris au moment du clic.

La variable `s` fait référence à l’objet `Screen` qui possède les deux méthodes :

- `onclick(f)` pour installer une fonction de rappel f() pour un clic de sours,
- `listen()` pour commencer à *écouter* les événements de la souris.

Le programme suivant dessine un point à la position du clic et affiche les coordonnées dans la console.

```{codeplay}
from turtle import *
s = getscreen()

hideturtle()
speed(0)
up()

def f(x, y):
    print('clic à', x, y)
    goto(x, y)
    dot()

s.onclick(f)
s.listen()
```

**Exercice** : Cliquez dans les 4 coins et au centre.

## Tortue ou écran

Une fonction `onclick()` existe pour l'écran et pour chaque tortue.
Donc nous avons deux fonctions de rappel. Une pour des clics dans tout l'écran, l'autre que pour des clics dans la tortue.

Quand nous cliquons dans la tortue, la position est écrit dans la console et la tortue avance de 20 pixels.

```{codeplay}
from turtle import *
shape('turtle')

def f(x, y):
    print('écran à ', x, y)
    
def g(x, y):
    print('tortue à', x, y)
    forward(20)

t = getturtle()
s = getscreen()

t.onclick(g)
s.onclick(f)
s.listen()
```

**Exercice** : Cliquez dans dans la tortue et à côté et observez la différence.

## Dessiner une forme

Dans ce programme nous dessinons une ligne entre les clics successifs.
C'est pour cette raison nous appelons la fonction `ligne(x, y)` au lieu de `f(x, y)`.

Nous réagissons également à deus touches du clavier :

- `u` (up) pour lever le stylo
- `c` (clear) pour effacer le canevas

```{codeplay}
from turtle import *
hideturtle()
speed(0)
up()

def ligne(x, y):
    goto(x, y)
    down()
    dot()
    
getscreen().onkey(up, 'u')
getscreen().onkey(clear, 'c')
    
getscreen().onclick(ligne)
getscreen().listen()
```

**Exercice** : Dessinez une maison. Utilisez la touche `u` (up) pour dessiner une forme disjointe, par exemple la fenêtre.

## Remplir une forme

Dans ce programme nous dessinons une ligne entre les clics successifs.
C'est pour cette raison nous appelons la fonction `ligne(x, y)` au lieu de `f(x, y)`.

Nous réagissons également à deus touches du clavier :

- `u` (up) pour lever le stylo
- `c` (clear) pour effacer le canevas
- `b` (begin fill)
- `e` (end fill)


```{codeplay}
from turtle import *
hideturtle()
fillcolor('pink')
speed(0)
up()

def ligne(x, y):
    goto(x, y)
    down()
    dot()
    
getscreen().onkey(up, 'u')
getscreen().onkey(clear, 'c')
getscreen().onkey(begin_fill, 'b')
getscreen().onkey(end_fill, 'e')
    
getscreen().onclick(ligne)
getscreen().listen()
```

**Exercice** : Dessinez une maison. Utilisez la touche `b` (begin) pour commencer le remplissage et la touche `e` (end) pour terminer le remplissage.

## Echiquier

Ici nous dessinons d'abord un tableau de jeu. Ensuite nous détectons la case dans laquelle le clic a eu lieu et y ajoutons un disque noir.

```{codeplay}
from turtle import *
hideturtle()
speed(0)
up()

x0, dx, nx = -160, 40, 10
y0, dy, ny = -160, 40, 8
x1 = x0 + nx * dx
y1 = y0 + ny * dy

def ligne(x0, y0, x1, y1):
    goto(x0, y0)
    down()
    goto(x1, y1)
    up()

for i in range(ny + 1):
    y = y0 + i * dy
    ligne(x0, y, x1, y)
    
for i in range(nx + 1):
    x = x0 + i * dx
    ligne(x, y0, x, y1)

def f(x, y):
    if x0 < x < x1:
        i = (x - x0) // dx
    if y0 < y < y1:
        j = (y - y0) // dy

    x = x0 + i * dx + dx/2
    y = y0 + j * dy + dy/2
    
    goto(x, y)
    dot(dx)
    
getscreen().onclick(f)
getscreen().listen()
```

**Exercice** : Cliquez dans chaque deuxième case.

## Héritage

Dans l'exemple suivant nous définissons une classe parent `Object`. Elle possède les méthodes 

- `draw_box()` pour dessiner un contour rectangulaire
- `fill_box()` pour dessiner un rectangle rempli
- `inside(x, y)` pour tester si le point `(x, y)` se trouve dans le rectangle

Les trois fonctions `Dot`, `Rect` et `Text` héritent tous les méthodes de la classe parent `Object`.

```{codeplay}
from turtle import *
up()
speed(0)
hideturtle()
getscreen().bgcolor('lightgray')

class Object:
        
    def draw_box(self):
        goto(self.pos)
        down()
        for d in self.size * 2:
            forward(d)
            left(90)
        up()
        
    def fill_box(self):
        goto(self.pos)
        color(*self.col)
        width(self.width)
        begin_fill()
        self.draw_box()
        end_fill()
        width(1)

    def inside(self, x, y):
        x0, y0 = self.pos
        x1 = x0 + self.size[0]
        y1 = y0 + self.size[1]
        return x0 < x < x1 and y0 < y < y1
        
    def __str__(self):
        return f'{self.__class__.__name__}({self.pos}, {self.size})'

class Dot(Object):
    def __init__(self, pos, d=20, col='red'):
        self.pos = pos
        self.size = d, d
        self.col = col
        self.draw()
        
    def draw(self):
        r = self.size[0] / 2
        goto(self.pos[0]+r, self.pos[1]+r)
        pencolor(self.col)
        dot(self.size[0])
        self.draw_box()
    
class Rect(Object):
    def __init__(self, pos, size, width=1, col=('black', 'white')):
        self.pos = pos
        self.size = size
        self.width = width
        self.col = col
        self.draw()
        
    def draw(self):
        self.fill_box()        
             
class Text(Object):
    def __init__(self, pos, text, col='red', font=(None, 12, 'normal'), align='left'):
        super()
        self.text = text
        self.pos = pos
        self.col = col
        self.font = font
        self.align = align
        self.draw()
        
    def draw(self):
        goto(self.pos)
        color(self.col)
        x0 = xcor()
        write(self.text, font=self.font, align=self.align, move=True)
        self.size = xcor() - x0, self.font[1]
        self.draw_box()
        
d0 = Dot((0, 0))
d1 = Dot((100, 20), 50, 'lime')

t0 = Text((0, 50), 'origin', font=(None, 18, 'bold'))
t1 = Text((0, 100), 'pad', font=(None, 80), col='blue')
t2 = Text((-100, 100), '夢', font=(None, 60), col='blue')
t3 = Text((-200, 100), '📺', font=(None, 60), col='blue')

r0 = Rect((-100, 0), (50, 80))
r1 = Rect((-150, -20), (60, 80), width=5, col=('black', 'pink'))

def f(x, y):
    for obj in (d0, d1, t0, t1, t2, t3, r0, r1):
        if obj.inside(x, y):
            print('clicked in', obj)
    
getscreen().onclick(f)
getscreen().listen()
```

**Exercice** : Clickez dans tout les objets et observez les info affichés dans la console.

## ondrag-onrelease

Le programme suivant permet de déplacer la tortue avec la souris

- `onclick` la tortue devient rouge,
- `ondrag` la tortue devient orange et suit la souris,
- `onrelease` la tortue devient vert et s'arrête,

**Note** La fonction on `onrelease` ne fonction pas ici, mais elle fonctionne dans l'éditeur externe Thonny.

```{codeplay}
from turtle import *
shape('turtle')
speed(0)

def f(x, y):
    fillcolor('red')
    print('click at', x, y)
    
def g(x, y):
    fillcolor('orange')
    print('drag')
    goto(x, y)
      
def h(x, y):
    fillcolor('green')
    print('release at', x, y)

onclick(f)
ondrag(g)
onrelease(h)
```

**Exercice** : Essayez de tirez la tortue lentement avec la souris.
