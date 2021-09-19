La fonction c()
================

## Fonction générale

La fonction `c()` est l’une des fonctions de base (rarement utilisée en
pratique, au cours de projets sérieux) pour créer des vecteurs « à la
main ».

## Exemples

Vecteurs numériques

    c()
    c(1) # Same as 1
    c(1, 2, 3) # Same as 1:3
    c(2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31) # Primes

Vecteurs de chaînes de caractères

    c('H', 'T') # Coin flipping

**NB 1** Un vecteur ne peut contenir qu’un type d’objet à la fois comme
le démontre l’exemple suivant :

``` r
c(1, 2, 'text')
```

    [1] "1"    "2"    "text"

**NB 2** D’autres opérateurs et fonctions permettent de créer des
vecteurs :

-   L’opérateur `:`
-   Les fonctions `seq()`, `seq_along()`, `seq_len()`
-   Les fonctions pseudo-aléatoires `sample()`
-   Les fonctions de réplication `replicate()`
-   Les fonctions de la famille d’`apply()`
-   Les fonctions permettant le [calcul vectorisé](calcul_vectorise)
