# Source Tiers

Used by the Research Assistant and Fact-Checking skills to rank source credibility. A claim's confidence rating in the fact-check table should reflect the lowest tier among the sources backing it.

## Tier 1 — Primary / Official (highest confidence)

- Government ministries and regulators: State Bank of Pakistan (SBP), Pakistan Bureau of Statistics (PBS), FBR, SECP, NEPRA, OGRA, PTA
- Court judgments and case filings
- Company filings, annual reports, stock exchange (PSX) disclosures
- Official legislation, gazette notifications, government budget documents

## Tier 2 — International institutions

- World Bank, IMF, Asian Development Bank
- UN agencies (UNDP, UNICEF, etc.)
- Credit rating agencies (Moody's, Fitch, S&P) for sovereign/corporate ratings

## Tier 3 — Established journalism

- Dawn, The News, Business Recorder, Profit (Pakistan Today), The Express Tribune, Bloomberg, Reuters, AP
- Use for reporting on events, quotes, and context; cross-check any statistic against a Tier 1/2 source when possible

## Tier 4 — Analysis, think tanks, opinion

- PIDE, think-tank reports, columnists, academic papers
- Useful for interpretation and context — never cite as the sole source for a factual claim ("X caused Y")
- Always attribute explicitly ("according to [analyst/org]...")

## Tier 5 — Unverified (do not use as sole source)

- Social media posts, forums, unsourced viral claims
- May be used only as a pointer to go find a Tier 1–3 source, or explicitly flagged on screen as an unverified claim/rumor being addressed

## Rule

Any claim in a script must trace to at least one Tier 1–3 source before it's marked "Verified" in the fact-check table. Tier 4 sources support interpretation, not facts. Tier 5 never stands alone.

## Running source log

Log frequently reused sources below so future episodes don't re-discover them from scratch.

| Source | Tier | Use case | Link/Access notes |
|---|---|---|---|
| PBS — Pakistan Bureau of Statistics | 1 | Inflation, population, economic surveys | |
| SBP — State Bank of Pakistan | 1 | Monetary policy, reserves, exchange rate | |
| PSX — Pakistan Stock Exchange | 1 | Listed company filings | |
| Ministry of Finance (finance.gov.pk) | 1 | Pakistan Economic Survey, budget documents, debt data | |
| Ministry of Commerce (commerce.gov.pk) | 1 | Trade/tariff policy documents | PDFs on this site are Cloudflare-protected — `WebFetch` gets a bot-challenge page, not the document. Use Tavily's extraction tool instead. |
| Competition Commission of Pakistan (cc.gov.pk) | 1 | Market concentration, cartel/enforcement cases across sectors | Has published sector-specific competitive-structure studies (e.g. automobile industry, Feb 2026) that are unusually rich, direct-from-regulator sources — worth checking for any industry episode. |
| Engineering Development Board / Ministry of Industries and Production (moip.gov.pk, engineeringpakistan.com) | 1 | Auto and engineering-sector policy documents | |
| PAMA — Pakistan Automotive Manufacturers Association (pama.org.pk) | 1 (sales data) / 4 (advocacy positions) | Auto industry sales data and policy PDFs | Some PDFs hosted here use font encodings that don't extract cleanly with basic tools — Tavily's extraction succeeded where manual extraction failed. |
| Ministry of Federal Education / pie.gov.pk | 1 | School enrollment, education statistics | |
| Dawn Business | 3 | General business reporting | |
| Profit by Pakistan Today | 3 | Business/economy deep dives | |

**On PDFs and blocked sites:** several official Pakistani government sites (`.gov.pk` domains especially) either serve documents as PDFs that basic fetch tools can't read, or sit behind bot-protection. Try `WebFetch` first; if it fails or returns garbled/binary content, try the Tavily connector's extraction tool before falling back to a secondary source describing the document instead of the document itself — see the Research Assistant skill's Tools section for detail.
