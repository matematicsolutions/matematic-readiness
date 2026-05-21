# Raport audytu gotowosci kancelarii do AI - {{NAZWA_KANCELARII}}

| Klient audytu | {{NAZWA_KANCELARII}} |
|---|---|
| Audytor | {{AUDYTOR}} |
| Data audytu | {{DATA_AUDYTU}} |
| Czas trwania | {{CZAS_TRWANIA}} |
| Osoby uczestniczace | {{UCZESTNICY}} |

---

## 1. Streszczenie wykonawcze

**Pozycja kancelarii**: Poziom **{{POZIOM}}** ({{ETYKIETA_POZIOMU}}).

**Pelna ocena**:
- Wymiar 1 - RODO compliance: **{{SUM_R}}/30**
- Wymiar 2 - Tajemnica zawodowa: **{{SUM_T}}/30**
- Wymiar 3 - AI Act gotowosc: **{{SUM_A}}/30**
- Wymiar 4 - Kompetencje zespolu: **{{SUM_K}}/30**
- Wymiar 5 - Architektura techniczna: **{{SUM_I}}/30**
- **Suma**: {{SUM_TOTAL}}/150
- **Minimum z wymiarow**: {{MIN_WYMIAR}}/30 (decydujace dla poziomu)

**Glowne wnioski** (3-5 zdan):

{{WNIOSKI_KLUCZOWE}}

**Rekomendacja na najblizsze 90 dni**:

{{REKOMENDACJA_90_DNI}}

---

## 2. Wymiar 1: RODO compliance ({{SUM_R}}/30)

### Ocena per pytanie

| # | Pytanie | Ocena | Uzasadnienie |
|---|---|---|---|
| R1 | Kategoryzacja danych | {{R1_OCENA}}/5 | {{R1_UZASADNIENIE}} |
| R2 | Mapa transferow do panstw trzecich | {{R2_OCENA}}/5 | {{R2_UZASADNIENIE}} |
| R3 | Polityka korzystania z AI | {{R3_OCENA}}/5 | {{R3_UZASADNIENIE}} |
| R4 | Procedura zgloszenia incydentu | {{R4_OCENA}}/5 | {{R4_UZASADNIENIE}} |
| R5 | Rejestr czynnosci przetwarzania (RCP) | {{R5_OCENA}}/5 | {{R5_UZASADNIENIE}} |
| R6 | Ocena skutkow dla ochrony danych (DPIA) | {{R6_OCENA}}/5 | {{R6_UZASADNIENIE}} |

### Wnioski

{{WNIOSKI_RODO}}

---

## 3. Wymiar 2: Tajemnica zawodowa ({{SUM_T}}/30)

### Ocena per pytanie

| # | Pytanie | Ocena | Uzasadnienie |
|---|---|---|---|
| T1 | Mapa narzedzi AI w obrocie kancelarii | {{T1_OCENA}}/5 | {{T1_UZASADNIENIE}} |
| T2 | Klauzula w umowach z klientami | {{T2_OCENA}}/5 | {{T2_UZASADNIENIE}} |
| T3 | Klauzula w umowach z pracownikami | {{T3_OCENA}}/5 | {{T3_UZASADNIENIE}} |
| T4 | Procedura dla bezplatnych narzedzi | {{T4_OCENA}}/5 | {{T4_UZASADNIENIE}} |
| T5 | Stanowisko izby adwokackiej/radcowskiej | {{T5_OCENA}}/5 | {{T5_UZASADNIENIE}} |
| T6 | Test sprawdzajacy (art. 6 PoA / art. 3 URP) | {{T6_OCENA}}/5 | {{T6_UZASADNIENIE}} |

### Wnioski

{{WNIOSKI_TAJEMNICA}}

---

## 4. Wymiar 3: AI Act gotowosc ({{SUM_A}}/30)

### Ocena per pytanie

| # | Pytanie | Ocena | Uzasadnienie |
|---|---|---|---|
| A1 | Klasyfikacja systemow AI | {{A1_OCENA}}/5 | {{A1_UZASADNIENIE}} |
| A2 | Audyt high-risk | {{A2_OCENA}}/5 | {{A2_UZASADNIENIE}} |
| A3 | Transparentnosc (art. 50) | {{A3_OCENA}}/5 | {{A3_UZASADNIENIE}} |
| A4 | AI literacy (art. 4) | {{A4_OCENA}}/5 | {{A4_UZASADNIENIE}} |
| A5 | Procedura w razie naruszenia | {{A5_OCENA}}/5 | {{A5_UZASADNIENIE}} |
| A6 | Daty wejscia w zycie | {{A6_OCENA}}/5 | {{A6_UZASADNIENIE}} |

