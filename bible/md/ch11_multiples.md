<!-- Markdown notes generated from the LaTeX chapter; tables and formulas kept in LaTeX syntax. The PDF is the reference version. -->
# Valuation Multiples

\emph{Based on Lecture L11 (file ``L10 -- Multiples'', 32 slides): ``Valuation Multiples'', 2--3 November 2026, and on the official solution file \texttt{Bridge\_SOL.xlsx} (Equity Value vs Enterprise Value). Workflow step: **multiples** and **value bridge**.}

## Plan for the Day
**Last time**: FCFE discount models; differences between DDM and FCFE (Chapter~\ref{ch:fcfe}).\\
**Today**: the principles of relative valuation; the basic steps for using common multiples.\\
**Agenda**: (1) use of relative valuation: overview, principles, why; (2) using multiples: metrics, steps, deal multiples; (3) common multiples: P/E, P/BV, EV/EBITDA, EV/Sales.

% =====================================================================

## Use of Relative Valuation

### Overview (Reminder)

[Figure: redrawn diagram, see PDF]

> **Added explanation (not on slides)**
The ``mix'' is exactly the DCF with a TV computed from a multiple (Chapter~\ref{ch:growth}): if the multiple comes from comparables, the TV turns the DCF into a partly relative valuation.

### Principles
In a relative valuation, the value of an asset is compared to the values the market assesses for **comparable** assets. Two basic components:

  - **Standardized prices**: prices are converted into multiples of earnings (P/E), BV (P/BV), sales (EV/Sales), etc., so that they are **independent of size**.
  - **Similar or comparable firms** (peers): **no two firms are identical**, and firms in the same business can still differ in risk, growth and cash flows.

Multiples can be sourced from two markets:

  - **Stock market (market or trading multiples)**: stand-alone values (no acquisition premiums or minority discounts embedded);
  - **M\&A market (deal or transaction multiples)**: prices paid in M\&A deals (acquisition premiums or minority discounts embedded).

> **Key point**
Ignoring speculative phenomena (bubbles, \dots), the difference between market and deal multiples is explained by **acquisition premiums** or **minority discounts**.

\subsubsection*{Numerator and denominator}

[Figure: redrawn diagram, see PDF]

> **Consistency rule** *(added, not on slides)*
Numerator and denominator must refer to the **same claimholders**: equity value with equity measures (net income, EPS, BV of equity, FCFE); EV with firm measures (revenues, EBITDA, EBIT, FCFF, invested capital). Mixing them (e.g., P/Sales or EV/Net income) is inconsistent, and the slide on revenue multiples calls P/S ``inconsistent'' for this reason.

\subsubsection*{From EV to equity value: the bridge-to-equity}

[Figure: redrawn diagram, see PDF]

\medskip
[Figure: redrawn diagram, see PDF]

\[
\text{EqV}=\text{EV}-\text{Net debt}+\text{Associates}-\text{Pension deficit}-\text{NCI}-\text{Preferred shares}\pm\text{Surplus items}
\]

> **Added explanation (not on slides)**
This is the same bridge as Chapter~\ref{ch:fcf} (there with the tax adjustment on pension and debt-like provisions). EV refers to the operating business only, so all non-operating assets are added and all non-common-equity claims are subtracted.

### Official Exercise: Equity Value vs Enterprise Value (Bridge\_SOL Excel)

> **Firm A: from equity value to EV (\euro m, except per share)**
Share price \euro18.76; basic shares 1,342.7m; diluted shares 1,351.6m. LTM revenue 11,858; LTM EBITDA 2,099; LTM net income 755.

\small
\begin{tabular}{@{}lr@{}}
\toprule
Diluted equity value ($1{,}351.6\times18.76$) & 25,356.0\\
$-$ Cash \& cash equivalents & (868)\\
$-$ Equity investments & (290)\\
$-$ Other non-core assets, net & (17,983)\\
$+$ Total debt & 12,243\\
$+$ Preferred stock & 0\\
$+$ Noncontrolling interests & 1,659\\
$+$ Unfunded pension obligations & 674\\
$+$ Restructuring \& legal liabilities & 2,849\\
\midrule
**Enterprise value** & **23,640.0**\\
\bottomrule
\end{tabular}

