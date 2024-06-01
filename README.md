# Système de Recommandation basé sur l'Analyse de Sentiment et les Avis Faux

Ce projet vise à développer un système de recommandation personnalisé en se basant sur l'analyse de sentiment et la détection d'avis faux dans les commentaires. Le modèle est construit en utilisant des techniques de deep learning et des algorithmes de filtrage collaboratif.

## Objectif

L'objectif principal de ce projet est de recommander des produits de manière personnalisée aux utilisateurs en tenant compte de leurs préférences et en filtrant les avis frauduleux.

## Architecture du Modèle

Le modèle est construit en plusieurs étapes :

1. **Collecte de Données** :
   - Les données sont collectées à partir de l'ensemble de données IMDb pour construire un modèle capable de prédire le score de sentiment dans un commentaire.

2. **Prétraitement des Données** :
   - Les données sont prétraitées en effectuant la tokenization, la suppression des mots vides, le padding, etc.
   - Un vocabulaire est construit à partir des données et un modèle pré-entraîné BERT est utilisé pour représenter les mots sous forme de vecteurs (construction de vecteurs latents).

3. **Modèles Hybrides** :
   - Quatre modèles hybrides sont construits, chacun comprenant :
     - Une couche CNN ou RNN pour l'extraction de caractéristiques.
     - Une couche LSTM ou BiLSTM pour la modélisation de la séquence.
     - Une couche d'attention pour se concentrer sur les parties importantes du commentaire.
     - Une couche dense finale avec un seul neurone en sortie avec activation sigmoïde pour le score de sentiment.

4. **Matrice de Confiance** :
   - Une matrice de confiance est utilisée pour améliorer la fiabilité et la précision des recommandations.
   - Elle combine les évaluations des utilisateurs sur les produits avec la confiance associée aux commentaires analysés.

5. **Modèles de Filtrage** :
   - Deux algorithmes de filtrage sont utilisés : GMF (Factorisation Matricielle Généralisée) et MLP (Perceptron Multi-Couches).
   - Ces modèles de filtrage sont entraînés avec un ensemble de données provenant d'Amazon.

## Plus d'Informations

Pour plus de détails sur le projet, vous pouvez consulter le document de recherche suivant : [Lien vers le document](https://www.scitepress.org/Papers/2023/121930/121930.pdf).

## Installation

Pour exécuter ce projet localement, suivez ces étapes :

1. Assurez-vous d'avoir Python 3.x installé sur votre système.
2. Installez les dépendances en exécutant `pip install -r requirements.txt`.

## Utilisation

1. Clonez ce dépôt sur votre machine.
2. Exécutez les scripts de collecte de données, de prétraitement et de construction de modèles.
3. Lancez le système de recommandation et testez-le avec de nouvelles données.

## Contributions

Les contributions sont les bienvenues ! Si vous avez des suggestions d'amélioration ou des correctifs à apporter, veuillez ouvrir une issue ou soumettre une pull request.

## Licence

Ce projet est sous licence MIT. Voir le fichier LICENSE pour plus de détails.


