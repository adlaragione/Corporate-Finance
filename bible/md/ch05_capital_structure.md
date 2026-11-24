<!-- Markdown notes generated from the LaTeX chapter; tables and formulas kept in LaTeX syntax. The PDF is the reference version. -->
# Leverage, Value, and Optimal Capital Structure

*Based on Lecture 05 (file L05, 28 slides): ``Leverage, Value, and Optimal Capital Structure''. Part One (workflow step: discount rate $\to$ capital structure recommendation).*

## Where We Are in the Valuation Workflow

Equity story $\to$ Financial statements $\to$ Forecasts $\to$ Cash flows $\to$ **Discount rate** $\to$ Terminal value $\to$ Multiples $\to$ Value bridge $\to$ Recommendation.

> **Today**
**Financing policy $\longrightarrow$ WACC/APV $\longrightarrow$ Enterprise Value $\longrightarrow$ Capital Structure Recommendation**

**Today's professional task.** You advise a firm considering whether to change its leverage. Your job is to estimate **whether the recapitalization creates value**:

  - estimate how leverage changes the cost of equity and the cost of debt;
  - estimate how leverage changes WACC;
  - estimate how leverage changes tax benefits and expected bankruptcy costs;
  - identify the debt ratio that maximizes firm value;
  - quantify the value consequence of moving to the optimal debt ratio.

**Plan for today.**

\small
\begin{tabularx}{\textwidth}{@{}lXX@{}}
\toprule
**Layer** & **What we learn** & **Why it matters**\\
\midrule
CORE & How leverage affects value & Capital structure intuition\\
CORE & WACC approach & Standard corporate finance tool\\
PRO & Choosing WACC vs APV & Practical valuation/interviews\\
TECH & Ratings, default spreads, cost of debt & Avoid mechanical WACC analysis\\
PRO & APV optimization & Leveraged transactions and known debt paths\\
PRACTICE & Discussion Questions & Turn leverage theory into value impact\\
\bottomrule
\end{tabularx}

% =====================================================================

## From Valuation Method to Financing Decision

The first three slides repeat Chapter~\ref{ch:wacc}. Summary:

> **CoC and APV (reminder)**
**Cost of capital**: firm value $=$ FCFO discounted at WACC. Embedded: (i) tax benefits of debt (after-tax $k_d$); (ii) the extra risk of debt (higher $k_e$ and $k_d$ at higher $D/E$).
\[
\text{Firm Value}_0=\frac{\text{FCFO}_1}{\text{WACC}-g_n},\qquad g_n=\text{Reinvestment rate}\times\text{Return on capital}
\]
**APV**: $V_l=V_u+TB-BC$, with $V_u=\mathbb{E}[\text{FCFO}_1]/(\rho_u-g_n)$; $TB=\tau_C D$ (low, fixed debt) or $\sum\frac{\tau_C k_d D_t}{(1+\rho_u)^t}+\frac{\tau_C k_d D}{(\rho_u-g_n)(1+\rho_u)^n}$ (high or predetermined debt); $BC=\pi_d\times\text{LGD}$.

Limitations of the stable-growth model (as in Chapter~\ref{ch:wacc}): sensitive to $g_n$, more so with WACC (lower than $k_e$); sensitive to CapEx relative to depreciation; the cost of capital must reflect a stable-growth firm ($\beta$, $D/E$). Depending on assumptions about future growth, both approaches have 2-stage and 3-stage versions.

% =====================================================================

## How Leverage Changes Firm Value

### Effect of Leverage on Firm Value: Introduction I

  - Because both the cost of capital and the APV approach make firm value a function of leverage, there is likely **some mix of debt and equity at which firm value is maximized**.
  - With the cost of capital approach, firm value is the PV of expected FCFO at the cost of capital:
  \[
  \text{Firm Value}_0=\sum_{t=1}^{\infty}\frac{\mathbb{E}[\text{FCFO}_t]}{(1+\text{WACC})^t}
  \]
  
    - If FCFO are **unaffected** by the financing mix and the cost of capital falls as debt increases, firm value increases.
    - If the objective is to maximize firm value, it can be achieved by **minimizing the cost of capital**.
    - In the more general case where cash flows depend on the debt-equity mix, **the optimal mix is the one that maximizes firm value**.
  

### Introduction II: The Trade-Off Theory of Firm Value

