# Polski kontekst regulacyjny dla decyzji Build vs Buy

Decyzja **build vs buy** w polskiej kancelarii jest podejmowana w bardziej restrykcyjnym srodowisku niz w USA czy UK. Trzy warstwy regulacyjne nakladaja sie:

1. **RODO** - rozporzadzenie 2016/679 (CELEX 32016R0679).
2. **Tajemnica zawodowa** - ustawy zawodowe (PoA, URP), kodeksy etyki (KEA, KEZRP).
3. **AI Act** - rozporzadzenie 2024/1689 (CELEX 32024R1689) wchodzace etapami 2025-2027.

Plus dodatkowe akty: **DPF** (Data Privacy Framework UE-USA z 2023, podtrzymany przez Sad UE 2025-09-03), **Digital Services Act**, **Digital Markets Act**, branzowe akty sektorowe (DORA, NIS2 jezeli klient jest objety).

---

## 1. RODO - transfery do panstw trzecich

### Co mowi prawo

**Art. 44 RODO** - transfer danych osobowych do panstwa trzeciego (poza EOG) wymaga jednej z podstaw z art. 45-49:

- Decyzja Komisji o adekwatnosci (art. 45) - dla USA: **DPF** (Data Privacy Framework, decyzja 2023-07-10, podtrzymana 2025-09-03 przez Sad UE).
- Odpowiednie zabezpieczenia (art. 46) - standardowe klauzule umowne (SCC), wiazace reguly korporacyjne (BCR).
- Wyjatki (art. 49) - sytuacje szczegolne (zgoda, niezbednosc do wykonania umowy z klientem).

### Co to znaczy w praktyce dla "buy US legal SaaS"

Harvey, CoCounsel, Ruli AI - hostowane w USA. Aby polska kancelaria mogla wysylac tam dane:

1. Dostawca MUSI byc certyfikowany pod DPF (sprawdzic na https://www.dataprivacyframework.gov/).
2. Lub MUSI byc podpisana umowa SCC.
3. Lub MUSI byc inny tryb z art. 49 (zazwyczaj zgoda klienta - patrz nizej, dla aktow sprawy bezprzedmiotowa).
4. Kancelaria MUSI miec DPIA (art. 35 RODO) dla tego transferu.
5. Kancelaria MUSI miec wpis w RCP (art. 30 RODO).
6. Klient kancelarii MUSI byc poinformowany - art. 13/14 RODO.

### Wyrok Schrems II i jego nastepstwa

**TSUE C-311/18 Schrems II** (2020) - uniewaznienie Privacy Shield (poprzednik DPF). Konsekwencja: kazdy transfer do USA wymagal SCC + analiza ryzyka inwigilacji.

**DPF** (2023) zastapil Privacy Shield. **Sad UE T-553/23 La Quadrature du Net** (decyzja 2025-09-03) - **DPF utrzymany w mocy**, transfer do USA pod DPF jest legalny w warunkach DPF.

Mit "Schrems III obala DPF" - **NIEPRAWDA na 2026-05** (patrz fakty DPF i AI Act na 2026-05).

---

## 2. Tajemnica zawodowa - bezwzgledna

### Co mowi prawo

**Ustawa Prawo o adwokaturze, art. 6**:
> "Adwokat jest obowiazany zachowac w tajemnicy wszystko, o czym dowiedzial sie w zwiazku z udzielaniem pomocy prawnej. (...) Obowiazek zachowania tajemnicy zawodowej nie moze byc ograniczony w czasie. Adwokata nie mozna zwolnic od obowiazku zachowania tajemnicy zawodowej co do faktow, o ktorych dowiedzial sie udzielajac pomocy prawnej lub prowadzac sprawe."

**Ustawa o radcach prawnych, art. 3 ust. 3-6**:
> "Radca prawny jest obowiazany zachowac w tajemnicy wszystko, o czym dowiedzial sie w zwiazku z udzielaniem pomocy prawnej. Obowiazek zachowania tajemnicy zawodowej nie moze byc ograniczony w czasie. Radca prawny nie moze byc zwolniony z obowiazku zachowania tajemnicy zawodowej co do faktow, o ktorych dowiedzial sie udzielajac pomocy prawnej lub prowadzac sprawe."

### Co to znaczy dla AI

Transfer akt sprawy do platformy SaaS = **ujawnienie operatorowi platformy**. Nawet jezeli operator nie czyta, nie trenuje, nie udostepnia osobom trzecim - **samo ujawnienie** jest naruszeniem.

**Wyrok SN II CSK 419/12** i kolejne - tajemnica jest **bezwzgledna**, klient NIE moze "zwolnic" prawnika z tajemnicy w zakresie zakazu ujawnienia. Klient moze zgodzic sie na specyficzne dzialania (np. publikacje case study po anonimizacji), ale nie na blanket transfer do dostawcy chmury.

### Praktyczne konsekwencje

Dla buy US SaaS z aktami sprawy:
- Sama subskrypcja Enterprise nie wystarczy. Wymagane: zero-data-retention, brak treningu modelu, **lokalizacja danych w UE** (jezeli platforma to oferuje).
- Plus: ustalenie procedury w razie incydentu (kto, kiedy, jak zglasza).
- Plus: rejestr osob ktore moga dotykac akt przez AI (rozszerzenie listy z tajemnica).

Dla **build** (Patron, Cline + Ollama, lpm-pl) - dane fizycznie zostaja w kancelarii. Tajemnica zachowana bez transferu.

### Buy PL legal SaaS

LEX (Wolters Kluwer Polska), Legalis (CH Beck Polska), Mecenas IT, Praktyczne - dostawcy polscy / europejscy. **Lepiej** niz buy US, ale wciaz wymaga:
- DPA (zazwyczaj jest standard).
- DPIA (kancelaria robi sama).
- Wpis w RCP.
- Rzetelne sprawdzenie gdzie sa fizycznie serwery (zazwyczaj UE).

---

## 3. AI Act - rozporzadzenie 2024/1689

### Daty wejscia w zycie

- **2025-02-02**: rozdz. II (zakazy z art. 5) + AI literacy (art. 4).
- **2025-08-02**: rozdz. III sek. IV (notyfikacja organow), rozdz. V (GPAI, art. 51-55), rozdz. VII (governance), rozdz. XII (sankcje art. 99) + EU AI Office.
- **2026-08-02**: rozdz. III (high-risk AI z Annex III i Annex I - **w tym Annex III pkt 8 administracja sprawiedliwosci**), rozdz. IV (transparentnosc art. 50), wiekszosc obowiazkow obowiazkowych.
- **2027-08-02**: pozostale obowiazki dla zakresow z art. 6(1) (komponenty bezpieczenstwa produktow w Annex I).

### Co to znaczy dla kancelarii uzywajacej AI

Kancelaria moze byc w 3 roli wedlug AI Act:

1. **Provider** (dostawca) - tworzy system AI lub udostepnia pod swoja marka. Najwiekszy zakres obowiazkow.
2. **Deployer** (uzytkownik biznesowy) - uzywa systemu AI dostarczonego przez kogos innego. **Najczestsza rola kancelarii**.
3. **Distributor / Importer** - inne role.

Jako deployer kancelaria ma obowiazki (art. 26-27 AI Act):
- Stosowac instrukcje uzycia dostarczone przez providera.
- Zapewnic ludzki nadzor.
- Monitorowac dzialanie systemu i raportowac incydenty.
- Przechowywac logi (record-keeping, art. 12).
- Informowac osoby objete decyzja (transparentnosc, art. 50).

### Czy AI w kancelarii to high-risk?

**Annex III pkt 8 AI Act** - high-risk obejmuje AI uzywane w:

> "(a) AI systems intended to be used by a judicial authority or on their behalf to assist a judicial authority in researching and interpreting facts and the law and in applying the law to a concrete set of facts, or to be used in a similar way in alternative dispute resolution."

**Interpretacja**: AI uzywane przez **sad** lub **na zlecenie sadu**. Kancelaria uzywajaca AI do **wlasnego** researchu **NIE** wpada w to wprost.

**Ale**: jezeli kancelaria uzywa AI w postepowaniu mediacyjnym/arbitrazowym ("similar way in alternative dispute resolution") - prawdopodobnie tak.

**Ostatnie slowo**: konsultacja z komisja AI nadzorcza Polska (wyznaczana przez Minister Cyfryzacji do 2025-08).

---

## 4. Implikacje dla 8 kryteriow Build vs Buy

| Kryterium | Polski kontekst zmienia... |
|---|---|
| 1. Tajemnica zawodowa | **Drastycznie zwieksza wage** vs USA/UK. Akta sprawy do USA = wysokie ryzyko. |
| 2. Wolumen | Bez zmian vs miedzynarodowo. |
| 3. Specyfika | **Zwieksza** - polskie prawo wymaga specyficznych narzedzi, ktorych US SaaS nie ma (analiza KRS, polskie cytaty orzeczen, sygnatury sadowe). |
| 4. Czas do wartosci | Bez zmian. |
| 5. TCO 3-letni | **Skomplikowane** - dochodzi koszt audytu RODO/DPIA, koszt komentarza prawnika do kazdej decyzji, koszt szkolen AI literacy. |
| 6. Audit trail | **Drastycznie zwieksza wage** - AI Act art. 12 wymaga record-keeping dla high-risk. Plus tajemnica wymaga sciezki audytowej "kto co zobaczyl". |
| 7. Maintenance | Bez zmian. |
| 8. Vendor independence | **Zwieksza** - polskie kancelarie sa ostrozne wobec lock-in (lekcje z migracji LEX -> Legalis). |

---

## 5. Plan zgodnosci kancelarii - timeline

Niezaleznie czy build, czy buy, kancelaria potrzebuje:

| Termin | Dzialanie | Podstawa prawna |
|---|---|---|
| Przed wyborem AI | DPIA | RODO art. 35 |
| Przed wdrozeniem | Wpis w RCP | RODO art. 30 |
| Przed wdrozeniem | Klauzula w umowie z klientem | KEA / KEZRP + RODO art. 13/14 |
| Do 2025-02-02 | AI literacy dla zespolu | AI Act art. 4 |
| Do 2025-08-02 | Stanowisko nt. uzycia GPAI (art. 51-55) | AI Act |
| Do 2026-08-02 | Jezeli high-risk: technical documentation, instrukcja, record-keeping | AI Act art. 11-12 |
| Do 2026-08-02 | Transparentnosc w komunikacji z klientem (art. 50) | AI Act |

## 6. Powiazane zrodla

- Decyzja Komisji UE z 2023-07-10 ws. DPF: <https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32023D1795>
- Wyrok Sad UE T-553/23 (2025-09-03 podtrzymanie DPF): <https://curia.europa.eu/>
- AI Act CELEX 32024R1689: <https://eur-lex.europa.eu/legal-content/PL/TXT/?uri=CELEX:32024R1689>
- RODO CELEX 32016R0679.
- Ustawa Prawo o adwokaturze: <https://isap.sejm.gov.pl/isap.nsf/DocDetails.xsp?id=WDU19820160124>
- Ustawa o radcach prawnych: <https://isap.sejm.gov.pl/isap.nsf/DocDetails.xsp?id=WDU19820190145>
- Kodeks Etyki Adwokackiej (NRA).
- KEZRP (KIRP).

> **Wazne**: ten dokument NIE jest opinia prawna. Konsultuj kazda decyzje z radca prawnym, adwokatem, IOD swojej kancelarii.
