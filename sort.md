La fonction sort()
================

## Fonction générale

La fonction `sort()` trie (numériquement) son argument.

## Exemples

-   `sort(sample(1:10, size=3))` : tirer trois boules (sans remise)
    d’une urne de 10 boules et les trier par ordre croissant

-   `sort(sample(1:52, size=13))` : tirer treize cartes et les trier par
    ordre croissant

-   Vérifier visuellement la présence d’un anniversaire commun dans une
    liste de 23 anniversaires

``` r
b = sample(1:365, size=23, replace=TRUE)
sort(b)
```

     [1]   7  14  14  26  90  91  91 118 137 137 153 179 195 197 229 244 254 256 299
    [20] 306 328 348 355

``` r
anyDuplicated(b)
```

    [1] 9

Voir aussi [sample](sample)() et [anyDuplicated](anyDuplicated)().