[Figure: redrawn diagram, see PDF]

> **Reading the trade-off graph** *(added, not on slides)*

  - Without frictions other than taxes, every \$1 of permanent debt adds $T_C\times\$1$ of value (the PV of the tax shield): $V_L=V_U+T_C D$, a straight line.
  - As debt grows, the probability of distress rises and **expected financial distress costs** grow faster and faster.
  - Actual value $=V_U+T_CD-\text{PV(distress costs)}$. It rises while the marginal tax benefit exceeds the marginal distress cost, peaks at $D^*$ (where they are equal) and then falls.

### Introduction III: Leverage and the Cost of Capital

[Figure: redrawn diagram, see PDF]

> **Added explanation (not on slides)**
As $D/E$ rises, the cost of equity $R_E$ rises (more financial risk for shareholders) and the after-tax cost of debt $R_D(1-T_C)$ is lower but eventually rises too (default risk). WACC first falls, because more weight goes to cheaper, tax-advantaged debt, then rises as $R_E$ and $R_D$ climb. The minimum WACC at $D^*/E^*$ corresponds to the maximum value in the previous graph, **if FCFO do not depend on leverage**.

% =====================================================================

## Finding the Debt Ratio That Maximizes Value

### Cost of Capital Approach I--II: Inputs and Cost of Equity

Three basic inputs to compute the cost of capital: (1) **cost of equity**; (2) **(after-tax) cost of debt**; (3) **weights on debt and equity**.

**1. Cost of equity.** The equity $\beta$ is a function of (i) the market debt-to-equity ratio and (ii) the unlevered $\beta$:

> **Key point**
\[
\beta_{\text{levered}}=\beta_{\text{unlevered}}\times\left[1+\frac{D}{E}\right]\qquad\qquad k_e=\text{Risk-free rate}+\beta_{\text{levered}}\times\text{ERP}
\]
If we can estimate the unlevered $\beta$, we can estimate the levered $\beta$, and hence $k_e$, at every debt ratio.

> **Added explanation (not on slides)**
In terms of the debt ratio $d=D/(D+E)$: $D/E=d/(1-d)$, so $\beta_l=\beta_u/(1-d)$. Example: $\beta_u=0.7333$, $d=40\%$ $\Rightarrow$ $\beta_l=0.7333/0.6=1.2222$.

### Cost of Capital Approach III: Cost of Debt

**2. (After-tax) cost of debt.** $k_d$ is a function of the firm's **default risk**; as firms borrow more, default risk increases and so does $k_d$. Using bond ratings to measure default risk, estimate $k_d$ in four steps:

  - estimate (i) the firm's dollar debt and (ii) interest expenses at each debt ratio (as firms borrow more, both rise);
  - at each debt level, (i) compute the financial ratio(s) measuring default risk and (ii) use them to estimate a rating (as firms borrow more, ratings decline);
  - add a **default spread** based on the estimated rating to the risk-free rate to get the **pre-tax** $k_d$;
  - apply the **marginal tax rate** to get the after-tax $k_d$.

### Cost of Capital Approach IV: Coverage, Ratings and Spreads

\small
\begin{tabular}{@{}cccr@{}}
\toprule
\multicolumn{2}{c}{**Interest coverage ratio**} & & \\
\multicolumn{2}{c}{**(non-financial firms)**} & & \\
**Large cap** & **Small cap** & **Estimated bond rating** & **Default spread (2026)**\\
\midrule
$>8.50$ & $>12.50$ & Aaa/AAA & 0.69\%\\
$[6.50,\,8.49]$ & $[9.50,\,12.49]$ & Aa2/AA & 0.85\%\\
$[5.50,\,6.49]$ & $[7.50,\,9.49]$ & A1/A+ & 1.07\%\\
$[4.25,\,5.49]$ & $[6.00,\,7.49]$ & A2/A & 1.18\%\\
$[3.00,\,4.24]$ & $[4.50,\,5.99]$ & A3/A$-$ & 1.33\%\\
$[2.50,\,2.99]$ & $[4.00,\,4.49]$ & Baa2/BBB & 1.71\%\\
$[2.25,\,2.49]$ & $[3.50,\,3.99]$ & Ba1/BB+ & 2.31\%\\
$[2.00,\,2.24]$ & $[3.00,\,3.49]$ & Ba2/BB & 2.77\%\\
$[1.75,\,1.99]$ & $[2.50,\,2.99]$ & B1/B+ & 4.05\%\\
$[1.50,\,1.74]$ & $[2.00,\,2.49]$ & B2/B & 4.86\%\\
$[1.25,\,1.49]$ & $[1.50,\,1.99]$ & B3/B$-$ & 5.94\%\\
$[0.80,\,1.24]$ & $[1.25,\,1.49]$ & Caa/CCC & 9.46\%\\
$[0.65,\,0.79]$ & $[0.80,\,1.24]$ & Ca2/CC & 9.97\%\\
$[0.20,\,0.64]$ & $[0.50,\,0.79]$ & C/C & 13.09\%\\
$<0.20$ & $<0.50$ & D2/D & 17.44\%\\
\bottomrule
\end{tabular}

