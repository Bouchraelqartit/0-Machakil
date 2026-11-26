# Contribution à 0machakil

Chaque collaborateur réalise l'interface, l'API, les vérifications et la documentation utiles à sa fonctionnalité.

## Branches et commits

Créer une branche courte depuis main pour chaque ticket, par exemple feature/NK0-11-signalement. Commencer le message de commit par la clé réelle, par exemple NK0-11 Ajouter la catégorie au formulaire.

Le titre de pull request contient également la clé, par exemple NK0-11 Signaler un problème avec photo et localisation. Ces références seront exploitées par l'intégration GitHub pour Jira une fois installée et vérifiée.

## Revue

Ouvrir une pull request et demander la relecture d'un autre collaborateur. Décrire le résultat, le ticket et les vérifications réalisées. Intégrer régulièrement pour détecter les incompatibilités entre modules.

## Catégories et services

Les doublons doivent concerner le même problème. La proximité et la catégorie sont des indices, sans fusion automatique. La catégorie propose un service référent ; le gestionnaire confirme son orientation. Une catégorie désactivée conserve son historique.

## Secrets et données

Ne pas commiter de mot de passe, de jeton ni de donnée réelle de citoyen. Utiliser des données fictives et une configuration propre à chaque environnement.

## Terminé

Un ticket est terminé lorsque ses critères passent, que sa pull request a été relue et intégrée, et que la documentation utile est à jour.
