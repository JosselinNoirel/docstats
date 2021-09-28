La fonction diff()
================

## Fonction générale

`diff()` calcule la différence des éléments consécutifs contenus dans le
vecteur *V* qui lui est passé en argument

    diff(V)

Le résultat, si *V* contient *n* éléments, contient *n* − 1 valeurs.

## Exemples

Calculer le nombre de jours qui séparent des dates d’anniversaire:

``` r
n = 23
birthdays = sort(sample(1:365, size=n, replace=TRUE))
diff(birthdays)
```

     [1]  7  0 12 64  1  0 27 19  0 16 26 16  2 32 15 10  2 43  7 22 20  7

**NB** Nous ne tenons pas compte ici de la périodicité de l’année.

## Utilisation avancée

La fonction inverse de `diff()` est [cumsum](cumsum)().

**NB** TODO

Voir aussi les fonctions [sort](sort)().