> **Added explanation (not on slides)**
Interest coverage ratio $=$ EBIT / interest expense. Small caps need a *higher* coverage for the same rating, because they are riskier. Pre-tax $k_d=r_f+$ default spread. Example: coverage 7.0 for a large cap $\Rightarrow$ AA $\Rightarrow$ $k_d=3.5\%+0.85\%=4.35\%$.

### Cost of Capital Approach V: Yield to Maturity vs Cost of Debt

  - We only observe the **promised yield** (yield to maturity), not the cost of debt $k_d$.
  - We can estimate $k_d$ as an **IRR using expected cash flows** (payments) and the current price:
  \[
  \frac{\mathbb{E}_0[CF_1]}{(1+k_d)}+\frac{\mathbb{E}_0[CF_2]}{(1+k_d)^2}+\frac{\mathbb{E}_0[CF_3]}{(1+k_d)^3}+\dots+\frac{\mathbb{E}_0[CF_T]}{(1+k_d)^T}-\text{Price}_0=0
  \]

> **General rule**
**(Promised) yield to maturity $\geq$ cost of debt.** The inequality is **strict iff there is any probability of default with less than 100\% recovery**:

  - the difference between YTM and the cost of debt increases with the probability of default;
  - **YTM $-$ cost of debt $=$ expected default loss**.

> **Illustration (not on slides)**
A 1-year bond with face 100 and a 10\% coupon trades at 100, so the YTM is 10\% (promised payment 110). Default probability 5\%, recovery 40\%:
\[
\mathbb{E}[CF_1]=0.95\times110+0.05\times(0.40\times110)=104.5+2.2=106.7\quad\Rightarrow\quad k_d=\frac{106.7}{100}-1=6.7\%
\]
Expected default loss $=10\%-6.7\%=3.3\%$. Using the 10\% YTM as $k_d$ would overstate the cost of debt.

### Cost of Capital Approach VI: Weights

**3. Weights on debt and equity.** The effect of capital structure on value is isolated by **keeping EBIT fixed and varying only the cost of capital**. Two assumptions:

  - the debt ratio is decreased by raising new equity and retiring debt; conversely, it is increased by borrowing and buying back stock (**recap**);
  - pre-tax **EBIT is unaffected** by the financing mix and thus by the bond rating.

If EBIT changes with default risk, the analysis is the same but **minimizing WACC may not be optimal**, since value depends on both cash flows and WACC: firm value must be computed at each debt level, and the optimal ratio is the one that **maximizes firm value**.

### WACC Optimization: The Algorithm

[Figure: redrawn diagram, see PDF]

### Case: Financial Data for Disney

> **Disney: inputs**
\small
\begin{tabular}{@{}lr@{\hspace{1.2cm}}lr@{}}
Market value of debt & \$16,682m & Treasury bond rate & 3.5\%\\
Market value of equity & \$45,193m & Equity risk premium & 6.0\%\\
Market price per share & \$24.34 & Marginal tax rate & 38.0\%\\
Shares outstanding & 1,856.7m & Pre-tax $k_d$ & 6.0\%\\
Unlevered $\beta$ & 0.7333 & After-tax $k_d$ & $3.72\%=6\%\times(1-38\%)$\\
\end{tabular}

\medskip
\begin{tabular}{@{}lrr@{}}
\toprule
 & **Last fiscal year** & **Trailing 12 months**\\
