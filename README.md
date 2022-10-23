# Artificial-Intelligence
Réalisé par: 
EL ABDI MAJDA
IRCHADE BEN HASSAN


Learning Rate :
-valeur par défaut de “Adam” soit 0,001, car toute valeur supérieure conduit à des loss très élevés.
On a essayé aussi d’utiliser RMSprop()  mais ça n’a pas marché pour le projet choisi, ça donnait des erreurs, pourtant sur d’autres cela fonctionnait.

-Metrics =’Accuracy’


Régularisation :

    BatchNormalization(), appliquée à chaque filtre
    Dropout(0.25), appliquée aux filtres de départ et de fin, car la loss devient minimale lorsqu’on l’applique à tous les filtres avec un temps de traitement par EPOCH de 43s contre 60s mais ne donnait pas une meilleur valeur pour val_loss    


Structures :

On a 5 filtres dont 2 de 32, un de 64, 128 et 256.
-le code de base avait 3 couches, dont deux de 32 et une de 64, nous en avons ajouté de 128 et 256 et le résultat s’est amélioré




Fonction d’activation :
on a changé aussi la fonction dense de softmax à sigmoid.

EPOCHS :
De base, le projet tournait avec 50 EPOCHS, mais la compilation n’atteignait jamais les 50, le programme est fait à s'arrêter lorsqu’on a plus d’amélioration.
Et on a trouvé que au bout d’une quarantaine, on atteignait les meilleurs scores, au final on tourne avec 40 EPOCHS.

DataSets :
- data_set du training
-data_set des validations
-data_set des test
Analyses de l'entraînement et de la validation : 

On peut observer qu’on n’a pas d'overfitting, le model comporte des data generators évitant cela, et on arrive à atteindre 95% pour le training et 90% validation, ce n’est pas parfait mais mieux que le model initial.
Pour les pertes : on peut atteindre 0.2 pour le le training, et 0.6 pour validation, ce sont les meilleurs scores qu’on a pu obtenir.
Les graphes ainsi que les résultats suivront.
