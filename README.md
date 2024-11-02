# Création du Modèle de Recommandation Attentional Sentiment and Confidence Aware Neural Recommender

## Description

Ce projet vise à développer un système de recommandation avancé pour un cas d'utilisation e-commerce, en utilisant un modèle hybride combinant filtrage collaboratif et cognitif. Le modèle se base sur les évaluations et les commentaires des utilisateurs, qui ont été analysés à l'aide de plusieurs modèles d'analyse de sentiment. Chaque modèle d'analyse de sentiment est équipé d'une couche d'attention et d'un module de confiance pour améliorer la précision des recommandations.

## Composants du Projet

### 1. **Analyse de Sentiment**

- **Modèles Utilisés :** Plusieurs modèles d'analyse de sentiment ont été développés, notamment LSTM, BiLSTM, LSTM-CNN, BiLSTM-CNN, LSTM-RNN, et BiLSTM-RNN.
- **Données d'Entraînement :** Les modèles ont été entraînés sur le dataset IMDB pour classer les commentaires en sentiments positifs ou négatifs.

### 2. **Filtrage Hybride**

- **Filtrage Collaboratif :** Utilise les évaluations des utilisateurs pour générer des recommandations basées sur les comportements d'achat similaires entre les utilisateurs.
- **Filtrage Cognitif :** Intègre les analyses de sentiment des commentaires pour affiner les recommandations en tenant compte des avis exprimés.

### 3. **Système d'Attention et Module de Confiance**

- **Couche d'Attention :** Chaque modèle d'analyse de sentiment inclut une couche d'attention pour focaliser le traitement sur les parties les plus significatives des commentaires.
- **Module de Confiance :** Évalue la fiabilité des sentiments extraits pour ajuster l'impact des commentaires dans le système de recommandation.

### 4. **Entraînement des Modèles**

- **Analyse de Sentiment :** Entraînée sur le dataset IMDB pour obtenir des embeddings contextuels des commentaires.
- **Filtrage Hybride :** Entraîné sur le dataset Amazon pour générer des recommandations précises basées sur les évaluations et les sentiments analysés.

## Fonctionnement

Le système combine les résultats des modèles d'analyse de sentiment avec les techniques de filtrage collaboratif et cognitif pour fournir des recommandations personnalisées. Les évaluations et les commentaires des utilisateurs sont analysés pour créer des profils d'achat et des préférences affinées, intégrant des couches d'attention pour capturer les détails importants et un module de confiance pour valider les recommandations.

## Conclusion

Le modèle de recommandation Attentional Sentiment and Confidence Aware Neural Recommender combine des techniques avancées d'analyse de sentiment avec des approches hybrides de filtrage pour offrir des recommandations e-commerce précises et personnalisées, en prenant en compte à la fois les évaluations des utilisateurs et les sentiments exprimés dans les commentaires.

## Contributeurs
- [Fella DIB](github.com/felladib)
- [Lina IGHILAZA](github.com/liAghZn)