\midrule
Revenues & \$37,843 & \$36,990\\
EBITDA & \$8,986 & \$8,319\\
D\&A & \$1,582 & \$1,693\\
EBIT & \$7,404 & \$6,726\\
Interest expense & \$712 & \$728\\
EBITDA (adjusted for leases) & \$9,989 & \$8,193\\
EBIT (adjusted for leases) & \$7,708 & \$6,500\\
Interest expenses (adjusted for leases) & \$815 & \$831\\
Capital expenditures (assumption) & \$1,628 & \$1,628\\
\bottomrule
\end{tabular}

**Discussion Questions I.** (i) What are Disney's current $\beta_{\text{levered}}$, $k_e$, and WACC? (ii) What is Disney's $\beta_{\text{levered}}$ at each $D/(D+E)$ ratio? (iii) What are the interest coverage ratio, bond rating, interest rate, and after-tax $k_d$ at each $D/(D+E)$? (iv) What is the WACC at each $D/(D+E)$? (v) Is Disney currently at its optimal debt ratio? What would be the value consequence of moving to the optimal $D/(D+E)$?

> **Official solution (Class 5 Excel), with the value step completed by us**
**Conventions of the class solution.** Total firm value held fixed at $V=16{,}682+45{,}193=\mathbf{61{,}875}$ (recapitalization: debt replaces equity). $\$$Debt $=d\times61{,}875$. $\beta_l=\beta_u(1+D/E)$ with $D/E=d/(1-d)$. Interest coverage ratio uses the \textbf{trailing, lease-adjusted EBIT $=6{,}500$}: ICR $=6{,}500/\$\text{Interest}$. Rating from the large-cap table; interest rate $=r_f+$ spread; $k_d(1-t)$ with $t=38\%$.

**(i) Current.** $D/E=16{,}682/45{,}193=0.3691$; $\beta_l=0.7333\times1.3691=\mathbf{1.004}$; $k_e=3.5\%+1.004\times6\%=\mathbf{9.52\%}$;
\[
\text{WACC}=9.52\%\times\tfrac{45{,}193}{61{,}875}+6\%(1-0.38)\times\tfrac{16{,}682}{61{,}875}=9.52\%\times0.7304+3.72\%\times0.2696=\mathbf{7.96\%}
\]
**(ii)--(iv)** The class table:

\scriptsize
\setlength{\tabcolsep}{3.5pt}
\begin{tabular}{@{}rrrrrrcrrr@{}}
\toprule
$\frac{D}{D+E}$ & $D/E$ & $\beta_l$ & $k_e$ & \$Debt & \$Interest & Rating & Rate & ICR & $k_d(1-t)$\ \ **WACC**\\
\midrule
0\% & 0.00 & 0.7333 & 7.90\% & 0 & 0 & AAA & 4.19\% & -- & -- \quad\ \ 7.90\%\\
10\% & 0.11 & 0.8148 & 8.39\% & 6,188 & 259 & AAA & 4.19\% & 25.07 & 2.60\% \quad 7.81\%\\
20\% & 0.25 & 0.9166 & 9.00\% & 12,375 & 519 & AAA & 4.19\% & 12.54 & 2.60\% \quad 7.72\%\\
30\% & 0.43 & 1.0476 & 9.79\% & 18,563 & 807 & AA & 4.35\% & 8.05 & 2.70\% \quad 7.66\%\\
40\% & 0.67 & 1.2222 & 10.83\% & 24,750 & 1,131 & A+ & 4.57\% & 5.75 & 2.83\% \quad 7.63\%\\
50\% & 1.00 & 1.4666 & 12.30\% & 30,938 & 1,448 & A & 4.68\% & 4.49 & 2.90\% \quad 7.60\%\\
60\% & 1.50 & 1.8332 & 14.50\% & 37,125 & 1,793 & A$-$ & 4.83\% & 3.62 & 3.00\% \quad 7.60\%\\
**70\%** & 2.33 & 2.4443 & 18.17\% & 43,313 & 2,092 & A$-$ & 4.83\% & 3.11 & 3.00\% \quad **7.55\%**\\
80\% & 4.00 & 3.6665 & 25.50\% & 49,500 & 2,579 & BBB & 5.21\% & 2.52 & 3.23\% \quad 7.68\%\\
90\% & 9.00 & 7.3330 & 47.50\% & 55,688 & 5,257 & B$-$ & 9.44\% & 1.24 & 5.85\% \quad 10.02\%\\
\bottomrule
\end{tabular}

