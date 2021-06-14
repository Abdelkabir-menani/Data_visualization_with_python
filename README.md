# Data visualization sur Tips dataset:

## I. Introduction :

Le but de notre étude est dans un premier temps de mener une étude statistique sur les variables explicatives, après on essaie de chercher s’il y’a des dépendances entre le montant de la facture et le montant du pourboire avec les autres variables significatives respectivement. Enfin, on étudie la dépendance entre le montant de la facture et le montant du pourboire.

Durant cette présentation, on essaie à chaque fois d’ajouter des graphiques ou des tableaux significatives en les commentant qui nous permet de bien comprendre les données et les dépendances de nos variables.

## II. Résultats intermédiaires :

### 1. Etude statistique sur les variables :

On dispose une dataset composée de « 244 » enregistrements. Chaque ligne comporte un ensemble d’informations (Facture, Pourboire, sex, Fumeur, Jour_semaine, soir_jour,
nb_personne) de la facture. Voici quelques lignes du fichier « pourboire.txt » :

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image1.png)

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image2.png)

Le tableau en haut présente quelques lignes de notre Dataset. Dans l’ensemble des données il y a 7 variables significatives (Facture, Pourboire, sex, Fumeur, Jour_semaine, soir_jour, nb_personne). On remarque aussi qu’on dispose des variables quantitatives et d’autres qualitatives. Variables qualitatives comme la variable « sex » qui est une variable qualitative ordinale (M, F) qui représente le sexe du client qui a payé la facture soit femme(F) soit homme(M). Des variables quantitatives comme la variable « Facture » qui représente le montant de la facture en dirhams.

Donc, on est déjà entrain de construire une idée sur la structure de base de nos données.
Maintenant nous allons faire une étude statistique descriptive sur la base de données.

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image3.png)

Le tableau ci-dessus récapitule les principales statistiques descriptives qui nous permet de bien comprendre nos données. En gros, il y a 244 valeurs valides pour toutes les variables de la Dataset. La moyenne indique les bornes inférieur et supérieur des valeurs des variables de la Dataset considérons par exemple la variable facture : le montant minimal des factures est de 27.02 dirhams et le montant maximal est de 447.13 dirhams. Les valeurs du max et du min des variables semblent naturelles alors on déduit la justesse et la bonne récupération de notre dataset. L’écart-type (std) de la variable facture est très élevé 78.34. Cela signifie que les prix sont très dispersés par rapport à la moyenne, en d’autres termes, si on assume qu’on a une distribution normale, la majorité des montants des factures (95% de notre dataset plus précisément) sont inclus dans l’intervalle [17.44,330.8].

Après qu’on a effectué une petite analyse de statistiques descriptives sur nos données enfin de les bien comprendre, on passe maintenant à la représentation graphique à chacune de nos variables afin que nous ayons une compréhension de la distribution de chaque variable dans l&#39;ensemble de données.

## Sex :

Sex est une variable qualitative nominale qui représente le sexe du client qui a payé la facture soit homme ou femme. L’objectif d’étudier cette variable c’est pour savoir la tendance de donner des pourboires à travers le sexe des clients ce qui va différer sans doute.

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image4.png)

On constate qu’un grand pourcentage des clients de ce restaurant (64.34%) sont masculin et 35.66% des clients sont féminin.

## Fumeur :

Fumeur est une variable qualitative booléene qui représente l’emplacement de la table était elle dans la zone fumeur.

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image5.png)
![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image6.png)

On remarque que 151 des clients (62.13%) sont non-fumeurs de ce restaurant et le reste des clients sont probablement des fumeurs qui ont réservé des tables dans la zone fumeur.

## Jour_semaine :

Jour_semaine est une variable qualitative nominale qui indique le jour de la consommation du client dans le restaurant.

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image7.png)

On constate que parmi les 244 enregistrements des factures des clients du restaurant qu’on a, les jours de la semaine où les factures ont été payé sont « ‘Jeudi’, ’Vendredi’, ’Samedi’, ’Dimanche’ ». Le restaurateur a choisi ces jours particuliers de la semaine lors de cette étude peut-être parce qu’ils sont les jours de la semaine où il reçoit beaucoup de clients, donc automatiquement il sera intéressé de l’étude de ces jours.

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image8.png)

L’histogramme ci-dessus est un countplot qui calcule la fréquence de chaque jour de la semaine qu’on a dans les enregistrements dans notre dataset. On remarque que le samedi est
le jour qui a enregistré le plus de factures suivies par le dimanche, ce qui est logique puisque dans les jours du weekend, les personnes ont tendance à sortir pour manger ailleurs puisqu’ils sont des jours fériés.

## Soir_jour :

Soir_jour est une variable qualitative nominale qui indique le moment de la consommation du client soit soirée (soir) ou journée (jour).

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image9.png)
![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image10.png)

