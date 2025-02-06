# Databricks-Accidents-Project

## Présentation du Projet
Ce projet a pour objectif de créer le modèle permettant de prédire la gravité d’un accident en fonction de plusieurs informations sur cet accident. 
Le modèle sera évalué en utilisant les algorithmes suivants :
- K plus proche voisin: KNeighborsClassifier
- Arbre de décision: DecisionTreeClassifier
- Forêt aléatoire: RandomForestClassifier
Les performances des modèles seront comparées.

## Sources des Données
Les données utilisées dans ce projet proviennent du site [data.gouv.fr](https://www.data.gouv.fr). Nous avons utilisé les fichiers suivants :
- `carac.csv` : Caractéristiques des accidents
- `lieux.csv` : Données sur les lieux des accidents
- `veh.csv` : Informations sur les véhicules impliqués
- `vict.csv` : Informations sur les victimes

## Étapes de Pré-Processing
1. Suivre toutes les étapes de pré-traitement du tutoriel d'Ilyes Talbi de la revue IA.
2. Construire l'échantillon d'entraînement et de test avec 10% des données pour l'apprentissage.

## Modèles Utilisés
### K plus proche voisin: KNeighborsClassifier
Pour trouver les meilleurs paramètres du modèle, nous avons utilisé GridSearchCV pour optimiser le paramètre `n_neighbors`.

### Arbre de décision: DecisionTreeClassifier
Pour optimiser les paramètres du modèle, nous avons utilisé GridSearchCV pour ajuster :
- `max_depth`
- `min_samples_leaf`

### Forêt aléatoire: RandomForestClassifier
Pour optimiser les paramètres du modèle, nous avons utilisé GridSearchCV pour ajuster :
- `n_estimators`
- `max_depth`
- `min_samples_leaf`

## Comparaison des Performances des Modèles
Les métriques suivantes ont été calculées pour chaque modèle afin de comparer leurs performances :
- Accuracy
- F1-score

Le meilleur modèle parmi les trois a été enregistré dans Databricks sous le nom de **BestModel**.

## Références
- [Tutoriel d'Ilyes Talbi](https://github.com/ilyestalbi)

## Contributeurs
- SAMAIN Jad
- TRUONG David

## Dossier

- README.md : Document de présentation du projet

### CSV/

- carac.csv : Caractéristiques des accidents

- lieux.csv : Données sur les lieux des accidents

- veh.csv : Informations sur les véhicules impliqués

- vict.csv : Informations sur les victimes

### Notebooks/

- Modelisation.dbc : Notebook pour l'entraînement du modèle

- Test_API.dbc : Notebook pour tester le modèle

### Models/

- BestModel.pkl : Meilleur modèle enregistré


