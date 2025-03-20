# Fork de Cryengine-Converter pour Star Citizen 4.0.2

Ce fork du [Cryengine-Converter](https://github.com/Markemp/Cryengine-Converter) original par Markemp ajoute la compatibilité avec les fichiers de Star Citizen 4.0.2.

## Problème résolu

Dans Star Citizen 4.0.2, le format des fichiers CGF a été modifié, et la clé '5' qui était présente dans le dictionnaire `StreamMasks` des sous-ensembles de maillage n'est plus présente. Cela provoque une erreur `KeyNotFoundException` lors de la conversion des modèles 3D.

## Solution implémentée

Nous avons ajouté une vérification qui s'assure que la clé '5' existe dans le dictionnaire avant de tenter d'y accéder. Si la clé n'existe pas, elle est ajoutée avec une valeur par défaut.

## Comment utiliser ce fork

1. Clonez ce dépôt ou téléchargez-le sous forme de ZIP
2. Compilez la solution avec Visual Studio
3. Utilisez l'exécutable généré pour convertir vos fichiers Star Citizen 4.0.2

Pour des instructions détaillées, consultez le fichier [INSTRUCTIONS-FORK.txt](INSTRUCTIONS-FORK.txt).

## Fichiers inclus

- `patch-key5-fix.diff` - Le patch qui corrige l'erreur
- `INSTRUCTIONS-FORK.txt` - Instructions détaillées pour appliquer le patch et compiler le projet
- `README-FORK.md` - Ce fichier

## Contribuer

Si vous trouvez d'autres problèmes avec Star Citizen 4.0.2 ou des versions ultérieures, n'hésitez pas à soumettre des pull requests ou à ouvrir des issues.

## Remerciements

Merci à Markemp pour le convertisseur original et à la communauté Star Citizen pour son soutien continu. 