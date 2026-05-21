# Audyt gotowosci kancelarii do AI - 30 pytan w 5 wymiarach

Audyt prowadzony przez konsultanta (lub skill `matematic-readiness-audit` w Claude Code). 30 pytan w 5 wymiarach. Kazde pytanie z scoring 1-5 zgodnie z [SCORING.md](SCORING.md).

**Czas trwania**: 60-90 minut rozmowy z managing partnerem + IT/Office Manager + IOD jezeli istnieje.

**Output**: raport .docx z ocena 5-wymiarowa, mapa pozycji na 5-poziomowej skali progresji, lista priorytetow z [PROGRESSION_MAP.md](PROGRESSION_MAP.md).

---

## Wymiar 1: RODO compliance (6 pytan)

### R1. Kategoryzacja danych
Czy kancelaria ma spisana **kategoryzacja** danych ktore przetwarza (klienci, sprawy, kontrahenci, pracownicy)? Czy wie ktore z nich sa danymi wrazliwymi w rozumieniu art. 9 RODO (zdrowie, seksualnosc, polityka, religia, swiatopoglad, dane biometryczne, dane karne)?

### R2. Mapa transferow do panstw trzecich
Czy kancelaria zidentyfikowala wszystkie systemy SaaS gdzie obecnie transferuje dane klienta poza EOG (Microsoft 365, Google Workspace, Slack, Asana, Adobe, etc.)? Czy ma podpisane DPA z kazdym?

### R3. Polityka korzystania z AI w kancelarii
Czy istnieje **pisemna polityka** zawierajaca: co wolno wpisywac do narzedzi AI, jakie kategorie danych sa zabronione, co wymaga zgody wspolnika? Czy zespol ja przeczytal?

### R4. Procedura zgloszenia incydentu
Czy kancelaria ma procedure zgloszenia incydentu RODO w 72h do UODO (art. 33 RODO)? Czy w procedure wpisany jest **incydent AI** (wyciek danych przez ChatGPT, halucynacja z danymi klienta w outpucie, etc.)?

### R5. Rejestr czynnosci przetwarzania (RCP, art. 30 RODO)
Czy RCP istnieje? Czy zawiera czynnosc "uzycie generatywnej AI w pracy nad sprawami klientow"?

### R6. Ocena skutkow dla ochrony danych (DPIA, art. 35 RODO)
Czy DPIA zostala przeprowadzona dla biezacych use case ow AI? Czy zawiera ocene ryzyka wlasnie tych narzedzi (nie generycznego "AI")?

---

## Wymiar 2: Tajemnica zawodowa (6 pytan)

### T1. Mapa narzedzi AI w obrocie kancelarii
Czy kancelaria wie **ktore** narzedzia AI uzywaja pracownicy (konkretne aplikacje, nie "AI ogolem")? Czy istnieje rejestr?

### T2. Klauzula w umowach z klientami
Czy umowy z klientami zawieraja klauzule "kancelaria moze korzystac z narzedzi AI w zakresie sprawy"? Czy klauzula precyzuje rodzaje AI (cloud SaaS / self-host / lokalne narzedzia)?

### T3. Klauzula w umowach z pracownikami i wspolpracownikami
Czy umowy o prace / B2B zawieraja ograniczenie uzycia AI z danymi klienta? Czy aplikanci sa zwiazani?

### T4. Procedura dla bezplatnych narzedzi (ChatGPT, Claude free, Gemini)
Czy kancelaria zakazuje korzystania z bezplatnych narzedzi z danymi klienta (free tier ChatGPT trenuje na inpucie do polowy 2024, po opt-out od 2023)? Czy ma podpisany Enterprise/Team plan dla narzedzi ktore wymagaja?

### T5. Stanowisko izby adwokackiej / radcowskiej
Czy kancelaria zna stanowisko swojej izby (NRA / KIRP) wobec uzycia AI? Czy je stosuje?

### T6. Test sprawdzajacy: czy gdyby pracownik wgral akta sprawy do ChatGPT przez przypadek, to byloby naruszenie tajemnicy?
(Pytanie kontrolne - **prawidlowa odpowiedz brzmi "tak, naruszenie nawet bez wycieku, samo ujawnienie operatorowi platformy jest naruszeniem art. 6 PoA / art. 3 URP".)

---

## Wymiar 3: AI Act gotowosc (6 pytan)

### A1. Klasyfikacja systemow AI
Czy kancelaria wie ktore systemy AI uzywa, w jakiej kategorii AI Act (art. 5 prohibited / art. 6 high-risk / GPAI z art. 51 / minimal risk)? **Uwaga**: AI w prawie czesto wpada w high-risk (Annex III pkt 8 - administracja sprawiedliwosci).

### A2. Audyt high-risk
Jezeli kancelaria uzywa systemu high-risk - czy ma dokumentacje wymagana art. 11 AI Act (technical documentation, instrukcja uzycia, record-keeping)?

