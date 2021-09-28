La fonction unique()
================

## Fonction générale

`unique()` retire toutes les occurrences redondantes des valeurs
contenue dans le vecteur *V* qui lui est passé en argument

    unique(V)

## Exemples

Combien de faces différentes obtient-on en lançant un dé six fois?

``` r
length(unique(sample(1:6, size=6, replace=TRUE)))
```

    [1] 3

Voir aussi la fonction [length](length)().
