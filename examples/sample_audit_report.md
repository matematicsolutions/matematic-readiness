# Raport audytu gotowosci kancelarii do AI - Kancelaria Przyklad sp.k.

> Zanonimizowany przyklad raportu wygenerowanego przez skill matematic-readiness-audit. Nazwy, dane, oceny fikcyjne. Realistyczna kancelaria 8 osob, specjalizacja gospodarcza, srednio zaawansowana w temacie AI.

| Klient audytu | Kancelaria Przyklad sp.k. |
|---|---|
| Audytor | Konsultant MateMatic |
| Data audytu | 2026-05-15 |
| Czas trwania | 75 minut |
| Osoby uczestniczace | Managing Partner (1) + Office Manager (1) |

---

## 1. Streszczenie wykonawcze

**Pozycja kancelarii**: Poziom **2 (Adopter)**.

**Pelna ocena**:
- Wymiar 1 - RODO compliance: **14/30**
- Wymiar 2 - Tajemnica zawodowa: **12/30** *(minimum, decydujace)*
- Wymiar 3 - AI Act gotowosc: **8/30**
- Wymiar 4 - Kompetencje zespolu: **17/30**
- Wymiar 5 - Architektura techniczna: **15/30**
- **Suma**: 66/150
- **Minimum z wymiarow**: 8/30 (decydujace dla poziomu)

**Glowne wnioski**:

Kancelaria jest **typowym Adopterem** - kilka osob uzywa AI z subskrypcjami (Claude Pro, ChatGPT Plus), ale brak systemu. Mocnym punktem sa **kompetencje zespolu** (champion AI istnieje, eksperymentowanie w piaskownicy). Najslabszym wymiarem jest **AI Act gotowosc** (8/30) - kancelaria nie sledzila wejscia w zycie obowiazku AI literacy z art. 4 (2025-02-02, juz minelo). Drugi problem to **tajemnica zawodowa** (12/30) - brak klauzul w umowach, brak procedury dla bezplatnych narzedzi.

**Rekomendacja na najblizsze 90 dni**:

Najwyzszy priorytet = **AI Act art. 4 - AI literacy obowiazkowy** (juz po terminie, kancelaria ma to spelnic asap). Drugi priorytet = klauzula tajemnicy zawodowej w umowach. Trzeci = DPIA dla glownych use case ow. Po tych 3 dzialaniach kancelaria ma podstawy do podjecia decyzji Build vs Buy.

---

## 2. Wymiar 1: RODO compliance (14/30)

### Ocena per pytanie

| # | Pytanie | Ocena | Uzasadnienie |
|---|---|---|---|
| R1 | Kategoryzacja danych | 3/5 | Wspolnik wymienia kategorie ("klienci gospodarczy, ich pracownicy, kontrahenci"), brak spisanej tabeli. Sklasyfikowane sporadycznie w opisie sprawy. |
| R2 | Mapa transferow do panstw trzecich | 2/5 | Wie ze Microsoft 365 jest "gdzies w UE", nie sprawdzal DPA. Brak DPA dla Claude Pro (zywe konto prywatne wspolnika). |
| R3 | Polityka korzystania z AI | 2/5 | Powiedziane na spotkaniu zespolu "uwazajcie z AI", brak pisemnej polityki. |
| R4 | Procedura zgloszenia incydentu | 3/5 | Procedura RODO istnieje z 2018, niezaktualizowana o AI. |
| R5 | Rejestr czynnosci przetwarzania | 2/5 | RCP istnieje, brak czynnosci "uzycie generatywnej AI". |
| R6 | DPIA | 2/5 | DPIA dla SIP Lex zrobiona w 2020. Brak DPIA dla narzedzi AI. |

### Wnioski

Kancelaria zaczela podstawowe RODO w 2018 (Microsoft 365 wdrozony z polityka), ale **nie zaktualizowala o AI**. Krytyczne dzialanie: DPIA dla narzedzi AI uzywanych przez zespol (Claude Pro, ChatGPT Plus). Plus aktualizacja RCP i procedury incydentu.

---

## 3. Wymiar 2: Tajemnica zawodowa (12/30) - **minimum z wymiarow, decydujace dla pozycji**

