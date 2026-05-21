# Scoring rubric - jak oceniac kazde pytanie

Kazde z 30 pytan w [CHECKLIST.md](CHECKLIST.md) ocenione w skali **1-5**. Kazda ocena MA uzasadnienie tekstowe - liczba bez slow to pieczatka pseudonaukowa (Art. 4 Konstytucji).

## Skala uniwersalna

| Punkty | Etykieta | Charakterystyka |
|---|---|---|
| **1** | Nieznane | Kancelaria NIE wie, nie ma stanowiska, nie zajmuje sie tematem. |
| **2** | Swiadomosc | Wie ze temat istnieje, **brak** dzialan, brak dokumentacji. |
| **3** | Podejscie ad hoc | Pojedyncze dzialania bez systemu, niespisane, niezarchiwizowane. |
| **4** | Spisane i wdrozone | Procedura/polityka/dokumentacja istnieje, zespol ja zna, jest stosowana. |
| **5** | Mierzalne i ulepszane | Procedura mierzona (KPI, audit trail), regularnie aktualizowana, **udokumentowane** ulepszenia. |

## Przyklady oceny per wymiar

### Przyklad R1 - "Kategoryzacja danych"

- **1 punkt**: Managing partner nie wie czy ma sporadyczne dane wrazliwe.
- **2 punkty**: Wie ze ma dane wrazliwe (np. sprawy karne), nie sklasyfikowal ich.
- **3 punkty**: Aplikant zrobil tabelke w Excelu, lezy w folderze, nikt nie zaktualizowal od poltora roku.
- **4 punkty**: Kategoryzacja istnieje w postaci dokumentu, zaakceptowana przez IOD, aktualizowana raz do roku.
- **5 punkty**: Kategoryzacja jest **zapisana** w systemie kancelaryjnym przy kazdej sprawie (pole "klasa danych"), uzywana do kierowania spraw do wlasciwych workflow, audytowana.

### Przyklad T6 - "Test sprawdzajacy"

- **1 punkt**: Wspolnik odpowiada "nie naruszenie, dopoki nie ma wyciekow z platformy".
- **2 punkty**: Wspolnik niepewny, mowi "chyba lepiej tego nie robic".
- **3 punkty**: Wspolnik wie ze naruszenie, nie umie wskazac artykulu.
- **4 punkty**: Wspolnik powoluje sie na art. 6 PoA / art. 3 URP, wie ze ujawnienie operatorowi platformy = naruszenie nawet bez wycieku do osoby trzeciej.
- **5 punkty**: Kancelaria ma spisane stanowisko z analiza orzecznictwa, polityka zabrania uzycia narzedzi free tier dla danych klienta.

### Przyklad A4 - "AI literacy (art. 4 AI Act)"

- **1 punkt**: Nikt w kancelarii nie slyszal o obowiazku z art. 4 AI Act.
- **2 punkty**: Managing partner slyszal, plan szkolen w gowie, niezrealizowany.
- **3 punkty**: Pojedyncze osoby zrobily kurs online "Wprowadzenie do AI" bez weryfikacji uczestnictwa.
- **4 punkty**: Wszyscy pracownicy ukonczyli szkolenie z certyfikatem, rejestr szkolen istnieje.
- **5 punkty**: Szkolenie jest cykliczne (rocznie), prowadzone z aktualnymi przykladami z praktyki kancelarii, **mierzony jest poziom wiedzy** przed i po (test).

### Przyklad I4 - "Mozliwosc self-host AI"

- **1 punkt**: Nikt w kancelarii nie wie co to znaczy "self-host".
- **2 punkty**: CTO wie ze istnieje opcja, nigdy nie sprawdzal infrastruktury.
- **3 punkty**: Kancelaria ma serwer ale bez GPU lub z 8 GB RAM - tylko male modele.
- **4 punkty**: Infrastruktura pozwala na uruchomienie modelu 7-13B parametrow lokalnie (CPU + 32+ GB RAM, lub GPU 8-12 GB VRAM).
- **5 punkty**: Self-host LLM JUZ dziala w piaskownicy (Ollama / vLLM / llama.cpp), zespol go uzywa do eksperymentow bez ryzyka tajemnicy.

## Reguly oceny

1. **Domyslny scoring**: 1 (Nieznane). Punkt powyzej 1 wymaga **dowodow** (dokument, screen, opis procesu) - nie samego "tak".
2. **Roznica 1 vs 2**: 2 punkty wymagaja swiadomosci tematu - czyli umieleenia powiedziec ze on istnieje i czemu jest istotny. Sama mglista znajomosc nie wystarcza.
3. **Roznica 3 vs 4**: 4 wymaga **dokumentacji**. "Robimy to" bez papieru = 3.
4. **Roznica 4 vs 5**: 5 wymaga **pomiaru** i **udokumentowanej iteracji**. Procedura w segregatorze ale niezmieniona od dwoch lat = 4, nie 5.
5. **Pytania kontrolne** (np. T6 - test wiedzy): scoring na podstawie tresci odpowiedzi, nie samego zaznaczenia "tak".

## Co zrobic z niepewnoscia

Audytor MOZE wpisac scoring "2-3" lub "3 (warunkowo)" z notatka. Konsultant podejmuje decyzje konserwatywna (nizszy z dwoch) i zaznacza w raporcie "wymaga doprecyzowania".

## Anti-pattern: scoring sredni

NIE liczymy "srednia" z 30 pytan jako jedna ocena kancelarii. Srednia ukrywa krytyczne luki (np. RODO 2/5 ale Kompetencje 4/5 = srednia 3 - falszywie optymistyczne). Liczymy **sumy per wymiar** i **minimum z wymiarow** jako wlasciwa pozycja.

## Powiazane

- [CHECKLIST.md](CHECKLIST.md) - 30 pytan.
- [PROGRESSION_MAP.md](PROGRESSION_MAP.md) - mapa wynikow na 5 poziomow.
- [REPORT_TEMPLATE.md](REPORT_TEMPLATE.md) - szablon raportu.
