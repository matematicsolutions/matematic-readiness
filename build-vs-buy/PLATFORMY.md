# Porownanie platform - widok z perspektywy polskiej kancelarii

Subjektywne porownanie 9 opcji dostepnych dla polskiej kancelarii w 2026-05. Nie jest to ranking - kazda kancelaria moze miec inne priorytety. Tabela porownuje wedlug 8 kryteriow z [FRAMEWORK.md](FRAMEWORK.md).

**Ostrzezenie**: rynek legal AI ewoluuje szybko. Ceny i funkcjonalnosci moga sie zmienic w kazdej chwili. Sprawdzaj na bezposrednio na stronach dostawcow.

---

## Tabela porownawcza

| Platforma | Typ | Hosting | Cena (per uzytkownik, mc) | Tajemnica/RODO | Polskie prawo | Audit trail | Vendor lock-in |
|---|---|---|---|---|---|---|---|
| **Patron** | Build (open source) | Self-host (kancelaria) | API LLM 30-100 USD | Pelne, dane lokalnie | Tak (5 konektorow MCP) | Hash-chain wbudowany | Brak |
| **Harvey** | Buy US legal SaaS | USA (Azure/AWS) | 200-500+ USD | Wymaga DPF + DPA + DPIA, akta wrazliwe niemozliwe | Slabe, US-focused | Eksport logow ograniczony | Wysoki |
| **CoCounsel (Thomson Reuters)** | Buy US legal SaaS | USA | 200-400 USD | Jak Harvey | Slabe | Eksport logow | Wysoki |
| **Lexis AI / Lexis+ AI** | Buy US legal SaaS | USA | 200-500 USD | Jak Harvey | Slabe | Eksport logow | Wysoki |
| **Ruli AI** | Buy US legal SaaS | USA | Plany od 150 USD | Wymaga DPA, mlody produkt | Brak | Funkcjonalnosc DataGrid + Monitor | Sredni-wysoki |
| **LEX AI / Legalis AI** | Buy PL legal SaaS | UE (Polska/UE) | 100-300 PLN (orient.) | DPA standard, dane czesto w UE | Tak, ale wczesny etap | Funkcjonalnosc rosnie | Sredni |
| **Mecenas AI / Practice** | Buy PL legal SaaS | UE | 100-300 PLN (orient.) | DPA, UE hosting | Tak, ograniczony zakres | Sredni | Sredni |
| **Claude Enterprise / Team** | Buy general Enterprise | USA (AWS, DPF) | 60-100 USD (Team), Enterprise negotiable | DPA + DPF, zero-data-retention dla Enterprise | Brak natywnego polskiego prawa, ale Claude rozumie polski | Limited (logi w Anthropic Console) | Sredni |
| **ChatGPT Enterprise** | Buy general Enterprise | USA (Azure) | 60-100 USD | DPA + DPF, zero-data-retention | Brak | Audit logs w Admin Console | Sredni |
| **Microsoft 365 Copilot** | Buy general Enterprise | UE (jezeli M365 EU Data Boundary) | 30 USD | Dobra (jezeli EU Data Boundary skonfigurowane) | Brak natywnego polskiego prawa | M365 logi | Wysoki (Microsoft) |
| **Cline + Ollama + Claude Code skille** | Build sredni | Self-host | API LLM 20-100 USD + sprzęt | Pelne | Tak (przez MCP konektory + skille) | Custom logging | Brak |

---

## Glebsze omowienie kazdej opcji

### Patron - flagship MateMatic Build (AGPL-3.0)

