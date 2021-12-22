# Répéter - `for`

Un programme exécute souvent certaines instructions multiples fois. Dans ce cas une boucle permet de rendre le code plus court et mieux structuré.
Une boucle ne représente pas seulement une économie de lignes de code, mais donne en plus la possibilité de contrôler facilement le nombre de répétitions.

En Python nous avons deux types de boucle :

- la boucle `for` pour parcourir un ensemble de valeurs,
- la boucle `while` pour répéter pendant qu'une condition est vraie.

## Répéter x fois

Le programme suivant demande comme entrée le nombre `x` de sommets, et dessine alors un polygone régulier. C'est un cas ou il faut **répéter x fois**.

```{codeplay}
from turtle import *

x = input('Nombre de sommets: ')
x = int(x)

for i in range(x):
    forward(50)
    left(360/x)
```

**Exercice** : Testez avec des nombres différents entre 3 et 13.

## Itérer x fois

Le mot **itérer** veut dire parcourir un ensemble un par un. Dans la boucle `for` une variable d'itération va parcourir un ensemble qui peut être :

- une plage numérique avec `range()`
- une chaîne de caractères
- une liste

La **variable d'itération** prend successivement les valeurs 0 à x-1.
Quand la variable d'itération est de type entier (`int`) on l'appelle souvent `i`.

Nous reprenons l'exemple précédent du polygone, mais cette fois nous dessinons pas les segments mais seulement les sommets. La valeur de la variable d'itération `i` est affichée à chaque sommet du polygone.

```{codeplay}
from turtle import *

x = int(input('Nombre de sommets: '))
up()

for i in range(x):
    forward(50)
    left(360/x)
    dot()
    write(i, font=(None, 12))
```

**Exercice** : Testez avec des nombres différents entre 5 et 13.

## Itérer avec `range()`

La fonction `range(start, stop, step)` permet de produire une séquence linéaire d'entiers. Les entiers se trouvent dans l'intervalle semi-fermé `[start, stop[` avec un incrément de `step`.

Le sens des paramètres :

- `start` est la valeur de départ
- `stop` est la valeur finale, mais sans l'inclure
- `step` est l'incrément

```{codeplay}
start = int(input('start = '))
stop = int(input('stop = '))
step = int(input('step = '))

for i in range(start, stop, step):
    print(i, end=' ')
```

**Exercice** : Affichez les entiers entre 100 et 200 avec un incrément de 3.

La fonction range fonctionne aussi dans l'ordre décroissant. Dans ce cas il faut choisir pour `step` une valeur négative.

```{codeplay}
for i in range(-100, -200, -3):
    print(i, end=' ')
```

**Exercice** : Affichez les entiers de +10 à -10.

La fonction `range()` peut fonctionner avec 1, 2 ou 3 paramètres. Les valeur par défaut sont :

- 0 pour `start`,
- 1 pour `step`.

```{codeplay}
from time import sleep

for i in range(10):
    print(i, end=' ')
    sleep(0.1)
print()

for i in range(10, 20):
    print(i, end=' ')
    sleep(0.1)
print()

for i in range(10, 100, 7):
    print(i, end=' ')
    sleep(0.1)
```

## Itérer sur une chaîne

La ligne de code `for c in mot:` signifie que la variable `c` va prendre à chaque répétition un caractère différent de la chaîne `mot`.

Quand la variable d'itération est un caractère on l'appelle souvent `c`.

```{codeplay}
from time import sleep
mot = input('Entrez un mot: ')

for c in mot:
    print(c)
    sleep(0.1)
```

**Exercice** : Testez avec différents textes.

## Itérer sur une liste

La ligne de code `for color in colors:` signifie que la variable `color` va prendre à chaque répétition un élément différent de la liste `colors`.

Quand on itère sur une liste la convention est d'utiliser un mot au pluriel pour la liste (`colors`) et le même mot en singulier pour la variable d'itération (`color`).

```{codeplay}
from turtle import *

colors = ['hotpink', 'lime', 'beige', 'pink']
left(120)
speed(1)

for color in colors:
    getscreen().bgcolor(color)
    write(color, font=(None, 18))
    forward(50)
```

**Exercice** : Ajoutez d'autres couleurs à la liste.

## Dessiner une spirale

Si nous dessinons un polygone mais augmentons la longueur de chaque segment successif en utilisant la variable d'itération `i`, nous obtenons une spirale.

```{codeplay}
from turtle import *

for i in range(100):
    forward(i)
    left(30)
```

## Du polygone au cercle

Plus que le polygone régulier a de sommets, plus il ressemble à un cercle.
Avec 36 sommets, il ressemble déjà raisonnablement à un cercle.

```{codeplay}
from turtle import *

def polygon(n, a):
    for i in range(n):
        forward(a)
        left(360/n)

polygon(36, 10)
```

## La fonction `circle(r)`

La fonction `circle(r)` dessine un cercle de rayon `r`.
Le cercle est dessiné :

- vers la gauche si r est positif,
- vers la droite si r est négatif.

```{codeplay}
from turtle import *

forward(50)
circle(40)
forward(100)
circle(-30)
forward(100)
```

**Exercice** : Inversez le signe du rayon.

Cette fonction peut avoir un deuxième paramètre sous la forme `circle(r, angle)`
ou `angle` représente l'angle du cercle dessiné.
Par défaut c'est 360°, donc un cercle entier.

Voici un exemple qui utilise deux demi-cercles de 180°.

```{codeplay}
from turtle import *

forward(100)
circle(40, 180)
forward(50)
circle(-30)
forward(50)
circle(40, 180)
```

**Exercice** : Dessinez un bonhomme de neige et utilisez `dot()` pour les yeux.

## Dessiner une fleur

Dessinons des cercles dans une boucle, et tournons à chaque fois.

```{codeplay}
from turtle import *

n = 6
for i in range(n):
    circle(50)
    left(360/n)
```

Il est également possible d'imbriquer des cercles en faisant varier le rayon dans une boucle `for` avec une expression `range()`.

```{codeplay}
from turtle import *

for r in range(20, 100, 20):
    circle(r)
```

**Exercice** : Dessinez les cercles empilés les uns sur les autres.

## Deux boucles imbriquées

Dans Excel, les cellules sont désignées avec une lettre et un nombre. 
Pour recréer les noms de cellule nous itérons dans une chaîne de chiffres et une deuxième fois dans une chaîne de lettres.

On appelle la première boucle avec `y` la **boucle extérieure** et la deuxième boucle avec `x` **la boucle intérieure**. 

Nous concaténons les deux éléments lettre et nombre (`x + y`) et nous ajoutons l'option `end=' '` pour remplacer le retour à la ligne par une espace.

Pour bien montrer l'ordre consécutif nous importons la fonction `sleep()` du module `time` pour ralentir le parcours de la boucle.

```{codeplay}
from time import sleep

for y in '1234567':
    for x in 'ABCDEFG':
        print(x + y, end=' ')
        sleep(0.1)
    print()
```

**Exercice** : Transformez le code pour afficher 20 colonnes de cellules.