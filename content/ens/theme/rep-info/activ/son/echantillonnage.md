# 3. Echantillonnage 

Classe : 1M, 2M

<span style="color:green">Difficulté : basique </span> 
<sup> [1](#myfootnote1)</sup>
    

## 3.1. Objectifs 

### 3.1.1. Objectif informatique

Le premier objet de cette activité est de permettre à l'élève d'appréhender la problématique de la représentation de l'information au sens large, comme le passage d'un univers symbolique à un autre.  
Il s'agit tout d'abord de passer d'un espace physique sensoriel (l'audition) à un autre espace sensoriel (la vue) et à la modélisation mathématique permettant de représenter ce phénomène acoustique : la représentation pseudo-sinusoïdale continue d'une onde sonore théorique, puis sa représentation numérique discrète.  
Ce premier travail intellectuel doit permettre aux élèves d'une part de se familiariser avec le matériau servant de support aux activités suivantes (quelques notions élémentaires relatives au son), et d'autre part de faciliter leur compréhension du changement de paradigme ultérieur entre l'espace physique (plutôt que mathématique) et l'espace numérique et le codage binaire de l'information.  

Le second objet de cette activité est de permettre aux élèves de se familiariser avec l'outil Audacity, ses fonctionnalités de visualisation graphique et de reproduction sonore, offrant deux modes de représentation du son.  
En particulier la notion de fréquence d'échantillonnage et le critère de Shannon, essentiel en traitement du signal, sont perçus visuellement et auditivement (découpage de l'onde sonore en une multitude de points et perception des effets de la fréquence d'échantillonnage sur la qualité du rendu).
    

### 3.1.2. Objectif mathématique et physique (transversal)

L'activité permet de réactiver, confirmer ou souligner des savoirs mathématiques relatifs aux relations fonctionnelles,  aux représentations dans le plan et à la trigonométrie.
L'activité permet de réactiver, confirmer ou souligner des savoirs mécaniques et physiques relativement aux ondes, à la notion de milieu de propagation, de période et de fréquence.
</br> </br>

## 3.2. Spécifications

### 3.2.1. Mode

**«Branché/débranché»** utilisation de l'ordinateur et du logiciel Audacity - pas d'environnement de développement.  Cette activité peut permettre de faire utiliser le tableur et ses fonctionnalités aux élèves et coïncider avec un enseignement de type bureautique - science informatique transversal.

### 3.2.2. Pré-requis  

- Informatique :
        <span style="color:green">utilisation de l'ordinateur et familiarisation avec l'environnement informatique
        </span> 
        
    
- Mathématique :
        <span style="color:orange">fonctions,</span>
        <span style="color:orange">fonctions trigonométriques simples,</span> 
        <span style="color:orange">notions d'amplitude, de période et de fréquence,</span> 
        <span style="color:green">représentation sur un repère plan,</span> 
        <span style="color:green">notion d'espace continu / discret</span> 
        
    
- Physique :
        <span style="color:orange">notion d'onde mécanique (pression, compression-dilatation) et sa représentation</span>    


### 3.2.3. Moments didactiques

 **1er moment didactique.** Mise en situation - Première séance (cours) - <span style="color:violet">45mn</span>
</br> **2ème moment didactique.** Exploration individuelle : chaque élève prend possession du matériel, des outils : ordinateur, environnement de travail, logiciel Audacity, matériel audio - Deuxième séance (activité proprement dite) - <span style="color:violet">15-25mn</span>
</br> **3ème moment didactique.** Moment technique et technologique : les élèves manipulent le programme Audacity, lancent les exécutions, manipulent les fenêtres graphiques (interfaces), observent les graphes et écoutent différentes portions de morceaux de musique (3 maximum) - <span style="color:violet">20-30mn</span>
</br> **4ème moment didactique.** Mise en commun et institutionnalisation : l'enseignant reprend la main au tableau et vidéoprojecteur. Examen des modes de représentation visuel et audio : sens, interprétation. Interprétation du visuel de la courbe sonore dilatée temporellement : la *discrétisation numérique* est mise en évidence. L'enseignant recueille de manière guidée les appréciations des élèves sur la qualité du morceau de musique écouté à différentes *fréquences d'échantillonnage*. Cette notion est simplement posée à ce stade, elle sera reprise et développée dans le temps suivant. Le recueil des appréciations concernant la qualité sonore peut être réalisé via un tableau où figurent en première ligne toutes les fréquences autour de la fréquence médiane 48000 Hz, et dans la ligne suivante la qualité perçue par les élèves : Mauvaise / Convenable / Bonne ; l'enseignant inscrit un segment (représentation au tableau) pour chaque choix de chaque qualité associée, ou travaille de préférence directement sur un [tableau excel](/tab/appqualson.ods) complété avec les retours élèves  - <span style="color:violet">20-30mn</span>
</br> **5ème moment didactique.** Travail sur la technique : les élèves sont laissés en autonomie une bonne partie du temps sur leurs postes de travail, expérimentent les outils et concepts institutionnalisés en manipulant les paramètres d'Audacity en fin de troisième séance - <span style="color:violet">15-25mn</span>
</br> **6ème moment didactique.** Evaluation. {download}`Devoir - évaluation maison de type quizz moodle<quizzech.ods>`  - <span style="color:violet">20-30mn</span>
</br>


