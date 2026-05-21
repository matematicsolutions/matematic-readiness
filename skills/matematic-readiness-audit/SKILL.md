---
name: matematic-readiness-audit
version: 0.1.0
description: Przeprowadza audyt gotowosci polskiej kancelarii do wdrozenia AI - 30 pytan w 5 wymiarach (RODO compliance / tajemnica zawodowa / AI Act gotowosc / kompetencje zespolu / architektura techniczna), scoring 1-5 per pytanie z uzasadnieniem, umieszcza kancelarie na 5-poziomowej mapie progresji (Eksplorator -> Adopter -> Konstruktor -> Architekt -> Orkiestrator), generuje raport .docx z lista priorytetow na 90 dni. Plus opcjonalnie wykonuje framework Build vs Buy dla konkretnego use case (8 kryteriow z waga, polski kontekst regulacyjny). Uzywaj gdy uzytkownik mowi "zrob audyt AI dla kancelarii X", "ocena gotowosci [klient] do AI", "build vs buy [use case]", "polskie ryzyka AI dla kancelarii", "ile kosztuje AI w kancelarii", "od czego zaczac z AI". NIE uzywaj do audytu RODO konkretnego procesu (to robi IOD), audytu produktu pod katem AI Act (to robi notified body), audytu konkretnego skille AI (od tego sa testy A/B i benchmarki). Skill jest narzedziem **diagnostycznym**, nie rekomendacyjnym - decyzje zostaja w kancelarii.
---

# MateMatic Readiness Audit

Skill prowadzi audyt gotowosci kancelarii do wdrozenia AI. Przeprowadza rozmowe z managing partnerem (lub zarzadem) wedlug 30 pytan w 5 wymiarach, scoring kazdego pytania 1-5 z uzasadnieniem, klasyfikuje kancelarie na 5-poziomowej mapie progresji, generuje raport z lista priorytetow.

Skill **NIE jest ankieta do wypelnienia w 5 minut**. To **prowadzony dialog** trwajacy 60-90 minut z dokumentacja.

## 1. Kiedy uzywac

### Triggery

- "Zrob audyt AI dla kancelarii X"
- "Ocena gotowosci [klient] do AI"
- "Od czego zaczac z AI w kancelarii"
- "Build vs buy dla [use case]"
- "Ile bedzie kosztowac AI dla kancelarii [X] osob"
- "Polskie ryzyka AI dla kancelarii"

### Kiedy NIE uzywac

- Audyt RODO konkretnego procesu - to IOD lub partner z certyfikatem RODO.
- Audyt AI Act dla produktu (provider) - to notified body.
- Benchmark konkretnego modelu (Claude vs GPT-5) - to testy A/B i wlasciwy ewaluator.
- Audyt jakosci konkretnego skill / promptu - to evaluation harness.
- Audyt klienta kancelarii (nie samej kancelarii) - to inny zakres pracy.

## 2. Metodyka rdzenia

### 2.1 Trzy zasady audytu

1. **RODO i tajemnica to pierwsze pytania**, nie ostatnie. Wymiary R i T sa lokowane jako 1 i 2 z premedytacja.
2. **Scoring opisowy, nie liczbowy bez podstawy**. Kazdy punkt ma uzasadnienie tekstowe (Konstytucja Art. 4). Liczba bez slow = pieczatka pseudonaukowa.
3. **Pozycja = minimum z wymiarow**, nie srednia. Krytyczna luka RODO unicestwia zaawansowane kompetencje techniczne. (Patrz [PROGRESSION_MAP.md](../../audit/PROGRESSION_MAP.md).)

### 2.2 Neutralnosc dostawcow

Skill **NIE rekomenduje konkretnego produktu** jako odpowiedz na audyt. Skill mowi gdzie kancelaria jest i co ma zrobic na nastepny poziom. Wybor narzedzia (Patron, Harvey, CoCounsel, LEX AI, Claude Enterprise) jest wtorny i odbywa sie w osobnym Build vs Buy.

Wyjatek: jezeli Build vs Buy jest wywolany w audycie - skill moze wskazac konkretne platformy z porownaniem alternatyw i jawnie nazwanymi ograniczeniami.

### 2.3 Polski kontekst regulacyjny

Skill **CYTUJE konkretne polskie i unijne akty**:
- RODO (CELEX 32016R0679) - art. 5/9/25/30/32/33/35/44+.
- Ustawa Prawo o adwokaturze art. 6 - tajemnica.
- Ustawa o radcach prawnych art. 3 - tajemnica.
- AI Act (CELEX 32024R1689) - art. 4/5/6/11/12/26/50/51 + Annex III.
- KEA / KEZRP - obowiazki etyczne.