How a row is built (e.g., 40\%): $D/E=0.4/0.6=0.667$; $\beta_l=0.7333\times1.667=1.2222$; $k_e=3.5\%+1.2222\times6\%=10.83\%$; \$Debt $=0.4\times61{,}875=24{,}750$; at the A+ rate $4.57\%$ interest $=1{,}131$, ICR $=6{,}500/1{,}131=5.75\in[5.50,6.49]\Rightarrow$ A+ (consistent); $k_d(1-t)=4.57\%\times0.62=2.83\%$; WACC $=10.83\%\times0.6+2.83\%\times0.4=7.63\%$.\\
\footnotesize (At 90\% the ICR of 1.24 falls in the band $[0.80,1.24]$, i.e.\ a \textbf{CCC} rating; the class Excel assigns B$-$, an inconsistency of the file. In the exam, read the rating strictly from the table.)\normalsize

**(v) Optimal ratio and value consequence.** WACC is minimized at **70\% debt (7.55\%)** vs the current 7.96\%: Disney is **under-levered**. The Excel stops at the WACC; we complete the value step with the standard method (EBIT fixed, implied growth):
\begin{align*}
\text{FCFO}_0 &= 6{,}500\times(1-0.38)+1{,}693-1{,}628 = 4{,}095\\
61{,}875 &= \frac{4{,}095(1+g)}{0.0796-g}\ \Rightarrow\ g=\frac{61{,}875\times0.0796-4{,}095}{61{,}875+4{,}095}=1.26\%\\
V_{70\%} &= \frac{4{,}095\times1.0126}{0.0755-0.0126} = \mathbf{65{,}940}\quad\Rightarrow\quad \Delta V\approx+\$4{,}065\text{m}\ (\approx\$2.19\text{ per share})
\end{align*}
\footnotesize **Correction to our earlier version**: we had used last-year lease-adjusted EBIT (7,708) for the coverage ratio, which kept the ratings higher and moved the minimum WACC to 80\%. The class uses trailing EBIT (6,500). Note how flat the WACC curve is between 40\% and 70\% (7.55--7.63\%).

% =====================================================================

## APV Optimization

### Same Question, Different Decomposition

\small
\begin{tabular}{@{}ll@{}}
\toprule
**WACC approach** & **APV approach**\\
\midrule
Debt affects WACC & Debt creates tax benefits and distress costs\\
Find the debt ratio minimizing WACC & Find the debt ratio maximizing $V_u+TB-BC$\\
Best when target leverage ratios are stable & Best when dollar debt or debt path is explicit\\
\bottomrule
\end{tabular}

### APV Approach I

  - In the APV approach we begin with **firm value without debt**.
  - Adding debt, we consider the benefits and costs of borrowing and their net effect on value.
  - The value of the levered firm is then estimated at different levels of debt: \textcolor{keyred}{**the debt level that maximizes firm value is the optimal debt ratio**}.
  - The unlevered firm value is **independent of expected leverage**: estimate it by discounting FCFO at the unlevered $k_U$. If you prefer not to estimate it and are willing to assume the current market value is correct, back it out by (i) subtracting the tax benefits and (ii) adding back the expected bankruptcy cost of the existing debt:

> **Key point**
\begin{align*}
\text{Current firm value} &= \text{Firm value}_{\text{unlevered}}+PV(TB)-PV(BC)\\
\textcolor{keyred}{\text{Firm value}_{\text{unlevered}}} &= \text{Current firm value}-PV(TB)+PV(BC)
\end{align*}

### APV Approach II: Five Steps

The only components that change with leverage are (i) **expected tax benefits** and (ii) **expected bankruptcy costs**. To obtain them:

  - holding firm value fixed, compute how much dollar debt the firm will have at 20\% $D/E$, 30\% $D/E$, and so on;
  - **tax benefits of debt $=$ dollar debt $\times$ tax rate** (assumes debt and tax benefits are permanent);
  - estimate the debt rating, interest rate, and interest expense at each debt ratio;
  - use the rating to estimate a **probability of default** (empirical studies);
  - **expected bankruptcy cost $=$ probability of bankruptcy $\times$ bankruptcy cost**, stated as \% of firm value.

