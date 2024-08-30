# Modèles d'Analyse de Sentiment dans `model_sa.py`

## Description

Dans le fichier `SA_modul.py`, plusieurs modèles d'analyse de sentiment ont été développés pour évaluer la polarité des commentaires collectés depuis la base de données IMDB. Les commentaires sont annotés avec un score binaire : 1 pour les sentiments positifs et 0 pour les sentiments négatifs.

## Modèles Implémentés

Les modèles suivants ont été créés et testés dans ce projet :

- **LSTM (Long Short-Term Memory)**
- **BiLSTM (Bidirectional LSTM)**
- **LSTM-CNN**
- **BiLSTM-CNN**
- **LSTM-RNN**
- **BiLSTM-RNN**

## Processus de Prétraitement

Les données ont été prétraitées avant d'être introduites dans les modèles :

1. **Collecte des Données :** Les commentaires sont extraits de la base de données IMDB.
2. **Nettoyage des Données :** Les textes sont nettoyés pour enlever les caractères spéciaux, les balises HTML, etc.
3. **Suppression des Mots Vides :** Les mots sans signification importante (mots vides) sont supprimés.
4. **Padding :** Les séquences de texte sont normalisées à une longueur fixe à l'aide du padding.
5. **Splitting :** Les données sont divisées en ensembles d'entraînement et de test.
6. **Indexation :** Les mots sont convertis en indices numériques.
7. **Création du Vocabulaire :** Un vocabulaire est créé à partir des mots indexés.
8. **Utilisation de BERT :** Le modèle préentraîné BERT est utilisé pour obtenir les embeddings des mots, offrant une représentation dense et contextuelle de chaque mot.

## Entraînement des Modèles

Les embeddings générés par BERT sont ensuite passés dans les modèles de réseaux de neurones listés ci-dessus. Chaque modèle a été entraîné et évalué sur les données prétraitées.

## Résultats et Conclusion

Après avoir testé tous les modèles, les résultats montrent que le modèle **BiLSTM-CNN** est celui qui obtient les meilleures performances. Cela est dû à la capacité de BiLSTM à capturer les relations contextuelles dans les deux directions (avant et arrière) et à la capacité des couches CNN à extraire des caractéristiques locales pertinentes, ce qui renforce la précision de la classification.

## Conclusion

Le modèle BiLSTM-CNN a surpassé les autres modèles, montrant l'importance de combiner l'analyse contextuelle bidirectionnelle avec l'extraction de caractéristiques locales pour l'analyse de sentiment.


