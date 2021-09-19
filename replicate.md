La fonction replicate()
================

## Fonction générale

Puisque la probabilité s’interprète comme une fréquence lorsque le
nombre *R* de réplications de l’expérience aléatoire tend vers l’infini
(*R* → ∞), il est important dans le cadre des simulations de pouvoir
répéter une expérience aléatoire pour en tirer des fréquences.

La fonction `replicate()` permet de faire ceci à l’aide de la syntaxe :

<pre>
replicate(<span class='meta'>replicates</span>, {
    <span class='meta'>simulation</span>
})
</pre>

La dernière ligne du corps de la simulation situé entre les accolades
`{...}` est celle qui renvoie un résultat. La fonction `replicate()`
retourne un vecteur (une liste) des valeurs constituées de ce résultat
pour chacune des réplications.

## Exemples

-   Simuler 100 pièces de 23 personnes pour obtenir des statistiques sur
    les anniversaires communs dans des groupes constitués de 23
    personnes.

``` r
replicate(100, {
    b = sample(1:365, size=23, replace=TRUE)
    anyDuplicated(b)
})
```

      [1]  9 15  0  0  0  0  0 17 12  0  0  0 12 21 17 21  0  0 15  0 10  0 17 11  0
     [26]  0  0  0  0  0  0  0  0  0  0 21 22 23 15  0 22  0  3 23  0  0  0 20 16 19
     [51]  0 21  0  0  0 17  0  3  0 21 18 23 19  0  0 15  0 17 18  8 21  0  0 23 16
     [76] 16 19 13  0 15  8  2 23 12 18  0  0 19  0  7 20  0  8 15  0  0  0 19 10  0

**NB 1** Dans le cadre de ce cours, le nombre de réplications sera
souvent enregistré dans une variable `R`.

**NB 2** Si le deuxième argument de `replicate()` ne dépend pas d’une
expérience pseudo-aléatoire, alors la réplication ne servira à rien car
c’est le même calcul qui sera fait un grand nombre de fois.
