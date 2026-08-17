[English](README.md) | [Français](README.fr.md)

<p align="center">
  <strong>Your AI writes like a brochure. Make it write like a technical manual.</strong>
</p>

<p align="center">
  A skill for producing clear, precise, and consistent technical documentation in French.<br>
  It adapts the principles of the ASD-STE100 controlled language to French.
</p>

<p align="center">
  <a href="https://agentskills.io"><img src="https://img.shields.io/badge/SKILL.md-standard_Agent_Skills-blue?style=flat" alt="Agent Skills"></a>
  <a href="skills/francais-simple/SKILL.md"><img src="https://img.shields.io/badge/version-1.0.0-blue?style=flat" alt="version 1.0.0"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/licence-MIT-lightgrey?style=flat" alt="MIT"></a>
</p>

## Why

AI-generated technical texts often accumulate long sentences, unnecessary synonyms, and vague wording. Français Simple enforces verifiable rules:

- a maximum of 20 words for an instruction;
- a maximum of 25 words for a description;
- one action per instruction;
- the condition before the action;
- active voice and simple tenses;
- one term for each concept;
- no filler or marketing claims.

## Example

**Without the skill:**

> Une erreur inattendue est malheureusement survenue lors de la tentative de connexion. Veuillez vous assurer que vos identifiants ont été correctement configurés avant de réessayer.

**With the skill:**

> La connexion à la base de données a échoué. Le mot de passe de l'utilisateur `app` est incorrect. Corrigez `DB_PASSWORD`, puis reconnectez-vous.

See more rewrites in [`examples/before-after.md`](examples/before-after.md).

## Installation

```bash
npx skills add sachahjkl/FrancaisSimple
```

The skill follows the [Agent Skills standard](https://agentskills.io). It works with Claude Code, Cursor, Codex, Gemini CLI, OpenCode, and compatible tools.

To try the skill without installing it:

```bash
npx skills use sachahjkl/FrancaisSimple --skill francais-simple
```

If your tool does not support `SKILL.md`, use [`prompts/system-prompt.md`](prompts/system-prompt.md).

## Contents

- [`skills/francais-simple/SKILL.md`](skills/francais-simple/SKILL.md): complete rules;
- [`skills/francais-simple/references/checklist.md`](skills/francais-simple/references/checklist.md): pre-delivery check;
- [`skills/francais-simple/references/use-cases.md`](skills/francais-simple/references/use-cases.md): adaptations by text type;
- [`output-styles/francais-simple.md`](output-styles/francais-simple.md): Claude Code output style;
- [`prompts/system-prompt.md`](prompts/system-prompt.md): standalone prompt;
- [`examples/before-after.md`](examples/before-after.md): complete examples.
- [`NOTICE.md`](NOTICE.md): origin of the fork and scope of the adaptation.

## Limitations

ASD-STE100 defines *Simplified Technical English*. It does not define simplified technical French. This project takes its structural principles and adapts them to French.

The project therefore does not guarantee ASD-STE100 compliance. It does not replace human, terminology, regulatory, or domain validation.

## Inspiration and attribution

This repository is a fork and French adaptation of [AminBlg/SimpleEnglish](https://github.com/AminBlg/SimpleEnglish), created by AminBlg. The skill structure, its modes, and several control principles come from that project.

The original project's benchmarks measure English texts. They were removed from this adaptation because their results do not apply to French.

## License

MIT License. The original project's copyright and license are retained in [`LICENSE`](LICENSE).

Unofficial project with no affiliation with ASD or STEMG. ASD-STE100 is a registered trademark of ASD.
