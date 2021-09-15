La fonction `sum()`
================

**Fonction générale** La fonction `sum()` calcule la somme des éléments
qui composent le vecteur *x* qui lui est passé en argument.

    sum(x)

**Exemples**

-   `sum(1:10)` pour calculer 1 + 2 + ⋯ + 10

**Cas des expressions booléennes** Dans le cas d’expressions booléennes
comme `x - y + 1 < 0` faisant intervenir des vecteurs (*x*, *y*), le
[calcul vectorisé](calcul_vectorise) fait que la fonction `sum()`
s’applique à un vecteur de booléen dont la *i*-ième valeur donne la
valeur de vérité de l’expression
*x*<sub>*i*</sub> − *y*<sub>*i*</sub> + 1. Ce vecteur est converti en
vecteur numérique où les valeurs `TRUE` deviennent des 1 et les valeurs
`FALSE` des 0. Le résultat de l’opération `sum()` est donc le nombre de
fois que l’expression booléenne aura été vraie.
