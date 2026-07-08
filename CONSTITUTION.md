# matematic-readiness Constitution

**Version**: 1.0.0
**Date**: 2026-05-21

## Mission

Give a law firm a tool for a **realistic** assessment of where it stands on the path to a safe AI deployment - and a basis for a **build vs buy** decision that accounts for Polish regulatory risk, not American risk.

## Article 1 - Vendor neutrality

The audit does NOT recommend a specific product as its first answer. The audit says **where you are** and **what specifically to do**. The choice of tool (Patron, Harvey, CoCounsel, Lexis AI, Ruli, Cline + Ollama, ChatGPT Enterprise) is **secondary** to defining the use cases and the risk.

Exception: the Build vs Buy framework may name specific platforms as examples, but ALWAYS alongside alternatives and with the explicitly stated limitations of each.

## Article 2 - GDPR and professional secrecy are the first questions, not the last

The audit begins every dimension with questions about protecting client data. We do NOT move the "GDPR discussion" into a separate chapter - it is the **base layer** of every AI decision.

## Article 3 - Polish regulatory context

The audit cites specific Polish and EU acts:

- **GDPR** - Regulation 2016/679 (art. 5, 25, 30, 32, 44+).
- **Law on the Bar (Prawo o adwokaturze)** art. 6 - advocate's professional secrecy.
- **Law on Legal Advisers (Ustawa o radcach prawnych)** art. 3 - legal adviser's professional secrecy.
- **Code of Advocate Ethics (KEA)** - ethical obligations.
- **Code of Professional Ethics for Legal Advisers (KEZRP)**.
- **AI Act** - Regulation 2024/1689 (CELEX 32024R1689), entering into force in stages 2025-2026.
- **DPF** (Data Privacy Framework) - EU Commission decision 2023, upheld by the EU General Court 2025-09-03.

The audit CITES specific articles. A "watch out, GDPR!" tone without naming the article is **unacceptable**.

## Article 4 - Descriptive scoring, not numeric without basis

The audit uses 1-5 scoring per dimension, but **every score has a textual justification**. A number without justification is a pseudo-scientific rubber stamp. The data protection officer is meant to read the justification, not the sum of points.

## Article 5 - The audit is a dialogue, not a questionnaire

The audit is **conducted** by a consultant (or by Claude in the `matematic-readiness-audit` skill), NOT filled in independently by the firm's management in 5 minutes. An honest answer to "Does the team understand what prompt injection is?" requires a conversation, not a checkbox.

## Anti-goals (what we do NOT do)

- We do NOT sell a specific product in the audit. The audit is neutral.
- We do NOT issue a GDPR/AI Act compliance certificate - that is not our role.
- We do NOT assess specific legal use cases (e.g. "can I upload a contract to Claude") - that requires a lawyer.
- We do NOT audit the firm's client's management - we audit the FIRM, not its clients.

## Roles

- **Auditor**: a MateMatic consultant or a licensed data protection officer from partners.
- **Validator**: a diligent lawyer at the firm - checks that the audit's conclusions do not conflict with the firm's policy.
- **Decision-maker**: the firm's managing partner - decides on priorities from the progression map.

## Gates for publishing audit conclusions

1. Internal review of the full report BEFORE handing it to the client.
2. A data protection officer (of the client or a MateMatic partner) confirms the GDPR/AI Act conclusions.
3. The firm's managing partner signs off on the report.

## Refinement log

- **2026-05-21** v1.0.0 - ratification. Cherry-pick of the OneC0de/legal-ai-architect-toolkit pattern (MIT). Polish dimensions, scoring rubric, Polish regulatory context.
