La fonction table()
================

## Fonction générale

`table()` dénombre les occurrences des valeurs contenue dans le vecteur
*V* qui lui est passé en argument

    table(V)

## Exemples

On peut lancer (virtuellement) un dé *R* = 100 fois et compter le nombre
de uns, de deux, etc., de la façon suivante

``` r
R = 100
throws = sample(1:6, size=R, replace=TRUE)
table(throws)
```

    throws
     1  2  3  4  5  6 
    19 15 18 11 16 21 

Les fréquences peuvent être obtenues en divisant le résultat par *R*

``` r
table(throws)/R
```

    throws
       1    2    3    4    5    6 
    0.19 0.15 0.18 0.11 0.16 0.21 

Voir aussi la fonction [sample](sample)().