LTM EV/Revenue $=23{,}640/11{,}858=\mathbf{1.99\times}$; LTM EV/EBITDA $=23{,}640/2{,}099=\mathbf{11.26\times}$; LTM P/E $=25{,}356/755=\mathbf{33.58\times}$.

> **What happens to EqV, EV and the multiples after each transaction of \euro1,000? (official Excel)**
\small
\begin{tabular}{@{}lrrrrrrr@{}}
\toprule
Transaction & $\Delta$Cash & $\Delta$Debt & $\Delta$Equity & $\Delta$Pref. & **EqV** & **EV** & **P/E**\\
\midrule
Base case & -- & -- & -- & -- & 25,356 & 23,640 & 33.58$\times$\\
Issue \euro1,000 of shares & $+1{,}000$ & 0 & $+1{,}000$ & 0 & 26,356 & 23,640 & 34.91$\times$\\
Raise \euro1,000 of debt & $+1{,}000$ & $+1{,}000$ & 0 & 0 & 25,356 & 23,640 & 33.58$\times$\\
Repurchase \euro1,000 of shares & $-1{,}000$ & 0 & $-1{,}000$ & 0 & 24,356 & 23,640 & 32.26$\times$\\
Repay \euro1,000 of debt & $-1{,}000$ & $-1{,}000$ & 0 & 0 & 25,356 & 23,640 & 33.58$\times$\\
Pay \euro1,000 of dividends & $-1{,}000$ & 0 & $-1{,}000$ & 0 & 24,356 & 23,640 & 32.26$\times$\\
Issue \euro1,000 of preferred & $+1{,}000$ & 0 & 0 & $+1{,}000$ & 25,356 & 23,640 & 33.58$\times$\\
\bottomrule
\end{tabular}

\medskip
EV/Revenue (1.99$\times$) and EV/EBITDA (11.26$\times$) are **unchanged in every case**. Example (issue shares): EqV $25{,}356+1{,}000=26{,}356$; cash $-868-1{,}000=-1{,}868$; EV $=26{,}356-1{,}868-290-17{,}983+12{,}243+1{,}659+674+2{,}849=23{,}640$.

> **Key point of the exercise (official Excel)**
No matter how a company is financed, its **enterprise value stays the same**. Equity value may change depending on the mix of equity, debt, cash and preferred stock. As a result, **EV-based multiples do not change** when financing changes (at least immediately after the change). In real life EV *is* affected by capital structure, because WACC changes with financing (Chapter~\ref{ch:capstr}), but EV still changes by **far less** than equity value.

> **Reading the table** *(added, not on slides)*
Equity value changes only when cash flows between the firm and its *shareholders* (share issue, buyback, dividend). Debt and preferred transactions swap cash for a claim of equal amount, so EqV is unchanged; EV never moves because cash and the claim offset in the bridge. P/E therefore moves with buybacks and dividends, but EV/EBITDA does not. In the Excel, pension and restructuring liabilities are added without the $(1-t)$ adjustment of Chapter~\ref{ch:fcf}: in an exam, follow the data given.

### Why Relative Valuation?
Reasons why relative valuations are widely used:

  - **Few explicit assumptions**: far fewer explicit assumptions and far quicker than DCF valuations.
  - **Market-oriented**: more likely to reflect the current **market mood**, since they measure relative (not intrinsic) value.
  - **Simplicity**: simpler to understand and easier to present (easier to frame an asset as cheap or expensive).

Most valuations on Wall Street are relative: almost all equity reports and almost all acquisition valuations are based on multiples and comparables; rules of thumb based on multiples are common and often the basis for final judgments.

**The strengths are also the major weaknesses**:

  - **Few explicit assumptions**: the ease of relative valuation can produce **inconsistent estimates** where key variables (risk, growth, cash flows) are ignored.
  - **Market oriented**: values are too high/low when the market is **over/undervaluing comparables**.
  - **Simplicity (bias)**: the **lack of transparency** on underlying assumptions makes multiples vulnerable to manipulation.

