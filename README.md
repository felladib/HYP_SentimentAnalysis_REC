# H_SentimentAnalysis_REC

# H-SCARS: 
Hyperid sentiment confidence aware recommandation Systeme :
ce model utilise une module de confinace qui permet de calculer le degre de confiace pour chaque utilisateur par rapport un item , ce dergre sera combiner avec la valeur de sentiment .
le score de sentiment est deduit en utilisant plusieur model hypride d'analyse de sentiment, pretraitement des commentaire , preprocesing avec le model BERT ce qui nous donne le feature vecteur de chaque reviews , ces dernier entre dans un couche LSTM/BILSTM puis une couche CNN/RNN puis une couche d'attenetion qui permet de se concentrée sur les parties les plus important de reviews . 
au finale tout ces information sur l'utilisateur passe par une couche GMF et des couche MLP pour predire le score d'evaluation final. 
## CASA-REC: ce model ce compose de 2 module le 1er d'analyse de sentiment puis le modul de filtrage collaboratif et basé contenu(cognitif)
# SA_Modul : 
ensemble des model d'analyse de sentiment en utilisant les technique de deep learning tel que LSTM , BILSTM , CNN ...
ces model utilise le model bert (c'est model de NLP preentrainner permet la preprocessing des mots (reviews) avant d'utilise ce model les reviews doit etre pretraiter (tokinization : faire des token decoupage de reviews puis suppression des mot vide ....  puis le padding : modifier la taille de reviews par exemple tout commentaire doit avoir le meme nombre de mot , le review est un vecteur donc ce qu'on doit faire c'est de mettre tout les commentaire dans un vectuer de meme taille  ) 
ces vecteur entre dans les model de SA pour donner le score de sentiment qui est entre 0 et 1.
