class: center, middle

# Introduction à Python

.left[Intervenant : Jean-Christophe Gay]

.left[Mail : jean-christophe.gay@dauphine.fr]

.left[Bureau : B038]

---

name: plan

# Plan du cours

1. [Introduction](#Introduction)
2. [Premiers pas avec Python](#fisrtSteps)
3. [Utilisation de Python en Quelques Lignes](#name: UsingPythonAsCalculator)

???

3. Structures de Données
4. Nombres Aléatoires
5. Chaînes de caractères
6. Parsing Web
7. Gestion de Documents
8. Automatisation de tâches
9. Préparation des Projets 

---

name: Introduction

# Introduction

Jean-Christophe Gay :
- mail: jean-christophe.gay@dauphine.fr
- Bureau: B038 (de temps en temps et surtout le matin)

Expérience :
- 5 ans de développement en laboratoire
- 5 ans de développement pour l'Université Paris-Dauphine

???

Parler de
- Responsable du Pôle Infrastructure et Intégration
- RSSI de l'université Paris-Dauphine
- Docteur en Informatique

---


# Notes et examens

Réalisation d'un projet au choix dans une liste. Le projet sera l'unique moyen 
d'évaluation de ce cours.

---

name: whatIsPython

# Qu'est-ce que Python ?



---

name: firstSteps

# Premiers pas en Python

???

- Pourquoi Python ?

- Python 2.7.13 ?7?
- Python 3.6.0 ???

- Installation

- Lancer Python et le quitter
---

name: whyPython

# Premiers pas en Python

.left-column[
### Pourquoi Python ?
]
.right-column[
- Nous vivons dans un monde d'information
- Il y a beaucoup trop d'informations disponible à un moment donné
- Il faut un moyen de réduire l'information, particulièrement l'information financière
]
---

# Premiers pas en Python

.left-column[
### Pourquoi Python ?
]
.right-column[
- Python est gratuit ;
- Python est puissant, flexible et simple à apprendre ;
- Python est plus adapté au Big Data que R ;
- Python se compose de nombreux modules.
]
---
name: PythonVersion

# Premiers pas en Python

.left-column[
### Pourquoi Python ?
### Version de Python ?
]
.right-column[
- Il existe deux versions concurrentes de python : 2.7 et 3.6
- Les différences majeures sont :
 - print 'Hello World' fonctionne en version 2 mais pas en 3
 - les divisions entières sont différentes
 - plus sur
   [http://sebastianraschka.com/Articles/2014_python_2_3_key_diff.html](http://sebastianraschka.com/Articles/2014_python_2_3_key_diff.html)
- Pour ce cours les différences ne seront pas très importantes.
]

---
name: InstallingPython

# Premiers pas en python

.left-column[
### Pourquoi Python ?
### Version de Python ?
### Installation de Python
]
.right-column[

## Procédure d'installation :
- Se rendre sur le site de Python : [www.python.org](www.python.org)
- Section "Download" puis "Windows"
- Choisir l'installer qui convient
]
---

name: InstallingPython

# Premiers pas en python

.left-column[
### Pourquoi Python ?
### Version de Python ?
### Installation de Python
]
.right-column[

## Procédure d'installation :
- Se rendre sur le site de Python : [www.continuum.io](www.continuum.io)
- Section "Download" puis "Windows"
- Choisir l'installer qui convient

]
---
name: fisrtLaunch

# Premiers pas en python

.left-column[
### Lancement de l'interpréteur
]
.right-column[

Dans un "terminal" lancer la commande python.

Cet interpréteur peut être utilisé pour lancer des commandes python et ainsi réaliser des calculs. Nous allons essayer rapidement.

]

---

# Premiers pas en python

.left-column[
### Lancement de l'interpréteur
### Une premiere opération
]
.right-column[

Dans l'interpréteur :

```python
>>> 1 + 1
2
>>> a = 1
>>> print a
1
>>> a + 2
3
```
]

---

# Premiers pas en python

.left-column[
### Lancement de l'interpréteur
### Une premiere opération
### On quitte
]
.right-column[

Dans l'interpréteur :

```python
>>> quit
Use quit() or Ctrl-D (i.e. EOF) to exit
>>> quit()
```
]

---

name: secondLaunch

# Une première utilisation de Python

Si nous estimons qu'un retour de 100€ est attendu au bout d'un an avec 
une remise annuelle de 10%. La valeur actuelle d'une rentrée future d'argent
est la suivante :

$$PV = { FV \over (1+R)^n }$$

Dans cette équation PV représente la valeur présente et FV la valeur 
future, R est la remise et n le nombre de périodes.

Quelle est la valeur actuelle ?

```python
>>> 100 / (1 + 0.1)
```
---

# Une première utilisation de Python

Si nous estimons qu'un retour de 100€ est attendu au bout d'un an avec 
une remise annuelle de 10%. La valeur actuelle d'une rentrée future d'argent
est la suivante :

$$PV = { FV \over (1+R)^n }$$

Dans cette équation PV représente la valeur présente et FV la valeur 
future, R est la remise et n le nombre de périodes.

Quelle est la valeur actuelle ?

```python
>>> 100 / (1 + 0.1)
90.9090909090909090
>>>
```

---

# Une première erreure

Que se passe-t-il pour la prochaine période ?
```python
>>> 100 / (1+0.1)^2
```

---

count: false

# Une première erreure

Que se passe-t-il pour la prochaine période ?
```python
>>> 100 / (1+0.1)^2
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
* TypeError: unsupported operand type(s) for ^: 'float' and 'int'
>>>
```

En Python il faut utiliser '\*\*' et non '^' pour les puissances.

---
count: false
# Une première erreure

Que se passe-t-il pour la prochaine période ?
```python
>>> 100 / (1+0.1)^2
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
* TypeError: unsupported operand type(s) for ^: 'float' and 'int'
>>>
```

En Python il faut utiliser '\*\*' et non '^' pour les puissances.

```python
>>> 100 / (1+0.1)**2
82.64462809917354
```
---

# Attention à la case !

```python
>>> x=2
>>> X
```

---
count: false
# Attention à la case !

```python
>>> x=2
>>> X
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
*NameError: name 'X' is not defined
>>>
```
--


Lorsque l'on nomme des variables ou des fonctions il faut faire attention à la
case que l'on utilise. En effet Python est sensible à la case.

---

# Type des variables

En Python les variables n'ont pas de type propre. Elles ont le type de la
valeur qu'elles contiennent.

```python
>>> x = 2
>>> x
2
*>>> # x est un entier
>>> x="aa"
>>> x
'aa'
*>>> # x est une chaîne de caractères
>>>
```

---

name: findingHelp

# Trouver de l'aide

Facile : on en demande

```python
>>> help()

Welcome to Python 2.7!  This is the online help utility.

If this is your first time using Python, you should definitely check out
the tutorial on the Internet at http://docs.python.org/2.7/tutorial/.

Enter the name of any module, keyword, or topic to get help on writing
Python programs and using Python modules.  To quit this help utility and
return to the interpreter, just type "quit".

To get a list of available modules, keywords, or topics, type "modules",
"keywords", or "topics".  Each module also comes with a one-line summary
of what it does; to list the modules whose summaries contain a given word
such as "spam", type "modules spam".

help>
```
---

# Trouver de l'aide

```python
help> keywords

Here is a list of the Python keywords.  Enter any keyword to get more help.

and                 elif                if                  print
as                  else                import              raise
assert              except              in                  return
break               exec                is                  try
class               finally             lambda              while
continue            for                 not                 with
def                 from                or                  yield
del                 global              pass                

help> 
```
---
# Trouver de l'aide en ligne

* Google + Stackoverflow
* Python Site
* Tutoriels divers...

---

# Version de Python

* Avec un terminal :
** python --version
** python -V
* Avec Python
```python
>>> import sys
>>> print sys.version
2.7.12 (default, Nov 19 2016, 06:48:10)
[GCC 5.4.0 20160609]
```

---

# Exercices

* Trouver l'aire d'un disque de diamètre 10 cm ;
* Trouver la longueur de la diagonale d'un carré de côté 1 ;
* Quelle est la circonférence d'un champs trapézoidal dont les côté font 127
  mètres chacuns ?

---

count: false

# Solutions

- Exercice 1
```python
>>> aire=3.141592653*10**2
>>> aire
314.1592653
>>>
```
--
- Exercice 2
```python
>>> diag=2**0.5
>>> diag
1.4142135623730951
```
--
- Exercice 3
```python
>>> 127 + 127 + 127 + 127
508
```
---

name: UsingPythonAsCalculator
# Utilisation de Python en Quelques Lignes
<br/>
## Jouons avec les variables
## Le module mathématique
## Quelques fonctions utiles
## Les tuples

---

# Utilisation de Python en Quelques Lignes

.left-column[
### Jouons avec les variables
]
.right-column[
* On assigne des valeurs aux variables :
```python
>>> a = 1
>>> aa = 'Salut'
>>> b = 2
>>> a + b
3
```

* Afficher le contenu d'une variable :
```python
>>> a
1
>>> aa
'Salut'
>>> print a
1
>>> print aa
Salut
```
]

---

# Utilisation de Python en Quelques Lignes

.left-column[
### Jouons avec les variables
]
.right-column[
* Quelques erreurs :
```python
>>> aaa
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
*NameError: name 'aaa' is not defined
```
```python
>>> sqrt(1)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
*NameError: name 'sqrt' is not defined
```
]

---

# Utilisation de Python en Quelques Lignes

.left-column[
### Jouons avec les variables
]
.right-column[
* Du nommage des variables
```python
>>> # Mauvais exemple
>>> x = 100
>>> y = 0.1
*>>> z = x / ( 1 + y )
>>> print "Le résultat est", z
Le résultat est 90.9090909091
```
```python
>>> # Bon exemple
>>> FV = 100
>>> R = 0.1
*>>> PV = FV / ( 1 + R )
>>> print "Le résultat est", PV
Le résultat est 90.9090909091
```
]

---

# Utilisation de Python en Quelques Lignes

.left-column[
### Jouons avec les variables
]
.right-column[
Introspection
```python
>>> dir
['__builtins__', '__doc__', '__name__', '__package__']
```

dir() permet d'accèder à l'ensemble des nom définis à un instant

```python
>>> a = 1
>>> dir()
['__builtins__', '__doc__', '__name__', '__package__', 'a']
```

dir(a) permet d'avoir les fonctions applicable à a :
```python
>>> type(a)
<type 'int'>
>>> dir(a)
['__abs__', '__add__', '__and__', '__cmp__',  ...
'denominator', 'imag', 'numerator', 'real']
```
]

---

# Utilisation de Python en Quelques Lignes

.left-column[
### Jouons avec les variables
]
.right-column[
Suppression d'une variable
```python
>>> dir
<built-in function dir>
>>> dir()
['__builtins__', '__doc__', '__name__', '__package__']
>>> maVariable=1
>>> dir()
['__builtins__', '__doc__', '__name__', '__package__', 'maVariable']
>>> del(maVariable)
>>> dir()
['__builtins__', '__doc__', '__name__', '__package__']
```
]

---

# Utilisation de Python en Quelques Lignes

.left-column[
### Jouons avec les variables
### Le module mathématique
]
.right-column[
* Les opérations de base
```python
>>> # Addition
>>> 1 + 1
2
>>> # Soustraction
>>> 1 - 2
-1
>>> # Multiplication
>>> 2 * 2
4
>>> # Divisions
>>> 3 / 2
1
>>> 3 / 2.
1.5
>>> 3//2.
1.0
>>> int(2.5)
2
```
]

---

# Utilisation de Python en Quelques Lignes

.left-column[
### Jouons avec les variables
### Le module mathématique
]
.right-column[
* Plus de mathématiques, le module
```python
>>> dir()
['__builtins__', '__doc__', '__name__', '__package__']
>>> import math
>>> dir()
[... , 'math']
>>> dir(math)
['__doc__', '__name__', '__package__', 'acos', 'acosh',
... , 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'trunc']
>>> math.pow(2,2)
4.0
```
]

---

# Utilisation de Python en Quelques Lignes

.left-column[
### Jouons avec les variables
### Le module mathématique
]
.right-column[
* Plus de mathématiques, le module

```python
>>> help(pow)
Help on built-in function pow in module __builtin__:

pow(...)
    pow(x, y[, z]) -> number
    
    With two arguments, equivalent to x**y.  With three arguments,
    equivalent to (x**y) % z, but may be more efficient (e.g. for longs).

>>> pow(3,10,4)
1
>>> 3**10
59049
>>> 59049%4
1

```
]

---

# Utilisation de Python en Quelques Lignes

.left-column[
### Jouons avec les variables
### Le module mathématique
]
.right-column[
* Choisir la précision
```python
>>> 3/7.
0.42857142857142855
>>> payement=3/7.
>>> pay2=round(payement,4)
>>> pay2
0.4286
```
* Mais attention...
```python
>>> payement*pow(10,6)
428571.4285714285
>>> pay2*pow(10,6)
428600.0
```
]

---

# Utilisation de Python en Quelques Lignes

.left-column[
### Jouons avec les variables
### Le module mathématique
]
.right-column[
* e, Pi, log et exp
```python
>>> math.e
2.718281828459045
>>> math.pi
3.141592653589793
>>> math.log(math.e)
1.0
>>> math.log(math.exp(2))
2.0
```
]

---

# Utilisation de Python en Quelques Lignes

.left-column[
### Jouons avec les variables
### Le module mathématique
### Une note sur import
]
.right-column[
* import math
```python
>>> dir()
['__builtins__', '__doc__', '__name__', '__package__']
>>> import math
>>> dir()
[..., 'math']
```

* from math import
```python
>>> dir()
['__builtins__', '__doc__', '__name__', '__package__']
>>> from math import pow
>>> dir()
['..., 'pow']
>>> from math import *
>>> dir()
['...', 'acos', 'acosh', 'asin', 'asinh', 'atan',
..., 'sqrt', 'tan', 'tanh', 'trunc']
```
]

---

## Les tuples




---

# Programmation Fonctionnelle

- Une première fonction
- Notre propre module
- Un peu de mathématiques
- Utilisation de notre module

---

name: ToDo

# A suivre...

???

# Introduction aux modules

# Premier code depuis un fichier

# Fonctions classes et méthodes

# Automate the boring stuff with python

# A la marge :
Git
GitHub

---

# Bibliographie

- Python for Finance, Yuxin Yan, PACK, date ?
- Automate the boring stuff with Python
- Python for Finance, O'Reilly
- Mettre au moins un autre livre

---

# Some Code Inside

Code:

```python
def add(a,b):
    return a + b
```

---
count: false

# Some Code Inside

Code:

```python
def add(a,b):
*   return a + b
```

Notice the return statement

---

# Display and Inline

1. This is an inline integral: `\(\int_a^bf(x)dx\)`
2. More `\(x={a \over b}\)` formulae.

Display formula:

$$e^{i\pi} + 1 = 0$$

 