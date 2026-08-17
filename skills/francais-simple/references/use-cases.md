# Cas d'usage

## Messages d'erreur

Mode : procédure.

Donne les informations dans cet ordre :

1. le résultat observé ;
2. la cause, si elle est connue ;
3. l'action corrective.

**Avant :** Une erreur inattendue est survenue. Veuillez vérifier vos paramètres et réessayer.

**Après :** La connexion a échoué. Le mot de passe de `app` est incorrect. Corrigez `DB_PASSWORD`, puis reconnectez-vous.

## Runbooks et procédures

Mode : procédure stricte.

- Utilise l'impératif pour chaque étape.
- Donne une seule action par étape.
- Place la condition avant l'action.
- Place un avertissement avant l'étape dangereuse.
- Garde chaque phrase sous 20 mots.

## Rapports d'incident

Mode : description.

Utilise des faits datés. Donne l'impact mesuré, la chronologie, la cause connue et les actions correctives.

**Avant :** Nous avons identifié un incident qui a pu affecter certains utilisateurs. Nos équipes ont rapidement rétabli le service.

**Après :** Entre 14 h 02 et 14 h 31 UTC, 12 % des requêtes ont échoué. Le déploiement de 14 h 00 a supprimé le préchauffage du cache.

## Commits et demandes de fusion

Utilise un objet impératif : « Corrige le délai de connexion ». Décris ensuite les faits au présent ou au passé composé.

Supprime les formulations comme « cette demande vise à ».

## Notes de version

Mode : description, avec procédure pour une migration.

Décris un changement par entrée. Pour une rupture, donne d'abord l'action nécessaire, puis la conséquence.

> **Rupture :** Utilisez `/v2/users`. Le champ `name` sera nul à partir du 1er septembre 2026.

## Instructions pour agents IA

Mode : procédure.

- Écris une instruction indépendante par phrase.
- Utilise le même verbe pour la même opération.
- Place « si » au début de la règle conditionnelle.
- Remplace « devrait » par « doit » pour une obligation.

## Messages d'assistance et pages d'état

Mode : description.

Donne la durée, l'impact et l'état actuel. Supprime les excuses génériques qui n'ajoutent aucune information.

## Préparation à la traduction

Mode : strict.

Utilise un glossaire validé. Évite les pronoms ambigus. Garde les articles et une grammaire complète. N'emploie pas un mot avec plusieurs sens techniques.

## Interface utilisateur

Les boutons et libellés sont des noms techniques. Le texte d'aide suit les règles ordinaires.

> Aucun projet. Créez un projet pour commencer.

## Usages déconseillés

Ce style ne convient pas aux pages marketing, aux billets éditoriaux et aux textes littéraires. Il supprime volontairement la persuasion et la voix de marque.
