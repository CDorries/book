# Projet

Dans ce chapitre, nous allons faire un projet de dessin. Nous allons mettre en pratique un certain nombre de concepts de ce cours :

- dessiner
- définir
- colorier
- répéter
- cercler
- parcourir
- calculer
- typographier
- itérer
- paramétrer
- randomiser

## Consignes

Vous devez créer un dessin avec un programme Python.

En concret, vous devez :

- créer un dessin concret (pas abstrait)
- choisir un sujet libre : nature, ville, intérieur, jeux vidéo, science-fiction, etc.
- utiliser le module turtle pour dessiner
- écrire 500 à 1000 lignes de code
- commencer le programme avec un commentaire (auteur, date, description)
- utiliser des dots, lignes et le remplissage
- varier l'épaisseur du trait
- lever et baisser le stylo
- utiliser des cercles et des arcs de cercle
- utiliser des couleurs de ligne, point, remplissage et arrière-fond
- décomposer en fonctions appropriées, avec une taille de 2-15 lignes
- décrire chaque fonction avec un commentaire de 1-2 ligne
- utiliser des variables pour nommer vos entités (largeur, hauteur, rayon, couleur)
- utiliser des expressions mathématiques (largeur/n, 2*rayon, etc.)
- avoir une hiérarchie de fonctions (des plus complexes qui appellent des plus simples)
- définir d'abord toutes les fonctions pour dessiner
- définir une dernière fonction main() qui utilise ces fonctions pour créer un dessin
- appeler main() vers la fin du programme pour créer le dessin
- suivre la typographie standard PEP8 (espacement, noms des variables)
- vérifier votre code en ligne [pep8online.com](http://pep8online.com)
- parcourir avec for des séquences de couleurs, angles, distances, et tailles
- répéter avec for en 1D (par exemple: hublots, traverses, fenêtres, roues, clôtures)
- répéter avec for en 2D (par exemple: fenêtres, grilles, pixels, etc.)
- utiliser des fonctions aléatoires (module random) pour introduire de la variété
- utiliser la perspective : des objets plus près sont plus grands
- utiliser `random.seed(n)` pour rendre votre dessin reproductible
- exporter en format image : EPS, PNG, JPG
- déposer sur Moodle les 4 fichiers avec un nom de forme `prénom_projet1` (par exemple `alice_projet1.py`, `alice_projet1.eps`, etc.)

## Exemples

Ces exemples ont été créés par des élèves en 3M, en option complémentaire informatique, après 2 mois de cours sur la programmation en Python (environ 24 périodes au total).

### Jeu vidéo

![projet](media/projet_alex.png)

### Maison de campagne

![projet](media/projet_alice.png)

### Cadre des Pyrénées

![projet](media/projet_andi.png)

### Japon

![projet](media/projet_arthur.png)

### Swiss space

![projet](media/projet_emilien.png)

### Maison meublée

![projet](media/projet_enrico.png)

### Casque d'astronaute

![projet](media/projet_florent.png)

### Urbain et rural

![projet](media/projet_garance.png)

### Star Trek

![projet](media/projet_gregory.png)

### Loup sous la lune

![projet](media/projet_hugo.jpg)

### Fantaisie psychédélique

![projet](media/projet_samuel.png)

### Bateaux de pêche

![projet](media/projet_walid.png)

## Refactoring

Le Refactoring (réusinage) de code est l'opération consistant à retravailler le code source d'un programme informatique, de façon à en améliorer la lisibilité et, la maintenance, ou à le rendre plus générique.

Le refactoring est une réécriture de code pour le rendre

- plus lisible
- plus standard
- plus réutilisable
- plus général

Téléchargez le code source {download}`project1.py <code/projet1.py>`

## Style PEP 8

PEP est un acronyme anglais signifiant Python Enhancement Proposal que l'on pourrait traduire en français par « Proposition d'Amélioration de Python » (PAP donc 😄).

Le document [PEP 8](https://peps.python.org/pep-0008/) présente les bonnes conventions pour écrire du code lisible.

- Utilisez 4 espaces pour l'indentation
- Limitez les lignes à 79 caractères au maximum
- Séparez des fonctions par 2 lignes vides
- Écrivez les importations sur des lignes séparées

Espaces

- Ne mettez pas d'espace entre nom de fonction et parenthèse (faux: `f (x)`)
- Ne mettez pas d'espace à l'intérieur des parenthèses (faux: `f( x, y )`)
- Ne mettez pas d'espace avant `,`, `;`, `:` (faux: `def f(x , y) :`)
- Mettez un espace avant et après un opérateur (`+`, `-`, `*`, `/`, etc.)
- Mettez un espace avant et après le symbole d'affectation `=`

Allez sur le site [pep8online.com](http://pep8online.com)
et copiez-y votre code.

Corrigez les 77 erreurs de styles.

- Mettez un espace après `#`
- Mettez deux lignes vides entre fonctions
- Mettre un espace après `,`

## Nom de fonction

En Python les variables sont écrites avec des minuscules. Si une variable consiste en plusieurs mots, utilisez un tiret bas (`_`) pour séparer les mots.
En Python, les noms commençant avec des majuscules sont réservés pour les classes. Par exemple

`player = Player()`

Donc changez le noms suivants : 

- Exporter → exporter
- Niveau → niveau
- RepositionnementFin → repositionnement_fin
- PlateformePiques → plateforme_piques
- TriangleDrapeau → triangle_drapeau
- BatonDrapeau → baton_drapeau
- ReplacementPiques → replacement_piques
- Player → player
- Brique → brique
- Mur → mur
- ReplacementMur → replacement_mur
- Plateforme → plateforme

Comme un nom de fonction peut être utilisé à différents endroits nous avons avantage d'utiliser la fonction **rechercher et remplacer**
![dialogue remplacer](media/projet_remplacer.png)

Dans VS Code nous avons aussi une fonction **Remplacer Symbol F2**

![dialogue remplacer](media/projet_remplacer2.png)

## Conseils

Ce programme est récursif - La fonction `main()` appelle `begin()` qui appelle `nuages()` qui appelle `soleil()` etc.
Pour avoir des fonctions réutilisable au maximum, vous devez écrire des fonctions indépendantes les unes des autres, avec beaucoup de paramètres.

Donc voici les conseils essentiels :

- utilisez la fonction `goto()` pour positionner la tortue (il ne faut pas inclure la position dans la fonction)
- créez des fonctions indépendants (il ne faut pas les enchaîner)
- créez des fonctions avec plein de paramètres (taille, couleur, épaisseur, etc.)
- utilisez des valeurs par défaut pour préconfigurer les paramètres de la fonction

## Soleil

La fonction `soleil()` m'a pas d'argument et utilise un cercle pour dessiner un disque. La position de départ est le bord inférieur du disque.

```{codeplay}
from turtle import *
getscreen().bgcolor('cyan')
up()

def soleil():
    # Dessine un soleil à 3 rayons
    seth(0)
    color("yellow")
    begin_fill()
    circle(50)
    end_fill()
    left(90)
    forward(50)
    left(90)
    down()
    width(10)
    for i in range(3):
        forward(100)
        backward(100)
        left(45)
    up()

goto(100, 80)
soleil()
```

Une meilleure façon est de créer une fonction `soleil(d, col, a, angle, n)` avec :

- un diamètre `d`
- une longueur de rayons `a`
- un angle entre les rayons `angle`
- un nombre de rayons `n`
- une couleur `col`
- une position initiale au centre du cercle

```{codeplay}
from turtle import *
getscreen().bgcolor('cyan')
speed(0)
up()

def soleil(d=100, a=100, angle=45, n=3, col='yellow'):
    color(col)
    dot(d)
    seth(180)
    down()
    width(10)
    for i in range(n):
        forward(a)
        backward(a)
        left(angle)
    up()

goto(100, 100)
soleil(80, a=400, n=10)
```

## Nuage

Dans ce projet, les nuages sont créés par 6 disques de taille aléatoire avec 2 niveaux de gris.

```{codeplay}
from turtle import *
from random import *
getscreen().bgcolor('cyan')
hideturtle()
up()

def nuage(taille):
    #Dessine un nuage avec une taille aléatoire
    for x in ("darkgray", "darkgray","lightgray") :
        taille = randint(2,4)
        dot(26*taille, x)
        forward(50)
    left(90)
    forward(30)
    left(90)
    forward(50)
    for i in range(3):
        taille = randint(2,4)
        dot(30*taille, "lightgray")
        forward(50)

nuage(100)
goto(-200, 0)
nuage(50)
```

La fonction `nuage()` possède un argument taille, mais cet argument n'a pas d'effet. La variable `taille` est remplacée par une valeur aléatoire dans l'intervalle [2, 4]. Voici ci-dessous cette fonction corrigée, pour créer des nuages de taille variable.

```{codeplay}
from turtle import *
from random import *
getscreen().bgcolor('cyan')
hideturtle()
up()

def nuage(taille):
    # Dessine un nuage avec une taille aléatoire
    seth(0)
    for x in ("darkgray", "darkgray","lightgray") :
        dot(taille * randint(2, 4), x)
        forward(1.7 * taille)
    left(90)
    forward(taille)
    left(90)
    forward(taille)
    for i in range(3):
        dot(taille * randint(2, 4), "lightgray")
        forward(1.8 * taille)

goto(-200, 0)
nuage(10)

goto(0, 0)
nuage(30)
```

## Arbre

La fonction `arbre_AP(angle)` (AP = arrière-plan):

- spécifie comme argument l'angle
- ne spécifie pas l'épaisseur du tronc
- ne permet pas de varier la taille
- laisse le stylo en position basse

```{codeplay}
from turtle import *

def arbre_AP(angle):
    # Dessine les arbres d'arrière-plan(=AP)
    color("sienna")
    right(angle)
    forward(30)
    dot(20, "green")
    up()
    backward(30)
    left(angle)
    color("limegreen")
    down()

arbre_AP(-90)
forward(100)
arbre_AP(-70)
forward(100)
arbre_AP(-50)
```

Une meilleure façon est de créer une fonction `arbre(h)` dont

- la direction est toujours verticale
- la taille (hauteur `h`) est un argument
- l'épaisseur du tronc et 0.2 fois la hauteur
- le diamètre du feuillage est 1.0 fois la hauteur
- qui laisse le stylo en position haute
- retourne au point de départ

```{codeplay}
from turtle import *
up()

def arbre(h):
    # Dessiner un abre de hauteur h
    color("sienna")
    down()
    width(0.2 * h)
    sety(ycor() + h)
    dot(1.0 * h, "green")
    up()
    sety(ycor() - h)

arbre(30)
forward(80)
arbre(60)
forward(120)
arbre(90)
```

## Montagne

La fonction `montagne_AP()`:

- n'a aucun argument
- dessine en arrière (de droite à gauche)
- nécessite deux fonctions supplémentaires (`colorier` et `replacement`)
- n'est pas réutilisable pour le premier plan (PP)

```{codeplay}
from turtle import *
speed(0)

def arbre_AP(angle):
    # Dessine les arbres d'arrière-plan(=AP)
    color("sienna")
    right(angle)
    forward(30)
    dot(20, "green")
    up()
    backward(30)
    left(angle)
    color("limegreen")
    down()

===
def montagne_AP():
    # Dessine les montagnes d'arrière-plan
    color("limegreen")
    begin_fill()
    down()
    width(5)
    left(38)
    for x in (100, 45, 150, 72):
        circle(x, 90)
        arbre_AP(128)
        forward(50)
        arbre_AP(128)
        circle(-x, 90)
        if x == 72:
            left(145)
        else:
            arbre_AP(38)

goto(300, 0)
left(90)
montagne_AP()
```

Une meilleure façon est de créer une fonction `montagne(h, rayons, couleur)` qui :

- accepte la taille des arbres `h`
- accepte une liste de rayons `rayons`
- accepte une couleur `couleur`
- mémorise le point de départ `p`
- descend vers -180
- mémorise une liste des positions des arbres
- dessine les arbres à ces positions
- peut être réutilisée pour le premier plan
- dessine de gauche à droite

```{codeplay}
from turtle import *
speed(0)
up()

def arbre(h):
    # Dessiner un abre de hauteur h
    color("sienna")
    down()
    width(0.2 * h)
    sety(ycor() + h)
    dot(1.0 * h, "green")
    up()
    sety(ycor() - h)
===
def montagne(h, rayons, couleur='lime'):
    arbre_pos = []
    p = pos() # memorize starting position
    fillcolor(couleur)
    begin_fill()
    seth(50)
    for r in rayons:
        circle(-r, 90)
        arbre_pos.append(pos())
        forward(50)
        arbre_pos.append(pos())
        circle(r, 90)
        arbre_pos.append(pos())
    sety(-180)
    setx(p[0])
    goto(p)
    end_fill()

    for p in arbre_pos[:-1]:
        goto(p)
        arbre(h)
        
goto(-280, 100)
montagne(30, (80, 50))
goto(-280, -50)
montagne(40, (80, 155, 150, 72), 'silver')
```

## Joueur

La fonction `joueur()` n'a aucun argument.

```{codeplay}
from turtle import *

def jambes():
    # Dessine les jambes du joueur
    left(45)
    width(5)
    forward(50)
    right(45)
    forward(50)
    backward(50)

def torse():
    # Dessine le torse du joueur
    left(90)
    width(10)
    forward(40)

def bras():
    # Dessine les bras du joueur
    width(3)
    right(135)
    forward(50)
    backward(50)
    left(270)
    forward(50)
    backward(50)
    right(45)

def tete():
    # Dessine la tête du joueur
    fillcolor("black")
    begin_fill()
    left(180)
    circle(20)
    end_fill()
    up()
    left(90)
    backward(40)
    left(135)
    forward(50)
    left(135)

def player():
    # Dessine le joueur
    jambes()
    torse()
    bras()
    tete()
    color("black")

player()
```

Une meilleure façon est de créer une fonction `joueur(a, bras, jambes, col)` qui :

- accepte la taille des membres `a`
- accepte une liste d'angles pour les `bras`
- accepte une liste d'angles pour les `jambes`
- accepte une couleur `col`

```{codeplay}
from turtle import *
up()

def member(angle, a):
    seth(270 - angle)
    width(a/10)
    forward(a)
    backward(a)

def player(a=50, bras=(45, 45), jambes=(45, 90), col='black'):
    color(col)
    down()
    seth(-90)
    width(a/5)
    dot(0.8 * a)
    forward(a/2)
    member(+bras[0], a)
    member(-bras[1], a)
    width(a/5)
    sety(ycor() - 0.8 * a)
    member(+jambes[0], a)
    member(-jambes[1], a)
    up()

player()
goto(180, 0)
player(70, bras=(80, 100), col='red')
```

## Mur

Nous utilisons la fonction `rectangle` pour dessiner un mur.
La fonction `mur(h, w, a, b)` dessine un mur avec h x w briques de taille a x b.

```{codeplay}
from turtle import *
speed(0)
up()

def rectangle(a, b, couleur='darkgoldenrod'):
    fillcolor(couleur)
    begin_fill()
    for x in (a, b, a, b):
        forward(x)
        left(90)
    end_fill()

def mur(h=5, w=1, a=150, b=50):
    # Mur de Brique qui forme la plateforme où le joueur peut se déplacer
    width(1)
    down()
    for j in range(w):
        for i in range(h):
            rectangle(a, b)
            sety(ycor()+b)
        sety(ycor() - h*b)
        forward(a)
    up()

goto(-280, -180)
mur()

goto(0, -180)
mur(5, 2, 80, 40)
```

## Piques

La fonction `piques()` dessine une série de 6 triangles de taille fixe.

```{codeplay}
from turtle import *
speed(0)
up()

def piques():
    # Dessine les piques
    fillcolor("gray")
    for i in range(6):
        begin_fill()
        for x in (60, 240, 240):
            left(x)
            forward(70)
        end_fill()
        backward(70)
        right(180)

goto(-200, -100)
down()
piques()
```

Une meilleure façon est de créer deux fonctions. Une fonction `triangle(a)` qui :

- peut être utilisé seul
- avec un côté `a``

et une fonction `piques(n, a)` qui répète le triangle `n` fois.

```{codeplay}
from turtle import *
speed(0)
up()

def triangle(a):
    begin_fill()
    for i in range(3):
        forward(a)
        left(120)
    end_fill()

def piques(n=6, a=70):
    down()
    fillcolor('gray')
    for i in range(n):
        triangle(a)
        forward(a)
    up()

goto(-200, -100)
piques()
goto(-200, -180)
piques(10, 40)
```

## Drapeau

La fonction `drapeau()` dessine un seul type de drapeau.

```{codeplay}
from turtle import *

def triangle_drapeau():
    # drap du drapeau
    fillcolor("red")
    begin_fill()
    right(120)
    forward(50)
    right(120)
    forward(50)
    right(120)
    forward(50)
    end_fill()
    backward(32)
    up()
    right(90)
    forward(5)
    color('black')
    write("WIN")

def baton_drapeau():
    # Baton du drapeau
    left(90)
    width(3)
    forward(100)

def drapeau():
    # Création du drapeau à atteindre
    baton_drapeau()
    triangle_drapeau()

drapeau()
```

Une meilleure façon est de créer une fonction `drapeau(h, a, col, text)` qui dessine un drapeau avec :

- une hauteur `h`
- un triangle de côté `a`
- de couleur `col`
- qui affiche `text`

```{codeplay}
from turtle import *

def triangle(a):
    begin_fill()
    for i in range(3):
        forward(a)
        left(120)
    end_fill()

def drapeau(h=100, a=50, col='red', text='WIN'):
    seth(90)
    down()
    forward(h)
    fillcolor(col)
    triangle(-a)
    backward(a/2)
    color('black')
    write(' '+ text)
    up()

drapeau()
goto(100, 0)
drapeau(150, 70, 'yellow', 'You loose')
```

## Plateforme

La fonction `plateforme_piques()` dessine deux plateformes fixes.

```{codeplay}
from turtle import *
hideturtle()

def plateformes_piques():
    # Plateformes qui se trouvent au-dessus des piques
    down()
    width(5)
    color("blue")
    forward(100)
    left(90)
    up()
    forward(70)
    right(90)
    forward(70)
    down()
    color("red")
    forward(100)
    up()

plateforme_piques()
```

Une meilleure façon est de créer une fonction `plateforme(col, a, w)` qui dessine une plateforme :

- de couleur `col`
- de longueur `a` et
- d'une épaisseur `w`

```{codeplay}
from turtle import *
hideturtle()
up()

def plateforme(col='red', a=100, w=5):
    down()
    width(w)
    color(col)
    forward(a)
    up()

plateforme()
goto(100, 50)
plateforme('blue')
goto(200, 100)
plateforme'lime')
```

Téléchargez le code source du projet réusiné {download}`project1b.py <code/projet1b.py>`