Compute the value of the levered firm at each debt level: \textcolor{keyred}{**the debt level that maximizes firm value is the optimal debt ratio**}.

**Discussion Questions II.** (vi) Tax benefits at each $D/(D+E)$ for Disney? (vii) Bond ratings, default probabilities, and expected bankruptcy costs at each $D/(D+E)$? (viii) Levered firm value at each $D/(D+E)$ using APV?

> **Official solution (Class 5 Excel)**
**Conventions.** Ratings from the WACC table above; default probabilities from Altman (2009, Chapter~\ref{ch:wacc}); bankruptcy costs $=\mathbf{25\%}$ of firm value; current rating A ($\pi_d=0.66\%$); $TB=t\times D$ (permanent debt).

**Unlevered value** (back-out from today's market value):
\begin{align*}
V_u &= V-t\cdot D+\pi_d\cdot\text{BC\%}\cdot V=61{,}875-0.38\times16{,}682+0.0066\times0.25\times61{,}875\\
&= 61{,}875-6{,}339+102=\mathbf{55{,}638}
\end{align*}
At each debt ratio: $TB=0.38\times D$; $BC=(V_u+TB)\times\pi_d\times25\%$; $V_L=V_u+TB-BC$.

\small
\begin{tabular}{@{}rrrcrrr@{}}
\toprule
$\frac{D}{D+E}$ & \$Debt & $TB=0.38D$ & Rating & $\pi_d$ & $BC$ & $V_L$\\
\midrule
0\% & 0 & 0 & AAA & -- & 0 & 55,638\\
10\% & 6,188 & 2,351 & AAA & 0.07\% & 10 & 57,979\\
20\% & 12,375 & 4,703 & AAA & 0.07\% & 11 & 60,330\\
30\% & 18,563 & 7,054 & AA & 0.51\% & 80 & 62,612\\
40\% & 24,750 & 9,405 & A+ & 0.60\% & 98 & 64,945\\
50\% & 30,938 & 11,756 & A & 0.66\% & 111 & 67,283\\
60\% & 37,125 & 14,108 & A$-$ & 2.50\% & 436 & 69,310\\
70\% & 43,313 & 16,459 & A$-$ & 2.50\% & 451 & 71,646\\
**80\%** & 49,500 & 18,810 & BBB & 7.54\% & 1,403 & **73,045**\\
90\% & 55,688 & 21,161 & B$-$ & 45.00\% & 8,640 & 68,159\\
\bottomrule
\end{tabular}

Example row (80\%): $TB=0.38\times49{,}500=18{,}810$; $BC=(55{,}638+18{,}810)\times7.54\%\times25\%=1{,}403$; $V_L=55{,}638+18{,}810-1{,}403=73{,}045$.

**Interpretation.** APV value peaks at **80\% debt** and then falls sharply at 90\%, when the rating collapses to B$-$ (default probability 45\%). The APV optimum (80\%) differs from the WACC optimum (70\%), and APV values are much higher because $TB=tD$ treats all tax shields as permanent and riskless, while bankruptcy costs stay small until junk ratings. This illustrates why the two methods agree *only under consistent assumptions*.

\footnotesize **Correction to our earlier version**: we had used 30\% bankruptcy costs, the AA current rating and BC on $V_u$ only; the class uses 25\%, current rating A, BC on $(V_u+TB)$ and the ratings from the trailing-EBIT table, which brings the B$-$ rating and the value drop at 90\%.

% =====================================================================

## Conclusion

### Common Mistakes in Capital-Structure Optimization (slide)

  - Treating more debt as always value-increasing because of tax shields.
  - Minimizing WACC while ignoring that operating cash flows may fall with distress risk.
  - Using promised yield to maturity as the true cost of debt when default risk is material.
  - Holding equity $\beta$ fixed while changing leverage.
  - Holding the cost of debt fixed while increasing leverage.
  - Using book weights instead of market-value weights without justification.
  - Double-counting tax benefits in both WACC and APV.
  - Calling the lowest WACC ``optimal'' without checking the value consequence.

### Takeaways

  - Leverage can **create** value through interest tax shields.
  - Leverage can **destroy** value through higher required returns and expected distress costs.
  - In the WACC approach, leverage affects value through the **discount rate**.
  - In the APV approach, leverage affects value through **separately valued** tax benefits and bankruptcy costs.
  - Minimizing WACC maximizes value **only if operating cash flows are unaffected by leverage**.
  - The optimal debt ratio is the one that **maximizes firm value**, not necessarily the one with the most debt.
  - Capital-structure analysis is a **recapitalization question**: how much value is created or destroyed by moving from current to target leverage?

% =====================================================================

## Formula Summary Sheet

\small
\renewcommand{\arraystretch}{1.45}
\begin{tabular}{@{}p{5cm}p{10cm}@{}}
\toprule
**Concept** & **Formula**\\
\midrule
Trade-off value & $V_L=V_U+T_C D-PV(\text{distress costs})$\\
Levered beta at each ratio & $\beta_l=\beta_u(1+D/E)=\beta_u/(1-d)$,\ $d=D/(D+E)$\\
Cost of equity & $k_e=r_f+\beta_l\times\text{ERP}$\\
Interest coverage & EBIT / Interest expense $\to$ rating $\to$ spread\\
Pre-tax cost of debt & $k_d=r_f+\text{default spread(rating)}$\\
After-tax cost of debt & $k_d(1-t_{\text{marginal}})$\\
WACC at each ratio & $k_e(1-d)+k_d(1-t)\,d$\\
Firm value at each ratio & $V=\text{FCFO}_1/(\text{WACC}-g)$ (EBIT fixed)\\
Implied growth & $g=\dfrac{V\cdot\text{WACC}-\text{FCFO}_0}{V+\text{FCFO}_0}$\\
Cost of debt as IRR & $\sum_t \mathbb{E}_0[CF_t]/(1+k_d)^t-\text{Price}_0=0$\\
YTM vs $k_d$ & YTM $\geq k_d$;\ YTM $-k_d=$ expected default loss\\
APV & $V_L=V_u+TB-BC$\\
Unlevered value (back-out) & $V_u=\text{Current value}-PV(TB)+PV(BC)$\\
Tax benefit (permanent) & $TB=t\times D$\\
Expected bankruptcy cost & $BC=\pi_d\times\text{bankruptcy cost (\% of firm value)}$; class: $(V_u+TB)\times\pi_d\times\text{BC\%}$\\
Unlevered value (class) & $V_u=V-tD+\pi_d\cdot\text{BC\%}\cdot V$\\
\bottomrule
\end{tabular}

% =====================================================================

## Common Mistakes and Exam Traps

> **Exam traps -- Chapter 5**

  - More debt is **not** always better: the tax shield ($T_C D$) is offset by rising distress costs; the optimum $D^*$ is where marginal benefit $=$ marginal cost.
  - Minimizing WACC $=$ maximizing value **only if FCFO are unaffected by leverage**; otherwise compute value at each debt ratio.
  - When leverage changes, **relever beta** ($\beta_l=\beta_u(1+D/E)$) and **re-estimate $k_d$** (coverage $\to$ rating $\to$ spread). Holding either fixed is a mistake.
  - The coverage ratio is **EBIT / interest**; small caps need higher coverage for the same rating.
  - Pre-tax $k_d=r_f+$ default spread; after-tax uses the **marginal** tax rate.
  - **YTM $\geq$ cost of debt**; strictly greater whenever default is possible with recovery $<100\%$; the difference is the expected default loss. Do not use YTM as $k_d$ for risky debt.
  - In the recap analysis, EBIT is held fixed and only the mix changes (borrow to buy back stock, or issue equity to retire debt).
  - Use **market-value** weights.
  - WACC and APV answer the same question with different decompositions; do not count tax benefits in both.
  - APV: $V_u$ is independent of leverage; it can be backed out as current value $-$ PV(TB) $+$ PV(BC).
  - APV five steps: dollar debt at each ratio; $TB=t\times D$ (permanent debt); rating and interest; default probability from the rating; $BC=\pi_d\times$ bankruptcy cost (\% of firm value).
  - Ignoring or underestimating bankruptcy costs makes APV value increase monotonically with debt (the 100\%-debt trap).
  - Disney (class solution): coverage on **trailing** lease-adjusted EBIT; WACC minimum at 70\% (7.55\% vs 7.96\% today); APV maximum at 80\%; the two optima differ because the methods embed different assumptions.
  - The lowest WACC is not ``optimal'' until its value consequence is checked; the answer to a capital-structure question is a **value change** from current to target leverage.