D’après l’histogramme et le tableau ci-dessus, on aperçoit que les clients de ce restaurant consomment fréquemment dans la soirée de la journée (72% des factures ont été effectué dans les soirées).

## Nb_personne :

Nb_personne est une variable quantitative discrète qui représente le nombre de personne ayant consommé dans le restaurant.

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image11.png)

On constate que parmi les 244 enregistrements des factures des clients du restaurant que le nombre des personnes qui ont consommé est compris entre 1 est 6.

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image12.png)

L’histogramme ci-dessus montre que le nombre de personne le plus fréquent qui consomme dans ce restaurant est 2 suivis de 3 et 4 avec des fréquences égales. Ça peut nous
donner une idée sur le type de la clientèle du restaurant, puisque les personnes viennent au restaurant soit en couple ou avec un nombre limité de personnes donc il n’est pas un
restaurant familial mais c’est un restaurant où les amis se rencontrent.

## Pourboire :

Pourboire est une variable quantitative continue qui représente le montant du pourboire en dirham payé par le client.

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image13.png)

La plupart des montants des pourboires sont compris entre 10 et 35 dirhams qui est un montant assez bien pour un montant de pourboire dans un restaurant marocain.

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image14.png)
![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image15.png)

On remarque que la valeur minimale du montant des pourboires est 8.6 dirhams et la valeur maximale est égale à 86, Le médian est 25.79, et on a Q2=24.94 signifiants que 50%
des pourboires ont un montant inférieur à 24.94 dh. Q1=17.2, c’est-à-dire que 25% des pourboires ont un prix inférieur à 17.2 dh. Q3=30.64, c’est-à-dire que 75% des pourboires ont un prix inférieur à 30.64 dh.

## Facture :

Facture est une variable quantitative continue. C’est l’un des deux variables les plus importantes lors de notre étude de cet ensemble de données. Il représente le montant de la
facture en dirham. Les autres variables dont nous avons discuté peuvent influencer dramatiquement sur la hausse ou la baisse de ce montant.

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image16.png)

D’après cet histogramme en haut qui une valeure de skewness positive, on remarque que plus que la moitié des factures en des montants compris entre 100 et 200 dirhams. On
remarque que plus les montants dépassent 200 dirhams la fréquence diminue et cela reste vrai pour les factures ayant des montants entre 25 et 100 dirhams.

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image17.png)

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image18.png)

On constate que la valeur minimale du montant des factures est 27.02 dirhams et la valeur maximale est égale à 447.13, Le médian est 174.12, et on a Q2=156.6 signifiants que 50% des factures ont un montant inférieur à 156.6 dh. Q1=117.46, c’est-à-dire que 25% des factures ont un prix inférieur à 117.46 dh. Q3=212.32, c’est-à-dire 75% des factures ont un prix inférieur à 212.32 dh.

Cependant, il est très difficile bien comprendre ces deux variables précédentes à savoir le prix et la facture. Donc, il s’avère important de savoir les variables parmi notre dataset qui influencent sur la variation de ces deux variables. C’est l’objectif de la partie suivante de notre analyse.

### 2. Dépendances entre Facture et les autres caractéristiques :

#### a) Avec la variable Sex :

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image19.png)

Puisqu’on a déjà vu que +60% des clients qui payent les factures sont des hommes, on peut déduire que les hommes par le principe de la société tendent à payer la facture plus que la femme, de plus on pourrait clairement voir que les factures les plus chères sont payés par les hommes. Alors, plus la facture est chère, plus il est fort probable que l’homme qui va la payer et vice versa.

#### b) Avec la variable Fumeur :

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image20.png)

Dans le diagramme du violinplot ci-dessus, on remarque que pour les tables qui existent dans la zone fumeur les montants des factures sont distribués plus également en comparaison avec les factures des tables dans la zone non-fumeur avec des probabilités très élevé pour les montants des factures entre 100 et 200. De plus, les factures des tables dans la zone fumeur ont une probabilité un peu élevée de commander des factures avec des montants plus qu’environ 325 dh et moins que 75 dirhams.

#### c) Avec la variable Jour_semaine :

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image21.png)

La distribution des montants des factures par jour est un peu semblable pour chaque jour avec des nuances différentes. On aperçoit que la probabilité que les montants des factures soient plus chers que 250 dh est plus élevé pour les factures effectuées dans les jours du weekend à savoir le samedi et le dimanche que les autres jours.

#### d) Avec la variable Soir_jour :

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image22.png)

Depuis le diagramme des bloxplot ci-dessus, on remarque que les factures avec les montants les plus chères ont été commandé le soir. Donc ces factures chères ont une probabilité élevée d’être effectué le soir.

#### e) Avec la variable Nb_personne :

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image23.png)

D’après le diagramme précédent, on constate que plus que le nombre de personnes dans la table augmente, le montant minimale des factures augmentent et cela est totalement normal
puisque qui dit un nombre élevé de personnes pour la même facture dit plus de consommation d’où une facture chère.

