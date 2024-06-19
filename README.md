# Approches variationnelles pour l'analyse des séquences génomiques évolutives
### Amine Remita, Ph.D.

Ma thèse de doctorat en informatique porte sur la classification des séquences nucléotidiques, la modélisation évolutive des données génomiques et l'inférence bayésienne des paramètres phylogénétiques. Ces domaines de l'analyse des séquences biologiques revêtent une importance cruciale pour notre compréhension de la diversité biologique et de l'évolution des espèces, d'autant plus dans le contexte actuel de la génomique où la quantité croissante de données génétiques nécessite des méthodes et des outils avancés. Plus concrètement, ces disciplines trouvent des applications essentielles dans l'annotation fonctionnelle et structurelle des génomes, la métagénomique pour explorer la diversité microbienne, la détection des pathogènes, la surveillance épidémiologique, notamment lors de pandémies telles que l'influenza et la COVID-19, la conception de vaccins et de médicaments, ainsi que la prédiction des résistances aux médicaments.

Au cours de cette thèse, j'ai eu l'opportunité de soumettre trois articles scientifiques qui ont été acceptés et publiés dans des conférences de grande envergure au sein de la communauté de la bioinformatique et de la phylogénétique. De plus, j'ai réalisé des présentations orales ainsi que des présentations par affiches.

## 1. Modèles statistiques linéaires pour la classification sans alignement des génomes de virus
La classification des séquences virales est confrontée à des défis en raison de leur complexité intrinsèque, notamment en raison des phénomènes de recombinaison et des taux de mutation élevés, qui engendrent une grande diversité génomique.
De plus, les nouvelles générations de technologies de séquençage posent d'autres difficultés en générant d'importantes quantités de séquences fragmentées.
Dans ce travail, nous présentons une évaluation et une discussion des performances des modèles d'apprentissage statistique linéaire pour la classification des séquences virales en utilisant une représentation basée sur les *k*-mers.
Plusieurs variables sont prises en compte dans cette évaluation, telles que les types de classifieurs (génératifs et discriminatifs) et leurs hyperparamètres, la tâche de classification (génotypage et sous-typage), la longueur des séquences testées (partielle et complète) et la longueur des *k*-mers.

Ce travail a été publié lors de la conférence *IEEE International Conference on Bioinformatics and Biomedicine* en 2019 sous le titre : **Statistical Linear Models in Virus Genomic Alignment-free Classification: Application to Hepatitis C Viruses**.
La rédaction de l'article, la conception et la mise en place des modèles et du cadre d'évaluation, ainsi que l'exécution des expérimentations ont été réalisées par Amine Remita sous la supervision du professeur Abdoulaye Baniré Diallo.

