---
title: Introduction aux principes SOLID en programmation orientée object
subtitle: Comment écrire du code propre, maintenable et extensible ?
category:
  - Les principes SOLID
author: Eddine Omar
date: 2020-01-04T18:00:00.00Z
featureImage: /uploads/marc-olivier-jodoin-nqoinj-ttqm-unsplash.jpg
---

# Introduction

En informatique, plus précisément en programmation orientée objet, les principes **SOLID** regroupent des principes qui aide le développeur à mieux concevoir son programme et *in fine* permettent d'écrire du code orienté objet, **tolérant au changement, fiable, robuste et évolutif. Du qualitatif en résumé, et nous les dev on aime beaucoup le qualitatif !**

Ces principes ont été popularisés par *Robert C. Martin* (également connu sous le pseudonyme Uncle Bob) dans son livre *Agile Software Development : Principles, Patterns, and Practices*

L'acronyme SOLID englobe les principes suivants :
* **S**ingle Responsibility principle ou principe de responsabilité unique
* **O**pen/Closed principle ou principe ouvert/fermé
* **L**iskov substitution ou substitution de Liskov
* **I**nterface segregation principle ou principe de ségrégation des interfaces
* **D**ependency inversion principle ou principe d'inversion des dépendances

# SOLID

## Single Responsibility Principle
"A class should have one reason to change."

Une classe ou une méthode ne devrait avoir qu'une seule raison de changer, autrement dit une classe ou une methode ne doit avoir qu'une seule responsabilité.

C'est le principe le plus connu : cela rend le code plus clair et le rend surtout mieux testable !

Illustration : j'ai une machine à faire des gauffres. Si cette machine fait des gauffres ET des crêpes, alors cette machine a plusieurs respnsabilité. Et donc ce c'est pas une machine à faire des gauffres uniquement, mais une machine à faire des gauffres et des crêpes !

Généralement, il suffit d'expliquer ce que fait sa classe à voix haute et de ne pas rajouter de *ET* ou de *OU* dans l'énoncé.


## Open/Closed Principle
"Classes, methods should be open for extension, but closed for modifications."

Une classe ou une méthode devrait être ouverte à l'extension et fermée à la modification. 

L'idée est de ne pas toucher à ce qui fonctionne, mais plutôt étendre si besoin.
Pour ce faire on peut utiliser les solutions suivantes :
* [Polymorphisme](https://www.wikiwand.com/fr/Polymorphisme_(informatique))
* [Abstraction](https://www.wikiwand.com/fr/Abstraction_(informatique))
* [Héritage](https://www.wikiwand.com/fr/H%C3%A9ritage_(informatique))
* [Surcharge](https://www.wikiwand.com/fr/Surcharge_de_fonction)

## Liskov Substitution Principle
"Subtypes must be substituable for their base types."

Une instance d'une classe de base peut être remplacée par une instance d'une classe dérivée sans que cela ne modifie la cohérence du programme.

Pour cela, une classe dérivée ne doit pas modifier les valeurs des attributs de la classe mère, et doit également respecter le contrat défini par la méthode.

Le principe de substitution de Liskov est lié à la programmation par contrat.

Par exemple : une classe `Carré` peut hériter d'une classe `Rectangle`, en effet un carré possède les mêmes attributs qu'un rectangle (longueur, largeur, position, nombre de côté, angles droit) mais avec quelques spécificités.

## Interface Segregation Principle
"Clients should not be forced to depend on methods that they do not use."

Les clients ne devraient pas être forcés à dépendre des méthodes dont ils n'utilisent pas.

Afin de réduire les couplages dans notre code, nous allons préférer utiliser un style de programmation par contrat plutôt que de rajouter de l'abstraction à nos classes. Pour ce faire nous devrions utiliser des interfaces spéficiques pour chaque client.

Exemple 1 : 
* Chaque constructeur de smartphone présentera une interface adaptée pour son appareil (soit USBC, microUSB ou autre) et c'est à l'utilisateur d'utiliser le bon chargeur pour recharger charger son smartphone.
* L'inverse aurait été que chaque smartphone soit compatible avec tous les types de chargeurs (microUSB, USBC, thunderbolt...), ce afin que chaque smartphone s'adapte à un utilisateur.

Il existe donc une sorte de contrat entre le constructeur et l'utilisateur qui définit l'interface permettant de recharger son smartphone.

## Dependency Inversion Principle
"High level modules should not depend on low level modules. Both should depend on abstractions."

Enfin le dernier principe qui est celui de l'injection de dépendance. Il stipule que l'on devrait dépendre des abstractions et non des implémentations.

Il s'agit de découpler les modules haut-niveau et les modules bas-niveau.

Illustration : lorsqu'on exécute la commande `ping google.fr`, celle-ci fonctionnera notamment si nous sommes connectés à internet (quelque soit la manière dont nous sommes connectés à internet : en câble, par réseau mobile, en wifi via bluetooth ou en USB tethering).

# Conclusion

Les principes SOLID aident à mieux architecturer un projet informatique lorsqu'ils sont compris et bien appliqués.
Et vous connaissiez-vous ces principes ? Les utilisez-vous au quotidien ? Dites-le moi en commentaire ci-dessous.

Inscrivez-vous à la newsletter pour ne rater aucun article.

------------------------------------------

Sources :
* https://essential-dev-skills.com/poo/principe-solid
* https://www.wikiwand.com/fr/SOLID_(informatique)
* http://blog.ezoqc.com/5-exemples-faciles-pour-comprendre-les-principes-solid/
* https://www.wikiwand.com/fr/Programmation_orient%C3%A9e_objet#/overview