Tone "uwaga, RODO!" bez wskazania artykulu jest **niedopuszczalny**.

## 3. Wejscie

### Wymagane

- **Dostep do rozmowy** z managing partnerem (lub upowaznionym czlonkiem zarzadu) + IT/Office Manager + IOD (jezeli istnieje).
- **60-90 minut** czasu na pelen audyt.

### Opcjonalne

- **Pisemne dokumenty** kancelarii: polityka AI (jezeli istnieje), RCP, DPIA, mapa systemow IT, umowa z dostawcami (DPA).
- **Konkretne use case y** ktorymi kancelaria sie interesuje (jezeli ma wybor) - audyt moze byc rozszerzony o Build vs Buy per use case.

## 4. Wyjscie

### 4a. Raport audytu

**Plik**: `[Kancelaria]_audyt_AI_[YYYY-MM-DD].docx` z naglowkiem MateMatic (lub zewnetrznego audytora).

Struktura (template w `templates/audit_report_template.md`):

1. Streszczenie wykonawcze - pozycja kancelarii, 5 sum, glowne wnioski, rekomendacja 90 dni.
2. Wymiar 1 - RODO compliance (6 ocen z uzasadnieniem).
3. Wymiar 2 - Tajemnica zawodowa (6 ocen).
4. Wymiar 3 - AI Act gotowosc (6 ocen).
5. Wymiar 4 - Kompetencje zespolu (6 ocen).
6. Wymiar 5 - Architektura techniczna (6 ocen).
7. Lista priorytetow na 90 dni (3-5 dzialan).
8. Rekomendacja Build vs Buy (jezeli wywolany).
9. Termin nastepnego audytu (6-12 miesiecy).

### 4b. Opcjonalny output - Build vs Buy dla konkretnego use case

**Plik**: `[Kancelaria]_build_vs_buy_[UseCase]_[YYYY-MM-DD].docx`.

Struktura (template w `templates/build_vs_buy_template.md`):

1. Use case - opis.
2. Tabela 8 kryteriow z ocena Build/Buy + waga + zwyciezca.
3. Suma wag.
4. Rekomendacja z uzasadnieniem.
5. Plan implementacji.
6. Kalkulator TCO 3-letni (z [TCO_CALCULATOR.md](../../build-vs-buy/TCO_CALCULATOR.md)).

## 5. Workflow (7 krokow)

### Krok 1 - Przygotowanie

Skill pyta o:
- Nazwa kancelarii.
- Liczba osob w kancelarii (wplyw na TCO).
- Specjalizacja (cywilne / karne / gospodarcze / publiczne / international).
- Glowne use case y interesujace (research / contract review / drafting / due diligence / litigation support).
- Dostepni uczestnicy rozmowy (managing partner / IT / IOD).

### Krok 2 - Wymiar 1: RODO compliance

Skill zadaje 6 pytan z [CHECKLIST.md](../../audit/CHECKLIST.md) sekcja Wymiar 1. Per pytanie:
- Zadaje pytanie w wersji rozwinetej (nie wprost kopia z checklisty - jako rozmowa).
- Slucha odpowiedzi.
- Stosuje [SCORING.md](../../audit/SCORING.md) rubric.
- Zaznacza ocene 1-5 z uzasadnieniem.
- Jezeli scoring niepewny - zadaje pytanie kontrolne.

### Krok 3 - Wymiar 2: Tajemnica zawodowa

Jak krok 2. Pytanie T6 (test sprawdzajacy) wymaga szczegolnej uwagi - jezeli odpowiedz "nie naruszenie dopoki nie ma wycieku z platformy" -> scoring 1, automatyczne ostrzezenie w raporcie.

### Krok 4 - Wymiar 3: AI Act gotowosc

Jak krok 2.

### Krok 5 - Wymiar 4 i 5: Kompetencje + Architektura

Jak krok 2. Wymiar 5 (architektura) wymaga uczestnictwa IT / CTO / Office Managera - jezeli nie dostepny, scoring opisowy "wymaga doprecyzowania".

### Krok 6 - Obliczenia + identyfikacja poziomu

Skill liczy:
- Sumy per wymiar.
- Suma pelna (30-150).
- Minimum z wymiarow (kluczowe dla pozycji).
- Pozycja na 5-poziomowej skali ([PROGRESSION_MAP.md](../../audit/PROGRESSION_MAP.md)).