% =====================================================================

## Using Multiples

### Metrics: Time Frame
Suppose it is 30/9/2026. The denominator can be:

  - **Actual**: last fiscal year (LFY, 31/12/2025);
  - **Forward**: next FY (2026) or following years (2027, \dots);
  - **Trailing**: last four quarters (LTM): Q4 2025 $+$ Q1/Q2/Q3 2026 (the slide writes ``Q4 2015'', a typo).

Choice: **LFY/LTM** if no estimates exist (for comparables or target); **F+1, F+2, \dots** if LFY/LTM figures are negative and/or for growing or innovative businesses. Business plans usually forecast growth: EBITDA 27E $>$ EBITDA 26A $\Rightarrow$ **forward multiple $<$ actual multiple**.

> **Key point**
**The numerator never changes!** Future EV and EqV do not exist: the numerator is always today's market value.

> **Slide question: forward (T+1) EBITDA multiple -- target's EqV at end-2025**

\small
\begin{tabular}{@{}lrrr@{}}
\toprule
& 2025 & 2026 & 2027\\
\midrule
\multicolumn{4}{@{}l}{*Peer company*}\\
Market cap & 1,000 & & \\
EBITDA & 100 & 120 & 150\\
Net debt & 200 & 205 & 215\\
\multicolumn{4}{@{}l}{*Target company*}\\
Equity value & ? & & \\
EBITDA & 20 & 25 & 30\\
Net debt & 10 & 15 & 20\\
\bottomrule
\end{tabular}

