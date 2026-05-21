# AGENTS.md - matematic-readiness

Plik standardu [agents.md](https://agents.md) (Linux Foundation / Agentic AI Foundation) - kanoniczne instrukcje dla agentow AI pracujacych z tym repozytorium. Czytany natywnie przez Cursor, Codex (OpenAI), Jules (Google), Devin / Windsurf, Aider, Amp, Factory, GitHub Copilot.

## Cel projektu

`matematic-readiness` to **otwarty pakiet narzedzi do oceny gotowosci polskiej kancelarii do AI** + framework decyzyjny **Build vs Buy** z polskim kontekstem regulacyjnym (RODO, tajemnica zawodowa, AI Act art. 6).

Trzy artefakty:

1. **Audyt gotowosci** ([audit/](./audit/)) - 30 pytan w 5 polskich wymiarach (RODO / tajemnica zawodowa / AI Act / kompetencje zespolu / architektura), scoring 1-5, mapa progresji 5-poziomowa (Eksplorator -> Adopter -> Konstruktor -> Architekt -> Orkiestrator).
2. **Build vs Buy** ([build-vs-buy/](./build-vs-buy/)) - 8 kryteriow decyzyjnych z waga, porownanie 9 platform (Patron / Harvey / CoCounsel / Lexis AI / Ruli / ChatGPT Enterprise / Claude Max / LEX AI / Mecenas), TCO 3-letni.
3. **Skill Claude Code** ([skills/matematic-readiness-audit/](./skills/matematic-readiness-audit/)) - przeprowadza audyt przez prompty, produkuje raport `.docx`.

## Kontekst MateMatic (TWARDE OGRANICZENIA)

Repo prowadzi [MateMatic Solutions](https://matematicsolutions.com). To jest **leadgenowy artefakt drabiny sprzedazowej** (audyt 2-5k -> Konstytucja AI 15-40k -> wdrozenie 30-150k) - ale **NIE pitch deck**. Twarda zasada redakcyjna:

- **Neutralnosc** - audyt nie sprzedaje Patrona ani zadnego konkretnego produktu. Pisany z perspektywy "co kancelaria potrzebuje wiedziec", nie "co kupic".
- **Polski kontekst regulacyjny first** - kazda rekomendacja ma odniesienie do PoA art. 6 / URP art. 3 / RODO / AI Act (CELEX 32024R1689). Bez referencji = bez wartosci.
- **Bez marketingu** - jezeli czytasz draft i brzmi jak sales deck, jest zly. Marko-pl loop 2x runda PRZED commit ([feedback w MEMORY MateMatic](https://github.com/matematicsolutions)).

## Struktura repo

```
audit/                     - 30 pytan w 5 wymiarach + scoring rubric + interpretacja
build-vs-buy/              - 8 kryteriow + decision tree + porownanie 9 platform + TCO
skills/
  matematic-readiness-audit/ - skill Claude Code do przeprowadzenia audytu
examples/                  - zanonimizowane przyklady raportow audytu
CONSTITUTION.md            - zasady redakcyjne (neutralnosc, polski kontekst, anti-pitch)
CHANGELOG.md               - historia wersji (v0.1.0-alpha)
```

## Build i test

Repo to dokumenty Markdown + skill Claude Code. Brak kompilacji.

"Test" = przeprowadzenie audytu na **3 archetypach kancelarii** (solo praktyk / kancelaria 5-15 osob / kancelaria 50+) - wynik musi byc rozny dla kazdego (jezeli wszystkie wychodza "poziom 1" to scoring jest zly).

Instalacja skill (Claude Code):

```bash
cd ~/.claude/skills/
git clone https://github.com/matematicsolutions/matematic-readiness
ln -s matematic-readiness/skills/matematic-readiness-audit matematic-readiness-audit
```

Na Windows zamiast symlinka - kopia folderu.

## Zasady pisania (CRITICAL)

- **Polski jezyk wszedzie** - bez kalek z angielskich materialow (audit upstream byl US-centric, my piszemy pod PL).
- **CELEX dla AI Act** (32024R1689), **art. dla RODO/PoA/URP** - precyzyjne cytaty.
- **5 polskich wymiarow** w audicie (nie kopiuj 9 NIST AI RMF) - to wlasna ramka MateMatic.
- **Bez "rozwiazan w 4 krokach"**, bez "transformacji", bez "innowacyjnosci" - sprawdz lista anti-patternow w [CONSTITUTION.md](./CONSTITUTION.md).
- **Marko-pl 2x runda** przed kazdym commitem zmieniajacym tresc audytu.
- **Build vs Buy nie zachwala nikogo** - Patron ma byc jedna z 9 platform z neutralnym scoringiem, nie "rekomendacja MateMatic".
- **Bez polskich znakow w commit messages**.

## Czego NIE robic (twarde reguly)

- **NIE wpisuj rekomendacji konkretnego produktu** w audicie. Audyt mowi "twoja kancelaria jest na poziomie N, brakuje X i Y" - decyzja Build vs Buy jest osobnym dokumentem.
- **NIE dodawaj US-only platform** bez polskiej alternatywy w porownaniu.
- **NIE obniżaj poziomu polskim kancelariom** "zeby pasowalo do framework upstream" - rzeczywistosc jest taka jaka jest (wiekszosc na poziomie 1-2), to wlasnie wartosc tego audytu.
- **NIE commituj prawdziwych danych kancelarii** w `examples/` - tylko zanonimizowane archetypy.

## Zrodla prawdy (kolejnosc czytania)

1. [README.md](./README.md) - opis dla ludzi
2. [CONSTITUTION.md](./CONSTITUTION.md) - zasady redakcyjne
3. [audit/](./audit/) - 30 pytan + rubryka
4. [build-vs-buy/](./build-vs-buy/) - 8 kryteriow + porownanie platform
5. [CHANGELOG.md](./CHANGELOG.md) - historia wersji

## Kompatybilnosc agentow

Standard [AGENTS.md](https://agents.md). Dla Claude Code dodatkowo plik [CLAUDE.md](./CLAUDE.md).

Skill `matematic-readiness-audit` pisany pod Claude Code, ale prompty sa agent-agnostic - przeniesienie na Cursor / Codex wymaga tylko adaptacji frontmatter.

## Licencja i atrybucja

- **CC BY-SA 4.0** - patrz [LICENSE](./LICENSE). Mozesz kopiowac, modyfikowac, sprzedawac wdrozenia. Wymagamy atrybucji MateMatic + udostepnienia pochodnych na tej samej licencji.
- Pattern strukturalny (Maturity Model 5-poziomowy, Build vs Buy 8 kryteriow): cherry-pick z [OneC0de/legal-ai-architect-toolkit](https://github.com/OneC0de/legal-ai-architect-toolkit) (MIT, autorka Donna Scaffidi).
- Tresc napisana od zera pod polski rynek.

Cytowanie: *MateMatic Solutions (2026), matematic-readiness - audyt gotowosci polskiej kancelarii do AI, https://github.com/matematicsolutions/matematic-readiness, CC BY-SA 4.0.*
