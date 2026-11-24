# Chapter 1 — From Financial Statements to Free Cash Flows

Source: Lecture 02 (file L01.pdf, 53 slides) — "From Financial Statements to Free Cash Flows: Valuation Methods, Enterprise vs Equity Value, FCFO and FCFE". Sessions 2–3 of Part One (workflow step: Accounting → Cash flow). Running case: JJ Jones (accounting numbers → FCFO and FCFE).

Slide-layer tags used by the professor: **CORE** (exam, JJ Jones, all valuation methods), **PRO** (interviews, project, real work), **TECH** (avoid model errors), **PRACTICE** (discussion question).

---

## 1.1 Where we are in the workflow

Equity story → **Financial statements** → Forecasts → **Cash flows** → Discount rate → Terminal value → Multiples → Value bridge → Recommendation.

Today: **Financial statements → Cash flows → Enterprise/Equity Value.**

## 1.2 Today's professional task

You receive a company's income statement, balance sheet and cash-flow statement. Your job: produce **valuation-ready FCFO and FCFE**:
- separate **operating, financing and non-core** items;
- compute cash flows **consistently**;
- **avoid mixing enterprise value and equity value.**

## 1.3 Plan for today

| Layer | What we learn | Why it matters |
|---|---|---|
| CORE | Enterprise vs equity value; FCFO vs FCFE | Exam, JJ Jones, all valuation methods |
| CORE | Reorganizing financial statements | Turn accounting into valuation inputs |
| PRO | Enterprise-to-Equity Value bridge | Interviews, project, real valuation work |
| TECH | Statement reconciliation and adjustments | Avoid model errors |
| PRACTICE | Discussion question | Convert formulas into skill |

---

# PART A — Valuation Procedures

## 1.4 Starting point: financial view of the P&L and of the balance sheet

**Financial view of the P&L account** (built in layers):

| Layer | Item | Result |
|---|---|---|
| Operations | Revenues − operating expenses (cash) | **= EBITDA** |
| + Investments | − D&A | **= EBIT** |
| + Capital structure | + financial result | **= Earnings before taxes** |
| + Exceptional items and taxes | + exceptional items − taxes − minority interests | **= Net income** |

**Financial view of the balance sheet**:
- Left side (**capital employed**): **Fixed assets** + **Working capital** (incl. WC-like provisions).
- Right side (**invested capital** / sources): **Shareholders' equity**, **Minority interests**, **Debt-like provisions** (pension liabilities, restructuring, etc.), **Net financial debt**.

[Figure redrawn]

*(Added explanation)* The point of the layered P&L: each layer "belongs" to a different decision. EBITDA = operations; D&A = past investment decisions; financial result = capital structure decision; exceptional items/taxes/minorities = everything else. The balance-sheet view mirrors it: what the business *uses* (fixed assets + WC) is funded by equity-like and debt-like claims. Valuation needs this split because operating value (EV) and claims on it (debt, equity, etc.) are valued separately.

## 1.5 Valuation methods: one map

| Approach | Main question | Examples |
|---|---|---|
| **Income approach** | What are future cash flows worth today? | DCF, DDM, FCFO, FCFE |
| **Market approach** | What do comparable firms/transactions imply? | Trading multiples, deal multiples |
| **Asset approach** | What are assets minus liabilities worth? | Net asset value, liquidation value |
| **Economic profit** | Does the firm earn above its cost of capital? | EVA, residual income |

This course focuses on **income** and **market** approaches … but **all methods require clean financial statements**.

## 1.6 Enterprise Value to Equity Value bridge (CORE)

Diagram: **Operating invested capital** generates **FCFO** → discounted → **Assets Value (EV)**. The invested capital is financed by **Debt** and **Equity**. **Equity** receives **FCFE** → discounted → **Equity Value**. Alternatively: Assets value **minus the market value of net financial debts** → Equity Value.

> **Equity Value + Net Debt = Enterprise Value (Assets Value)**

## 1.7 Valuation perspective: asset side vs equity side (CORE)

| Cash flow | Discounting | Result |
|---|---|---|
| **FCFO** | **WACC** | **EV** (asset side) |
| **FCFE** | **k_e** | **Equity value** (equity side) |

## 1.8 The matching principle of valuation (KEY)

| Cash flow | Includes net debt issues/repayment? | Discount rate | Value |
|---|---|---|---|
| FCFO / FCFF | **No** | **WACC** | **Enterprise value** |
| FCFE | **Yes** | **Cost of equity** | **Equity value** |

**Bottom line: Never mix FCFO with cost of equity; never mix FCFE with WACC.**

*(Added explanation)* Why: FCFO is the cash available to **all** capital providers (before any payment to debt or equity) so it must be discounted at the blended return those providers require (WACC), giving the value of the whole business. FCFE is what remains for shareholders **after** debt service and net borrowing, so it is discounted at the shareholders' required return k_e, giving equity value directly. Mixing them gives a number that is neither EV nor equity value: FCFO at k_e (> WACC) undervalues the firm; FCFE at WACC (< k_e) overvalues equity.

## 1.9 EV to Equity Value bridge — detailed items (PRO)

Start from **ENTERPRISE VALUE**, then:

