---
name: francais-simple
version: 1.0.0
description: |
  Rédiger ou réécrire un texte technique en français clair, précis et sans
  remplissage. Utiliser ce skill pour la documentation, les README, les
  procédures, les runbooks, les messages d'erreur, les notes de version, les
  rapports d'incident et les guides API. L'utiliser aussi quand l'utilisateur
  demande du « français simple », un texte lisible, un style direct, une
  rédaction pour des lecteurs non spécialistes ou un texte facile à traduire.
  Applique des principes adaptés de l'ASD-STE100 : phrases courtes, un terme par
  concept, voix active, temps simples et condition avant l'action.
license: MIT
compatibility: claude-code cursor codex gemini-cli opencode
metadata:
  inspiration: ASD-STE100 Issue 9 and AminBlg/SimpleEnglish
  language: fr
---

# Français Simple

Produis un texte technique français qu'un lecteur fatigué comprend en une seule lecture. Supprime les ambiguïtés, le remplissage et les effets de style inutiles.

Ce skill adapte des principes du *Simplified Technical English*. L'ASD-STE100 norme l'anglais, pas le français. Ne présente jamais le résultat comme conforme à l'ASD-STE100.

## Tâche

Quand tu rédiges ou réécris un texte technique :

1. Choisis le mode pragmatique ou strict.
2. Classe chaque passage comme procédure ou description.
3. Choisis un terme unique pour chaque concept.
4. Applique les règles de ce document.
5. Exécute l'autocontrôle avant de livrer le texte.
6. Ne modifie jamais le code, les identifiants, les commandes et les erreurs citées.

Quand l'utilisateur demande un contrôle, indique pour chaque problème : la règle, le texte concerné et une correction.

## Modes

| Mode | Usage | Application |
|---|---|---|
| **Pragmatique** par défaut | Documentation courante et messages | Toutes les règles de structure. Le vocabulaire métier reste autorisé. |
| **Strict** | Texte critique, réglementé ou destiné à la traduction | Toutes les règles, avec terminologie imposée et contrôle complet. |

En mode strict, demande ou utilise le glossaire du projet. Sans glossaire validé, signale que le contrôle terminologique reste incomplet.

## Classification

| | Procédure | Description |
|---|---|---|
| But | Dire quoi faire | Expliquer un fait ou un fonctionnement |
| Forme | Impératif | Présent, passé composé ou futur simple |
| Limite | 20 mots par phrase | 25 mots par phrase |
| Unité | Une action par phrase | Un sujet par paragraphe |

Ne mélange pas une procédure et une description dans le même passage. Place une explication dans une note distincte.

## Règles

### 1. Vocabulaire

1.1. Utilise des mots courants ou les termes du domaine.

1.2. Utilise un seul terme pour un concept dans tout le document.

1.3. N'alterne pas entre « configuration », « paramètres » et « réglages » pour varier le style.

1.4. Définis un sigle lors de sa première utilisation, sauf si le public le connaît nécessairement.

1.5. Évite le jargon interne si le lecteur ne le connaît pas.

1.6. Préfère le mot court quand deux mots ont le même sens exact.

1.7. Conserve le vocabulaire métier nécessaire, comme `webhook`, « idempotent » ou « déploiement ».

### 2. Verbes

2.1. Utilise la voix active quand l'acteur est connu.

2.2. Utilise l'impératif pour une instruction.

2.3. Préfère le présent, le passé composé et le futur simple.

2.4. Évite le conditionnel quand il masque une obligation ou un fait.

2.5. Remplace « devrait » par « doit » pour une obligation. Supprime-le pour une simple préférence.

2.6. Remplace une tournure nominale par un verbe direct.

**Avant :** Procédez à la vérification de la configuration.

**Après :** Vérifiez la configuration.

### 3. Phrases

3.1. Limite une instruction à 20 mots.

3.2. Limite une description à 25 mots.

3.3. Donne une seule instruction par phrase.

3.4. Donne une seule information nouvelle par phrase.

3.5. Garde une grammaire complète. N'utilise pas un style télégraphique.

3.6. Utilise une liste verticale pour plus de deux étapes ou éléments complexes.

