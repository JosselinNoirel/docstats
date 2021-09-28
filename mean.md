La fonction mean()
================

## Fonction générale

La fonction `mean()` calcule la moyenne arithmétique des valeurs
contenues dans le vecteur *V* qui lui est passé en argument

    mean(V)

Quand ce vecteur est issu d’un processus aléatoire répété un très grand
nombre de fois *R* →  + ∞, on peut identifier cette moyenne à
l’espérance mathématique.

## Exemple

Distance moyenne entre les deux anniversaires les plus proches dans un
groupe de *n* = 23 personnes:

``` r
R = 100000
n = 23
sims = replicate(R, {
    birthdays = sample(1:365, size=n, replace=TRUE)
    birthdays = sort(birthdays)
    min( diff(birthdays),
        (birthdays[1] + 365) - birthdays[n])
})

mean(sims)
```

    [1] 0.63521
