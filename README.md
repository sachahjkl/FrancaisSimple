<p align="center">
  <strong>Votre IA écrit comme une brochure. Faites-la écrire comme un manuel technique.</strong>
</p>

<p align="center">
  Un skill pour produire une documentation technique en français clair, précis et cohérent.<br>
  Il adapte au français les principes du langage contrôlé ASD-STE100.
</p>

<p align="center">
  <a href="https://agentskills.io"><img src="https://img.shields.io/badge/SKILL.md-standard_Agent_Skills-blue?style=flat" alt="Agent Skills"></a>
  <a href="skills/francais-simple/SKILL.md"><img src="https://img.shields.io/badge/version-1.0.0-blue?style=flat" alt="version 1.0.0"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/licence-MIT-lightgrey?style=flat" alt="MIT"></a>
</p>

## Pourquoi

Les textes techniques générés par IA accumulent souvent les phrases longues, les synonymes inutiles et les formulations vagues. Français Simple impose des règles vérifiables :

- 20 mots au maximum pour une instruction ;
- 25 mots au maximum pour une description ;
- une action par instruction ;
- la condition avant l'action ;
- la voix active et des temps simples ;
- un seul terme pour chaque concept ;
- aucun remplissage ou argument commercial.

## Exemple

**Sans le skill :**

> Une erreur inattendue est malheureusement survenue lors de la tentative de connexion. Veuillez vous assurer que vos identifiants ont été correctement configurés avant de réessayer.

**Avec le skill :**

> La connexion à la base de données a échoué. Le mot de passe de l'utilisateur `app` est incorrect. Corrigez `DB_PASSWORD`, puis reconnectez-vous.

Consultez d'autres réécritures dans [`examples/before-after.md`](examples/before-after.md).

## Installation

```bash
npx skills add sachahjkl/FrancaisSimple
```

Le skill suit le [standard Agent Skills](https://agentskills.io). Il fonctionne avec Claude Code, Cursor, Codex, Gemini CLI, OpenCode et les outils compatibles.

Pour essayer le skill sans l'installer :

```bash
npx skills use sachahjkl/FrancaisSimple --skill francais-simple
```

Si votre outil ne prend pas en charge `SKILL.md`, utilisez [`prompts/system-prompt.md`](prompts/system-prompt.md).

## Contenu

- [`skills/francais-simple/SKILL.md`](skills/francais-simple/SKILL.md) : règles complètes ;
- [`skills/francais-simple/references/checklist.md`](skills/francais-simple/references/checklist.md) : contrôle avant livraison ;
- [`skills/francais-simple/references/use-cases.md`](skills/francais-simple/references/use-cases.md) : adaptations par type de texte ;
- [`output-styles/francais-simple.md`](output-styles/francais-simple.md) : style de sortie Claude Code ;
- [`prompts/system-prompt.md`](prompts/system-prompt.md) : prompt autonome ;
- [`examples/before-after.md`](examples/before-after.md) : exemples complets.
- [`NOTICE.md`](NOTICE.md) : origine du fork et portée de l'adaptation.

## Limites

L'ASD-STE100 définit le *Simplified Technical English*. Il ne définit pas de français technique simplifié. Ce projet reprend ses principes structurels et les adapte au français.

Le projet ne garantit donc aucune conformité ASD-STE100. Il ne remplace pas une validation humaine, terminologique, réglementaire ou métier.

## Inspiration et attribution

Ce dépôt est un fork et une adaptation française de [AminBlg/SimpleEnglish](https://github.com/AminBlg/SimpleEnglish), créé par AminBlg. La structure du skill, ses modes et plusieurs principes de contrôle proviennent de ce projet.

Les benchmarks du projet original mesurent des textes anglais. Ils ont été retirés de cette adaptation, car leurs résultats ne s'appliquent pas au français.

## Licence

Licence MIT. Le copyright et la licence du projet original sont conservés dans [`LICENSE`](LICENSE).

Projet non officiel, sans affiliation avec ASD ou STEMG. ASD-STE100 est une marque déposée d'ASD.