### Ocena per pytanie

| # | Pytanie | Ocena | Uzasadnienie |
|---|---|---|---|
| T1 | Mapa narzedzi AI w obrocie kancelarii | 2/5 | Wspolnik wymienia "Claude, ChatGPT, czasami Gemini", nie wie czy aplikanci nie uzywaja DeepL czy GPTs niestandardowych. |
| T2 | Klauzula w umowach z klientami | 1/5 | Umowy stare, brak klauzuli AI. Wspolnik mowi "doliczymy aneks gdy bedzie potrzeba". |
| T3 | Klauzula w umowach z pracownikami | 2/5 | Klauzula tajemnicy ogolna ("dane klientow chronione"), brak specyfiki AI. |
| T4 | Procedura dla bezplatnych narzedzi | 1/5 | Brak procedury. Wspolnik mowi "kazdy ma swoja glowe". Aplikanci moga uzywac darmowego ChatGPT. |
| T5 | Stanowisko izby (NRA / KIRP) | 3/5 | Wspolnik czytal stanowisko NRA z 2024, stosuje "z duza ostroznoscia". |
| T6 | Test sprawdzajacy (art. 6 PoA / art. 3 URP) | 3/5 | Wspolnik wie ze "nie wolno wgrywac aktow do darmowego ChatGPT", umie powiedziec o tajemnicy ale **nie cytuje konkretnego artykulu**. |

### Wnioski

**Najslabszy wymiar.** Pytania T2, T4 z ocena 1 = krytyczne luki. Klauzula tajemnicy w umowach z klientami **musi byc** aktualizowana przed kazdym wdrozeniem AI poza biezacym pracownikiem. Procedura dla bezplatnych narzedzi **musi byc** napisana - obecny stan to ryzyko dyscyplinarki.

---

## 4. Wymiar 3: AI Act gotowosc (8/30)

### Ocena per pytanie

| # | Pytanie | Ocena | Uzasadnienie |
|---|---|---|---|
| A1 | Klasyfikacja systemow AI | 1/5 | Wspolnik nie zna podzialu prohibited / high-risk / GPAI / minimal. |
| A2 | Audyt high-risk | 1/5 | Brak. |
| A3 | Transparentnosc (art. 50) | 2/5 | Wspolnik mowi klientowi "wykorzystujemy nowoczesne narzedzia" bez konkretu. |
| A4 | AI literacy (art. 4) | 1/5 | **Termin minal 2025-02-02. Brak realizacji.** |
| A5 | Procedura w razie naruszenia | 1/5 | Nie wie kto egzekwuje AI Act w Polsce. |
| A6 | Daty wejscia w zycie | 2/5 | Wspolnik wie ze "AI Act dziala", nie zna konkretnych dat. |

### Wnioski

**AI Act = krytyczne pole nieugruntowane.** Art. 4 (AI literacy) **juz po terminie** (2025-02-02) - kancelaria musi to spelnic asap. Brak klasyfikacji systemow AI nie pozwala ocenic ryzyka regulatorskiego.

---

## 5. Wymiar 4: Kompetencje zespolu (17/30) - **najmocniejszy wymiar**

### Ocena per pytanie

| # | Pytanie | Ocena | Uzasadnienie |
|---|---|---|---|
| K1 | Mapa kompetencji | 3/5 | Wspolnik wie kto sie zna na AI ("aplikant Jan dobrze, Anna podstawowo"). Nieformalna. |
| K2 | Szkolenia | 2/5 | Brak dedykowanego szkolenia, indywidualne kursy online. |
| K3 | Eksperymentowanie w piaskownicy | 4/5 | Konto Claude Pro wspolnika dziala jako piaskownica zespolu. |
| K4 | Identyfikacja championa | 4/5 | Aplikant Jan funkcjonuje jako nieformalny champion. |
| K5 | Prompt engineering | 2/5 | Bazowy. Zespol nie zna roznicy miedzy promptem zerowym a few-shot. |
| K6 | Halucynacje i weryfikacja | 2/5 | Wspolnik wie czym jest halucynacja, brak formalnej procedury weryfikacji. |

### Wnioski

