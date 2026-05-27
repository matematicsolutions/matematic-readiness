# Konstytucja matematic-readiness

**Wersja**: 1.0.0
**Data**: 2026-05-21

## Misja

Daj polskiej kancelarii narzedzie do **realistycznej** oceny gdzie jest na drodze do bezpiecznego wdrozenia AI - i podstawy do decyzji **build vs buy** uwzgledniajacej polskie ryzyko regulacyjne, nie amerykanskie.

## Artykul 1 - Neutralnosc dostawcow

Audyt NIE rekomenduje konkretnego produktu jako pierwszej odpowiedzi. Audyt mowi **gdzie jestes** i **co konkretnie zrobic**. Wybor narzedzia (Patron, Harvey, CoCounsel, Lexis AI, Ruli, Cline + Ollama, ChatGPT Enterprise) jest **wtorny** wobec zdefiniowania use case ow i ryzyka.

Wyjatek: framework Build vs Buy moze wskazac konkretne platformy jako przyklady, ale ZAWSZE z drugiej strony alternatyw i jawnie nazwanymi ograniczeniami kazdej.

## Artykul 2 - RODO i tajemnica zawodowa to pierwsze pytania, nie ostatnie

Audyt zaczyna kazdy wymiar od pytan o ochrone danych klienta. NIE przesuwamy "dyskusji RODO" do osobnego rozdzialu - to **bazowa warstwa** kazdej decyzji o AI.

## Artykul 3 - Polski kontekst regulacyjny

Audyt powoluje sie na konkretne polskie i unijne akty:

- **RODO** - rozporzadzenie 2016/679 (art. 5, 25, 30, 32, 44+).
- **Ustawa Prawo o adwokaturze** art. 6 - tajemnica adwokacka.
- **Ustawa o radcach prawnych** art. 3 - tajemnica radcy prawnego.
- **Kodeks Etyki Adwokackiej** (KEA) - obowiazki etyczne.
- **Kodeks Etyki Zawodowej Radcy Prawnego** (KEZRP).
- **AI Act** - rozporzadzenie 2024/1689 (CELEX 32024R1689), wejscie w zycie etapami 2025-2026.
- **DPF** (Data Privacy Framework) - decyzja Komisji UE 2023, podtrzymana przez Sad UE 2025-09-03.

Audyt CYTUJE konkretne artykuly. Tone "uwaga, RODO!" bez wskazania artykulu jest **niedopuszczalny**.

## Artykul 4 - Scoring opisowy, nie liczbowy bez podstawy

Audyt uzywa scoring 1-5 per wymiar, ale **kazda ocena ma uzasadnienie tekstowe**. Liczba bez uzasadnienia = pieczatka pseudonaukowa. Inspektor ochrony danych ma czytac uzasadnienie, nie sume punktow.

## Artykul 5 - Audyt to dialog, nie ankieta

Audyt jest **prowadzony** przez konsultanta (lub przez Claude w skillu `matematic-readiness-audit`), NIE wypelniony samodzielnie przez zarzad kancelarii w 5 minut. Rzetelna odpowiedz na pytanie "Czy zespol rozumie czym jest prompt injection?" wymaga rozmowy, nie checkboxa.

## Antygoals (czego NIE robimy)

- NIE sprzedajemy konkretnego produktu w audytie. Audyt jest neutralny.
- NIE wystawiamy certyfikatu zgodnosci z RODO/AI Act - to nie nasza rola.
- NIE oceniamy konkretnego use case ow prawnych (np. "czy moge wgrac umowe do Claude") - to wymaga prawnika.
- NIE robimy audytu dla zarzadu klienta kancelarii - audytujemy KANCELARIE, nie jej klientow.

## Roles

- **Audytor**: konsultant MateMatic albo licencjonowany inspektor ochrony danych z partnerow.
- **Walidator**: rzetelny prawnik kancelarii - sprawdza ze wnioski audytu nie kola sie z polityka kancelarii.
- **Decydent**: managing partner kancelarii - decyduje o priorytetach z mapy progresji.

## Bramki publikacji wnioskow audytu

1. wewnetrzny review pelnego raportu PRZED przekazaniem klientowi.
2. Inspektor ochrony danych (klienta lub partnera MateMatic) potwierdza wnioski RODO/AI Act.
3. Managing partner kancelarii podpisuje raport.

## Dziennik szlifu

- **2026-05-21** v1.0.0 - ratyfikacja. Cherry-pick patternu OneC0de/legal-ai-architect-toolkit (MIT). Polskie wymiary, scoring rubric, polski kontekst regulacyjny.