Options on the slide: 241; 235; 240; 236. *Solution (ours)*:
\begin{align*}
\text{Peer EV (today)}&=1{,}000+200=1{,}200\qquad\text{EV/EBITDA}_{26}=1{,}200/120=10.0\times\\
\text{Target EV}&=10.0\times25=250\qquad\text{Target EqV}=250-10\ (\text{today's net debt})=\mathbf{240}
\end{align*}
The wrong options come from using a future net debt: peer net debt 205 gives $1{,}205/120\times25-10=\mathbf{241}$ or $-15=\mathbf{236}$; target net debt 15 gives $250-15=\mathbf{235}$. Only the denominator moves forward; EV and net debt are today's.

> **Consistency between peers and target (slide)**

\small
\begin{tabular}{@{}lrrrrr@{}}
\toprule
& Mkt cap & NI 25A & NI 26E & P/E actual & P/E FWD\\
\midrule
Peers & 10,000 & 550 & 605 & $10{,}000/550=18.2\times$ & $10{,}000/605=16.5\times$\\
Target & & 190 & 240 & & \\
\bottomrule
\end{tabular}

Equity value as of end-2025:

  - with P/E actual: $190\times18.2=\mathbf{3{,}455}$ \checkmark
  - with P/E FWD: $240\times16.5=\mathbf{3{,}967}$ \checkmark
  - \textcolor{keyred}{incorrect}: $190\times16.5=3{,}140$ (actual earnings $\times$ forward multiple)
  - \textcolor{keyred}{incorrect}: $240\times18.2=4{,}364$ (forward earnings $\times$ actual multiple)

### Metrics: Calendarization
Assume the target's FY ends on 31/12 and the peers' FY ends on 31/3: the peers' figures must be **calendarized** as of 31/12.

[Figure: redrawn diagram, see PDF]

> **Key point**
Calendarized EBITDA for peers $=$ Q4 (of FY25, i.e., Jan--Mar 2026) $+$ Q1--Q2--Q3 (of FY26, i.e., Apr--Dec 2026).

> **Equivalent formula** *(added, not on slides)*
Calendar-year figure $=\frac{3}{12}\times\text{FY}_C+\frac{9}{12}\times\text{FY}_D$ (if quarterly data are not available). Example: FY C EBITDA 400, FY D 480 $\Rightarrow$ $0.25\times400+0.75\times480=460$.

### Steps

[Figure: redrawn diagram, see PDF]

**1. Identify peer companies -- comparability criteria**

\small
\begin{tabular}{@{}>{\bfseries}l p{11cm}@{}}
Business model & Activities, products, customers, \dots; operating risk: capital intensity (manufacturing vs outsourcing); growth prospects and stage in the business life cycle\\
Size & Absolute values of sales, EBITDA, market share, \dots\\
Margins & Similar EBITDA \% and NI \%\\
Debt & Similar financial risk and leverage (ND/EBITDA, ND/E, \dots)\\
Country & Developed vs emerging markets\\
\end{tabular}

**2. Compute multiples for peers**

  - **Numerator**: market cap: spot price vs 6/12/\dots-month average; **fully diluted EqV** $=$ market cap (price $\times$ shares outstanding) $+$ value of in-the-money options, convertible securities, \dots\ (if stock price $>$ strike price). Alternatively estimate the fully diluted number of shares with the **treasury stock method** and ignore treasury shares.
  - **Denominator**: exclude one-off or non-recurring items; apply the same accounting rules to every company.

> **Illustration (not on slides): treasury stock method**
Share price 20; basic shares 100m; 10m options with strike 15. Exercise proceeds $=10\times15=150$ buy back $150/20=7.5$m shares $\Rightarrow$ net new shares $=10-7.5=2.5$m; fully diluted shares $=102.5$m; diluted EqV $=102.5\times20=2{,}050$.

**3. Compute average multiples**

  - Exclude **negative multiples and outliers**.
  - Possible measures: mean, **median**, min, max, **trimmed mean** (without min and max).
  - **Value maps**: regress peer multiples on a reference variable (e.g., P/BV on ROE, EV/EBITDA on growth); estimate the target's multiple from the regression.
  - **Size discount**: if peers are much larger than the target, a size discount may apply.

> **Illustration (not on slides): mean, median, trimmed mean**
Peer EV/EBITDA: 6$\times$, 7$\times$, 8$\times$, 9$\times$, 25$\times$ (outlier). Mean $=55/5=11.0\times$; median $=8.0\times$; trimmed mean (without 6 and 25) $=(7+8+9)/3=8.0\times$. The outlier inflates the mean by 3 turns: use the median or trimmed mean.

**4. Apply the multiple to the target**

  - Apply to the target the **same adjustments** applied to peers.
  - Use a **consistent time horizon**: e.g., an F+2 multiple on the target's F+2 EBITDA.
  - Without a business plan for the target, forward multiples cannot be applied.
  - For unlisted targets, LTM figures are unavailable if they do not publish quarterly results.

**5. Compute the target's EV and EqV** with the bridge-to-equity.

### Deal Multiples

  - Retrieved from prices paid in M\&A deals; deals of the **last 3--5 years** are usually considered; typically based on actual or LTM data.
  - The challenge is obtaining reliable data about **private** companies involved in M\&A deals.
  - Prices for majority/controlling stakes include a **control premium** (vice versa for minority stakes); prices may also include the value of **synergies** paid to the seller.
  - To derive equity values, prices must be **divided by the stakes acquired**.
  - Prices may be paid in cash and/or shares: **both** must be included.

> **Illustration (not on slides): deal multiple from a partial stake**
A buyer pays 300 in cash $+$ 60 in its own shares for 60\% of a target with net debt 150 and EBITDA 70. Implied 100\% EqV $=360/0.60=600$; EV $=600+150=750$; deal EV/EBITDA $=750/70=10.7\times$ (includes a control premium).

% =====================================================================

## Common Multiples

### P/E: Definition

> **Key point**
\[
\frac{P}{E}=\frac{\text{Price}}{\text{EPS}}=\frac{\text{Market cap}}{\text{Net income}}
\]

Variants: (1) **price**: spot (current) vs average (to smooth volatility and one-off events); (2) **EPS**: *time* (LFY current, last four quarters trailing, next FY forward, or some future year); *shares* (primary vs fully or partially diluted EPS; subtract treasury shares and use the fully diluted count); *composition* (before or after extraordinary items).

Why EPS are hard to compare uniformly:

  - **Acquisitions**: firms account for acquisitions differently; all use purchase accounting and record goodwill, but discretion in asset recognition and impairment can materially change EPS.
  - **Management options**: diluted EPS may bring option shares into the multiple (beware deep or only slightly in-the-money options).
  - **Accounting choices**: discretion to expense or capitalize items; expensing CapEx shifts EPS across periods and **penalizes firms that reinvest more**.

### P/E: Determinants
From a stable-growth DDM, with DPS $=$ EPS $\times$ Payout:

> **P/E from fundamentals**
\[
P_0=\frac{\text{DPS}_1}{K_e-g_n}\ \Rightarrow\ \frac{P_0}{\text{EPS}_1}=\frac{\text{Payout}}{K_e-g_n}\quad\text{(forward)}\qquad\frac{P_0}{\text{EPS}_0}=\frac{\text{Payout}\,(1+g_n)}{K_e-g_n}\quad\text{(current)}
\]
With $\text{Payout}=1-g_n/\text{ROE}_n$:
\[
\frac{P_0}{\text{EPS}_1}=\frac{1-g_n/\text{ROE}_n}{k_e-g_n}
\]

\textcolor{keyred}{**Slide note**}: the slide writes the current P/E as Payout$/(K_e-g_n)$, using DPS $=$ EPS$_0\times$Payout in the numerator of $P_0$. Since $P_0$ needs next year's dividend, the current P/E carries the extra $(1+g_n)$ (as in Chapter~\ref{ch:ddm}); the forward version is exact.

\begin{tabular}{@{}ll@{}}
\toprule
**Factor** & **Relationship to P/E**\\
\midrule
Operating risk & Inverse\\
Leverage ratio & Inverse\\
Payout (growth rate being equal) & Direct\\
ROE (growth rate being equal) & Direct\\
Growth rate (payout being equal) & Direct\\
Growth duration & Direct\\
\bottomrule
\end{tabular}

> **Illustration (not on slides)**
$K_e=10\%$, $g=4\%$, ROE $=15\%$: payout $=1-4/15=73.3\%$; forward P/E $=0.733/0.06=\mathbf{12.2\times}$; current P/E $=12.2\times1.04=\mathbf{12.7\times}$. If ROE $=K_e=10\%$: payout $=60\%$, forward P/E $=0.6/0.06=10\times=1/K_e$: growth adds nothing (Chapter~\ref{ch:fcfe}).

### PEG

> **Key point**
\[
\text{PEG}=\frac{\text{P/E}}{\text{Expected }g\ \text{in EPS}}
\]

Be consistent: (1) $g$ must be the growth in **EPS**, not EBIT or other metrics; (2) P/E must be the **current** one (not forward), otherwise growth is counted twice (numerator and denominator); (3) use the **same $g$ estimates** for all firms. PEG can be computed only for firms with an expected EPS growth rate, usually from analysts: firms not tracked by analysts have no PEG, and since smaller, younger firms tend not to be followed, this creates **selection bias**.

> **Illustration (not on slides)**
Firm A: P/E 20$\times$, $g=10\%$ $\Rightarrow$ PEG $=20/10=2.0$. Firm B: P/E 15$\times$, $g=5\%$ $\Rightarrow$ PEG $=3.0$. A looks cheaper relative to its growth despite the higher P/E ($g$ is expressed in percentage points).

### P/BV: Definition

> **Key point**
\[
\frac{P}{BV}=\frac{\text{Price}}{\text{BV of equity}}
\]

Potential inconsistencies: **share classes** (different prices per class; unclear how to apportion BV); **preferred stock** (do **not** include the preferred portion in BV of equity: market value refers only to **common** equity); **BV of equity** is updated infrequently (use the same measure for all firms); **options outstanding** (add the estimated market value of management and conversion options to the market value of equity before computing P/BV).

### P/BV: Determinants
From the stable DDM, with DPS $=$ EPS $\times$ Payout and ROE $=$ EPS/BV$_0$:

> **P/BV from fundamentals**
\[
P=\frac{\text{BV}\cdot\text{ROE}\cdot\text{Payout}}{K_e-g_n}\ \Rightarrow\ \frac{P}{BV}=\frac{\text{ROE}\cdot\text{Payout}}{K_e-g_n}\ \overset{g=(1-\text{Payout})\text{ROE}}{=}\ \frac{\text{ROE}-g_n}{K_e-g_n}
\]
**P/BV of a stable firm is determined by the differential between ROE and $K_e$**: \ ROE $>k_e\Rightarrow$ price $>$ BV equity; \ ROE $<k_e\Rightarrow$ price $<$ BV equity.

> **Illustration (not on slides)**
ROE $=15\%$, $K_e=10\%$, $g=4\%$: P/BV $=(0.15-0.04)/(0.10-0.04)=\mathbf{1.83\times}$. With ROE $=8\%$: P/BV $=0.04/0.06=0.67\times$ (a bank earning below its cost of equity trades below book). Here ROE $=$ EPS$_1$/BV$_0$ (next year's earnings on current book).

### EV/EBITDA: Definition

> **Key point**
\[
\frac{\text{EV}}{\text{EBITDA}}=\frac{\text{Market cap}+\text{Market value of debt}-\text{Cash}}{\text{EBITDA}}
\]

  - Since interest income is not counted in EBITDA, **not netting out cash overstates** the multiple.
  - Useful for sectors with large CapEx and long gestation periods (telco, construction).
  - Widely used because of: **negative values** (fewer firms with negative EBITDA than negative EPS, so fewer firms are lost); **accounting choices** (D\&A differences affect operating and net income, not EBITDA); **leverage** (easier to compare across different leverage: the numerator is firm value, the denominator pre-debt).

### EV/EBITDA: Determinants
From the FCFO model $\text{EV}=\text{FCFO}/(\text{WACC}-g)$:
\begin{align*}
\text{FCFO}&=\text{EBIT}(1-t)-(\text{CapEx}-\text{D\&A}+\Delta\text{WC})\\
&=(\text{EBITDA}-\text{D\&A})(1-t)-(\text{CapEx}-\text{D\&A}+\Delta\text{WC})\\&=\text{EBITDA}(1-t)-\text{D\&A}(1-t)-\text{Reinvestment}
\end{align*}

> **EV/EBITDA from fundamentals**
\[
\frac{\text{EV}}{\text{EBITDA}}=\frac{(1-t)-\frac{\text{D\&A}}{\text{EBITDA}}(1-t)-\frac{\text{Reinvestment}}{\text{EBITDA}}}{\text{WACC}-g}
\]

(On the slide ``RR'' in this formula denotes the reinvestment *amount*, not the rate.) Five determinants (ceteris paribus):

  - **Tax rate**: lower tax rate $\Rightarrow$ higher EV/EBITDA.
  - **D\&A**: a greater portion of EBITDA from D\&A $\Rightarrow$ lower EV/EBITDA.
  - **Reinvestment**: the greater the portion of EBITDA reinvested to generate growth $\Rightarrow$ lower EV/EBITDA.
  - **Cost of capital**: lower WACC $\Rightarrow$ much higher EV/EBITDA.
  - **Expected growth**: higher growth $\Rightarrow$ much higher EV/EBITDA.

> **Illustration (not on slides)**
$t=25\%$, D\&A/EBITDA $=20\%$, reinvestment/EBITDA $=15\%$, WACC $=9\%$, $g=3\%$: EV/EBITDA $=(0.75-0.20\times0.75-0.15)/0.06=0.45/0.06=\mathbf{7.5\times}$.

### EV/Sales: Definition
Two revenue multiples:
\[
\frac{P}{S}=\frac{\text{Market cap}}{\text{Revenues}}\ \ \textcolor{keyred}{(\text{inconsistent!})}\qquad\qquad \frac{\text{EV}}{S}=\frac{\text{Market cap}+\text{MV debt}-\text{Cash}}{\text{Revenues}}\ \ (\text{consistent})
\]
EV/Sales is more robust: it divides the total value of operating assets by the revenues those assets generate, whereas P/S divides an *equity* value by revenues generated for the *firm*; consequently **P/S yields lower values for more highly levered firms**.

### EV/Sales: Determinants

> **EV/Sales from fundamentals**
\begin{gather*}
\text{EV}=\frac{\text{EBIT}(1-t)(1-\text{RR})}{\text{WACC}-g}\ \Rightarrow\ \frac{\text{EV}}{\text{Sales}}=\frac{\text{EBIT}(1-t)/\text{Sales}\times(1-\text{RR})}{\text{WACC}-g}\\
\frac{\text{EV}}{\text{Sales}}=\frac{\text{NOPAT margin}\times(1-\text{RR})}{\text{WACC}-g}
\end{gather*}
EV/S is determined by the **NOPAT margin**, **reinvestment** and **WACC**: firms with higher operating margins, lower reinvestment rates and lower costs of capital trade at higher EV/S.

> **Illustration (not on slides)**
NOPAT margin 12\%, RR $=30\%$, WACC $=9\%$, $g=3\%$: EV/Sales $=0.12\times0.70/0.06=\mathbf{1.4\times}$.

% =====================================================================

## Formula Summary Sheet

\small
\renewcommand{\arraystretch}{1.5}
\begin{longtable}{@{}p{4.6cm}p{10.4cm}@{}}
\toprule
**Concept** & **Formula**\\
\midrule
\endhead
Bridge-to-equity & EqV $=$ EV $-$ Net debt $+$ Assoc.\ $-$ Pension deficit $-$ NCI $-$ Preferred $\pm$ Surplus items\\
EV from equity & EqV $-$ cash $-$ non-core assets $+$ debt $+$ preferred $+$ NCI $+$ pension $+$ other debt-like\\
Forward multiple & Today's EV (or EqV) / next year's metric\\
Calendarization & Peer CY $=$ Q4 of FY$_C$ $+$ Q1--Q3 of FY$_D$ $\approx\frac{3}{12}$FY$_C+\frac{9}{12}$FY$_D$\\
Treasury stock method & New shares $=N_{opt}-N_{opt}K/P$ (in-the-money options)\\
Deal multiple & (Price paid / stake acquired) $+$ net debt, over the target's metric\\
P/E & Price/EPS $=$ Market cap/NI\\
Forward P/E & $\text{Payout}/(K_e-g)=(1-g/\text{ROE})/(K_e-g)$\\
Current P/E & $\text{Payout}(1+g)/(K_e-g)$\\
PEG & (current) P/E / expected EPS growth\\
P/BV & $\frac{\text{ROE}\cdot\text{Payout}}{K_e-g}=\frac{\text{ROE}-g}{K_e-g}$\\
EV/EBITDA & $\frac{(1-t)-\frac{\text{D\&A}}{\text{EBITDA}}(1-t)-\frac{\text{Reinv.}}{\text{EBITDA}}}{\text{WACC}-g}$\\
EV/Sales & $\frac{\text{NOPAT margin}\,(1-\text{RR})}{\text{WACC}-g}$\\
\bottomrule
\end{longtable}

## Common Mistakes and Exam Traps

> **Exam traps -- Chapter 11**

  - Relative valuation $=$ standardized prices $+$ comparable firms; no two firms are identical.
  - Trading multiples: stand-alone (no premium); deal multiples: include control premiums/minority discounts (and possibly synergies). The difference between the two $=$ premium/discount.
  - Match numerator and denominator: EqV with equity measures, EV with firm measures. P/S is inconsistent; EV/S is consistent.
  - **The numerator never changes**: use today's EV/EqV and today's net debt with forward denominators (slide question: 240, not 241/235/236).
  - Apply actual multiples to actual earnings and forward multiples to forward earnings (3,455 or 3,967; never 3,140 or 4,364).
  - Forward multiples are lower than actual ones when earnings grow.
  - Calendarize peers with different fiscal years (Q4 of C $+$ Q1--Q3 of D).
  - Fully diluted equity value (ITM options, convertibles; treasury stock method); exclude one-offs; same accounting for all firms.
  - Exclude negative multiples and outliers; prefer median or trimmed mean; consider value maps and size discounts.
  - Deal multiples: last 3--5 years; divide price by the stake; include cash *and* share consideration.
  - P/E rises with payout, ROE, growth and growth duration; falls with operating risk and leverage.
  - PEG: use current P/E and EPS growth; same $g$ source for all firms; selection bias toward covered firms.
  - P/BV $=(\text{ROE}-g)/(K_e-g)$: P/BV $>1$ iff ROE $>K_e$. Exclude preferred equity from BV; add option values to market equity.
  - EV/EBITDA: subtract cash (otherwise the multiple is overstated); higher with lower taxes, lower D\&A share, lower reinvestment, lower WACC, higher growth.
  - EV/Sales is driven by NOPAT margin, reinvestment and WACC.
  - **Financing transactions do not change EV** (Bridge\_SOL): EV/EBITDA and EV/Sales stay constant; P/E changes when equity changes (share issue $+$, buyback/dividend $-$); debt and preferred transactions leave EqV unchanged.

## Official exercises and solutions (Multiples_SOL.xlsx; Multiple_Exercises.pdf + Multiples_Exercises_Solved.xls)
- **Ex_1 (a)** slide question: EV peer 1,200; EV/EBITDA26 10×; EV target 250; **EqV 240** (official, confirms our earlier answer).
- **Ex_1 (b)**: EV = 25,000 + 3,200 + 4,000 − 2,200 = **30,000** (payables 7,600 are NOT debt); EV/EBITDA = **6.67×**.
- **Ex_2 treasury stock method**: price 10; 1,000 shares outstanding (+200 treasury, ignored); ITM tranches A (100 @6) and B (50 @4): new 150, cash 800, buyback 80, net **+70** → **1,070** shares, market cap **10,700** (= 10,000 + option intrinsic value 700).
- **Foglio1**: g 5%, ROE 14%, Ke 10% → payout 64.29%, P/E **12.86×**.
- **Trading/Deal/Valuation**: 8 lighting peers, averages EV/Sales 1.64×/1.53× (A/F+1), EV/EBITDA 11.82×/10.48×, P/E 24.66×/20.65×; 10 deals, averages EV/Sales 2.12×, EV/EBITDA 13.30×, P/E 27.96×; target EqV from ≈60,315 (EV/Sales 16F) to ≈153,852 (deal EV/EBITDA); bridge −736.2 (net cash +681.0, pensions −603.0, provisions −352.8, minorities −461.4).
- **Ex (convertibles)**: diluted mkt cap 240; bonds at MV 106.80; net debt 256.80; minorities at MV 150; pensions 50; associates −200; **EV 496.80**; NI adj **10.4**; EBITDA adj **33**; **EV/EBITDA 15.05×, P/E 23.08×**.
- **Problem 1 Zorzi**: peers EV/EBITDA 7.18/7.67/7.22 → avg **7.36** → EV **1,840**, equity **1,640**; current P/E 19.00/15.75/17.25 → avg **17.33** → equity **1,733** (EV 1,933); SOP (42×22 + 36×19 + 26×18)×0.75 = **1,557** (EV 1,757).
- **Problem 2 Rolling Mud**: EV/EBIT A 14.08, B 7.21 (**minority stake → excluded**), C 14.78 → avg **14.43**; Free SPA EV 57.71, equity 48.71, **offer for 80% $38.97m**.
- **Problem 3 Blizzard**: P/E F+1 avg **17.85** → equity **586.2**, EV 883.0; EV/Sales F+1 avg **0.995** → EV **1,056.8**, equity 760.0 (bridge +296.8); PEG (current P/E / g; g = 3.5%, 2%, 4.4%, Blizzard 3% — only in the Excel) avg 629.2 → equity **601.7**.
- **Regression value map**: EV/Sales = 0.2948 + 5.2497 × EBITDA%, R² 0.785; target 14.1% → 1.035× → EV **103.5** (vs 94.9 with the plain average 0.949×).
- **Trading Multiple (variant)**: EV **720**; NI adj **30.84**; EBITDA adj **88**; EV/EBITDA **8.18×**; P/E **23.35×**.
