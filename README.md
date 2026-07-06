# PayPal Holdings (NASDAQ: PYPL) — Leveraged Buyout Analysis

A LBO model for PayPal, built with an integrated three-statement operating model, supporting schedules, pro forma financials and schedules, a DCF, a precedent transaction analysis, and a comparable company analysis.  

In late February/ early March, there was a public debate about whether PayPal should be considered as a potential LBO or acquisition target. This project analyzes whether a sponsor could achieve a 15% return and whether a deal could be closed at a price that allows for such a return. 

**Author:** Tyler Spencer
**Last updated:** July 5, 2026
**Format:** Microsoft Excel 

---

## Thesis: returns clear sponsor hurdle, market premium below threshold

A PayPal buyout clears a sponsor's return hurdle at a financeable capital structure — but only at an offer price where the premium to market likely falls below the threshold a board would accept, and below the valuation of the company based on a discounted cash flow analysis, a precedent transaction analysis, and a comparable company analysis. 

At 7.0x LTM EBITDA, a $48.62/share offer (a 6.9% premium to the unaffected price) supports a 2.5x MOIC and a ~19.9% IRR over a ~4.5-year hold, financed with roughly 51% debt and 3.7x opening leverage — a structure leveraged credit markets would recognize.

The problem is price. The most a sponsor can pay and still clear a 15% return — a defensible hurdle for a stable, large-cap platform asset — is **$53.32/share, a 17.3% premium**. That ceiling sits *below* every other measure of the company's worth:

| Methodology | Implied value / share |
|---|---|
| **Max sponsor-affordable bid (15% IRR)** | **$53.32** |
| DCF (intrinsic) | $54.89 – $66.06 |
| Comparable companies | $77.95 – $90.01 |
| Precedent transactions | $100.73 – $115.62 |
| 52-week trading range | $38.46 – $79.50 |

The conclusion the model reaches is not "PayPal is a good LBO" — it is that **the deal clears the sponsor's return hurdle but the affordable premium lands below the market threshold, leaving a financial buyer structurally outbid in any competitive process at today's price.**

<img width="791" height="332" alt="image" src="https://github.com/user-attachments/assets/cdc334a5-d9c6-4f4b-90db-efb0a24a53f6" />

---

## Why model a deal that likely wouldn't happen?

The exercise was built to run the full valuation and structuring process to an *honest* conclusion rather than fitting the model to a predetermined outcome. Assumptions were calibrated to filings first, and the analytical verdict was allowed to follow the outputs. It demonstrates the judgment the deal actually requires: knowing when the math doesn't support the deal, and being able to say so with the evidence in hand. 

---

## Headline outputs (base case)

| Metric | Value |
|---|---|
| Entry multiple | 7.0x LTM EBITDA |
| Offer price / share | $48.62 (6.9% premium) |
| Total uses | $59.1B |
| New debt raised | $30.4B |
| Sponsor equity check | $19.2B (≈33% of total) |
| Opening gross leverage | 3.7x |
| Year-1 interest coverage | 3.9x |
| Hold period | ~4.5 years (exit FY2030) |
| Exit multiple | 7.0x (held flat to entry) |
| **Base-case MOIC / IRR** | **2.48x / 19.9%** |
| Bull / Bear IRR | 34.3% / (0.5%) |

Value creation is driven by de-levering and EBITDA growth, not multiple expansion (entry and exit multiples are held equal — no re-rating is assumed).

<img width="786" height="331" alt="Equity Value Creation Waterfall" src="https://github.com/user-attachments/assets/756e3da7-4ad9-4ad6-b383-0512ea086417" />

---

## What's in the model

A 26-tab workbook organized as a standalone operating model feeding a transaction layer:

**Operating model (historical + 5-year forecast)**
- Revenue build off TPV growth and a decomposed take-rate compression path
- Fully integrated Income Statement, Balance Sheet, and Cash Flow Statement
- Supporting schedules: working capital (days-based), PP&E / D&A, debt, income tax (with DTA reversal), and equity