### 3.2.4 Supports didactiques
    
Ordinateur individuel, logiciel Audacity, casque audio individuel connecté sur la sortie audio de l'ordinateur de chaque élève, documentation papier ou en ligne, supports papier pour la prise de notes. Ordinateur enseignant avec sortie audio (2 enceintes - stéréo), vidéoprojecteur, tableau.


### 3.2.5. Durée
La séquence d'enseignement se découpe en <span style="color:violet">trois séances de 45mn</span> : première période de <span style="color:violet">45mn</span> en classe entière, deux périodes suivantes de <span style="color:violet">45mn</span> en demi-classes.

</br> 

## 3.3. Déroulement

### 3.3.1. Première séance : éléments de cours sur l'information et le son en particulier

Cette première séance doit être vue comme une introduction à la problématique traitée par l'activité proprement dite. Elle est l'occasion de travailler la transdisciplinarité avec d'autres disciplines fondamentales (mathématiques, physique) mais également une discipline artistique, la musique.  
Elle peut donc s'effectuer en parallèle d'un de ces enseignements, en coordination avec un enseignant de ces disciplines : mathématiques, physique, ou musique.  
Les éléments mathématiques et physiques théoriques suffisants sont présentés dans cet ouvrage à la section 1.1 : Signal analogique (physique) temporel. L'enseignant peut également s'appuyer sur certains éléments de la section 1.2 Contenu fréquentiel (analyse spectrale).  
Une introduction sous l'angle de la musique pourra s'appuyer sur une approche instrumentale mettant en évidence les notions de hauteur (fréquence), de timbre (richesse harmonique), d'onde de pression transmise dans un espace matériel : ceci devra être fait en collaboration avec un enseignant de musique, avec le concours d'instruments divers : piano, flute, cordes, cuivres ou vents...  
</br>
Les éléments principaux à évoquer sont : 
    