Le code source supportant cette étude est encapsulé dans le package [`slm_kgenomvir`](https://github.com/maremita/slm_kgenomvir). 
Dans un travail ultérieur, qui n'a pas encore été publié, nous avons mené une évaluation des différentes stratégies de régularisation de la régression logistique multinomiale pour la classification des virus génomiques en utilisant les *k*-mers. 
Le code soutenant cette recherche, [`mlr_kgenomvir`](https://github.com/maremita/mlr_kgenomvir), a été développé en collaboration avec Nicolas de Montigny, étudiant à la maîtrise en informatique.

## 2. Modèles génératifs variationnels profonds pour l'estimation des paramètres évolutifs
Dans ce travail, nous présentons `EvoVGM`, un modèle génératif bayésien variationnel et profond conçu à l'estimation des paramètres évolutifs. 
`EvoVGM` rapproche la distribution postérieure des paramètres évolutifs tout en générant des alignements de séquences. 
En particulier, ce modèle est adapté aux modèles de substitution de chaîne de Markov en temps continu tels que \tb{JC69}, \tb{K80} et \tb{GTR}. 
L'approche de modélisation est validée sur des données synthétiques et appliquée à l'alignement de séquences du gène S des coronavirus. 
Les résultats démontrent la précision et la robustesse de `EvoVGM` dans l'estimation des paramètres évolutifs.

Les résultats préliminaires de cette étude ont été présentés lors des conférences *ISMB/ECCB* et *SMBE* en 2021.
Le travail complet de ce chapitre a été publié lors de la conférence *the 13th ACM International Conference on Bioinformatics, Computational Biology and Health Informatics, Association for Computing Machinery* en 2022 sous le titre : **`EvoVGM`: a Deep Variational Generative Model for Evolutionary Parameter Estimation**.
De plus, une version abrégée de l'article a été acceptée et présentée à l'atelier  *The 2022 ICML Workshop on Computational Biology* de la conférence *International Conference on Machine Learning* en 2022 sous le titre **Toward Inferring Ancestral States and Evolutionary Parameters using a Variational Generative Model for Multiple Sequence Alignments**.
La rédaction de l'article, la conception et la mise en place des modèles et du cadre d'évaluation, ainsi que l'exécution des expérimentations ont été réalisées par Amine Remita sous la supervision du professeur Abdoulaye Baniré Diallo.

Le code source soutenant cette étude est regroupé dans le package [`EvoVGM`](https://github.com/maremita/evoVGM). Par ailleurs, le projet [`evoVGM_Exp`](https://github.com/maremita/evoVGM_Exp) contient des scripts spécialement conçus pour l'exécution de `EvoVGM` selon divers schémas de grille, implémentant différents modèles évolutifs, types et tailles de données, ainsi que des configurations d'hyperparamètres. 
`EvoVGM` peut être exécuté aussi bien en environnement local que sur des grappes de calcul.

## 3. Apprentissage de la densité *a priori* dans l'inférence bayésienne variationnelle des paramètres phylogénétiques
Dans cette étude, nous présentons `nnTreeVB`, une approche pour l'inférence bayésienne variationnelle dans le cadre de la phylogénétique.
Cette approche met en œuvre des méthodes permettant la paramétrisation des densités variationnelles et *a priori* à l'aide de réseaux de neurones.
De plus, elle permet d'utiliser différentes distributions variationnelles, notamment des distributions de champ moyen et hétérogènes. 
En outre, `nnTreeVB` assouplit la rigidité des densités *a priori* fixes en apprenant leurs paramètres à l'aide d'une méthode basée sur les gradients ou en régularisant leur divergence de Kullback-Leibler avec les densités variationnelles.
Les performances de cette approche sont évaluées pour l'estimation des longueurs de branches et des paramètres de modèles évolutifs sous divers modèles de substitution de chaîne de Markov. 

Le travail de ce chapitre a été publié lors de la conférence *the 20th RECOMB Comparative Genomics Satellite Conference* en 2023 sous le titre : **Prior Density Learning in Variational Bayesian Phylogenetic Parameters Inference**.
Il est à noter que les résultats de cette étude ont également été présentés à la conférence *15th Great Lakes Bioinformatics Conference*.
La rédaction de l'article, la conception et la mise en place des modèles et du cadre d'évaluation, ainsi que l'exécution des expérimentations ont été réalisées par Amine Remita sous la supervision du professeur Abdoulaye Baniré Diallo. 
Golrokh Vitae, bioinformaticienne affiliée au Centre CERMO-FC de l'UQAM au moment de la rédaction de l'article, a contribué aux discussions concernant la conception des modèles et les résultats obtenus. 
Un autre article détaillant l'approche `nnTreeVB` ainsi que son évaluation est actuellement en préparation.

Le code source qui soutient cette étude est regroupé dans le package [`nnTreeVB`](https://github.com/maremita/nnTreeVB).
Le projet [`nnTreeVB_Exp`](https://github.com/maremita/nnTreeVB_Exp) inclut les fichiers de configuration des expériences conçues pour l'exécution de `nnTreeVB`.