[**matematicsolutions/patron**](https://github.com/matematicsolutions/patron) - lokalny RODO-safe agent AI dla polskiej kancelarii. **Akta sprawy NIE opuszczaja serwera kancelarii**. 5 konektorow MCP (SAOS, NSA, ISAP, KRS, EUR-Lex). Audit trail z hash-chain (AI Act art. 12). Bring-your-own-model (Gemini API, Claude API, Ollama lokalny).

**Plusy**:
- Tajemnica zawodowa zachowana bez transferu.
- AI Act audit trail wbudowany.
- 5 polskich konektorow prawa.
- Wdrozenie przez docker-compose.
- AGPL-3.0 - kancelaria nie ma obowiazku otwierania kodu, tylko SaaS reseller ma.

**Minusy**:
- Wymaga osoby do utrzymania (lub kontraktora MateMatic).
- Wdrozenie 30-150k PLN jednorazowo.
- Mlody projekt (2026-05), funkcjonalnosc rosnie.

**Najlepiej dla**: kancelarii z aktami sprawy w postepowaniach sadowych, dane wrazliwe, sprawy karne, klient public sector. Lub kancelaria budujaca przewage konkurencyjna przez self-host AI.

### Harvey - amerykanski lider rynku enterprise

Harvey AI - cloud-only platforma dla duzych kancelarii. Klienci globalni (Allen & Overy, A&O Shearman). Bardzo zaawansowane workflow dla M&A, due diligence, contract review.

**Plusy**:
- Funkcjonalnosc wysoka, dojrzaly produkt.
- Workflow gotowe dla M&A / DD / litigation.
- Inwestorzy w Sequoia, Kleiner Perkins (mainstream legitimacy).

**Minusy dla polskiej kancelarii**:
- Hosting USA, transfer wymaga DPF + DPA + DPIA + akceptacja ryzyka tajemnicy.
- Cena 200-500 USD per uzytkownik (orientacyjnie 2026, sprzedaz negocjowana).
- Brak polskiego prawa natywnie - kancelaria musi sama wgrac dane orzecznictwa.
- Vendor lock-in wysoki.

**Najlepiej dla**: bardzo duzych kancelarii pracujacych miedzynarodowo, gdzie wiekszosc spraw to anglojezyczne M&A bez aktow polskiej tajemnicy.

### CoCounsel (Thomson Reuters / Casetext)

CoCounsel kupiony przez Thomson Reuters w 2023 (Casetext za 650M USD). Integracja z Westlaw, Practical Law, HighQ.

**Plusy / minusy**: jak Harvey, plus integracja z ekosystemem Thomson Reuters. Czesto droga przez subskrypcje TR Pol (Lex Polska).

### Lexis AI / Lexis+ AI

LexisNexis enterprise legal AI. Integracja z Lexis Plus, Lexis Practical Guidance.

**Plusy / minusy**: jak Harvey. W Polsce dostepne przez LexisNexis Poland.

### Ruli AI

Mlodszy gracz amerykanski (od 2023). Specjalizacja: legal ops, knowledge management, regulatory monitor. Mlodsza i tansza alternatywa.

**Plusy / minusy**: jak inne US legal SaaS. Funkcjonalnosc DataGrid + Monitor unikatowa.

### LEX AI / Legalis AI

LEX (Wolters Kluwer Polska) i Legalis (CH Beck Polska) - dwie najwiekzze platformy systemow informacji prawnej w Polsce. **W 2025-2026 oba dodaja warstwy AI** do swoich SIP.

**Plusy**:
- Polski hosting (przewaznie UE).
- Polski natywny korpus orzecznictwa i ustaw.
- Integracja z workflow kancelarii (Lex Kancelaria / Legalis Office).
- Cena rzedu 100-300 PLN per uzytkownik miesiecznie (orientacyjnie 2026).

**Minusy**:
- Funkcjonalnosc AI swieza, mniej dojrzaly produkt niz Harvey.
- Vendor lock-in jezeli kancelaria juz na SIP.
- Brak transparentnosci czesto - jaki model? gdzie dokladnie hosting?

**Najlepiej dla**: kancelarii juz uzywajacych LEX lub Legalis chcacych dolozyc warstwe AI bez zmiany ekosystemu.

### Claude Enterprise / Team

Anthropic Claude w planie Enterprise (od mid-2024). Zero-data-retention, DPA, DPF.

**Plusy**:
- Zaawansowany model (Claude 4.7 Opus).
- Zero-data-retention dla Enterprise.
- Polski jezyk rozumiany dobrze.
- API + chat + Claude Code dla developerow.

**Minusy**:
- Hosting USA (AWS), wymaga DPF + DPIA.
- Brak natywnego polskiego prawa - kancelaria wgrywa orzecznictwo recznie.
- Workflow buduje sie samemu (lub kupuje Claude Code skille jak nasz [lpm-pl](https://github.com/matematicsolutions/lpm-pl)).

**Najlepiej dla**: kancelarii build minimalny lub sredni - osoba znajaca AI w zespole + Claude Team/Enterprise + Claude Code z naszymi skillami.

### ChatGPT Enterprise

OpenAI ChatGPT Enterprise. Zero-data-retention, DPA, DPF.

**Plusy / minusy**: podobne do Claude Enterprise. GPT-5 / GPT-4o / o1 / o3 jako modele.

### Microsoft 365 Copilot

Microsoft 365 Copilot dla kancelarii uzywajacych M365 (Outlook, Word, Excel, Teams, SharePoint).

**Plusy**:
- Najlatwiejsze wdrozenie (integruje sie z istniejacym M365).
- EU Data Boundary jezeli skonfigurowane (M365 hosting w UE).
- Cena 30 USD per uzytkownik miesiecznie (tania).

**Minusy**:
- Funkcjonalnosc legal-specific minimalna.
- Vendor lock-in Microsoft.
- AI w Word/Excel ograniczone do dokumentu, nie wieloplikowe workflow.

**Najlepiej dla**: kancelarii z duzym uzyciem M365 chcacych dolozyc warstwe AI bez wyjscia z ekosystemu.

### Cline + Ollama + Claude Code skille (build sredni)

Self-host AI ze sklejonych komponentow open source:

- **Cline** lub **Claude Code** jako agent IDE-style.
- **Ollama** lub **llama.cpp** jako lokalny LLM (Llama 3.1, Qwen 3, Mistral).
- Skille MateMatic ([lpm-pl](https://github.com/matematicsolutions/lpm-pl)) + 5 konektorow MCP.

**Plusy**:
- Tajemnica zachowana w pelni.
- Brak vendor lock-in.
- Najnizszy biezacy koszt (po wdrozeniu).

**Minusy**:
- Wymaga osoby technicznej w kancelarii lub partnera (MateMatic).
- Lokalne modele slabsze niz Claude/GPT-5 dla zlozonych zadan.
- Trzeba zlozyc samemu.

**Najlepiej dla**: kancelarii malych (1-15 osob) z osoba techniczna chcacych pelnej kontroli i niskiego TCO.

---

## Hybrydy (czesto najlepsze rozwiazanie)

Wiekszosc kancelarii powinna rozwazyc **hybryde**:

- **Patron / Build dla aktow sprawy** + **Claude Enterprise / ChatGPT Enterprise dla researchu publicznego** (orzecznictwo, akty prawne).
- **LEX AI / Legalis AI dla codziennej pracy** + **Patron dla wrazliwych spraw**.
- **Microsoft 365 Copilot dla automatyzacji biurowej** + **Cline + Ollama lokalnie dla aktów sprawy**.

Hybryd zmniejsza ryzyko (jezeli jedna platforma zniknie / podrozeje, mamy alternatywe), ale **zwieksza koszt utrzymania** (wiecej narzedzi do polityki, AI literacy, audytu).

---

## Co MateMatic rekomenduje (transparentnie)

MateMatic jest **autorem Patrona**. Wiec mowimy o nim z entuzjazmem. Ale:

- **Patron NIE jest dla kazdej kancelarii**. Wymaga osoby technicznej (lub kontraktora). Wymaga budzetu na wdrozenie.
- **Dla 80% polskich kancelarii** (kancelarii 2-20 osob) odpowiednia jest **kombinacja Claude Enterprise/Team + skille MateMatic + konektory MCP polskiego prawa** - lub odpowiednik z OpenAI. Nasz [audyt gotowosci](../audit/) pomoze wybrac.
- **Buy US legal SaaS (Harvey, CoCounsel, Lexis AI)** **rzadko** jest pierwszym wyborem dla polskiej kancelarii. Glownie ze wzgledu na tajemnice + RODO + cene.
- **Buy PL legal SaaS (LEX AI, Legalis AI)** jest **dobra opcja** dla kancelarii juz uzywajacych tych SIP, niezaleznie od MateMatic.

To jest ucziwa rekomendacja - nie zalezna od naszego interesu. **Jezeli Patron nie pasuje Twojej kancelarii - powiemy to wprost**.

## Powiazane

- [FRAMEWORK.md](FRAMEWORK.md) - 8 kryteriow decyzyjnych z waga.
- [POLSKI_KONTEKST.md](POLSKI_KONTEKST.md) - regulacyjne tlo.
- [TCO_CALCULATOR.md](TCO_CALCULATOR.md) - kalkulator kosztu 3-letniego.
