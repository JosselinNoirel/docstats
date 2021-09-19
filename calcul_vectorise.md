Calcul vectorisé
================

## Principe général

Le calcul vectorisé (en anglais *Array programming*) permet de manière
transparente de généraliser un certain nombre d’opérations (et de
fonctions) à des séquences de valeurs en procédant terme à terme.

Ce comportement peut se retrouver dans certains langages (mais pas
tous) : Matlab, Mathematica, etc. Python ne pratique pas le calcul
vectorisé mais la bibliothèque scientifique NumPy, elle, en tire un
grand profit.

Ainsi, si *x* est un vecteur de 10 valeurs numériques, on pourra
calculer `2 * x + 1` car R comprendra tout seul que l’opération
*a* ↦ 2 × *a* + 1 doit être accomplie pour toutes les valeurs de *x*. Le
résultat sera un vecteur de 10 valeurs contenant toutes les valeurs
2 × *x*<sub>*i*</sub> + 1.

Cela se généralise avec des opérations impliquant non pas un vecteur et
des valeurs scalaires mais aussi des opérations impliquant plusieurs
vecteurs. Ainsi l’expression `x + y` calculera-t-elle terme à terme les
valeurs *x*<sub>*i*</sub> + *y*<sub>*i*</sub> et `x + y/z` les valeurs
*x*<sub>*i*</sub> + *y*<sub>*i*</sub>/*z*<sub>*i*</sub>.

![](./figures/figures.001.png)

## Exemples

``` r
x = sample(1:10)
y = sample(1:10)
(x - y)/(x + y)
```

     [1] -0.538  0.333 -0.200  0.000  0.714  0.385 -0.714 -0.125 -0.167  0.333