Identyfikuje:
- 3-5 slabych pytan (ocena 1-2).
- 3-5 silnych pytan (ocena 4-5).
- Lista priorytetow z PROGRESSION_MAP "co dalej dla poziomu X".

### Krok 7 - Generowanie raportu + opcjonalnie Build vs Buy

Skill wypelnia [audit_report_template.md](templates/audit_report_template.md) i zapisuje .docx.

Jezeli uczestnik wywoluje Build vs Buy - przeplywa 8 kryteriow z [FRAMEWORK.md](../../build-vs-buy/FRAMEWORK.md), korzystajac z [PLATFORMY.md](../../build-vs-buy/PLATFORMY.md) jako referencji.

Jezeli pozycja kancelarii = Eksplorator (poziom 1) - skill **propunuje przelozenie Build vs Buy** na audyt poziomu 2-3. Eksplorator nie powinien decydowac o Build vs Buy zanim nie ma podstaw.

## 6. Cross-skill handoff

### Czyta od

- `[Kancelaria]_polityka_AI.md` (jezeli istnieje) - kontekst.
- `[Kancelaria]_RCP.md` (jezeli istnieje) - czynnosci przetwarzania.
- `[Kancelaria]_mapa_IT.md` (jezeli istnieje) - architektura.

### Pisze do

- `[Kancelaria]_audyt_AI_[YYYY-MM-DD].docx` - raport.
- `[Kancelaria]_build_vs_buy_[UseCase]_[YYYY-MM-DD].docx` (opcjonalnie).
- `[Kancelaria]_LPM_Memory.md` (jezeli kancelaria uzywa [lpm-pl](https://github.com/matematicsolutions/lpm-pl)) - aktualizacja "ostatni audyt AI: [data], poziom: [X]".

### Handoff points

- Po raporcie audytu, jezeli wynik = Architekt/Orkiestrator (poziom 4-5) - skill PROPONUJE konkretne use case y do dalszej automatyzacji.
- Po raporcie, jezeli wynik = Eksplorator (poziom 1) z slabym RODO - skill PROPONUJE **najpierw** audyt RODO przez IOD ZANIM jakiekolwiek AI.

## 7. Antywzorce

### NIE rekomenduj Patrona/produktu jako odpowiedz na audyt

Audyt **diagnozuje**. Decyzja produktowa nastepuje w osobnym Build vs Buy.

### NIE skacz ponad poziom

Eksplorator do Architekta w 6 miesiecy = przepalanie budzetu. Rekomendacje zawsze "+1 poziom".

### NIE wpisuj scoringu bez uzasadnienia

Kazdy punkt ma uzasadnienie tekstowe. Jezeli scoring jest nieskreslony bo audytor sie spieszy - zatrzymaj audyt, dopytuj.

### NIE redukuj audytu do checklisty

To dialog 60-90 minut z dokumentacja. NIE 30 pytan w formularzu Google.

### NIE oceniaj kancelarii za nieznanymi danymi

Jezeli uczestnik nie wie odpowiedzi - scoring 1 (Nieznane). NIE wymyslaj punktow z kontekstu.

### NIE wystawiaj certyfikatu

Audyt to mapa pozycji, NIE pieczatka jakosci. **Nigdy** "kancelaria jest zgodna z RODO" - tylko "kancelaria ma scoring X/30 w wymiarze R".

---

## Wymagane sprawdzenia po raporcie

```
PRZED PRZEKAZANIEM RAPORTU KLIENTOWI 5 PUNKTOW:

1. Kazda ocena 1-5 MA uzasadnienie tekstowe (nie sama liczba).
2. Pozycja = minimum z wymiarow (nie srednia).
3. Lista priorytetow 90 dni = konkretne dzialania (z wlasicielem i terminem), nie "popraw RODO".
4. Cytaty prawne maja CELEX / nr ustawy + brzmienie, nie parafraze.
5. Brak named-firm atrybucji konkurencyjnych ("Harvey jest zly") - opis przez kryteria.

Skill jest narzedziem diagnostycznym. Decyzje merytoryczne nalezace do prawnika + IOD.
```

---

## Dziennik szlifu

- **2026-05-21** v0.1.0 - pierwsza wersja. Cherry-pick patternu 5-poziomowego z OneC0de/legal-ai-architect-toolkit (MIT). 30 pytan w 5 polskich wymiarach napisane od zera. Scoring rubric DODANY (upstream go nie ma). Decision tree DODANE. Polski kontekst regulacyjny (PoA art. 6, URP art. 3, KEA, KEZRP, AI Act CELEX 32024R1689, DPF) DODANY.