| Item | Definition / rule |
|---|---|
| **− Net financial debt** | **Net Financial Debt = Financial Debt − Cash & Cash Equivalents.** Common practice: **book value** of debt. But think of **market value** of debt when applicable: if all or part of the debt is listed or traded OTC, or by discounting future debt flows at the market cost of debt. |
| **− Pension provisions** | **Pension provisions = (Projected Benefit Obligation − Fair Value of plan assets) × (1 − Tax rate).** Only for **Defined Benefit** regimes. If PBO and FVA are not available, take pension provisions net of deferred tax from the balance sheet. |
| **− Other debt-like items** | **Other debt-like items = Debt-like provisions × (1 − Tax rate).** Debt-like provisions (added to net debt) may include restructuring provisions (if not recurrent), environmental damage, certain claims and litigation. Check the footnotes on provisions and see which are tax deductible. |
| **+ Non-operating assets** | Financial stakes in associates, stakes in JVs (if not related to the company's business and **not in cash flows**), other non-operating assets (land, buildings). Use **fair value** if possible (listed, known market values…), else book value, P/E or P/B ratio. |
| **− Minority interests** | May be valued at fair value; at least by applying a P/B ratio to the equity value of the company, or at book value. |

= **EQUITY VALUE**

*(Added explanation — signs and logic)*
- **Equity value = EV − Net financial debt − Pension deficit (after tax) − Other debt-like items (after tax) + Non-operating assets − Minority interests.**
- Debt-like items are subtracted because they are claims of non-shareholders on the firm's value. They are multiplied by (1 − t) because paying them is tax-deductible, so the true after-tax burden is lower.
- Non-operating assets are **added** because their value is NOT in FCFO (FCFO only captures the operating business) — but only if their income was excluded from the cash flows; otherwise you'd double count.
- Minority interests are subtracted because consolidated FCFO includes 100% of subsidiaries' cash flows, but part of those subsidiaries belongs to minority shareholders.

**Illustrative example (added):** EV = 1,000; financial debt = 300; cash = 50; pension deficit (PBO − FVA) = 40; restructuring provision (non-recurrent, deductible) = 20; t = 25%; stake in a non-consolidated associate (fair value) = 30; minorities = 25.
- Net debt = 300 − 50 = 250.
- Pension = 40 × 0.75 = 30. Other debt-like = 20 × 0.75 = 15.
- Equity value = 1,000 − 250 − 30 − 15 + 30 − 25 = **710**.

### Full claims picture (W_assets)

The value of the firm's assets **W_assets** is shared by:
1. **Market value of financial debts**,
2. **Market value of debt "substitutes"** (debt-like items),
3. **Bond value of convertibles**,
4. **Current equity and other shareholders' rights**, which itself splits into the **value of the equity component embedded in outstanding warrants, stock option plans, etc.** and the **value of equity (W_equity)**.

[Figure redrawn]

*(Added explanation)* A convertible bond = straight bond + conversion option; its bond part is a debt claim, its option part an equity-like claim. Warrants and employee stock options are also claims on equity: to get the value per existing share, subtract their value from total equity value.

---

# PART B — Earnings and Cash Flows

## 1.10 Reorganization of the balance sheet: the functional view

To construct cash flows we use the **functional reorganization of the balance sheet**: aggregate assets and liabilities **based on the business operations they belong to**.
- Assets: Accounts receivable; Inventory; Net fixed assets; Surplus assets; Cash, marketable securities, financial credits.
- Liabilities: Accounts payable; Financial liabilities; Equity.

**Accounting classifies items for reporting; valuation reorganizes them by economic function.**

### Net working capital and net invested capital

Categories related to the cycle of business operations: **+ Inventory + Accounts Receivable − Accounts Payable** (for goods/services related to operations).

> The algebraic sum of these categories yields the **operating Net Working Capital (NWC)**:
> **NWC = Inventory + Accounts Receivable − Accounts Payable**

The **net (operating) invested capital (NIC)** is composed of:
1. **Net (operating) assets (NA)** — operating assets net of D&A and impairment losses. Size relative to business volume depends on the **capital intensity index** (the technical characteristics of the production process).
2. **Working capital (WC)** — size, for a given business volume, is directly related to the **length of the financial cycle** of operations (buy → transform → sell).

> **NIC = NA + WC = Fixed assets + Inventories + Accounts receivable − Accounts payable**

[Figure redrawn: Receivables + Inventories − Payables = WC; Fixed assets = NA; WC + NA = NIC]

### Benefits of the functional reorganization

- Precise link between **balance-sheet values and their flows in the income statement** → rigorous profitability analysis; simpler construction of economic and financial plans.
- A specific category of revenues and costs for **non-core activities** allows separate valuation of (i) the company's **core assets** and (ii) **surplus assets**.
- To value the company as a **sum of parts (SOP)**, reconstruct costs for each separate business area, normally **up to the EBIT level**.

### How the assets are financed

Net (operating and non-operating) assets — **NIC + Surplus assets + Cash/marketable securities/financial credits** — are covered by: (i) **financial liabilities** (short and medium/long term) and (ii) **equity**.

> **Net financial position = Financial liabilities − Cash & cash equivalents**
> The proportion of the net financial position with respect to equity determines the **financial structure** of the company.

## 1.11 Reorganization of the income statement: "at added value"

**Why we care: FCFO starts from operating income, not net income.**

1. **Sales revenues** (or production value achieved during the fiscal year)
   − Consumption of raw materials and components bought from third parties
   − Costs of services acquired from outside (supplies, ads, …)
   − Other external expenses (administration and control, organization, finance)
2. **= Added value**
   − Labor costs
3. **= EBITDA** (Earnings Before Interest, Taxes, Depreciation and Amortization)
   − Depreciation & Amortization and Provisions
4. **= Operating income or EBIT**
   − Financial expenses (+ financial revenues) / + Net result from non-core activities
5. **= Gross operating income from continuing operations**
   − Extraordinary losses (+ extraordinary gains)
6. **= EBT** (Earnings Before Taxes)
   − Tax expenses
7. **= Net income**

## 1.12 From earnings to cash flows: introduction (CORE)

Goal: consider **all monetary inflows and outflows for all business areas** — jointly they determine the firm's financial dynamics in a period.

Forces behind the financial dynamics:
- continuing business operations and related investment/divestment in NWC;
- investment and divestment in fixed assets;
- underwriting and repayment of financing instruments (incl. equity issuance);
- payment of interest/dividends to debt/equity holders;
- net flows for the purchase or disposal of surplus assets.

Reorganized into three areas: **(1) operating area; (2) financing area; (3) non-core area.**

## 1.13 Operating area (CORE)

Cash generated from current operations = operating result + all costs that do not generate monetary transactions (mainly **D&A** in industrial companies) → **this figure is EBITDA**.

- **EBITDA is not free cash flow: working capital can absorb cash.**
- You cannot always use EBITDA to finance outflows unrelated to current activities: the cash actually available depends on the **change in NWC** in the period. A **positive change in NWC = an employment of cash**, absorbing part of EBITDA. Therefore:

> **Monetary flow of current activities = EBITDA ± ΔWC** (an increase in WC is subtracted; a decrease is added)

*(Added explanation)* Example: EBITDA 100; receivables grow by 30 because sales grew and customers pay at 60 days. The 30 is revenue already in EBITDA but not yet collected → cash from current activities = 100 − 30 = 70.

## 1.14 Financing area (PRO)

Monetary flow from the financing area = all movements related to debt and equity capital:

− Passive interest payments
− Dividend distribution
+ New debt negotiated
− Expiring debt repaid
+ Equity increases
− Equity repayment
**= Monetary flow from the financing area**

All these flows are computed **net of fiscal adjustments for the company** (not for debt- or equity-holders) — e.g., interest is taken after the corporate tax shield.

## 1.15 Non-core area (PRO)

Flow from surplus (non-core) assets — easy, few elements:
1. **Income from non-core businesses**;
2. **New investments in non-core businesses − divestments of non-core businesses.**

Again **net of fiscal adjustments for the company**.

## 1.16 TECH layer: reconciling the statements

The formulas are simple; the model is harder: **every item must reconcile across the income statement, balance sheet and cash-flow statement.**

### Mechanics Part 1 — Exhibit 3.4 (Holthausen–Zmijewski): changes in balance sheet → cash-flow statement

[Screenshot of the exhibit + clean reconstruction]

Balance sheet items (Year 1, Year 2) and where their change goes:

| Balance sheet change | Goes to cash-flow statement line |
|---|---|
| Δ Cash (C) | = ΔC, change in cash balance (the bottom line) |
| Δ Current operating assets (COA), Δ Non-current operating assets (NCOA), Δ Current operating liabilities (COL), Δ Interest payable (INT/P), Δ Non-current operating liabilities (NCOL) | − ΔWCO, change in net operating working capital (in CFO) |
| Δ Net PP&E (PPEQ) | split into + NCEXP (depreciation, in CFO), − INVEST (capital expenditures) and + DISP (dispositions) in investing |
| Δ Current portion LT debt (CLTD), Δ Long-term debt (LTD) | + ΔDFIN, change in debt financing |
| Δ Preferred stock (PS) | + ΔPSFIN |
| Δ Common stock (CS) | + ΔCEFIN |
| Δ Retained earnings (RE) | via statement of retained earnings: RE_Y1 + NI − PSDIV − CDIV = RE_Y2 → + NI (in CFO), − PSDIV, − CDIV (in financing) |

Cash-flow statement:
- **CFO** = + NI + NCEXP − NCREV − ΔWCO
- **CAPEX (cash flow from investing)** = − INVEST + DISP
- **CFF** = − CDIV − PSDIV + ΔDFIN + ΔPSFIN + ΔCEFIN
- **ΔC = CFO + investing + CFF**

### Mechanics Part 2 — Exhibit 3.8: cash-flow statement → free-cash-flow schedule

Free cash flow schedule:

| Line | Item |
|---|---|
| + EBIT | Net income + interest + taxes |
| − TAX | Tax on EBIT |
| = UE | **EBIT after tax** (unlevered earnings) |
| + NCEXP | Non-cash expenses (depreciation) |
| − NCREV | Non-cash revenues |
| − ΔRC | **Required cash** |
| − ΔWCO | Change in net operating working capital |
| = **UCFO** | Unlevered cash flow from operations |
| − INVEST | Investments* |
| + DISP | Cash flow from dispositions* |
| = **UFCF** | **Unlevered free cash flow (= FCFO)** |
| − PSDIV | Preferred stock dividends |
| − INT | Interest paid |
| + ITS | Interest tax shield |
| + ΔDFIN | Change in debt financing |
| + ΔPSFIN | Change in preferred stock financing |
| = **EFCF** | **Equity free cash flow (= FCFE)** |
| − CDIV | Common equity dividends paid |
| + ΔCEFIN | Change in common equity financing |
| = ΔXC | **Change in excess cash** |
| + ΔRC | Required cash |
| = ΔC | Change in cash balance |

*CAPEX = INVEST − DISP.

*(Added explanation)* Key take-aways from Exhibit 3.8:
1. The free-cash-flow schedule ends at the **same ΔC** as the cash-flow statement → it reconciles.
2. **Required cash** (cash needed to run the business) is an **operating** investment, subtracted in UCFO like working capital; **excess cash** is what is left after paying shareholders.
3. **Tax on EBIT** ≠ income-tax expense: TAX on EBIT = tax expense + interest tax shield (ITS = t × INT). The ITS is added back in EFCF.
4. Dividends are **not** in FCFE: they are a **use** of FCFE (FCFE − dividends + new equity = change in excess cash).

## 1.17 Two cash-flow definitions to remember (KEY)

> **FCFO = EBIT × (1 − tax rate) + non-cash charges − CapEx − increase in non-cash WC**
>
> **FCFE = net income + non-cash charges − CapEx − increase in non-cash WC + net debt issued**

## 1.18 Cash-flow definitions in full

**1. FCFE — equity-side valuation**

  + Net income — adjusted
  +/− Non-cash expenditure (other than D&A) / non-cash revenues
  − **Net CapEx** (= Capital expenditures − D&A)
  − Changes in non-cash working capital
  − (Principal debt repayments − New debt issues)
  **= FCFE**

**2. FCFO — asset-side valuation (two equivalent routes)**

Route (a), from FCFE:
  + FCFE
  + Interest expense × (1 − tax rate)
  + (Principal debt repayments − New debt issues)
  **= FCFO**

Route (b), from EBIT:
  + Operating income (EBIT) — adjusted
  +/− Non-cash expenditure (other than D&A) / non-cash revenues
  − Taxes on EBIT
  − Reinvestment needs (Net CapEx and working capital)
  **= FCFO**

[Ignoring preferred dividends. If preferred stock exists, preferred dividends also need to be netted out (from FCFE).]

Compact relationship:
> **FCFE = FCFO − Interest × (1 − t) + (New debt issues − Principal repayments)**

*(Added explanation — proof that routes agree)* NI = (EBIT − Int)(1 − t) = EBIT(1 − t) − Int(1 − t). Plug into FCFE: FCFE = EBIT(1−t) − Int(1−t) + D&A − CapEx − ΔWC + Net borrowing = FCFO − Int(1 − t) + Net borrowing. ✓

## 1.19 Discussion Question (PRACTICE) — full solution

Data: EBIT $400; interest expensed and paid $100; tax rate on all income 40%; net income $180; depreciation $200; capital expenditures $540; increase in required non-cash working capital $80; increase in required cash $20; increase in debt financing $400; paid-in common dividends $90; change in cash balance on balance sheet $70; cash flow from operations $300.

Tasks: (i) cash-flow statement; (ii) FCFO; (iii) FCFE.

*(Solution written by us — not provided in the slides. Structure follows Exhibit 3.8.)*

**Preliminary check — net income:** EBT = 400 − 100 = 300; taxes = 300 × 40% = 120; NI = 300 − 120 = **180** ✓.

**(i) Cash-flow statement**

| | $ |
|---|---|
| Net income | 180 |
| + Depreciation | 200 |
| − Increase in non-cash WC | (80) |
| **= Cash flow from operations (CFO)** | **300** ✓ |
| − Capital expenditures | (540) |
| **= Cash flow from investing** | **(540)** |
| + Increase in debt financing | 400 |
| − Common dividends paid | (90) |
| **= Cash flow from financing (CFF)** | **310** |
| **= Change in cash balance** | 300 − 540 + 310 = **70** ✓ |

**(ii) FCFO (unlevered free cash flow)**

| | $ |
|---|---|
| EBIT | 400 |
| − Tax on EBIT (400 × 40%) | (160) |
| = EBIT × (1 − t) | 240 |
| + Depreciation | 200 |
| − Increase in required cash | (20) |
| − Increase in non-cash WC | (80) |
| = UCFO | 340 |
| − Capital expenditures | (540) |
| **= FCFO** | **(200)** |

Note: tax on EBIT (160) ≠ tax actually paid (120); the difference (40) is the interest tax shield, 100 × 40%.
(If one ignored required cash, FCFO would be −180; the lecture explicitly stresses "required cash is not excess cash", so required cash is an operating need and FCFO = −200.)

**(iii) FCFE**

Route from FCFO:

| | $ |
|---|---|
| FCFO | (200) |
| − Interest paid | (100) |
| + Interest tax shield (100 × 40%) | 40 |
| + Net debt issued | 400 |
| **= FCFE** | **140** |

Check via net income: FCFE = 180 + 200 − 540 − 80 − 20 + 400 = **140** ✓.

**Reconciliation with the cash balance:**
FCFE 140 − common dividends 90 = **change in excess cash 50**; + increase in required cash 20 = **change in cash 70** ✓ (matches the balance sheet).

**What these Discussion Questions test** (slide):
1. **CFO is not FCFO** (300 vs −200: CFO is after interest and before CapEx).
2. **FCFO excludes (debt) financing** (the 400 of new debt does not enter FCFO).
3. **FCFE includes net debt issuance** (+400).
4. **Dividends are a use of FCFE, not part of FCFO** (the 90 appears only after FCFE).
5. **Required cash is not excess cash** (the 20 is an operating investment).

*(Added remark)* FCFO is negative here because the company is in an investment phase (CapEx 540 ≫ depreciation 200): negative FCFO is not "bad" per se — a growing firm reinvests. It was financed by new debt, which makes FCFE positive.

## 1.20 Cash-flow definitions: interpretation

- These concepts apply to **projections** used in valuation techniques.
- **FCFO** (also **Free Cash Flow to Firm, FCFF**) = cash generated by the operating business. In FCFO the taxes are the **theoretical fiscal outflow on the operating result in a scenario of no debt**.
- **FCFE** = net cash available to shareholders. Its value depends not only on interest and taxes but also on the **change in the net financial position**. Therefore, projections for an FCFE valuation must include a **target financial structure** (FCFE depends on future financing choices involving debt).

---

## 1.21 From reported to actual earnings (overview)

Flowchart — **Measuring earnings** requires:
- **Normalize earnings** using the firm's history and comparable firms;
- **Cleanse operating items** of financial expenses, capital expenses and non-recurring expenses — notably **operating leases** (convert into debt, adjust operating income) and **R&D expenses** (convert into asset, adjust operating income);
- **Update**: trailing earnings, unofficial numbers.

[Figure redrawn]

## 1.22 Adjusting accounting earnings

1. **No financial expenses mixed with operating expenses.**
   - *Financial expense*: any **tax-deductible commitment that you have to meet no matter what your operating results**; failure to meet it leads to loss of control of the business.
   - Example — **operating leases**: accounting may treat them as operating expenses, but they are really financial expenses → reclassify. **No effect on equity earnings, but operating earnings change.**
2. **No capital expenses (CAPEX) mixed with operating expenses (OPEX).**
   - *Capital expense*: any expense expected to generate **benefits over multiple periods**.
   - Example — **R&D**: R&D is a capital expenditure, so operating income must be adjusted.

## 1.23 Operating leases

Chart: **Operating lease expenses as % of operating income** — Market ≈ 12.5%; Apparel stores ≈ 43.5%; Furniture stores ≈ 49.5%; Restaurants ≈ 26.5% (values read from the bar chart). → Leases matter most in retail/restaurants.

Treatment:
- Operating lease expenses may be treated as operating expenses, but more appropriately they should be treated as **financing expenses**:
  - **Debt value of operating leases = PV of operating lease commitments at the pre-tax cost of debt.**
  - Converting leases into debt also creates an **asset of the same value**.

> **Adjusted operating earnings = Operating earnings + Operating lease expense − Depreciation on leased asset**
>
> Approximation: **Adjusted operating earnings ≈ Operating earnings + Pre-tax cost of debt × PV of operating leases**

*(Added explanation)* The lease payment = interest + "repayment". Adding back the whole payment and subtracting depreciation leaves the interest component inside EBIT → this is "financing", so it is moved below EBIT. The approximation adds back only the imputed interest (k_d × lease debt), assuming depreciation ≈ principal part.

### Worked example — The GAP

Data: EBIT $1,012m; debt $1.97bn; pre-tax cost of debt 6%; operating lease payments this year $978m; commitments:

| Year | Commitment ($m) | Discount factor 1/1.06^t | PV at 6% |
|---|---|---|---|
| 1 | 899.00 | 0.94340 | 848.11 |
| 2 | 846.00 | 0.89000 | 752.94 |
| 3 | 738.00 | 0.83962 | 619.64 |
| 4 | 598.00 | 0.79209 | 473.67 |
| 5 | 477.00 | 0.74726 | 356.44 |
| 6 | 982.50 | 0.70496 | 692.62 |
| 7 | 982.50 | 0.66506 | 653.42 |
| 6 & 7 | 982.50 each year | | **1,346.04** |
| **Debt value of leases** | | | **4,396.85** (also value of leased asset) |

(Slide typo: it shows $1,356.04 for years 6–7; the correct figure is $1,346.04 — only this value sums to the slide's total of $4,396.85.)

*(How "6 & 7" arises — added)* Commitments beyond year 5 are often reported as a lump sum (here 1,965 = 2 × 982.5) and spread evenly over the remaining years.

- **Adjusted debt outstanding** = 1,970 + 4,397 = **$6,367m**.
- **Adjusted EBIT** = Reported EBIT + OL expense this year − Depreciation = 1,012 + 978 − 4,397/7 = 1,012 + 978 − 628 = **$1,362m** (7-year useful life, straight line).
- **Approximate EBIT** = 1,012 + 4,397 × 6% = 1,012 + 264 = **$1,276m**.

### Conventional accounting vs operating leases treated as debt (GAP)

| | Conventional accounting | Operating leases treated as debt |
|---|---|---|
| Income statement | EBIT before leases 1,990 − Op. leases 978 = **EBIT 1,012** | EBIT before leases 1,990 − Depreciation of leased assets 628 = **Adjusted EBIT 1,362**. Interest expense rises to reflect the conversion of leases into debt. |
| Balance sheet | Off balance sheet (not shown as debt or asset); only conventional debt of $1,970m | Asset: OL asset 4,397; Liability: OL debt 4,397. **Total debt = 4,397 + 1,970 = $6,367m** |
| Cost of capital | 8.20% × (7,350/9,320) + 4% × (1,970/9,320) = **7.31%** | 8.20% × (7,350/13,717) + 4% × (6,367/13,717) = **6.25%** |
| (inputs) | k_e = 8.20%; after-tax k_d = 4%; MV equity = 7,350 | same |
| ROIC | 1,012 × (1 − 0.35)/(3,130 + 1,970) = **12.90%** | 1,362 × (1 − 0.35)/(3,130 + 6,367) = **9.30%** (9.32% unrounded) |
| (inputs) | BV equity 3,130; t = 35% | same |

Step details: 9,320 = 7,350 + 1,970; 13,717 = 7,350 + 6,367; 1,012 × 0.65 = 657.8 and 657.8/5,100 = 12.90%; 1,362 × 0.65 = 885.3 and 885.3/9,497 = 9.32%.

*(Added explanation)* Capitalizing leases: **EBIT ↑, debt ↑, WACC ↓** (more weight on cheaper debt), **invested capital ↑ → ROIC ↓**. Equity value is essentially unaffected: higher EV but also more debt subtracted.

### IFRS 16

- Issued January 2016, superseding IAS 17; applies to reporting periods beginning on/after **1 January 2019**.
- **All leases have to be capitalized** (shown on the lessee's balance sheet): finance leases → capitalized (as before); **operating leases → capitalized (main novelty)**; short-term and/or low-value leases → **optional recognition exemption**.

[Figure redrawn]

*(Added explanation)* Under IFRS 16 the lease adjustment above is already done by the accountants (right-of-use asset + lease liability; depreciation + interest instead of rent). Under US GAAP (ASC 842), operating leases are on the balance sheet but the P&L expense remains a single operating lease cost — so the EBIT adjustment can still be needed. Exam point: under IFRS 16 lease liabilities are part of debt in the EV→equity bridge.

## 1.24 R&D expenses

Chart: **R&D as % of operating income** — Market ≈ 10.5%; Petroleum ≈ 30.5%; Computers ≈ 50% (values read from the bar chart).

### Worked example — SAP (EBIT before R&D = 3,045; R&D has a 5-year life)

Straight-line amortization: each year's R&D is amortized 1/5 = 20% per year; the unamortized portion of the R&D of year −j is (1 − j/5).

| Year | R&D expense | Unamortized portion | Unamortized amount | Amortization this year (R&D/5) |
|---|---|---|---|---|
| Current | 1,020.02 | 1.00 | 1,020.02 | — |
| −1 | 993.99 | 0.80 | 795.19 | 198.80 |
| −2 | 909.39 | 0.60 | 545.63 | 181.88 |
| −3 | 898.25 | 0.40 | 359.30 | 179.65 |
| −4 | 969.38 | 0.20 | 193.88 | 193.88 |
| −5 | 744.67 | 0.00 | 0.00 | 148.93 |
| **Total** | | | **2,914.02** | **903.14** |

- **Value of research asset = €2,914m** (sum of unamortized portions).
- **Amortization of research asset in current year = €903m** (sum of each layer's amortization).
- **Increase in operating income = 1,020 − 903 = €117m.**

(Convention, added: current-year R&D is not amortized this year; the R&D from year −5 receives its last amortization this year.)

### Conventional accounting vs capitalized R&D (SAP, t = 36.54%)

| | Conventional | Capitalized R&D |
|---|---|---|
| Income statement | EBIT before R&D 3,045 − R&D 1,020 = **Reported EBIT 2,025**; EBIT(1 − t) = 2,025 × 0.6346 = **1,285** | EBIT before R&D 3,045 − amortization 903 = **Adjusted EBIT 2,142** (+117m); Adjusted EBIT(1 − t) = 2,142 × 0.6346 = **1,359**. Ignored tax benefit = (1,020 − 903) × 0.3654 = **43**. Adjusted EBIT after tax benefit = 1,359 + 43 = **1,402** (= 1,285 + 117). Net income also rises by 117m. |
| Balance sheet | Off balance sheet; book equity 3,768m is **understated** because one of the biggest assets is off the books | R&D asset 2,914 ↔ book equity + 2,914. **Adjusted book equity = 3,768 + 2,914 = 6,682** |
| Capital expenditures | Conventional net CapEx = 2 | **Adjusted net CapEx = 2 + 1,020 − 903 = 119** |
| Cash flows | EBIT(1 − t) 1,285 − net CapEx 2 = **FCFF 1,283** | Adjusted EBIT(1 − t) 1,402 − adjusted net CapEx 119 = **FCFF 1,283** |
| ROIC | 1,285/(3,768 + 530) = **29.90%** | 1,402/(6,682 + 530) = **19.44%** |
| | Liabilities assumed = 530 | same |

**KEY insight: capitalizing R&D changes EBIT, invested capital, ROIC and net CapEx — but NOT the free cash flow (1,283 both ways)**, because the same 117 is added to EBIT and to reinvestment. ROIC falls because invested capital rises a lot.

### The tax benefit adjustment

R&D expenses are **tax deductible** ⇒ when capitalizing them, a tax benefit would be lost (the firm deducts the whole R&D, not just the amortization). So add the tax savings on (R&D expense − amortization) to the after-tax adjusted EBIT:

- Adjusted EBIT after tax_t = (EBIT_t + R&D_t − Amort_t) × (1 − τ_C)
- Additional tax benefit_t = (R&D_t − Amort_t) × τ_C
- **Corrected adjusted EBIT after tax_t = EBIT_t × (1 − τ_C) + R&D_t − Amort_t**

(Algebra: (EBIT + R&D − A)(1 − τ) + (R&D − A)τ = EBIT(1 − τ) + (R&D − A)(1 − τ) + (R&D − A)τ = EBIT(1 − τ) + R&D − A.)

> **When adjusting EBIT for R&D capitalization, we can use pre-tax R&D expenses and pre-tax estimated amortization of the R&D asset** (i.e., add R&D − amortization to after-tax EBIT, with no tax on the difference).

SAP check: 1,285 + 1,020 − 903 = 1,402 ✓.

## 1.25 Tax rate

### Effective tax rates of US firms
Histogram (frequency of firms by effective tax rate bucket): 5% ≈ 13; **10% ≈ 29**; 15% ≈ 26; 20% ≈ 17; 25% ≈ 7; 30% ≈ 4; 35% ≈ 0; 40% ≈ 0 (read from chart). → Effective rates are mostly far below the statutory/marginal rate.

### Impact on valuations — 2018 US tax reform (aggregate US equities)

Macro inputs: US T-bond rate (1/1/18) = 2.41%; ERP = 5.08%.

| | Pre-reform | Post-reform |
|---|---|---|
| Beta | 1.07 | 1.07 |
| Pre-tax cost of debt | 3.91% | 3.91% |
| Marginal tax rate | 38.00% | 24.00% |
| Debt to capital | 23.51% | 23.51% |
| Revenues | $12,254.10 | $12,254.10 |
| EBIT | $1,438.22 | $1,438.22 |
| Effective tax rate | 25.19% | 20.00% |
| After-tax return on capital | 12.76% | 13.65% |
| Reinvestment rate | 59.27% | 65.00% |
| Length of growth period | 5 | 5 |
| **Computed:** cost of equity | 7.85% | 7.85% |
| After-tax cost of debt | 2.42% | 2.97% |
| Cost of capital | 6.57% | 6.70% |
| Expected growth rate | 7.56% | 8.87% |
| PV of FCFF in high growth | $2,253.08 | $2,139.72 |
| Terminal value | $30,926.29 | $34,590.66 |
| **Value of firm today** | **$24,750.46** | **$27,151.37** |

Value with old tax code = $24,751bn; with new = $27,151bn; **change = $2,400bn; % change = 2,400/24,751 = 9.70%.**

Annotations (slide):
- **Marginal tax rate**: federal corporate rate 35% → 21% lowers the overall marginal rate (with state & local taxes) from 38% to 24%.
- **Effective tax rate**: lower US rate and shift to a regional (territorial) tax model for global taxes lower the effective rate from 25.19% to 20%.
- **Tax effect on debt**: lower marginal tax rate **increases** the after-tax cost of debt and the cost of capital (debt ratio fixed).
- **Higher ROIC/reinvestment**: ROIC rises proportionally with the drop in the effective tax rate; capital-expensing rules lead to marginally more reinvestment. **Expected growth = ROIC × reinvestment rate.**

Verification (added):
- k_e = 2.41% + 1.07 × 5.08% = 7.85% (CAPM).
- After-tax k_d: 3.91% × (1 − 0.38) = 2.42%; 3.91% × (1 − 0.24) = 2.97%.
- WACC: 7.85% × 0.7649 + 2.42% × 0.2351 = 6.57%; 7.85% × 0.7649 + 2.97% × 0.2351 = 6.70%.
- After-tax ROC: 12.76% × (1 − 0.20)/(1 − 0.2519) = 13.65%.
- g = 12.76% × 59.27% = 7.56%; 13.65% × 65% = 8.87%.

*(Added explanation)* Two opposite effects: lower taxes raise WACC (smaller debt tax shield → value ↓) but raise after-tax cash flows and growth (value ↑). The second dominates → +9.7%. Note that the **marginal** rate goes into the cost of debt (tax shield), the **effective** rate into operating cash flows in the near term.

### Which tax rate to use (summary)

Choice: **effective** vs **marginal**.
- In projections it is **safer to use the marginal tax rate**, since the effective one simply reflects differences between accounting and tax books.
  1. **Marginal rate**: biases after-tax operating income (NOPAT) in the early years, but more accurate in later years.
  2. **Effective rate** (= taxes due / taxable income): if used, **adjust it towards the marginal rate over time**, because tax-based revenues/expenses should converge to accruals (and thus cash) in the long run (i.e., in perpetuity).
- **Multinationals** — either:
  - a **weighted average of marginal tax rates**, weights = income from each country; or
  - the **marginal rate of the country of incorporation**, assuming income will eventually be repatriated (**safest approach**); or
  - keep each country's income separate and apply a different marginal rate to each income statement.

---

# PART C — Reinvestment Needs

## 1.26 Net capital expenditures I

FCFE and FCFF are computed **after reinvestment**, which includes **net CapEx** (long term) and **non-cash working capital** (short term):
- **Net CapEx = CapEx − D&A**
- **Non-cash working capital**: removes **excess cash** (beyond day-to-day operating needs).

Since we start from earnings **after** D&A (net income, EBIT), we add D&A back:

> **Cash flows from operations = EBIT × (1 − τ_C) + Non-cash expenses (e.g., D&A) − Non-cash revenues**

- D&A must be adjusted **consistently with the adjustments made to earnings** (D&A of capitalized operating leases, R&D…).
- **Net CapEx is a function of growth**: high-growth firms have much higher net CapEx than low-growth ones.
- Assumptions about net CapEx can **never be made independently of assumptions about future growth.**

*(Added explanation)* In steady state with no growth, CapEx ≈ D&A (maintenance only) → net CapEx ≈ 0. Growth requires net CapEx > 0. This anticipates the "Expected growth = ROIC × reinvestment rate" relation (tax-reform slide, and later chapters).

## 1.27 Net capital expenditures II

1. **Smoothing lumpy CapEx** — firms seldom have smooth CapEx; normalize:

> **Estimated net CapEx = (1/n) Σ_{i=1}^{n} CapEx_{t−i} − D&A_t**

   Caveats: (i) **do not average D&A** (already smoothed); (ii) choose carefully the number of historical years; (iii) check industry averages of (a) **CapEx/D&A (preferred)** and/or (b) CapEx/Sales.

2. **Acquisitions of other firms** — they are like CapEx; normalize:

> **Adjusted net CapEx = Net CapEx + Acquisitions of other firms − D&A of such acquisitions**

   Caveats: (i) most firms don't acquire every year → normalize (average over time); (ii) you **may ignore acquisitions if done at fair value** (zero-NPV, accounting also for synergies), **but then exclude growth from acquisitions** when estimating growth.

*(Added numerical illustration)* CapEx last 4 years: 80, 200, 60, 100 → average 110; current D&A 70 → estimated net CapEx = 110 − 70 = 40 (not 100 − 70 = 30, and D&A not averaged).

## 1.28 Net capital expenditures III — CapEx accounted as OpEx

If we re-categorize some OpEx as CapEx (e.g., R&D), adjust **consistently**:
- a) **Adjusted CapEx_t = CapEx_t + R&D_t**
- b) **Adjusted D&A_t = D&A_t + R&D asset amortization_t**
- c) **Adjusted net CapEx_t = Adjusted CapEx_t − Adjusted D&A_t = Net CapEx_t + R&D_t − R&D amortization_t**

The adjustment to net CapEx **mirrors** the adjustment to EBIT → consistent adjustments to operating earnings and to net CapEx (SAP: +117 on both).

## 1.29 Changes in non-cash working capital

Second component of reinvestment: cash for working-capital needs.

**Definition of non-cash WC:**
1. **Remove cash and marketable securities in excess** of the cash needed for day-to-day operations. That excess cash should be either (i) **deducted from debt** when estimating the cost of capital (net debt) or (ii) **included as a surplus asset** in the valuation.
2. **Remove interest-bearing debt** included in current liabilities (e.g., short-term bank debt, current portion of LT debt) — it belongs to debt for the cost of capital.

- Year-to-year changes in non-cash WC tend to be **volatile** → better to estimate non-cash WC as a **% of revenues** (firm and industry).
- Some firms have **negative non-cash WC**: this generates positive cash flows as the firm grows; feasible for some time but **not forever** → better to **set non-cash WC to zero in perpetuity** when negative over the first years of estimates.

*(Added explanation)* Negative WC = suppliers finance the firm (pay suppliers later than customers pay you — typical of Amazon, supermarkets). Growing revenue then *releases* cash. Assuming this forever would inflate terminal value.

### Volatility of changes in WC — example

| | Amazon | Cisco | Motorola |
|---|---|---|---|
| Revenues | $1,640 | $12,154 | $30,931 |
| Non-cash WC | −$419 | −$404 | $2,547 |
| % of revenues | −25.53% | −3.32% | 8.23% |
| Change from last year | −$309 | −$700 | −$829 |
| Average: last 3 years | −15.16% | −3.16% | 8.91% |
| Average: industry | 8.71% | −2.71% | 7.04% |
| **Assumptions in valuation** | | | |
| WC as % of revenue | 3.00% (?) | −3.32% | 8.23% |
| ΔWC as % of ΔRevenue in perpetuity | 25.53% (?) | 0% | 0% |

(−419/1,640 = −25.55%; −404/12,154 = −3.32%; 2,547/30,931 = 8.23%.)

*(Added explanation)* For a firm with stable WC/revenue ratio w, ΔWC_t = w × ΔRevenue_t. Amazon's −25.5% is far from its industry (+8.7%) → the "(?)" marks show the analyst's judgment in moving it towards a positive figure rather than extrapolating an unsustainable negative WC.

---

## 1.30 Common mistakes in converting earnings to cash flows (slide)

1. Treating **EBITDA** as free cash flow.
2. Including **interest expense** in FCFO.
3. Forgetting that **increases in NWC absorb cash**.
4. Treating **all cash as excess cash**.
5. Discounting **FCFO with cost of equity** or **FCFE with WACC**.
6. Adjusting EBIT for leases or R&D but forgetting the matching **balance-sheet / CapEx adjustment**.
7. Moving from EV to equity value using **only net debt** when there are other claims.

## 1.31 Takeaways

- **Enterprise value and equity value are different valuation objects**: EV (asset value) = Equity value + Net debt.
- **FCFO values the business; FCFE values the equity.**
- **Cash flows ≠ earnings**: adjust for non-cash expenses/revenues, ΔWC, CapEx and financing changes (as in a cash-flow statement).
- Financial statements must be reorganized: **operating, financing, non-core**.
- Most common errors: mixing cash-flow definitions, discount rates, value objects.
- **Income-tax disclosures are key**:
  - average tax rate on the company's books ≠ tax rate actually paid;
  - **income tax expense ≠ income taxes paid** (the latter is used for FCF);
  - differences stem from **permanent and temporary factors**, which reverse.

*(Added explanation)* Permanent differences (e.g., non-deductible expenses, tax-exempt income) never reverse and change the effective rate forever; temporary differences (e.g., accelerated tax depreciation) create deferred taxes that reverse over time — which is why the effective rate should converge towards the marginal rate in perpetuity.

---

## Formula Summary Sheet (Ch. 1)

| Concept | Formula |
|---|---|
| EV–equity identity | EV = Equity value + Net debt |
| Net financial debt | Financial debt − Cash & equivalents |
| Pension provision (DB) | (PBO − FV plan assets) × (1 − t) |
| Other debt-like items | Debt-like provisions × (1 − t) |
| Full bridge | Equity = EV − Net debt − Pension(1−t) − Debt-like(1−t) + Non-operating assets − Minorities |
| NWC | Inventory + Receivables − Payables |
| NIC | Net fixed assets + NWC |
| Net financial position | Financial liabilities − Cash |
| Operating cash flow of current activities | EBITDA − ΔWC |
| FCFO (short) | EBIT(1 − t) + non-cash charges − CapEx − ΔNon-cash WC |
| FCFO (net CapEx form) | EBIT(1 − t) − (CapEx − D&A) − ΔWC |
| FCFE (short) | NI + non-cash charges − CapEx − ΔWC + net debt issued |
| FCFE ↔ FCFO | FCFE = FCFO − Int(1 − t) + (New debt − Repayments) |
| Tax on EBIT | t × EBIT = Tax expense + t × Interest |
| Change in excess cash | FCFE − Dividends + New equity |
| Matching | FCFO @ WACC → EV; FCFE @ k_e → Equity |
| Lease debt | Σ Commitment_t / (1 + k_d,pre-tax)^t |
| Adjusted EBIT (leases) | EBIT + Lease expense − Depreciation of leased asset |
| Approx. adjusted EBIT | EBIT + k_d,pre-tax × PV(leases) |
| Adjusted debt | Debt + PV(leases) |
| R&D asset | Σ_j R&D_{−j} × (1 − j/N) |
| R&D amortization | Σ_{j=1}^{N} R&D_{−j}/N |
| Adjusted EBIT (R&D) | EBIT + R&D_t − Amort_t |
| Corrected adj. EBIT after tax | EBIT(1 − τ) + R&D_t − Amort_t |
| Adjusted net CapEx (R&D) | Net CapEx + R&D_t − Amort_t |
| Smoothed net CapEx | (1/n)ΣCapEx_{t−i} − D&A_t |
| Net CapEx w/ acquisitions | Net CapEx + Acquisitions − D&A of acquisitions |
| Expected growth | ROIC × Reinvestment rate |
| ROIC | EBIT(1 − t) / (BV equity + BV debt) (GAP, SAP); in Chs. 4 and 8 cash is netted out: BV equity + BV debt − cash |
| WACC | k_e × E/(D+E) + k_d(1 − t) × D/(D+E) |
| CAPM | k_e = r_f + β × ERP |
| ΔWC (stable ratio) | w × ΔRevenue |

## Common Mistakes & Exam Traps (Ch. 1)

1. **EBITDA ≠ FCF** — EBITDA ignores taxes, CapEx and ΔWC.
2. **CFO ≠ FCFO** — CFO (statement) starts from net income (after interest) and excludes CapEx; FCFO is unlevered and after CapEx. (DQ: CFO 300 vs FCFO −200.)
3. **Interest never enters FCFO** — neither the interest nor its tax shield (taxes are computed on EBIT as if unlevered).
4. **Tax on EBIT ≠ income tax expense**: difference = interest tax shield (DQ: 160 vs 120).
5. **Net borrowing enters FCFE, not FCFO**. A firm can have negative FCFO and positive FCFE if it borrows.
6. **Dividends are not subtracted in FCFE** — they are a use of FCFE.
7. **Required (operating) cash ≠ excess cash**: increases in required cash reduce FCFO; only excess cash is netted against debt/added as non-operating asset.
8. **Increase in WC = cash outflow** (sign!); decrease = inflow.
9. **Matching principle**: FCFO ↔ WACC ↔ EV; FCFE ↔ k_e ↔ Equity. Distractors will mix them.
10. **EV − net debt is not always equity**: also subtract pensions, other debt-like items (after tax), minorities, and add non-operating assets (if excluded from FCFO).
11. Pension and debt-like provisions are taken **after tax** (× (1 − t)); pension adjustment only for **defined benefit** plans.
12. Book value of debt is common practice, but **market value** is conceptually correct when available.
13. Operating leases: discount commitments at the **pre-tax** cost of debt; the lease asset = lease debt; adjusted EBIT adds back the **whole** lease expense and subtracts **depreciation** (not the lease payment).
14. Effects of lease capitalization: EBIT ↑, debt ↑, WACC ↓ (GAP 7.31% → 6.25%), ROIC ↓ (12.90% → 9.30%), equity value ≈ unchanged; **no effect on net income/equity earnings**.
15. R&D capitalization: EBIT ↑ by (R&D − amortization), book equity ↑ by the research asset, net CapEx ↑ by the same amount, ROIC ↓ (29.9% → 19.4%), **FCFF unchanged** (1,283).
16. R&D amortization: the **current** year's R&D is not amortized; with a 5-year life, the year −5 layer is fully amortized this year.
17. When capitalizing R&D, don't lose the tax deduction: corrected after-tax EBIT = EBIT(1 − τ) + R&D − amortization (adjustment is pre-tax).
18. Always make **matching** adjustments: EBIT adjustment ↔ CapEx/D&A/balance-sheet adjustment.
19. Lumpy CapEx: average **CapEx only**, never D&A; prefer industry **CapEx/D&A** ratio.
20. Acquisitions are CapEx; if ignored (fair value deals), exclude acquisition-driven growth.
21. Non-cash WC excludes **excess cash** and **interest-bearing short-term debt**.
22. Negative WC forever is not credible → set WC to zero in perpetuity.
23. **Use the marginal tax rate** in projections (or converge effective → marginal); for multinationals the safest choice is the country-of-incorporation marginal rate.
24. Lower tax rate → **higher** after-tax cost of debt → **higher** WACC (smaller tax shield), but value can still rise due to higher after-tax cash flows (2018 reform: +9.7%).
25. Sum-of-parts: reconstruct each business's costs up to **EBIT**.
26. FCFE valuation requires a **target financial structure** (FCFE depends on future borrowing).
27. Under **IFRS 16** (from 1 Jan 2019) operating leases are capitalized; exemptions only for short-term and low-value leases.