### Wnioski

{{WNIOSKI_AI_ACT}}

---

## 5. Wymiar 4: Kompetencje zespolu ({{SUM_K}}/30)

### Ocena per pytanie

| # | Pytanie | Ocena | Uzasadnienie |
|---|---|---|---|
| K1 | Mapa kompetencji | {{K1_OCENA}}/5 | {{K1_UZASADNIENIE}} |
| K2 | Szkolenia | {{K2_OCENA}}/5 | {{K2_UZASADNIENIE}} |
| K3 | Eksperymentowanie w piaskownicy | {{K3_OCENA}}/5 | {{K3_UZASADNIENIE}} |
| K4 | Identyfikacja championa | {{K4_OCENA}}/5 | {{K4_UZASADNIENIE}} |
| K5 | Prompt engineering | {{K5_OCENA}}/5 | {{K5_UZASADNIENIE}} |
| K6 | Halucynacje i weryfikacja | {{K6_OCENA}}/5 | {{K6_UZASADNIENIE}} |

### Wnioski

{{WNIOSKI_KOMPETENCJE}}

---

## 6. Wymiar 5: Architektura techniczna ({{SUM_I}}/30)

### Ocena per pytanie

| # | Pytanie | Ocena | Uzasadnienie |
|---|---|---|---|
| I1 | Mapa systemow kancelaryjnych | {{I1_OCENA}}/5 | {{I1_UZASADNIENIE}} |
| I2 | Hosting i lokalizacja | {{I2_OCENA}}/5 | {{I2_UZASADNIENIE}} |
| I3 | Backup i ciaglosc dzialania | {{I3_OCENA}}/5 | {{I3_UZASADNIENIE}} |
| I4 | Mozliwosc self-host AI | {{I4_OCENA}}/5 | {{I4_UZASADNIENIE}} |
| I5 | Single Sign-On i kontrola dostepu | {{I5_OCENA}}/5 | {{I5_UZASADNIENIE}} |
| I6 | Logging i audit trail | {{I6_OCENA}}/5 | {{I6_UZASADNIENIE}} |

### Wnioski

{{WNIOSKI_ARCHITEKTURA}}

---

## 7. Lista priorytetow na 90 dni

| # | Dzialanie | Wymiar | Wlasciciel | Termin |
|---|---|---|---|---|
| 1 | {{PRIORYTET_1}} | {{PRIORYTET_1_WYMIAR}} | {{PRIORYTET_1_WLASCICIEL}} | {{PRIORYTET_1_TERMIN}} |
| 2 | {{PRIORYTET_2}} | {{PRIORYTET_2_WYMIAR}} | {{PRIORYTET_2_WLASCICIEL}} | {{PRIORYTET_2_TERMIN}} |
| 3 | {{PRIORYTET_3}} | {{PRIORYTET_3_WYMIAR}} | {{PRIORYTET_3_WLASCICIEL}} | {{PRIORYTET_3_TERMIN}} |
| 4 | {{PRIORYTET_4}} | {{PRIORYTET_4_WYMIAR}} | {{PRIORYTET_4_WLASCICIEL}} | {{PRIORYTET_4_TERMIN}} |
| 5 | {{PRIORYTET_5}} | {{PRIORYTET_5_WYMIAR}} | {{PRIORYTET_5_WLASCICIEL}} | {{PRIORYTET_5_TERMIN}} |

## 8. Rekomendacja build vs buy

{{REKOMENDACJA_BVB}}

Pelny framework: [build-vs-buy/](../build-vs-buy/).

## 9. Nastepny audyt

Rekomendowany termin nastepnego audytu: **{{NASTEPNY_AUDYT}}** (zazwyczaj 6-12 miesiecy).

---

> *Raport audytu wygenerowany przez skill matematic-readiness-audit v{{SKILL_VERSION}} (matematicsolutions/matematic-readiness, CC BY-SA 4.0). Raport jest narzedziem diagnostycznym - decyzje merytoryczne nalezace do prawnika i inspektora ochrony danych.*
