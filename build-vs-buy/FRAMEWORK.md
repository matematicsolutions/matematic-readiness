# Framework decyzyjny: Build vs Buy AI dla polskiej kancelarii

Decyzja **build vs buy** w AI dla polskiej kancelarii nie jest tym samym, co dla amerykanskiej. **Polski kontekst regulacyjny** (RODO + tajemnica zawodowa + AI Act) zmienia waze poszczegolnych kryteriow.

Cherry-pick patternu 8 kryteriow z [OneC0de/legal-ai-architect-toolkit/build-vs-buy-decision-framework.md](https://github.com/OneC0de/legal-ai-architect-toolkit/blob/main/frameworks/build-vs-buy-decision-framework.md) (MIT). 8 kryteriow przepisane pod polski rynek, system wagowy DODANY, decision tree DODANY, [POLSKI_KONTEKST.md](POLSKI_KONTEKST.md) i [PLATFORMY.md](PLATFORMY.md) DODANE.

---

## Co oznacza "build" i "buy" w naszym kontekscie

### Build - 3 odmiany

1. **Build minimalny**: subskrypcja Claude Team / ChatGPT Team / Gemini for Workspace + zestaw promptow + procedury. Brak wlasnego kodu, ale **wlasny workflow**. **Czas wdrozenia**: 1-3 miesiace. **Koszt**: 30-100 USD per uzytkownik miesiecznie + czas konsultanta.
2. **Build sredni**: zlozenie z gotowych komponentow open source - Cline + Ollama / Claude Code + custom skille (jak [lpm-pl](https://github.com/matematicsolutions/lpm-pl)) + MCP konektory polskiego prawa. **Czas**: 3-6 miesiecy. **Koszt**: 100-500 USD per uzytkownik miesiecznie (LLM API + hosting).
3. **Build maximum**: wlasny agent self-host pod marka kancelarii lub na bazie [Patron](https://github.com/matematicsolutions/patron). **Czas**: 6-12 miesiecy. **Koszt**: 50-150 USD per uzytkownik miesiecznie + dedykowane wdrozenie 30-150k PLN jednorazowo.

### Buy - 4 odmiany

1. **Buy US legal SaaS**: Harvey, CoCounsel (Thomson Reuters), Lexis AI, Ruli AI. Cloud-only, dane w USA. **Koszt**: 200-1000 USD per uzytkownik miesiecznie. **RODO**: wymaga DPA + DPF + DPIA + akceptacja ryzyka. **Tajemnica**: krytyczne pytanie.
2. **Buy PL legal SaaS** (w przygotowaniu / wczesny etap): LEX AI (Wolters Kluwer), Legalis AI (CH Beck), Mecenas AI, Practice. **Koszt**: 100-500 PLN per uzytkownik miesiecznie (orientacyjnie). **RODO**: lepiej (dane czesto w UE), ale wczesny etap = mniejsza funkcjonalnosc.
3. **Buy general-purpose Enterprise**: ChatGPT Enterprise, Claude Enterprise, Gemini Workspace Enterprise. Cloud, ale z DPA i enterprise security. **Koszt**: 60-100 USD per uzytkownik miesiecznie. **RODO**: dobre DPA, ale transfer do US (DPF).
4. **Buy hybryda**: platforma + lokalne komponenty. Np. Microsoft Copilot dla Office + lokalna baza dokumentow z DLP.

## 8 kryteriow decyzyjnych (z waga polskiego kontekstu)

Polski kontekst zmienia wage. Nie kazda decyzja w US 1:1 dziala w PL. Wagi 1-5 (1 = niska istotnosc, 5 = krytyczne).

### Kryterium 1 - Tajemnica zawodowa (waga: 5)

**Pytanie**: Czy use case dotyczy danych objetych tajemnica zawodowa (akta sprawy, korespondencja z klientem, strategia procesowa)?

- Jezeli TAK -> **build** lub **buy PL/Enterprise z DPF** sa praktycznie jedyne opcje. Buy US bez gwarancji lokalizacji = naruszenie tajemnicy.
- Jezeli NIE (np. analiza publicznych orzeczen, edukacja, marketing) -> wszystkie opcje otwarte.

Polski kontekst: art. 6 Prawa o adwokaturze i art. 3 Ustawy o radcach prawnych sa **bezwzgledne** - klient nie moze "zwolnic" prawnika z tajemnicy w zakresie transferu danych do USA (decyzja Sad Najwyzszy II CSK 419/12 i kolejne).

### Kryterium 2 - Wolumen uzycia (waga: 4)

**Pytanie**: Ile razy w miesiacu kancelaria bedzie uzywac tego use case?

- < 10/mc -> **buy general-purpose** (ChatGPT Enterprise, Claude Team). Build sie nie zwraca.
- 10-100/mc -> **build minimalny** (custom prompty + workflow) lub **buy PL legal**.
- > 100/mc -> **build sredni/maximum** zaczyna sie zwracac, ROI buduje sie szybko.

### Kryterium 3 - Specyfika use case (waga: 4)

**Pytanie**: Czy use case jest **unikatowy** dla tej kancelarii / specjalizacji, czy ogolny?

- Ogolny (research orzecznictwa, streszczenia ustaw, draft maili) -> **buy** wystarczy.
- Unikatowy (specyficzna metodyka kancelarii, lokalna interpretacja klauzul, scoring specyficzny dla niszy) -> **build** lub **buy z mozliwoscia customizacji**.

### Kryterium 4 - Czas do wartosci (waga: 3)

**Pytanie**: Jak szybko kancelaria musi miec wartosc z tego use case?

- < 1 miesiac -> **buy** lub **build minimalny**. Maximum build = za pozno.
- 1-6 miesiecy -> **build sredni** mozliwy.
- > 6 miesiecy -> **build maximum** opcja, lub strategia hybrydowa.

### Kryterium 5 - Koszt 3-letni (TCO, waga: 4)

**Pytanie**: Jaki bedzie 3-letni koszt calkowity (licencja + wdrozenie + utrzymanie + szkolenie)?

Patrz [TCO_CALCULATOR.md](TCO_CALCULATOR.md) - kalkulator orientacyjny.

- Buy US legal SaaS dla kancelarii 10 osob = 720k-3.6M PLN/3 lata (ekspansywnie).
- Buy PL legal SaaS = 36-180k PLN/3 lata (orientacyjnie, etap rynku).
- Buy general-purpose Enterprise = 216-360k PLN/3 lata.
- Build minimalny = 80-200k PLN/3 lata.
- Build sredni = 200-500k PLN/3 lata.
- Build maximum = 200-800k PLN/3 lata (zalezne od wdrozenia).

**WAZNE**: cena buy SaaS rosnie z liczba osob (per seat). Build skaluje sie lepiej (jednorazowy koszt + LLM API).

### Kryterium 6 - Audit trail (waga: 4)

**Pytanie**: Czy kancelaria potrzebuje **per-request audit trail** (kto, kiedy, jaki prompt, jaki output)?

- TAK (system zakwalifikowany jako wysokiego ryzyka, klient z wymogiem compliance, sprawy karne) -> **build** (Patron ma audit trail z hash-chain wbudowany) lub **buy enterprise z eksportem logow**.
- NIE -> buy general-purpose wystarczy.

Polski kontekst: AI Act art. 12 wymaga rejestrowania zdarzen w systemach wysokiego ryzyka. Kancelaria, ktora uzywa AI do analizy dokumentow we wlasnej sprawie, **zwykle nie** wpada w Annex III pkt 8 - ten obejmuje systemy uzywane przez sad lub w jego imieniu (patrz [POLSKI_KONTEKST.md](POLSKI_KONTEKST.md)). Slad audytowy bywa potrzebny z innych powodow: wymog klienta, tajemnica zawodowa, dowod nalezytej starannosci.

### Kryterium 7 - Maintenance (waga: 3)

**Pytanie**: Kto bedzie utrzymywal narzedzie po wdrozeniu?

- Brak osoby technicznej w kancelarii -> **buy** wymusze. Build wymaga osoby albo partnera technicznego.
- Champion AI z mandate + budget na utrzymanie -> **build** mozliwe.
- Outsourcing do MateMatic / partnera -> **build** mozliwe (model "managed service").

### Kryterium 8 - Vendor independence (waga: 3)

**Pytanie**: Jak bardzo kancelaria boi sie vendor lock-in?

Polski kontekst: Harvey upadl w 2024-2025 (firma jeszcze nie, ale ryzyko biznesowe konsolidacji jest realne). CoCounsel kupil Thomson Reuters w 2023 (Casetext). Konsolidacja rynku legal AI = ryzyko ze platforma za 2 lata zniknie lub bedzie 5x drozsza.

- Wysokie obawy -> **build** z open source komponentami.
- Akceptujemy -> **buy**.

---

## Decision tree (graf decyzyjny)

```
Use case z danymi pod tajemnica zawodowa?
├── TAK -> Czy mozemy uzyc PL legal SaaS lub Enterprise z DPA + DPF?
│         ├── TAK (DPIA OK) -> Buy general-purpose Enterprise / PL legal
│         └── NIE (akta wrazliwe, sprawy karne, klienci publiczni)
│                  -> Build (self-host, Patron lub equivalent)
└── NIE -> Wolumen miesieczny?
          ├── < 10/mc -> Buy general-purpose Enterprise
          ├── 10-100/mc -> Czy use case unikatowy?
          │         ├── TAK -> Build minimalny
          │         └── NIE -> Buy PL legal SaaS / general-purpose Enterprise
          └── > 100/mc -> Czy audit trail wymagany (high-risk)?
                    ├── TAK -> Build sredni/maximum (Patron, audit trail z hash-chain)
                    └── NIE -> Build minimalny lub buy PL legal SaaS
```

## Scoring uzywajac kryteriow z waga

Per use case, audyt przeplynie wszystkie 8 kryteriow. Kazde kryterium ocenione **ktora opcja wygrywa** (Build vs Buy), pomnozone przez wage:

| Kryterium | Waga | Build | Buy | Wygrywa |
|---|---|---|---|---|
| 1. Tajemnica zawodowa | 5 | {{ARGUMENT_BUILD_1}} | {{ARGUMENT_BUY_1}} | {{WYGRYWA_1}} |
| 2. Wolumen uzycia | 4 | {{ARGUMENT_BUILD_2}} | {{ARGUMENT_BUY_2}} | {{WYGRYWA_2}} |
| 3. Specyfika | 4 | {{ARGUMENT_BUILD_3}} | {{ARGUMENT_BUY_3}} | {{WYGRYWA_3}} |
| 4. Czas do wartosci | 3 | {{ARGUMENT_BUILD_4}} | {{ARGUMENT_BUY_4}} | {{WYGRYWA_4}} |
| 5. TCO 3-letni | 4 | {{ARGUMENT_BUILD_5}} | {{ARGUMENT_BUY_5}} | {{WYGRYWA_5}} |
| 6. Audit trail | 4 | {{ARGUMENT_BUILD_6}} | {{ARGUMENT_BUY_6}} | {{WYGRYWA_6}} |
| 7. Maintenance | 3 | {{ARGUMENT_BUILD_7}} | {{ARGUMENT_BUY_7}} | {{WYGRYWA_7}} |
| 8. Vendor independence | 3 | {{ARGUMENT_BUILD_8}} | {{ARGUMENT_BUY_8}} | {{WYGRYWA_8}} |

**Suma wag dla Build**: {{SUMA_BUILD}}
**Suma wag dla Buy**: {{SUMA_BUY}}

**Decyzja**: {{DECYZJA_FINAL}}.

## Co dalej

1. Polski kontekst regulacyjny ([POLSKI_KONTEKST.md](POLSKI_KONTEKST.md)) - szczegoly RODO, tajemnicy, AI Act dla decyzji.
2. Porownanie konkretnych platform ([PLATFORMY.md](PLATFORMY.md)) - Patron / Harvey / CoCounsel / Lexis AI / Ruli AI / ChatGPT Enterprise / Claude Max / LEX AI / Legalis AI.
3. Kalkulator TCO ([TCO_CALCULATOR.md](TCO_CALCULATOR.md)) - liczby orientacyjne 3-letniego kosztu.

## Anti-patterns (czego unikac w decyzji)

- **Decyzja na podstawie ceny licencji rocznej** - TCO 3-letni rzadzi.
- **Decyzja na podstawie "co modne"** (Harvey 2024 hype) - kancelaria nie podaza za trendami, podaza za wartoscia.
- **Decyzja bez DPIA** - bez DPIA nie wiesz co bierzesz. Wymog RODO art. 35.
- **Decyzja "wszystko build" lub "wszystko buy"** - rozne use case y mozliwe ze beda mialy rozne odpowiedzi. **Hybryd jest normalny**.
- **Decyzja bez konsultacji z IOD** - decyzja w odejsciu od inspektora ochrony danych = niedopuszczalna.
