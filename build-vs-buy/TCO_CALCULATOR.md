# Kalkulator TCO 3-letni - Build vs Buy

Liczby **orientacyjne** na 2026-05. Aktualizuj sprawdzajac bezposrednio z dostawcami.

Zmienne:
- **N** = liczba osob w kancelarii korzystajacych z AI.
- **Koszt LLM API** dla build = zalezy od wolumenu uzycia (Claude 4.7 Sonnet: ~3 USD/M tokenow input, 15 USD/M tokenow output; Claude 4.7 Opus: ~15/75 USD/M; Gemini 2.5 Pro: ~1/5 USD/M; lokalne modele: koszt elektrycznosci + sprzet jednorazowo).

---

## Koszt 3-letni dla kancelarii 10 osob (przyklad)

### Buy US legal SaaS (Harvey / CoCounsel / Lexis AI)

| Pozycja | Koszt |
|---|---|
| Subskrypcja 10 osob x 300 USD/mc x 36 mc | ~108k USD = ~432k PLN |
| Wdrozenie / onboarding | ~10-30k PLN |
| Szkolenia | ~10-20k PLN |
| Audyt RODO / DPIA | ~10-30k PLN |
| Bezpieczenstwo / dodatkowe DPA | ~5-15k PLN |
| **Razem 3 lata** | **~470-530k PLN** |

### Buy PL legal SaaS (LEX AI / Legalis AI)

| Pozycja | Koszt |
|---|---|
| Subskrypcja 10 osob x 200 PLN/mc x 36 mc | ~72k PLN |
| Wdrozenie | ~5-15k PLN |
| Szkolenia | ~5-10k PLN |
| DPIA (latwiejsze, polski dostawca) | ~5-10k PLN |
| **Razem 3 lata** | **~85-105k PLN** |

### Buy general Enterprise (Claude Enterprise / ChatGPT Enterprise)

| Pozycja | Koszt |
|---|---|
| Subskrypcja 10 osob x 80 USD/mc x 36 mc | ~28.8k USD = ~115k PLN |
| Wdrozenie / konfiguracja | ~5-15k PLN |
| Szkolenia (workflow, prompt engineering) | ~10-20k PLN |
| DPIA + DPF assessment | ~10-20k PLN |
| Dodatkowe narzedzia (Notion, Slack, MCP konektory) | ~10-20k PLN |
| **Razem 3 lata** | **~150-190k PLN** |

### Build minimalny (Claude Team + skille + workflow)

| Pozycja | Koszt |
|---|---|
| Claude Team 10 osob x 30 USD/mc x 36 mc | ~10.8k USD = ~43k PLN |
| Skille MateMatic (lpm-pl, custom) - open source | 0 PLN |
| Konfiguracja konektorow MCP polskiego prawa | 0 PLN (open source) |
| Wdrozenie (konsultant zewn. lub osoba wewn.) | ~20-50k PLN |
| Szkolenia | ~10-20k PLN |
| DPIA | ~5-15k PLN |
| Utrzymanie (osoba wewn. 0.2 etatu lub kontraktor) | ~30-60k PLN/rok x 3 = ~90-180k PLN |
| **Razem 3 lata** | **~170-310k PLN** |

### Build sredni (Cline + Ollama + skille + lokalna infra)

| Pozycja | Koszt |
|---|---|
| Claude API jako fallback (ad hoc): ~50 USD/mc x 36 mc | ~7.2k PLN |
| Ollama + lokalne modele - jednorazowo sprzet GPU (RTX 4090 lub równowazne) | ~15-30k PLN |
| Wdrozenie | ~30-80k PLN |
| Skille MateMatic (lpm-pl, readiness audit) - open source | 0 PLN |
| Szkolenia | ~10-30k PLN |
| DPIA (lekka, dane lokalnie) | ~3-8k PLN |
| Utrzymanie (osoba wewn. 0.3 etatu lub kontraktor) | ~50-100k PLN/rok x 3 = ~150-300k PLN |
| **Razem 3 lata** | **~215-455k PLN** |

### Build maximum (Patron wdrozony)

