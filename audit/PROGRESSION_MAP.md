# Mapa progresji - 5 poziomow gotowosci kancelarii do AI

Po przejsciu audytu z [CHECKLIST.md](CHECKLIST.md) i scoring z [SCORING.md](SCORING.md), kancelaria umieszczona jest na jednym z 5 poziomow. **Poziom = minimum z 5 wymiarow**, nie srednia (uzasadnienie: krytyczna luka RODO niweczy zaawansowane kompetencje techniczne).

Cherry-pick patternu 5-poziomowego z [OneC0de/legal-ai-architect-toolkit](https://github.com/OneC0de/legal-ai-architect-toolkit) (MIT). Polski uklad poziomow przepisany - polskie kryteria progresji, polskie typowe rekomendacje "co dalej".

---

## Poziom 1: Eksplorator (Explorer)

**Gdzie jestes**: kancelaria slyszala o AI, niewiele wie. Pojedyncze osoby probowaly ChatGPT prywatnie, brak polityki, brak rozmow w zespole o ryzyku.

**Sumy per wymiar**: 6-12 punktow w wymiarze.

**Sygnaly**:
- Brak polityki uzycia AI.
- Brak RCP / DPIA dla AI.
- Pracownicy uzywaja darmowych narzedzi z danymi klienta (lub kancelaria nie wie czy uzywaja).
- Managing partner nie umie nazwac konkretnych narzedzi AI w kancelarii.
- Brak szkolen, brak championa.

**Niebezpieczenstwa**: na tym poziomie kancelaria ma **najwyzsze ryzyko incydentu** - bez polityki, ale czesto z aplikantami eksperymentujacymi. Pojedynczy wyciek do ChatGPT = naruszenie tajemnicy + RODO.

**Co konkretnie zrobic na poziom 2 (90 dni)**:

1. **Polityka AI w kancelarii** (30 dni) - 2-3 strony, co wolno / co zabronione, akceptacja zespolu na pismie.
2. **Mapa narzedzi** (60 dni) - kto co uzywa, rejestr.
3. **Szkolenie wprowadzajace** (90 dni) - 2-3h dla calego zespolu, podstawy AI + RODO + tajemnica.
4. **Pierwszy use case w piaskownicy** - jeden bezpieczny przyklad (np. streszczenia publicznie dostepnych orzeczen) bez danych klienta.

**Czego NIE robic**: NIE kupuj jeszcze platformy enterprise (Harvey, CoCounsel, Lexis AI). NIE wdrozaj agenta. NIE robic deklaracji "kancelaria uzywa AI" przed politykie.

---

## Poziom 2: Adopter

**Gdzie jestes**: kancelaria ma podstawowa polityke. Kilka osob aktywnie uzywa AI z subskrypcja (Claude Pro, ChatGPT Plus, Gemini Advanced). Use case ad hoc, bez systematyki. Pojawia sie champion.

**Sumy per wymiar**: 12-18 punktow w wymiarze.

**Sygnaly**:
- Istnieje pisemna polityka AI (2-3 strony).
- Rejestr narzedzi prowadzony, aktualizowany sporadycznie.
- Champion AI istnieje (nieformalnie).
- Plansy enterprise dla narzedzi gdzie wpisuje sie dane klienta (Claude Team / ChatGPT Team z opt-out z treningu).
- Eksperymenty w piaskownicy, ale brak miary efektu.

**Niebezpieczenstwa**: kancelaria sklonna do "zachłysniecia AI" - obietnice ze "AI zrobi wszystko". Brak procedury weryfikacji outputu = ryzyko halucynacji w pisme procesowym.

**Co konkretnie zrobic na poziom 3 (90 dni)**:

1. **DPIA dla glownych use case ow** - art. 35 RODO, dokument 5-8 stron per use case.
2. **Lista 3-5 production-grade use case ow** - co AI robi, jakie ma KPI, kto za to odpowiada.
3. **Procedura weryfikacji outputu** - kazdy output AI ma byc sprawdzony przez prawnika ZANIM trafi do klienta/sadu.
4. **Klauzula w umowach z klientami** o uzyciu AI - obowiazek transparentnosci (art. 50 AI Act).
5. **Szkolenie zaawansowane** - prompt engineering, halucynacje, weryfikacja zrodel.

**Decyzja kluczowa**: zrobic audyt **build vs buy** ([../build-vs-buy/](../build-vs-buy/)) - czas wybrac architekture na dluzej.

---

## Poziom 3: Konstruktor (Builder)

**Gdzie jestes**: kancelaria ma stabilne use case y w produkcji. AI uzywane regularnie z dokumentacja DPIA. Architektura zaczyna sie pojawiac (jednorodne narzedzie, integracje z systemami kancelaryjnymi).

**Sumy per wymiar**: 18-24 punkty w wymiarze.

**Sygnaly**:
- DPIA istnieja dla glownych use case ow.
- Procedura weryfikacji outputu jest stosowana (z dokumentacja).
- Klauzule w umowach z klientami i pracownikami.
- 3-5 use case ow w produkcji z mierzalnym KPI.
- Architektura: kancelaria zdecydowala build vs buy (lub pierwszy hybryd).
- Champion AI ma jasny mandat, miesieczne raporty z postepu.

**Co konkretnie zrobic na poziom 4 (90-180 dni)**:

1. **Audit trail per uzycie AI** (Patron, custom logging, lub platform-native) - kto, kiedy, co prompt, co output.
2. **Integracje z systemami kancelaryjnymi** - LEX Kancelaria / Mecenas IT / Comarch IBARD; lub dane lokalnie w SharePoint z DLP.
3. **AI literacy obowiazkowe** dla wszystkich pracownikow (art. 4 AI Act, obowiazek od 2025-02).
4. **Knowledge base z promptami** - zewnetrzny lub wewnetrzny, wspoldzielony.
5. **Pierwszy use case high-risk z dokumentacja AI Act** - jezeli kancelaria pracuje z tym jaki obszarem.

---

## Poziom 4: Architekt (Architect)

**Gdzie jestes**: kancelaria ma swiadoma architekture AI. Zna build/buy decyzje per use case. Audit trail dziala. Integracje z systemami sa **monitorowane**. Compliance z AI Act i RODO ma dokumentacje.

**Sumy per wymiar**: 24-27 punktow w wymiarze.

**Sygnaly**:
- Diagram architektury AI istnieje.
- Audit trail z hash-chain (lub equivalent) - art. 12 AI Act.
- DPIA przegladane raz na 6 miesiecy, aktualizowane.
- Mapa use case ow w klasyfikacji AI Act (high-risk / GPAI / minimal).
- Mierzalny ROI per use case (czas, koszt, jakosc).
- AI championship oficjalne - rola etatowa lub jasne 20% etatu osoby.

**Co konkretnie zrobic na poziom 5 (180-365 dni)**:

1. **Ciagle ulepszanie - regularne testy A/B promptow** z mierzeniem jakosci.
2. **Self-host LLM dla wrazliwych spraw** - Patron / Ollama z lokalnym modelem.
3. **Audit zewnetrzny zgodnosci RODO/AI Act** - przez certyfikowanego audytora.
4. **Publikacje kancelarii** o adopcji AI (artykuly, prelekcje) - kancelaria staje sie liderem mysli w swojej niszy.

---

## Poziom 5: Orkiestrator (Orchestrator)

**Gdzie jestes**: kancelaria jest liderem w swoim segmencie. AI jest w roli **operacyjnej** - nie eksperyment, nie projekt, **rutyna**. Audit trail per uzycie. Ciagle ulepszanie z miernikami. Klienci wiedza ze kancelaria uzywa AI i dlatego do niej trafiaja.

**Sumy per wymiar**: 27-30 punktow w wymiarze.

**Sygnaly**:
- AI w produkcji we wszystkich glownych workflow.
- Audit trail z hash-chain dziala 100% czasu.
- DPIA aktualizowane co kwartal.
- Wymierne wyniki - ROI dokumentowane, klienci widza redukcje kosztow / lepsza jakosc.
- AI literacy mierzony (test, certyfikat) dla wszystkich pracownikow.
- Polityka publiczna kancelarii - klient wie czego sie spodziewac.
- Kancelaria publikuje artykuly / prelekcje / case study z wdrozenia AI.

**Co konkretnie zrobic na poziomie 5**: utrzymac to. Audytowac corocznie. Edukowac branze przez publikacje. Nie spasc do 4 z powodu zmian regulacyjnych (AI Act fazy).

---

## Mapowanie pelnej sumy (30-150 pkt) na poziom

UWAGA: kluczowa metoda to **minimum z 5 wymiarow** (nie srednia). Mapa pelnej sumy ponizej jest tylko dodatkowa informacja:

| Suma punktow | Etykieta pomocnicza |
|---|---|
| 30-50 | Eksplorator (typowy) |
| 51-75 | Adopter (typowy) |
| 76-105 | Konstruktor (typowy) |
| 106-130 | Architekt (typowy) |
| 131-150 | Orkiestrator (typowy) |

Jezeli minimum z wymiarow daje INNY poziom niz suma - kierowac sie **minimum**. Jeden krytyczny gap niweczy zaawansowanie pozostalych wymiarow.

## Pulapki

- **Skok ponad poziom**: kancelaria Eksplorator chcaca byc Architektem w 6 miesiecy = przepalanie budzetu + ryzyko porazki + zniechecenie zespolu.
- **Slepa kopia "best practice"**: nie kazda kancelaria potrzebuje audit trail z hash-chain - to wymog AI Act dla **high-risk**, nie dla cotygodniowych streszczen artykulow prawnych.
- **Buy bez audytu**: kancelaria Eksplorator kupuje platforme enterprise za 100k PLN i potem nikt z niej nie korzysta. Najpierw poziom 2, potem build vs buy.
