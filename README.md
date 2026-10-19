# Mobilité urbaine dans la région de Dakar avec Apache Spark
 
Projet réalisé dans le cadre du cours **Big Data** à l'École Mohammadia d'Ingénieurs (EMI), sous l'encadrement de **Madame Leila Benhlima**.
 
**Réalisé par :** Oumaima Ouakil et Amadour Ihssane

## Objectif
 
Exploiter avec **PySpark** les données de l'enquête ménages-déplacements de la région de Dakar (45 605 déplacements) pour répondre à deux questions :
 
- **Qui paie pour se déplacer, et combien ?** Classification payant / gratuit (régression logistique, forêt aléatoire) et régression du coût.
- **Quels types de territoires se dégagent ?** Typologie des strates par K-Means et ACP.
## Contenu
 
| Fichier | Description |
| --- | --- |
| `projet_spark_mobilite.ipynb` | Notebook complet : nettoyage, imputation, variables, modèles, clustering et interprétations |
| `rapport/` | Rapport LaTeX (`rapport.tex`), figures et PDF |
 
## Principaux résultats
 
- 23,8 % des déplacements sont payants. Le premier déterminant est la distance : 61 % des trajets entre strates sont payants, contre 6,5 % des trajets internes.
- La forêt aléatoire prédit le caractère payant avec une AUC de 0,879, sans utiliser le mode de transport.
- Le montant payé dépend surtout du mode : le R² de la régression du coût passe de 0,20 sans le mode à 0,78 avec.
- La région se divise en deux types de territoires : un centre motorisé (8 strates) et une périphérie à mobilité de proximité, surtout pédestre (33 strates).
## Exécution
 
Prérequis : Python 3, Java 17 ou 21, et les paquets suivants :
 
```bash
pip install pyspark==4.0.1 openpyxl pandas matplotlib seaborn
```
 
