---
title: Fizz Buzz
subtitle: "FizzBuzz : un exercice devenu classique mondial en programmation"
category:
  - Interview questions
author: Eddine Omar
date: 2020-01-16T18:00:00.00Z
featureImage: /uploads/marc-olivier-jodoin-nqoinj-ttqm-unsplash.jpg
---
# Introduction
Il s'agit initialement un jeu pour apprendre aux enfants la division : assis autour d'un cercle, ils comptent l'un après l'autre et prononcent Fizz Buzz selon les règles décrites dans le paragraphe suivant.

Dans le monde de la tech, il s'agit d'un exercice simple qui permet de vérifier qu'un aspirant développeur possède des pré-requis pour postuler à un job. Cet exercice est souvent utilisé pour filter les développeurs de part sa trivialité. Une contrainte temporelle est éventuellement utilisée (15 min), une disqualification ayant lieu au delà du temps imparti, l'énoncé étant 'trivial'.

Dans cet article, je vais vous apprendre à résoudre ce problème en Python et en Javascript.

# Énoncé

```
Prenons N un entier étant égal à 20 (libre à vous de faire varier cet entier).
Pour chaque entier `i` allant de 1 à N-1 :
  - Si `i` est divisible par 3 alors on affiche `Fizz`.
  - Si `i` est divisible par 5 alors on affiche `Buzz`.
  - Si `i` est divisible par 3 **et** par 5 alors on affiche `Fizz Buzz`.
  - Sinon nous affichons le nombre `i`.
```

Comme vous le voyez, l'énoncé est plutot simple et il y a plusieurs manière de le résoudre.

Soulignons quelques points importants :
 1) Nous allons utiliser l'opérateur `modulo` (symbole %) : si `x % y == 0` cela signifie que `x est divisible par y`, sinon x n'est pas divisible par y. Cela signifie également que le reste de la division euclidienne de x par y est égale à 0.
  2) Nous utiliserons également la structure if-elsif afin de ne pas évaluer deux fois une des conditions de l'énoncé.
  3) Enfin nous utiliserons une disjonction de cas, c'est à dire que nous allons évaluer i%3 et i%5 et enfin décider selon les deux résultats.

# Diagramme de séquence
Voici le diagramme de séquence de l'algorithme dont nous allons implémenter.
![Diagramme de séquence FizzBuzz](/uploads/FizzBuzz.png  "Title")
# Implémentation
## Python
```code
N=20
for i in range(20):
  if i%3 == 0 and i%5 == 0:
    print("FizzBuzz")
  elif i%3 == 0 and i%5 != 0:
    print("Fizz")
  elif i%3 != 0 and i%5 == 0:
    print("Buzz")
  else:
    print(i)
```
## Javascript
```js
const N = 20
for (i = 1; i < N; i++) {
    if (i % 3 == 0 && i % 5 == 0) {
        console.log("FizzBuzz")
    } else if (i % 3 == 0 && i % 5 != 0) {
        console.log("Fizz")
    } else if (i % 3 != 0 && i % 5 == 0) {
        console.log("Buzz")
    } else {
        console.log(i)
    }
}
```
# Résultats
Les deux implémentations renvoient le résultat ci-dessous et sont strictement identiques.

```sh
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
16
17
Fizz
19
```


# En savoir plus
## FizzBuzz
* [Le Fizz Buzz le test d'embauche à la mode](https://nouvelle-techno.fr/actualites/le-fizz-buzz-le-test-dembauche-a-la-mode)
* [Fizz_Buzz (page Wikipedia)](https://www.wikiwand.com/en/Fizz_buzz)

## Diagramme UML
* [PlantUML](https://plantuml.com/) : un outil qui permet de décrire des diagrammes UML avec du texte.
* [Diagramme d'activité PlantUML](https://plantuml.com/activity-diagram-beta)

# À vous !

N'hésitez pas à donner vos avis dans les commentaires ou à y partager vos implémentations/améliorations.