Mocna baza. Champion istnieje, piaskownica dziala. **Brakuje formalizacji** - szkolenia dla calego zespolu, procedury weryfikacji, mapy kompetencji na papierze.

---

## 6. Wymiar 5: Architektura techniczna (15/30)

### Ocena per pytanie

| # | Pytanie | Ocena | Uzasadnienie |
|---|---|---|---|
| I1 | Mapa systemow kancelaryjnych | 3/5 | Office Manager zna systemy (Microsoft 365, Lex Kancelaria, Comarch ERP), brak diagramu. |
| I2 | Hosting i lokalizacja | 3/5 | Microsoft 365 EU Data Boundary skonfigurowane. Comarch lokalnie. Lex serwery w PL. |
| I3 | Backup i ciaglosc dzialania | 3/5 | Backup w chmurze (Microsoft 365). Brak planu BCP/DRP. |
| I4 | Mozliwosc self-host AI | 1/5 | Serwer kancelarii bez GPU. Self-host LLM niemozliwy obecnie. |
| I5 | Single Sign-On i kontrola dostepu | 3/5 | M365 SSO. Comarch i Lex osobne konta. Brak centralnego IDP. |
| I6 | Logging i audit trail | 2/5 | M365 logi standardowe. Brak audit trail per uzycie AI. |

### Wnioski

Sredni poziom. Infrastruktura Microsoft 365 dobrze ustawiona z EU Data Boundary - to atut. Slaba strona to brak GPU dla self-host AI (uniemozliwia opcje Build maximum z lokalnym modelem).

---

## 7. Lista priorytetow na 90 dni

| # | Dzialanie | Wymiar | Wlasciciel | Termin |
|---|---|---|---|---|
| 1 | **AI literacy szkolenie obowiazkowe dla zespolu** (art. 4 AI Act, juz po terminie) | A4 | Office Manager + Konsultant zewn. | 2026-06-30 (asap) |
| 2 | Aktualizacja klauzul w umowach z klientami i pracownikami (AI + tajemnica) | T2, T3 | Wspolnik prowadzacy + zewn. radca | 2026-07-31 |
| 3 | DPIA dla narzedzi AI uzywanych w kancelarii (Claude Pro, ChatGPT Plus, ewentualnie M365 Copilot) | R6 | IOD (zlecenie zewn.) | 2026-07-31 |
| 4 | Pisemna polityka AI w kancelarii (2-3 strony) + procedura dla bezplatnych narzedzi | R3, T4 | Wspolnik prowadzacy + champion | 2026-08-15 |
| 5 | Mapa narzedzi AI (rejestr) + aktualizacja RCP o czynnosc "uzycie generatywnej AI" | T1, R5 | Office Manager | 2026-08-15 |

Po wykonaniu tych 5 dzialan kancelaria osiagnie poziom 3 (Konstruktor) w wymiarach T i A. Wtedy ma podstawy do podjecia decyzji Build vs Buy dla konkretnych use case ow.

## 8. Rekomendacja build vs buy

**Skill nie przeprowadzal Build vs Buy w tym audycie** - kancelaria na poziomie Adopter nie jest gotowa do podjecia tej decyzji. Po wykonaniu 5 priorytetow z punktu 7 (90 dni) - powrocic do tego pytania.

Wstepna obserwacja: kancelaria nie ma GPU, wiec opcja **Build maximum z lokalnym modelem** odpada. Realne opcje: Build minimalny (Claude Team + skille) lub Buy PL legal SaaS (LEX AI / Legalis AI).

Pelny framework dla decyzji: [build-vs-buy/](../build-vs-buy/) - po osiagnieciu poziomu 3.

## 9. Nastepny audyt

Rekomendowany termin: **2026-09-15** (po wykonaniu listy priorytetow 90 dni). Cel: weryfikacja czy kancelaria przeszla z poziomu 2 (Adopter) na poziom 3 (Konstruktor) i jest gotowa do Build vs Buy.

---

> *Raport audytu wygenerowany przez skill matematic-readiness-audit v0.1.0 (matematicsolutions/matematic-readiness, CC BY-SA 4.0). Raport jest narzedziem diagnostycznym - decyzje merytoryczne nalezace do prawnika i inspektora ochrony danych.*
