 # Analyse descriptive des rendements et de la volatilité de l’action Apple (1980–2025)



![...]



## Description du projet



Ce projet consiste en la réalisation d’un tableau de bord interactif permettant une analyse descriptive des données boursières historiques de l’action Apple (AAPL) sur la période 1980–2025.



L’objectif est de comprendre :



l’évolution des rendements journaliers,



la distribution des variations quotidiennes,



l’évolution de la volatilité (risque) dans le temps,



certains indicateurs clés résumant le comportement historique du titre.



## Jeu de données



Actif analysé : Apple Inc. (AAPL)



Fréquence : quotidienne



Période : 1980 à 2025



Format : CSV / Excel



## Variables initiales



Date : date de cotation



Open : prix d’ouverture



High : prix le plus élevé de la journée



Low : prix le plus bas de la journée



Close : prix de clôture



Volume : nombre d’actions échangées



## Méthodologie de nettoyage des données



### Séparation correcte des colonnes



À l’origine, toutes les données étaient contenues dans une seule colonne.



Les colonnes ont été séparées via :



Données → Convertir



séparateur : virgule



### Vérification et correction des types de données



La colonne Date était déjà au bon format (Date).



Les colonnes numériques étaient interprétées comme du texte, notamment à cause du séparateur décimal (.).



Actions réalisées :



remplacement des points par des virgules via Ctrl + H



conversion correcte des valeurs en nombres réels



acceptation des limites de précision numériques d’Excel (sans impact sur l’analyse)



Une vérification des doublons a également été effectuée.



###Vérification de la cohérence logique des prix



Une vérification a été réalisée pour s’assurer que :



High ≥ Open et High ≥ Close



Low ≤ Open et Low ≤ Close



Formule utilisée :



=SI(ET(C2>=B2;C2>=E2;D2<=B2;D2<=E2);"OK";"ERREUR")



Les données se sont révélées cohérentes.

La colonne de vérification a ensuite été supprimée.



### Création et recalcul des variables dérivées



Afin d’assurer une cohérence complète, les variables suivantes ont été recalculées :



Rendement journalier



Daily_Return = (Close_t − Close_{t−1}) / Close_{t−1}



Amplitude quotidienne du prix



Price_Range = High − Low



Les valeurs ont été arrondies à 6 décimales.



Les données finales ont été organisées dans un tableau structuré, facilitant l’analyse, les tableaux croisés dynamiques et les visualisations.



## Analyse et visualisation

### Indicateurs clés (KPI)



Le dashboard présente plusieurs indicateurs synthétiques :



Volatilité moyenne historique : écart-type moyen des rendements journaliers



Rendement journalier maximum observé



Prix médian historique de l’action



Ces indicateurs offrent une lecture rapide du comportement global du titre.



### Volatilité annuelle



Calculée comme l’écart-type des rendements journaliers par année



Obtenue via des tableaux croisés dynamiques



Permet d’identifier :



les périodes de forte instabilité,



les périodes plus calmes du marché



### Distribution des rendements journaliers



Histogramme des rendements journaliers



Mise en évidence :



d’une forte concentration des rendements autour de 0 %



de la rareté des variations extrêmes



Illustration du caractère typique des distributions financières



## Tableau de bord interactif



Le dashboard regroupe :



un segment temporel permettant de filtrer les périodes,



des KPI synthétiques,



les visualisations principales (volatilité et distribution des rendements).



L’objectif du tableau de bord est de fournir une vue d’ensemble claire, lisible et interactive.



\##Architecture du classeur Excel



Données brutes : données originales

Données nettoyées : données nettoyées et structurées

Analyse descriptive : statistiques descriptives

Tableaux croisés dynamiques : tableaux croisés dynamiques

Graphiques exploratoires : graphiques individuels

Tableau de bord : tableau de bord final



## Outils utilisés



Microsoft Excel

Nettoyage et préparation des données

Fonctions statistiques

Tableaux croisés dynamiques

Visualisation et dashboard interactif



## Compétences mises en pratique



Nettoyage et structuration de données

Analyse exploratoire

Statistiques descriptives

Data visualisation

Construction d’un dashboard interactif

Lecture et interprétation d’indicateurs financiers



## Conclusion



Ce projet montre comment une analyse descriptive structurée permet d’extraire des informations pertinentes à partir de données financières historiques.

Il souligne l’importance de la préparation des données, du choix des indicateurs et de la visualisation dans la compréhension du comportement d’un actif.