##### Bilan :

D’après ce qui précède, la variable facture a des dépendances avec des degrés différentes avec toutes les autres variables à savoir : Sex, Fumeur, jour_semaine, soir_jour,
nb_personne. Ensuite, on passe à l’étude des dépendances de la variable pourboire avec les autres caractéristiques.

### 3. Dépendances entre Pourboire et les autres caractéristiques :

#### a) Avec la variable Sex :

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image24.png)

On remarque que les hommes ont tendance de donner des sommes des pourboire plus chère que les femmes.

#### b) Avec la variable Fumeur :

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image25.png)

Ce tableau montre que les personnes non-fumeurs ont tendance à donner du pourboire plus que les personnes qui consomment dans la zone fumeur.

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image26.png)

D’après le boxplot ci-dessus, on remarque que les deux boxplots ont à peu près les mêmes caractéristiques de la médiane et des interquartiles. D’où la variable Fumeur qui indique l’emplacement de la table soit dans la zone fumeur ou non-fumeur n’influence pas sur le montant des pourboires donnés aux serveurs de ce restaurant.

#### c) Avec la variable Jour_semaine :

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image27.png)

On constate que pour les jours du weekend « Samedi, dimanche » le nombre des pourboires données aux serveurs du restaurant est plus grand en comparant aves les autres jours. Cela peut être justifié que lorsque les amis sortent dans le weekend, ils ont l’air plus généreux que pendant la semaine puisque les promenades dans cette période de la semaine est probablement planifiée.

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image28.png)

On remarque que le jour du samedi qui a enregistré des sommes très chères en comparant avec les autres jours.

#### d) Avec la variable Soir_jour :

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image29.png)

On aperçoit que la médiane des montants des pourboires données au soir est plus grand que celui du jour. De plus, les personnes ayant consommé au soir enregistrent des sommes des pourboires maximales.

#### e) Avec la variable Nb_personne :

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image30.png)

D’après le diagramme précédent, on constate que plus que le nombre de personnes dans la table augmente, plus le montant des pourboires augmente et cela est logique puisque qui dit un nombre élevé de personnes pour la même facture dit qu’il y’a plus de chance du don des
pourboires avec des sommes plus importantes. 

##### Bilan :

D’après ce qui précède, la variable Pourboire a des dépendances avec des degrés différentes avec toutes les autres variables à savoir : Sex, Fumeur, jour_semaine, soir_jour,
nb_personne.

Enfin, on passe à l’étude des dépendances entre la variable facture et pourboire.

### 4. L’étude de la dépendance entre la variable Pourboire et Facture :

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image31.png)

D’après la matrice de corrélation, on aperçoit qu’il y’a une forte corrélation entre la variable Facture et le montant du pourboire.

![image.png](https://github.com/Abdelkabir-menani/Data_visualization_with_python/blob/main/Images/image32.png)

La combinaison nuage de point et histogramme ci-dessus nous permet d’identifier la distribution du nuage de points des pourboires en fonction des montants des factures tout en
indiquant la nature de la dépendance entre ces deux variable, qui se voit claire qu’il y’a une forte corrélation positive, plus le montant de la facture augment plus le montant du pourboire augmente.

## III. Conclusion finale :

Pour améliorer ses revenus, un restaurateur peut travailler à améliorer plusieurs variables qui peuvent mener au client à consommer plus et en même temps à donner plus de montants des pourboires à ces serveurs. C’est dans ce sens qu’inscrit notre étudie le montant des factures et des pourboires avec les autres caractéristiques de la consommation.

Notre DataSet contient les informations sur 244 factures en fonction de 7 variables quantitatives et qualitatives. La plupart des factures ont été effectué par des hommes dans la soirée du weekend en couple dans la zone non-fumeur.

On a constaté que la variable facture et pourboire dépend de toutes les autres caractéristiques avec des degrés différentes. Les hommes ont tendance à donner des montants de pourboires chères plus que les femmes et ce sont-ils aussi qui payent les chères consommations. Les personnes qui commandent dans les tables fumeur ont une probabilité plus importante de payer une facture chère que celles qui existent dans des sones non-fumeurs, cependant les personnes non-fumeurs ont tendance à donner du pourboire plus que les personnes qui consomment dans la zone fumeur. Les personnes qui vont au restaurant le weekend et plus particulièrement le samedi ont tendances à commander des factures et de donner des montants de pourboire plus chère que dans les autres jours. De plus, les personnes qui vont au restaurant le soir ont les mêmes tendances. Enfin, plus le nombre de personnes dans la table augmente plus le montant de la facture augmente et le montant des pourboires aussi.

En ce qui concerne la relation entre le montant de la facture et le montant des pourboires, on a trouvé qu’il y’a une forte corrélation entre ces deux variables l’augmentation de l’un signifie une forte probabilité de l’augmentation de l’autre.
