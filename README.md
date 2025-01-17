# Analyse-de-survie
# Analyse de survie chez les enfants de moins de 12 moins atteints de pneumonie nécessitant une hospitalisation
#Ce projet a été réalisé avec le langage R
Ce projet explore les facteurs de risque associés à la pneumonie chez les enfants âgés de 0 à 12 mois. À l'aide de modèles d'analyse de survie, nous cherchons à comprendre l'impact de différentes variables (allaitement, âge de la mère, environnement, etc.) sur le temps avant la survenue d'une pneumonie nécessitant une hospitalisation.

---

## Objectifs du projet
1. Identifier les facteurs influençant le délai avant la survenue d'une pneumonie.
2. Construire un modèle de Cox ajusté pour prédire le risque de pneumonie en fonction des covariables.

---

## Données utilisées
La base de données "pneumnon" du package "KMsurv" a été utilisée pour notre projet. Il s'agit d'observations sur 3 470 enfants définis par 15 variables dont :
- **chldage** : Âge de l'enfant en mois.
- **hospital** : Indicateur d'hospitalisation pour la pneumonie (1 = oui, 0 = non).
- **wmonth** : Mois où l'enfant a été sevré
- **mthage** : Âge de la mère lors de la naissance.
- **urban** : Type d'environnement (urbain/rural).
- **smoke** : Habitudes de tabagisme de la mère.
- **alcohol** : Habitudes de consommation d'alcool de la mère.
- **region** : Région géographique.
- **poverty** : Statut de pauvreté de la mère.
- **race** : Race de la mère.
- **bweight** : Poids de naissance (moins de 5,5 lbs ou 5,5 lbs et plus).
- **nsibs** : Nombre de frères et sœurs.
-**sfmonth**: Mois l'enfant a commencé à manger des aliments solides
-**agepn** : âge en mois où l'enfant a été hospitalisé pour une pneumonie
---

## Méthodologie
### Étapes principales :
1. **Préparation des données** :
   - Nettoyage des données (gestion des doublons et des valeurs manquantes).
   - Transformation de certaines variables en facteurs ou variables binaires.
   
2. **Analyse exploratoire** :
   - Distribution des variables et exploration des facteurs potentiels.
   - Visualisation des courbes de Kaplan-Meier.

3. **Modélisation de Cox** :
   - Modèle univarié pour tester l'association de chaque covariable.
   - Modèle multivarié ajusté pour prendre en compte plusieurs facteurs.

4. **Hypothèses testées** :
   - H0 : Pas de différence dans les fonctions de survie entre les groupes (allaitement/non allaitement).
   - Comparaison des modèles avec des tests de vraisemblance et de Wald.

---

## Résultats principaux
- **Impact de l'allaitement** :
  Les enfants allaités ont un risque significativement réduit de développer une pneumonie nécessitant une hospitalisation.

- **Autres facteurs associés** :
  - Le tabagisme de la mère augmente le risque de pneumonie.
  - Les enfants nés dans des familles nombreuses (plus de frères et sœurs) présentent un risque accru de pneumonie.

---

## Structure du projet
- **`Survie_new.Rmd`** : Script R Markdown contenant le code d'analyse.
- **`output/Survie_new.pdf`** : Rapport PDF généré à partir du fichier R Markdown.
  

---