3.7. N'utilise pas le point-virgule. Écris deux phrases.

3.8. Limite un paragraphe descriptif à un sujet et six phrases.

### 4. Conditions et enchaînement

4.1. Place la condition avant l'action.

**Avant :** Augmentez le délai si le réseau est lent.

**Après :** Si le réseau est lent, augmentez le délai.

4.2. Place chaque avertissement avant l'étape concernée.

4.3. Donne d'abord l'action interdite, puis sa conséquence.

**ATTENTION :** N'exécutez pas `reset --force` en production. Cette commande supprime les données locales.

4.4. Utilise « puis », « donc » ou « par conséquent » quand le lien entre deux phrases doit être explicite.

### 5. Précision

5.1. Remplace les qualificatifs vagues par des faits mesurables.

5.2. Indique la cause d'une erreur si elle est connue.

5.3. Donne une action concrète pour corriger une erreur.

5.4. N'invente aucune valeur, cause, date, mesure ou garantie.

5.5. Signale une information inconnue au lieu de l'atténuer avec « peut-être » ou « possiblement ».

### 6. Remplissage

Supprime une expression si elle n'ajoute aucun fait.

| Éviter | Écrire |
|---|---|
| afin de | pour |
| préalablement à | avant |
| dans le cas où | si |
| il convient de noter que | supprimer |
| il est important de | donner directement le fait ou l'obligation |
| simplement, facilement, aisément | supprimer ou prouver |
| robuste, puissant, complet | donner une propriété mesurable |
| de manière transparente | expliquer le comportement |
| tirer parti de | utiliser |
| permettre de | pouvoir, ou employer un verbe direct |
| au niveau de | dans, sur, pour, ou supprimer |
| problématique | problème, erreur ou risque précis |
| etc. | nommer les éléments utiles |

### 7. Écriture inclusive et accessibilité

7.1. Utilise une formulation neutre et naturelle quand elle existe.

7.2. Évite les formes abrégées avec point médian dans une procédure critique ou un texte destiné à la synthèse vocale.

7.3. N'utilise pas une couleur ou une position visuelle comme seul moyen d'identifier un élément.

## Éléments intouchables

Conserve exactement :

- les blocs de code et le code en ligne ;
- les identifiants, commandes, options et chemins ;
- les messages d'erreur et extraits de journaux cités ;
- les noms de produits et les routes d'API ;
- les clés de configuration et les valeurs techniques.

Une commande ou un identifiant entre accents graves compte comme un mot pour la limite de phrase.

## Cas particuliers

- **Messages d'erreur** : indique le résultat, la cause connue, puis la correction.
- **Runbooks** : utilise des étapes impératives, une action par étape et les conditions en premier.
- **Rapports d'incident** : donne les heures, l'impact, la cause connue et les actions. Supprime les excuses génériques.
- **Notes de version** : décris un changement par entrée. Place la migration avant le risque de rupture.
- **Instructions d'agents** : écris chaque règle comme une instruction indépendante. Remplace « devrait » par « doit » ou supprime la règle.
- **Préparation à la traduction** : impose le glossaire, explicite les pronoms et conserve une structure grammaticale complète.

Consulte `references/use-cases.md` pour les modèles détaillés.

## Autocontrôle

Avant de livrer le texte :

1. Compte les mots des trois phrases les plus longues.
2. Coupe les instructions de plus de 20 mots.
3. Coupe les descriptions de plus de 25 mots.
4. Recherche « devrait », « pourrait », « il convient », « afin de », « au niveau de », « etc. » et les points-virgules.
5. Vérifie que chaque phrase avec « si » place la condition avant l'action.
6. Vérifie la cohérence de la terminologie.
7. Vérifie que les éléments intouchables restent exacts.

Corrige chaque problème avant de livrer. Pour un audit complet, utilise `references/checklist.md`.

## Limites

N'applique pas ce style aux textes marketing, littéraires ou éditoriaux, sauf demande explicite. Ce style supprime volontairement les effets de persuasion et de voix.

Ce skill est une adaptation non officielle inspirée de l'ASD-STE100 et de `AminBlg/SimpleEnglish`. Il ne garantit aucune conformité à l'ASD-STE100.
