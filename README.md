# matematic-readiness - audyt gotowosci kancelarii do AI

Otwarty pakiet narzedzi do oceny gdzie polska kancelaria jest na drodze do bezpiecznego, RODO-safe wdrozenia AI - i decyzji **build vs buy** dla kazdego konkretnego use case.

Dwa frameworki, jeden skill:

1. **Audyt gotowosci** ([audit/](audit/)) - 30 pytan w 5 polskich wymiarach (RODO / tajemnica zawodowa / AI Act / kompetencje zespolu / architektura), scoring 1-5 per wymiar, mapa progresji "gdzie jestes -> co dalej".
2. **Framework Build vs Buy** ([build-vs-buy/](build-vs-buy/)) - 8 kryteriow decyzyjnych z waga, polski kontekst regulacyjny (transfer danych poza EOG, tajemnica zawodowa, AI Act art. 6 high-risk), porownanie platform (Patron / Harvey / CoCounsel / Lexis AI / Ruli / ChatGPT Enterprise / Claude Max).
3. **Skill Claude Code** ([skills/matematic-readiness-audit/](skills/matematic-readiness-audit/)) - przeprowadza audyt przez prompty, produkuje raport .docx z rekomendacjami.

## Dla kogo

- **Managing Partner / wspolnik zarzadzajacy** - ktora kancelaria zastanawia sie nad wdrozeniem AI, ale nie wie od czego zaczac.
- **CTO / Office Manager / dyrektor operacyjny** - przygotowuje rekomendacje dla zarzadu.
- **Inspektor ochrony danych** - audytuje propozycje wdrozenia AI pod katem RODO.
- **Konsultant LegalTech** - prowadzi warsztaty diagnostyczne dla swoich klientow.

## Czego NIE robi

- NIE sprzedaje konkretnego produktu (Patron / Harvey / Ruli / inny) - to neutralny audyt.
- NIE zastepuje prawnika ani inspektora ochrony danych - to assessment narzedziowy, decyzje merytoryczne nalezace do specjalistow.
- NIE jest certyfikatem - to mapa pozycji, nie pieczatka jakosci.

## Filozofia

Audyt zaczyna sie od **gdzie jestes**, nie od **co kupic**. Pierwsza wartosc to **realistyczne zlokalizowanie**:

- Eksplorator (poziom 1) - pierwsze rozmowy w zespole, brak narzedzi, brak polityki.
- Adopter (poziom 2) - kilka osob uzywa ChatGPT/Claude prywatnie, brak governance.
- Konstruktor (poziom 3) - kancelaria ma polityke AI, kilka use case ow w produkcji.
- Architekt (poziom 4) - architektura AI zaplanowana, integracje z systemami kancelaryjnymi, mierzalny ROI.
- Orkiestrator (poziom 5) - AI w roli operacyjnej, audyt-trail per uzycie, ciagla optymalizacja.

Polskie kancelarie najczesciej mieszcza sie na poziomach 1-2. **Skok ponad poziom = przepalanie budzetu**. Audyt mowi co konkretnie zrobic zeby z poziomu N przejsc do N+1.

## Build vs Buy - polski kontekst

W swiecie anglosaskim "buy" znaczy zazwyczaj amerykanska platforme cloud-only (Harvey, CoCounsel, Ruli). W polskim kontekscie regulacyjnym ta opcja niesie **wprost flagi**:

- Transfer danych poza EOG (RODO art. 44+) - wymaga DPA, oceny adekwatnosci, dokumentacji DPF.
- Tajemnica zawodowa (Prawo o adwokaturze art. 6, Ustawa o radcach prawnych art. 3) - bezwzgledna, transfer akt sprawy do USA wymaga niemozliwej zgody klienta.
- AI Act art. 6 (high-risk AI w prawie) - od 2026-08-02 wymogi raportowania, audytu, transparentnosci dla okreslonych zastosowan.

Framework Build vs Buy pomaga zrozumiec **kiedy** te flagi sa krytyczne (czesto), a **kiedy** mniej istotne (rzadko, w polskiej kancelarii). Plus porownanie z polonijnymi platformami (LEX AI w przygotowaniu, Praktyczne, Mecenas AI) i alternatywami self-host (Patron, Cline + Ollama).

## Pochodzenie i atrybucja

Pattern strukturalny (Maturity Model 5-poziomowy, Build vs Buy 8 kryteriow) - cherry-pick z [OneC0de/legal-ai-architect-toolkit](https://github.com/OneC0de/legal-ai-architect-toolkit) (MIT, autorka Donna Scaffidi, Head of AI & Legal Innovation @ Ruli AI).

Tresc napisana od zera pod polski rynek: polskie wymiary RODO/tajemnica/AI Act zamiast US-centric criteria, scoring rubric ktorego upstream nie ma, decision tree ktorego upstream nie ma, porownanie konkretnych platform PL i US z perspektywy polskiej kancelarii.

## Licencja

[Creative Commons Uznanie autorstwa - Na tych samych warunkach 4.0 (CC BY-SA 4.0)](LICENSE).

Wolno kopiowac, modyfikowac, sprzedawac wdrozenia. Wymagamy zachowania atrybucji MateMatic + udostepnienia pochodnych na tej samej licencji.

## Powiazane

- [matematicsolutions/patron](https://github.com/matematicsolutions/patron) - "build" w naszym kontekscie (RODO-safe self-host agent AI).
- [matematicsolutions/lpm-pl](https://github.com/matematicsolutions/lpm-pl) - skille zarzadzania portfelem spraw, drugi krok po audycie gotowosci.
- [matematicsolutions/praxis](https://github.com/matematicsolutions/praxis) - przewodniki praktyczne LegalTech.

## Status

`v0.1.0-alpha` - pierwsza publikacja. Wymaga walidacji na 3-5 polskich kancelariach przed v1.0.