- [L’oreille comme capteur](https://enseigner.modulo-info.ch/content/ens/theme/rep-info/support/son/visu-et-ecoute-son.html#Section1.1.2)

- Le son : [une onde sinusoïdale de compression-dilatation](https://enseigner.modulo-info.ch/content/ens/theme/rep-info/support/son/visu-et-ecoute-son.html#Section1.1.1)

- Notion de fréquence : nombre de battements par seconde. Nombre de fois où le signal redevient identique par seconde.

- Avec les fonctions python [**tracesinus**](#tracesinus) et [**listensinus**](#listensinus), l'enseignant affiche et fait écouter quelques exemples de sons «purs» (grave médium et aigu).

- L'enseignant ajoute ensuite plusieurs signaux sinusoïdaux avec la fonction python [**puresignalssum**](#puresignalssum)  : somme d’harmoniques écoutée et visualisée.

- À la fin de la première période : l'enseignant sensibilise les élèves à l'utilisation d'Audacity : ouverture du logiciel, écoute d'un ou plusieurs morceaux. Les élèves commencent à manipuler en toute fin de séance et s'exerceront concrètement au cours de la suivante.

*Problématique de la représentation :* fonction sinus, amplitude, fréquence, période. Rappels mathématiques et physiques sur les notions abordées : notion d'onde de pression, compression-dilatation, compréhension de la représentation graphique (sinus). L'enseignant traite rapidement la notion d'onde sonore comme la somme de «sons élémentaires».

</br>

### 3.3.2. Deuxième séance : activité proprement dite

**<span style="color:red">DE T0 À T1 = T0 + 30mn</span>**


</br>
<left> 
<html>
    <head>
        <title> audio1.mp3 </title>
    </head>
    <body>
        <div id="player">
        <audio controls>
        <source src="https://maitre.edunumsec2.ch/_videos/Audio1.mp3" type="audio/mpeg">
        </audio> 
        </div>
    </body> 
</html>     

```{figure} png/
---
alt:
width: 100%
align: left
---
**Ecoute d'un morceau de musique sur Audacity**
```

</br> </br>


```{figure} png/Im39.png
---
alt:
width: 100%
align: left
---
**Visualisation d'un morceau de musique sur Audacity**
```

</br> </br>
<left> 
<html>
    <head>
        <title> Util_Audacity.mov </title>
    </head>
    <body>
        <div id="player">
        <video width="500" height="300" controls>
        <source src="https://maitre.edunumsec2.ch/_videos/Util_Audacity.mov" type="video/quicktime">
        </audio> 
        </div>
    </body> 
</html>     

```{figure} png/
---
alt:
width: 100%
align: left
---
**Manipulation d'un morceau de musique sur Audacity**
```
</br> </br>

Les élèves travaillent de manière autonome, au casque individuel, les échanges sont limités. L'enseignant circule dans la classe et s'assure de l'appropriation des outils. Il revient au tableau régulièrement afin de dérouler les consignes : lancement d'Audacity, manipulation, écoute des différents morceaux, zoom. 

<br>

```{figure} png/Im38.png
---
alt:
width: 100%
align: left
---
```

```{figure} png/Im37.png 
---
alt:
width: 100%
align: left
---
```

```{figure} png/Im36.png
---
alt:
width: 100%
align: left
---
```

```{figure} png/Im35.png
---
alt:
width: 100%
align: left
---
**Zoom sur une partie du morceau visualisé sous Audacity : dilatation temporelle, composition fréquentielle.**
```
</br> </br>

1ère phase.
L'enseignant s'assure de la bonne compréhension des phénomènes : notions d'amplitude et de fréquence, dilatation temporelle, fréquences «visibles» des composantes du signal. En particulier, sur la dernière visualisation, on observe qu'on peut mettre en évidence une «quasi-période» entre les instants 0,8320 et 0,8345. Le calcul de la période donne donc 0,8345-0,8320 = 0,0025s, soit une fréquence de 1/0,0025 = 400Hz. L'enseignant questionne les élèves sur cette fréquence : est-elle basse ? haute ? L'enseignant s'appuie ensuite sur la génération d'un son «pur» à 400Hz, via les fonctions python **tracesinus**, **listensinus**. Par la visualisation et l'écoute, les élèves peuvent se représenter l'information extraite du fichier audio (composante de fréquence ~ 400Hz), puis comprendre ce qui se passe quand on ajoute plusieurs signaux à différentes fréquences (ici un signal de fréquence fondamentale 400Hz, puis ses 4 harmoniques suivantes : 800, 1200, 1600, 2000Hz) quand l'enseignant utilise la fonction python **puresignalssum**.

<a name="tracesinus"></a>

```
from __future__ import print_function
import math
import numpy as np
import matplotlib.pyplot as plt
from pyo import *
from tkinter import Tk, StringVar, Label, Entry, Button, Frame, DoubleVar, Spinbox
from functools import partial

def tracesinus(freq):
#  sinus function at freq(Hz) frequency
    t = np.arange(0., 0.01, 0.00005)
    plt.plot(t,np.sin(2*pi*freq*t))
    label1 = "fonction sinus, fréquence " 
    label2 = str(freq) 
    label3 = "Hz"
    label = label1 + label2 + label3 
    plt.ylabel(label)
    plt.show()

tracesinus(400)
   ```

<a name="listensinus"></a>   
```
from __future__ import print_function
import math
import numpy as np
import matplotlib.pyplot as plt
from pyo import *
from tkinter import Tk, StringVar, Label, Entry, Button, Frame, DoubleVar, Spinbox
from functools import partial

def listensinus(freq):
#  sinus function at freq(Hz) frequency
   s = Server().boot()
   s.start()
   a = Sine(freq, mul=1, add=0).out()
   time.sleep(5)
   s.stop()

listensinus(400)   
   ```

<a name="puresignalssum"></a>   
```
from __future__ import print_function
import math
import numpy as np
import matplotlib.pyplot as plt
from pyo import *
from tkinter import Tk, StringVar, Label, Entry, Button, Frame, DoubleVar, Spinbox
from functools import partial

def puresignalssum(freq, harmo):
#  harmonic signals
   s = Server().boot()
   somme = 0
   for i in range (1,harmo+1):
      s.start()
      a = Sine(i*freq, mul=1, add=0).out()
      time.sleep(1)
#  graphic vizualisation       
      namesc = 'Signal '+str(i*freq)+' Hz'
      somme=somme+a
   s.stop
   sc = Scope(somme, 0.003, 0.2, wintitle='somme des signaux')
   somme.out
   s.gui(locals())

puresignalssum(400, 5)   

```

</br>

**<span style="color:red">DE T1 À T2 = T1 + 15mn = T0 + 45mn</span>**


2ème phase.
L'enseignant poursuit le zoom sur le signal et questionne les élèves sur l'interprétation de ce qu'ils voient. Il les amène progressivement à la compréhension de la notion de *discrétisation*, résultat du passage d'une représentation continue *apparente* correspondant à la **réalité physique** à une représentation discrète *réelle* correspondant à la **réalité numérique**.



```{figure} png/Im40.png
---
alt:
width: 100%
align: left
---
```

```{figure} png/Im41.png
---
alt:
width: 100%
align: left
---
**Zoom sur une partie du morceau visualisé sous Audacity : mise en évidence de la discrétisation.**
```

</br> </br>

### 3.3.3. Troisième séance : activité proprement dite - fin

**<span style="color:red">DE T0 À T1 = T0 + 20mn</span>**


3ème phase. 
L'enseignant propose aux élèves d'écouter une partie du morceau de musique choisi aux différentes fréquences proposées par Audacity, de 8000 à 384000 Hz. 

```{figure} png/Im55.png
---
alt:
width: 100%
align: left
---
**Ecoute à différentes fréquences d'échantillonnage sous Audacity.**
```

Après une dizaine de minutes d'écoute autonome, l'enseignant questionne les élèves sur ce qu'ils ont écouté et sur leur interprétation des fréquences indiquées - <span style="color:violet">10-15mn</span>.

</br> </br>

**<span style="color:red">DE T1 À T2 = T1 + 25mn = T0 + 45mn</span>**

L'enseignant met ensuite en commun et institutionnalise : il reprend la main au tableau et vidéoprojecteur. Examen des modes de représentation visuel et audio : sens, interprétation. Interprétation du visuel de la courbe sonore dilatée temporellement : la *discrétisation numérique* est mise en évidence. L'enseignant recueille de manière guidée les appréciations des élèves sur la qualité du morceau de musique écouté à différentes *fréquences d'échantillonnage*. Cette notion est simplement posée à ce stade, elle sera reprise et développée dans le temps suivant. Le recueil des appréciations concernant la qualité sonore peut être réalisé via un tableau où figurent en première ligne toutes les fréquences autour de la fréquence médiane 48000 Hz, et dans la ligne suivante la qualité perçue par les élèves : Mauvaise / Convenable / Bonne ; l'enseignant inscrit un segment (représentation au tableau) pour chaque choix de chaque qualité associée, ou travaille de préférence directement sur un {download}`fichier de type excel<appqualson.ods>` complété avec les retours élèves. 

```{figure} png/tabexcel.png
---
alt: Exemple de tableau excel enseignant récoltant les appréciations par les élèves de la qualité sonore de l'échantillon.
width: 100%
align: left
---
**Exemple de tableau excel enseignant récoltant les appréciations par les élèves de la qualité sonore de l'échantillon.**
```


Une fois le tableau complété, il est projeté : l'enseignant questionne les élèves sur l'interprétation qu'ils peuvent donner des graphes issus du tableau de données. Il doit faire ainsi ressortir la qualité perçue à partie de la fréquence d'échantillonnage de 44100Hz. La nécessité d'une *fréquence d'échantillonnage minimale* doit ici apparaître.
Dans un deuxième temps, l'enseignant interroge sur les résultats pour les fréquences supérieures. L'inutilité d'aller au-delà d'une certaine fréquence (en l'occurence 44100 Hz) doit ressortir.
L'étape suivante consiste à identifier cette valeur de 44100 Hz : à quoi correspond-elle ? L'enseignant revient sur le champ audible par l'oreille humaine : 20Hz - 20000Hz... Il situe alors 44100Hz par rapport à la fréquence la plus élevée que peut percevoir l'oreille humaine, 20000Hz... La fréquence d'échantillonnage apparaît comme devant être au moins égale au double de cette fréquence de 20000Hz.
En dernier lieu, l'enseignant revient sur la notion même de fréquence d'échantillonnage. Que signifie-t-elle ? C'est le nombre d'échantillons pris par unité de temps. L'enseignant illustre son propos par le dernier visuel de la figure 4 : entre les temps 6,8310s et 6,8315s, on dénombre à peu près 23 échantillons, soit 23/0,0005 = 46000Hz. On retrouve quasiment la fréquence 44100 Hz apparaissant en bas à gauche de la fenêtre Audacity - <span style="color:violet">15-20mn</span>.

```{figure} png/Im41.png
---
alt:
width: 100%
align: left
---
**Identification de la fréquence d'échantillonnage (ici 44100Hz).**
```

### 3.3.4. Evaluation : quizz moodle maison

L'évaluation pourra être réalisée via un quizz moodle open-book, en temps limité (<span style="color:violet">20-30mn</span>) créé par l'enseignant, et comportant 10-15 questions tirées du fichier excel {download}`Devoir - évaluation maison de type quizz moodle<quizzech.ods>`.
L'enseignant pourra également programmer un cycle d'entrainement préliminaire avec une partie des questions proposées dans ce fichier excel.




<br/>
<br/>
<br/>