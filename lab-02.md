Lab 02 - Plastic waste
================
Charlotte Bouchard
15-09-2025

## Chargement des packages et des données

``` r
library(tidyverse) 
```

``` r
plastic_waste <- read_csv("data/plastic-waste.csv")
```

Commençons par filtrer les données pour retirer le point représenté par
Trinité et Tobago (TTO) qui est un outlier.

``` r
plastic_waste <- plastic_waste %>%
  filter(plastic_waste_per_cap < 3.5)
```

## Exercices

### Exercise 1

``` r
ggplot(plastic_waste, aes(x=plastic_waste_per_cap,)) +
  geom_histogram(binwidth=0.1) +
  facet_wrap(~continent)
```

![](lab-02_files/figure-gfm/plastic-waste-continent-1.png)<!-- -->

### Exercise 2

``` r
ggplot(plastic_waste, aes(x = plastic_waste_per_cap, colour=continent, fill = continent)) + 
  geom_density(alpha = 0.3)
```

![](lab-02_files/figure-gfm/plastic-waste-density-1.png)<!-- -->

Le réglage de la couleur est dans « aes » et le réglage de la
transparence est dans « geom_density » car le premier est selon chaque
variable (le mapping), alors que la transparence fixe la propriété pour
tout le graphique (le setting).

### Exercise 3

Boxplot:

``` r
# insert code here
```

Violin plot:

``` r
# insert code here
```

Réponse à la question…

### Exercise 4

``` r
# insert code here
```

Réponse à la question…

### Exercise 5

``` r
# insert code here
```

``` r
# insert code here
```

Réponse à la question…

## Conclusion

Recréez la visualisation:

``` r
# insert code here
```