### A3. Transparentnosc (art. 50)
Czy kancelaria informuje klienta gdy generuje materialy przy pomocy AI (zgodnie z art. 50 AI Act, obowiazek transparentnosci, dla niektorych zastosowan obowiazkowe od 2026-08)?

### A4. AI literacy (art. 4)
Czy pracownicy maja **podstawowa znajomosc AI** (art. 4 AI Act - obowiazek od 2025-02-02)? Czy istnieje rejestr szkolen?

### A5. Procedura w razie naruszenia
Czy kancelaria wie jaka jest droga zgloszenia naruszenia AI Act i kto je w Polsce egzekwuje (Komisja AI nadzorcza wyznaczana przez Minister Cyfryzacji)?

### A6. Daty wejscia w zycie
Czy zarzad kancelarii zna daty wejscia w zycie poszczegolnych rozdzialow AI Act (2025-02, 2025-08, 2026-08, 2027-08)? Czy ma plan zgodnosci do kazdej daty?

---

## Wymiar 4: Kompetencje zespolu (6 pytan)

### K1. Mapa kompetencji
Czy kancelaria wie kto w zespole jest na jakim poziomie znajomosci AI? Czy istnieje mapa "ktora osoba na czym sie zna"?

### K2. Szkolenia
Czy w ostatnich 12 miesiacach odbylo sie szkolenie z AI dla calego zespolu? Jaki byl poziom (wprowadzenie / praktyczne uzycie / bezpieczenstwo)?

### K3. Eksperymentowanie w piaskownicy
Czy zespol ma **piaskownice** do eksperymentow (oddzielne konto Claude / ChatGPT bez danych klienta) zeby uczyc sie bez ryzyka?

### K4. Identyfikacja championa
Czy w zespole jest **osoba odpowiedzialna za AI** (champion, nie koniecznie etatowo)? Czy ma jasny mandate?

### K5. Prompt engineering
Czy zespol potrafi rozroznic prompt podstawowy od dobrego promptu? Czy istnieje wewnetrzna baza sprawdzonych promptow?

### K6. Halucynacje i weryfikacja
Czy zespol rozumie czym jest halucynacja AI? Czy ma procedure weryfikacji kazdego outputu AI ZANIM trafi do klienta lub sadu (ze szczegolnym uwzglednieniem cytatow orzeczen)?

---

## Wymiar 5: Architektura techniczna (6 pytan)

### I1. Mapa systemow kancelaryjnych
Czy kancelaria wie z czego sie sklada jej infrastruktura (LEX Kancelaria? Mecenas IT? Comarch IBARD? Microsoft 365? Lexis? Praktyczne?)? Czy ma diagram?

### I2. Hosting i lokalizacja
Czy dane sprawy sa fizycznie na serwerach w UE / Polsce, czy w US / Singapurze / chmurze hyperscaler bez konkretu? Czy istnieje deklaracja dostawcy?

### I3. Backup i ciagłosc dzialania
Czy backup jest lokalny czy w chmurze? Co sie stanie z dostepem do akt sprawy jezeli SaaS dostawca podejmie decyzje o wylaczeniu konta?

### I4. Mozliwosc self-host AI
Czy infrastruktura kancelarii pozwala na uruchomienie lokalnego modelu AI (Ollama, llama.cpp, vLLM)? Jaka jest dostepna moc GPU / RAM?

### I5. Single Sign-On i kontrola dostepu
Czy istnieje SSO dla wszystkich narzedzi? Czy odejscie pracownika powoduje wylaczenie dostepu w 24h do wszystkich systemow?

### I6. Logging i audit trail
Czy logi z systemow kancelaryjnych sa zachowywane? Czy gdyby wybuchla afera "AI uznalo halucynacje za fakt i przegrana sprawa" - czy mozna ustalic kto, kiedy, czego uzyl?

---

## Wynik

Po przejsciu wszystkich 30 pytan:

- **Suma punktow**: 30-150 (kazde pytanie 1-5).
- **Sumy per wymiar**: 6-30 (kazdy wymiar 6 pytan x 1-5).
- **Poziom progresji**: 1-5 wedlug [PROGRESSION_MAP.md](PROGRESSION_MAP.md) (mapowanie sumy na poziom).
- **Slabe wymiary**: te ponizej polowy sumy max (15/30) - priorytet do podniesienia.
- **Lista priorytetow**: 3-5 konkretnych dzialan na nastepne 90 dni.

Wynik trafia do [REPORT_TEMPLATE.md](REPORT_TEMPLATE.md).

---

## Zobacz tez

- [SCORING.md](SCORING.md) - rubric oceny per pytanie.
- [PROGRESSION_MAP.md](PROGRESSION_MAP.md) - 5 poziomow Eksplorator -> Orkiestrator.
- [REPORT_TEMPLATE.md](REPORT_TEMPLATE.md) - szablon raportu output.
- [../build-vs-buy/](../build-vs-buy/) - framework decyzyjny po audycie.
