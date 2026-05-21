# Changelog

Wszystkie istotne zmiany w projekcie matematic-readiness. Format: [Keep a Changelog](https://keepachangelog.com/), SEMVER.

## [Unreleased]

## [0.1.0-alpha] - 2026-05-21

### Added

- README.md z opisem produktu (audyt 30 pytan + Build vs Buy + skill Claude Code).
- LICENSE - CC BY-SA 4.0 z notka cherry-pick z OneC0de/legal-ai-architect-toolkit (MIT).
- CONSTITUTION.md v1.0.0 - 5 artykulow (neutralnosc dostawcow, RODO i tajemnica jako pierwsze, polski kontekst, scoring opisowy, audyt jako dialog).
- audit/CHECKLIST.md - 30 pytan w 5 polskich wymiarach (RODO compliance / tajemnica zawodowa / AI Act gotowosc / kompetencje zespolu / architektura techniczna).
- audit/SCORING.md - rubric oceny 1-5 z uzasadnieniem, przyklady per wymiar, anti-pattern "scoring sredni".
- audit/PROGRESSION_MAP.md - 5 poziomow (Eksplorator -> Adopter -> Konstruktor -> Architekt -> Orkiestrator) z polskimi opisami i typowymi rekomendacjami "co dalej".
- audit/REPORT_TEMPLATE.md - szablon raportu output (.docx).
- build-vs-buy/FRAMEWORK.md - 8 kryteriow z waga polskiego kontekstu, decision tree, scoring tabela.
- build-vs-buy/POLSKI_KONTEKST.md - RODO art. 44+, tajemnica zawodowa (PoA art. 6, URP art. 3), AI Act CELEX 32024R1689 z datami wejscia w zycie 2025-02 / 2025-08 / 2026-08 / 2027-08, DPF (decyzja Komisji 2023, podtrzymana Sad UE 2025-09-03).
- build-vs-buy/PLATFORMY.md - porownanie 9 opcji (Patron / Harvey / CoCounsel / Lexis AI / Ruli AI / LEX AI / Legalis AI / Mecenas AI / Claude Enterprise / ChatGPT Enterprise / Microsoft 365 Copilot / Cline + Ollama).
- build-vs-buy/TCO_CALCULATOR.md - koszt 3-letni dla 6 opcji (Buy US legal / Buy PL legal / Buy general Enterprise / Build minimalny / Build sredni / Build maximum) skalowany dla 1-100 osob.
- skills/matematic-readiness-audit/SKILL.md v0.1.0 - skill Claude Code prowadzacy audyt + opcjonalny Build vs Buy.
- examples/sample_audit_report.md - zanonimizowany przyklad raportu output dla kancelarii 8-osobowej typu Adopter.

### Architecture

- Cherry-pick patternu 5-poziomowego (Explorer -> Orchestrator) z OneC0de/legal-ai-architect-toolkit (MIT, Donna Scaffidi).
- Cherry-pick patternu 8-kryteriowego Build vs Buy z tego samego upstream.
- Wszystkie 30 pytan, scoring rubric, decision tree, polski kontekst regulacyjny, porownanie platform, TCO - napisane od zera pod polski rynek.
- 5 polskich wymiarow (R/T/A/K/I) zamiast US-centric narrative.
- Pozycja kancelarii = **minimum z wymiarow**, nie srednia (anti-pattern unikniony explicite).

### Known limitations

- Brak walidacji na zywym audycie kancelarii. v0.1.0-alpha jest pre-production.
- Tabela porownawcza platform (build-vs-buy/PLATFORMY.md) zawiera ceny **orientacyjne na 2026-05** - rynek ewoluuje szybko, sprawdzaj bezposrednio u dostawcow.
- Polskie SaaS legal AI (LEX AI, Legalis AI, Mecenas AI) sa we wczesnym etapie - opis bazuje na publicznie dostepnych komunikatach, niekoniecznie aktualnych.
- Skill `matematic-readiness-audit` testowany tylko na pojedynczych mock-audytach - wymagane 3-5 prawdziwych audytow przed v1.0.
