# Avant et après

Ces exemples montrent l'adaptation française du skill.

## Introduction de README

**Avant :**

> sqlpipe est un outil en ligne de commande robuste et performant permettant de synchroniser facilement vos tables PostgreSQL vers Amazon S3 sous forme de fichiers Parquet, sans avoir à mettre en place une plateforme ETL complète et complexe.

**Après :**

> sqlpipe copie des tables PostgreSQL vers Amazon S3 sous forme de fichiers Parquet. Il ne nécessite pas de plateforme ETL.

> sqlpipe lit les tables par lots. Il peut copier une table complète ou seulement les lignes ajoutées.

## Dépannage

**Avant :**

> Vous pouvez essayer d'augmenter `source.connect_timeout_seconds` dans votre configuration si votre réseau est lent, afin d'éviter que le délai par défaut ne provoque une erreur.

**Après :**

> Si le réseau est lent, augmentez `source.connect_timeout_seconds`. Cette valeur définit le délai de connexion.

## Message d'erreur

**Avant :**

> Oups ! Une erreur inattendue est malheureusement survenue lors de la tentative de connexion. Veuillez vérifier vos identifiants et réessayer.

**Après :**

> La connexion à la base de données a échoué. Le mot de passe de l'utilisateur `app` est incorrect. Corrigez `DB_PASSWORD`, puis reconnectez-vous.

## Rapport d'incident

**Avant :**

> Nous avons identifié un problème qui a potentiellement affecté certains utilisateurs. Nos équipes ont travaillé activement pour rétablir complètement le service.

**Après :**

> Entre 14 h 02 et 14 h 31 UTC, 12 % des requêtes ont échoué. Le déploiement de 14 h 00 a supprimé le préchauffage du cache. Nous avons annulé ce déploiement à 14 h 27.

## Rupture de compatibilité

**Avant :**

> Veuillez noter que nous avons apporté des changements au point d'accès des utilisateurs. Vous devrez peut-être adapter votre intégration en conséquence.

**Après :**

> **Rupture :** Utilisez `/v2/users`. Remplacez `name` par `first_name` et `last_name`. Le champ `name` sera nul après le 1er septembre 2026.
