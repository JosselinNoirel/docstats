La fonction sample()
================

## Fonction générale

Créer un échantillon (*sample*) aléatoire de taille *n* parmi les
éléments d’un ensemble *S*, qui peut être un intervalle d’entiers
\[*a*, *b*\] en utilisant la syntaxe `1:6` par exemple.

    sample(S, n, replace=bool)

Le booléen `bool` contrôle si l’échantillonnage se fait avec (`TRUE`) ou
sans remise (`FALSE`).

-   Avec remise (`replace=TRUE`), la fonction `sample()` réalise
    l’équivalent de *n* lancers de dé dont les faces seraient marquées
    avec les éléments de l’ensemble *S*.

-   Sans remise (`replace=FALSE`, l’option par défaut), la fonction
    `sample()` réalise l’équivalent du tirage de *n* boules dans une
    urne contenant des boules marquées avec les éléments de l’ensemble
    *S* (sans remise).

## Exemples

-   `sample(1:365, size=23, replace=TRUE)` : dans le paradoxe des
    anniversaires, choisir 23 dates d’anniversaires
-   `sample(c("H", "T"), size=10, replace=TRUE)` : dix lancers d’une
    pièce non truquée
-   `sample(1:6, size=8, replace=TRUE)` : huit lancers d’un dé non
    truqué avec

``` r
sample(1:365, size=23, replace=TRUE)
```

     [1] 179  14 195 306 118 299 229 244  14 153  90  91 256 197  91 348 137 355 328
    [20]  26   7 137 254

## Utilisation avancée

La fonction `sample()` admet un argument `prob` qui permet d’indiquer la
probabilité de tirer chaque élément de l’ensemble *S* (et contredire
l’équiprobabilité utilisée par défaut).

**NB** La fonction `sample()` produit des nombres pseudo-aléatoires qui
dépendent d’une graine aléatoire qui peut être initialisée avec
[set.seed](set.seed)().

Voir aussi les fonctions [anyDuplicated](anyDuplicated)() et
[replicate](replicate)().
