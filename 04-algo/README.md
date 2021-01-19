Exo Time .... Attrapes-moi si tu peux:woman_running::man_running: 
Contexte

On appelle graphe la donnée d'un ensemble de points appelés sommets et d'un ensemble de lignes appelées arêtes qui relient certains sommets entre eux.

Les bases

Le nombre de sommets d'un graphe s'appelle l'ordre du graphe.
 - Deux sommets reliés entre eux par une arête sont dits adjacents.
 - Le degré d'un sommet est le nombre d'arêtes issues de ce sommet.
 - Un sommet qui n'est adjacent à aucun autre sommet du graphe est dit isolé.

Un graphe est dit complet si deux sommets quelconques distincts sont toujours adjacents. Autrement dit, tous les sommets sont reliés deux à deux par une arête. Un graphe peut être orienté ou non-orienté. Dans un graphe orienté, chaque arête ne peut-être parcourue que dans un seul sens indiqué par une flèche. Un graphe (orienté ou non-orienté) peut contenir des boucles c'est-à-dire une arête dont l'origine et l'extrémité correspondent au même sommet (on a par exemple une boucle B sur la représentation précédente).

Posons le problème

Une possibilité pour représenter un graphe avec Python est d'utiliser un dictionnaire qui, à chaque sommet, associe un sous-dictionnaire composé de ses sommets adjacents associés à la pondération de l'arête incidente 

```
Graphe_ = { 
     'A':{'B':2, 'C':1}, 
     'B':{'A':2, 'C':2, 'D':1, 'E':3}, 
     'C':{'A':1, 'B':2, 'D':4, 'E':3, 'F':5}, 
     'D':{'B':1, 'C':4, 'E':3, 'F':6, 'G':5}, 
     'E':{'B':3, 'C':3, 'D':3, 'F':1}, 
     'F':{'C':5, 'D':6, 'E':1, 'G':2}, 
     'G':{'D':5, 'F':2} }
```
Ainsi Graphe'A' est le poids de l'arête incidente à A et B.

![alt text](./img/chemin-du-succes-500x375.jpg "Les gnocchis sont cuits")



Le parcours d'une telle structure permet de remplir ou vider deux dictionnaires. Le premier qui se remplira au fur et à mesure contiendra les sommets explorés (par exemple s_explore) et le second qui se videra au fur et à mesure contiendra les sommets à explorer (par exemple s_a_explorer).

Certains problèmes consistent à chercher entre deux points donnés le parcours qui a une "longueur" (durée, coût, distance) minimum.
Ces problèmes se ramènent à la recherche d'une chaîne ou d'un chemin de plus faible pondération entre deux sommets d'un graphe pondéré (les pondérations des arêtes étant toutes positives). On parlera de plus courte distance en interprétant les pondérations comme des distances entre les sommets.

1. Suivant le graphe (Graphe_) définit précédemment, écrire les fonctions permettant de parcourir tous les nœuds de ce graphe, décrire ce que fait réellement votre fonction.

2.Trouver 2 manière de parcourir un graphe de A à G. Quelle est la longueur de votre parcours

3. Proposer une fonction qui permet de passer en argument "de quel point à quel point" on souhaite aller et une fonction qui permet d'afficher par quel point l'algorithme est allé, et quelle distance le parcours de l'algorithme représente.

3. Un algorithme appelé "Dijkstra" permet de résoudre ce type de problème dans les graphes pondérés connexes et à pondérations positives. Implémenter cet algorithme.

## [Link to my work](./script-zone/algo_exo.ipynb)