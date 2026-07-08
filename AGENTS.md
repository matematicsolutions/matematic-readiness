# AGENTS.md - matematic-readiness

An [agents.md](https://agents.md) standard file (Linux Foundation / Agentic AI Foundation) - canonical instructions for AI agents working with this repository. Read natively by Cursor, Codex (OpenAI), Jules (Google), Devin / Windsurf, Aider, Amp, Factory, GitHub Copilot.

## Project goal

`matematic-readiness` is an **open toolkit for assessing a law firm's AI readiness** + a **Build vs Buy** decision framework with a Polish regulatory context (GDPR, professional secrecy, AI Act art. 6).

Three artifacts:

1. **Readiness audit** ([audit/](./audit/)) - 30 questions across 5 Polish dimensions (GDPR / professional secrecy / AI Act / team competence / architecture), 1-5 scoring, a 5-level progression map (Explorer -> Adopter -> Constructor -> Architect -> Orchestrator).
2. **Build vs Buy** ([build-vs-buy/](./build-vs-buy/)) - 8 weighted decision criteria, comparison of 9 platforms (Patron / Harvey / CoCounsel / Lexis AI / Ruli / ChatGPT Enterprise / Claude Max / LEX AI / Mecenas), 3-year TCO.
3. **Claude Code skill** ([skills/matematic-readiness-audit/](./skills/matematic-readiness-audit/)) - runs the audit through prompts, produces a `.docx` report.

## MateMatic context (HARD CONSTRAINTS)

The repo is maintained by [MateMatic Solutions](https://matematicsolutions.com). This is a **lead-generation artifact in the sales ladder** (audit 2-5k -> AI Constitution 15-40k -> deployment 30-150k) - but **NOT a pitch deck**. Hard editorial rule:

- **Neutrality** - the audit does not sell Patron or any specific product. Written from the perspective of "what a law firm needs to know", not "what to buy".
- **Polish regulatory context first** - every recommendation references PoA art. 6 / URP art. 3 / GDPR / AI Act (CELEX 32024R1689). No reference = no value.
- **No marketing** - if you read a draft and it sounds like a sales deck, it is wrong. Internal content review, 2 rounds, BEFORE commit.

## Repo structure

```
audit/                     - 30 questions across 5 dimensions + scoring rubric + interpretation
build-vs-buy/              - 8 criteria + decision tree + comparison of 9 platforms + TCO
skills/
  matematic-readiness-audit/ - Claude Code skill for running the audit
examples/                  - anonymized examples of audit reports
CONSTITUTION.md            - editorial rules (neutrality, Polish context, anti-pitch)
CHANGELOG.md               - version history (v0.1.0-alpha)
```

## Build and test

The repo is Markdown documents + a Claude Code skill. No compilation.

"Test" = running the audit against **3 law firm archetypes** (solo practitioner / firm of 5-15 people / firm of 50+) - the result must differ for each (if they all come out at "level 1", the scoring is wrong).

Skill installation (Claude Code):

```bash
cd ~/.claude/skills/
git clone https://github.com/matematicsolutions/matematic-readiness
ln -s matematic-readiness/skills/matematic-readiness-audit matematic-readiness-audit
```

On Windows, use a folder copy instead of a symlink.

## Writing rules (CRITICAL)

- **Polish language throughout** - no calques from English-language materials (the upstream audit was US-centric; we write for the Polish market).
- **CELEX for the AI Act** (32024R1689), **article numbers for GDPR/PoA/URP** - precise citations.
- **5 Polish dimensions** in the audit (do not copy the 9 NIST AI RMF ones) - this is MateMatic's own framework.
- **No "solutions in 4 steps"**, no "transformation", no "innovativeness" - check the anti-pattern list in [CONSTITUTION.md](./CONSTITUTION.md).
- **Internal review, 2 rounds** before every commit that changes the audit content.
- **Build vs Buy does not praise anyone** - Patron is to be one of 9 platforms with neutral scoring, not a "MateMatic recommendation".
- **No Polish diacritics in commit messages**.

## What NOT to do (hard rules)

- **Do NOT put a specific product recommendation** in the audit. The audit says "your firm is at level N, X and Y are missing" - the Build vs Buy decision is a separate document.
- **Do NOT add US-only platforms** without a Polish alternative in the comparison.
- **Do not lower the bar for law firms** to "make them fit the upstream framework" - reality is what it is (most sit at level 1-2), and that is precisely the value of this audit.
- **Do NOT commit real law firm data** in `examples/` - only anonymized archetypes.

## Sources of truth (reading order)

1. [README.md](./README.md) - description for humans
2. [CONSTITUTION.md](./CONSTITUTION.md) - editorial rules
3. [audit/](./audit/) - 30 questions + rubric
4. [build-vs-buy/](./build-vs-buy/) - 8 criteria + platform comparison
5. [CHANGELOG.md](./CHANGELOG.md) - version history

## Agent compatibility

The [AGENTS.md](https://agents.md) standard. For Claude Code there is an additional [CLAUDE.md](./CLAUDE.md) file.

The `matematic-readiness-audit` skill is written for Claude Code, but the prompts are agent-agnostic - porting to Cursor / Codex requires only frontmatter adaptation.

## License and attribution

- **CC BY-SA 4.0** - see [LICENSE](./LICENSE). You may copy, modify, and sell deployments. We require attribution to MateMatic + sharing derivatives under the same license.
- Structural pattern (5-level Maturity Model, 8-criteria Build vs Buy): cherry-picked from [OneC0de/legal-ai-architect-toolkit](https://github.com/OneC0de/legal-ai-architect-toolkit) (MIT, author Donna Scaffidi).
- Content written from scratch for the Polish market.

Citation: *MateMatic Solutions (2026), matematic-readiness - a law firm AI readiness audit, https://github.com/matematicsolutions/matematic-readiness, CC BY-SA 4.0.*