| Pozycja | Koszt |
|---|---|
| Wdrozenie Patrona (jednorazowo) | ~30-150k PLN |
| LLM API (jezeli bring-your-own-model Claude / Gemini): ~50 USD/mc x 36 mc | ~7.2k PLN |
| Lub: lokalne modele Ollama + sprzet GPU | ~15-30k PLN jednorazowo |
| Hosting / VPS / serwer | ~5-15k PLN/rok x 3 = ~15-45k PLN |
| Szkolenia | ~10-30k PLN |
| DPIA + AI Act assessment | ~10-20k PLN |
| Utrzymanie (MateMatic managed service lub osoba wewn.) | ~30-80k PLN/rok x 3 = ~90-240k PLN |
| Aktualizacje / iteracje | ~10-30k PLN/rok x 3 = ~30-90k PLN |
| **Razem 3 lata** | **~200-650k PLN** |

---

## Skalowanie kosztu z liczba uzytkownikow

| Liczba osob | Buy US legal | Buy PL legal | Build minimalny | Build maximum |
|---|---|---|---|---|
| 1 (solo prawnik) | ~50k PLN | ~10k PLN | ~50k PLN | ~150k PLN |
| 5 osob | ~250k PLN | ~50k PLN | ~120k PLN | ~200k PLN |
| 10 osob | ~470-530k PLN | ~85-105k PLN | ~170-310k PLN | ~200-650k PLN |
| 25 osob | ~1.1M PLN | ~200-250k PLN | ~350-500k PLN | ~300-800k PLN |
| 50 osob | ~2.2M PLN | ~400-500k PLN | ~600-800k PLN | ~400-1M PLN |
| 100 osob | ~4.5M PLN | ~800k-1M PLN | ~1.2-1.6M PLN | ~600k-1.5M PLN |

### Punkty przelomu (kiedy kazdy model sie zwraca)

- **Buy PL legal vs Build minimalny**: pomijalne, oba sa tanie. Decyzja zalezna od dodatkowych kryteriow (specyfika, audit trail).
- **Buy US legal vs Build maximum**: Build wygrywa od ok. 5-10 osob na korzystnie wdrozonym Patronie.
- **Buy general Enterprise vs Build sredni**: zaleznosc, ale typowo Build wygrywa od 10+ osob.

---

## Uwagi do TCO

1. **Cena licencji != TCO**. Buy SaaS ma ukryte koszty: szkolenia, audyt, DPIA, integracje.
2. **Build ma koszty operacyjne**. Osoba do utrzymania to glowny driver kosztu. Zlecenie dla partnera (MateMatic managed service) moze byc tansze i bezpieczniejsze niz etat.
3. **AI Act i RODO koszt rosnie** w czasie. DPIA aktualizowane co 6 mc. AI literacy szkolenia roczne. Audyt zewnetrzny przed 2026-08-02.
4. **Tajemnica zawodowa koszt**: dla buy US trzeba dolozyc do TCO koszt ryzyka prawnego (potencjalna dyscyplinarka, koszt obrony, koszt reputacji).
5. **Vendor risk koszt**: jezeli platforma znika (Casetext byla independent w 2022, kupiona przez TR w 2023, w 2026 raczej OK ale niewiadomo do 2029) - koszt migracji do alternatywy.

## Co jeszcze warto policzyc poza TCO

- **Czas zaoszczedzony**: kazdy use case ma potencjal X godzin tygodniowo. Stawka godzinowa prawnika x oszczedzony czas = wartosc.
- **Jakosc**: AI moze poprawic jakosc (mniej luk, lepsze badania) lub pogorszyc (halucynacje, schematycznosc). Mierzymy przez testy A/B.
- **Marketing**: kancelaria z AI = przewaga konkurencyjna na rynku gdzie 80% kancelarii jeszcze sie nie ruszylo (2026-05).

ROI = (Wartosc zaoszczedzonego czasu + Wzrost przychodu z marketingu) - TCO. Dla wiekszosci use case ow ROI > 1 (zwrot z inwestycji) wymaga 12-18 miesiecy.

## Powiazane

- [FRAMEWORK.md](FRAMEWORK.md) - 8 kryteriow.
- [PLATFORMY.md](PLATFORMY.md) - porownanie.
- [POLSKI_KONTEKST.md](POLSKI_KONTEKST.md) - regulacje.