**Transaction layer**
- Sources & uses with five debt tranches (revolver, TLA, TLB, senior secured and unsecured notes), tranche-level pricing over a SOFR proxy with floors, and capitalized financing-fee amortization
- Pro forma three statements with purchase accounting and goodwill flexing off the entry price
- Debt schedule with a 100% cash sweep, revolver circuit-breaker / compliance check, and mandatory amortization
- Exit waterfall and returns, including lender-side IRRs to each debt tranche, plus a value-creation bridge

**Valuation**
- DCF with dual terminal value (Gordon growth and exit multiple) and implied cross-checks between the two
- Comparable companies and precedent transactions (EV/EBITDA and EV/Gross Profit)
- Football-field summary spanning all five methodologies

**Analysis**
- Bull / base / bear scenario switch
- Sensitivity tables (exit multiple; and required IRR → maximum affordable offer price)
- Dynamic cover page stating the two-sided thesis off live outputs

---

## Key modeling decisions

These are the judgment calls behind the mechanics:

**Customer float is a pass-through, not debt capacity.** PayPal's ~$40B of custodial customer funds are modeled as a matched Funds Receivable / Funds Payable pair that passes through the transaction untouched. It provides *no* incremental leverage capacity but *does* generate real, rate-sensitive float income, which is modeled as an interest-earning balance. Treating this as either free debt capacity or as ignorable is a common and material error.

**Regulatory capital — not credit appetite — caps leverage.** At the tested structure the credit stats are financeable, but the binding constraint on a real PayPal LBO is money-transmitter licensing: state-level net-worth minimums trap cash at regulated subsidiaries and limit what can be upstreamed to service debt. The model flags this explicitly rather than assuming all free cash flow is sweepable.

**Take-rate compression is decomposed.** Reported FY2025 take-rate compression includes a non-structural FX-hedging component; only the structural, mix-driven compression is carried into the forecast, so the revenue build isn't penalized for a one-time effect.

---

## Build principles

- **Sourced to primary filings.** Operating assumptions are calibrated to FY2023–FY2025 10-K actuals, with ~100 cell comments tracing figures to specific 10-K pages (income statement, balance sheet, cash flows, debt footnote, regulated-cash disclosures, and diluted share count).
- **The argument follows the model.** Assumptions were set from filings, and the conclusion is derived from the outputs.
- **Integrity-checked.** Both balance sheets tie to zero in every projected year; the value-creation bridge foots; there are no error cells. 
- **Formatting discipline.** Consistent color convention (blue inputs, green cross-tab links, black calculations), Arial font, and dedicated sources tab.

---

## Deliberately out of scope

- **Syndication / financing-market capacity.** A $30B debt raise and $19B equity check would rank among the largest buyouts ever and could not be executed by a single sponsor or arranger; it presumes a consortium and a constructive financing window. The model demonstrates the *economics* of the structure, not the *certainty* of placing it.

---

## Data sources

- PayPal Holdings FY2025 Form 10-K (and FY2023–FY2024 for calibration)
- Comparable-company market data (Koyfin)
- Precedent-transaction filings for payments-sector deals (10-K / 20-F / 40-F, included in the accompanying data folder)

---
 
## How to read it

Start at the **Cover** for the thesis and headline outputs, then the **Summary Outputs** football field for the valuation picture. The operating model (**Revenue Build → IS / BS / CFS**) leads the beginning of the analysis, followed by valuation tabs (**DCF, Comparables, Precedents**) followed by the **LBO**, **LBO Debt Schedule**, and **LBO Returns** tabs carry the transaction mechanics, supported by pro forma financials and schedules; The **Sources** tab documents every external figure.

> The workbook uses native Excel features (data tables, live scenario switch). Open in Microsoft Excel for correct calculation and rendering.
