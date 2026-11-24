<!-- Markdown notes generated from the LaTeX chapter; tables and formulas kept in LaTeX syntax. The PDF is the reference version. -->
# From Cash Flows to Enterprise Value: WACC and APV

*Based on Lecture 04 (file L04, 31 slides): ``From Cash Flows to Enterprise Value -- WACC, APV, and the role of financing policy''. Sessions 6--7 of Part One (workflow step: cash flow $\to$ value).*

## Where We Are in the Valuation Workflow

Equity story $\to$ Financial statements $\to$ Forecasts $\to$ Cash flows $\to$ **Discount rate** $\to$ Terminal value $\to$ Multiples $\to$ Value bridge $\to$ Recommendation.

> **Today**
**Projected FCFO $\longrightarrow$ Enterprise Value using WACC and APV**

**Today's professional task.** You have forecast FCFO. Your job is to value the operating business and decide whether financing policy should be **embedded in the discount rate** or **valued separately**:

  - match FCFO to the correct discount rate;
  - estimate WACC under a target leverage policy;
  - estimate APV when debt levels are known or changing;
  - avoid double-counting tax shields and leverage risk;
  - understand when WACC and APV should give similar or different answers.

**Plan for today.**

\small
\begin{tabularx}{\textwidth}{@{}lXX@{}}
\toprule
**Layer** & **What we learn** & **Why it matters**\\
\midrule
CORE & FCFO $\to$ Enterprise Value & All DCF valuation\\
CORE & WACC approach & Standard enterprise DCF\\
PRO & Choosing WACC vs APV & Project, M\&A, LBO, leverage changes\\
TECH & $\beta$ levering/unlevering, tax shields, bankruptcy costs & Avoid model inconsistency\\
PRACTICE & Discussion Questions & Turn formulas into valuation skill\\
\bottomrule
\end{tabularx}

% =====================================================================

## From FCFO to Enterprise Value

### FCFO: From Earnings to Cash Flow (Reminder)

The two definitions of Chapter~\ref{ch:fcf}, Section 1.3.9, are repeated on the slide:

\small
\begin{tabular}{@{}rl@{\hspace{0.5cm}}rl@{}}
\multicolumn{2}{@{}l}{**1. FCFE -- equity-side valuation**} & \multicolumn{2}{l}{**2. FCFO -- asset-side valuation**}\\[3pt]
$+$ & Net income -- adjusted & $+$ & FCFE\\
$+/-$ & Non-cash expenditure / revenues & $+$ & Interest expense $\times(1-$tax rate$)$\\
$-$ & Net CapEx ($=$ CapEx $-$ D\&A) & $+$ & (Principal repayments $-$ new debt issues)\\
\cmidrule{3-4}
$-$ & Changes in non-cash WC & $=$ & **FCFO**\\[3pt]
$-$ & (Principal repayments $-$ new debt issues) & $+$ & EBIT -- adjusted\\
\cmidrule{1-2}
$=$ & **FCFE** & $+/-$ & Non-cash expenditure / revenues\\
&& $-$ & Taxes on EBIT\\
&& $-$ & Reinvestment needs (net CapEx and WC)\\
\cmidrule{3-4}
&& $=$ & **FCFO**
\end{tabular}

\slidefig{[Ignoring preferred dividends. If preferred stock exists, preferred dividends also need to be netted out.]}

### FCFO and Other Cash-Flow Measures

\small
\renewcommand{\arraystretch}{1.25}
\begin{tabularx}{\textwidth}{@{}>{\raggedright\arraybackslash}p{2.9cm}>{\raggedright\arraybackslash}p{3.6cm}X@{}}
\toprule
**Cash flow used** & **Definition** & **Use in valuation**\\
\midrule
**FCFO** & Free cash flow from operations & Discounting **FCFO at WACC** yields the **value of the operating assets** of a firm. Adding the value of non-operating assets, if any, yields firm value.\\
\midrule
**FCFE** & FCFO $-$ Interest $\times(1-\tau_C)$ $-$ Principal repaid $+$ Net debt issued $-$ Preferred dividends & Discounting **FCFE at $k_e$** yields the **value of equity** of a firm.\\
\midrule
**EBITDA** & FCFO $+$ EBIT $\times\tau_C$ $+$ CapEx $+\Delta$NWC & If you discount EBITDA at the cost of capital, you assume that there are **no taxes** and that the firm will actively **disinvest** non-cash over time. It would be inconsistent to assume a growth rate or an infinite life for this firm.\\
\midrule
**EBIT$(1-\tau_C)$** \newline {\footnotesize (NOPAT is a modified version that removes non-operating items affecting reported EBIT)} & FCFO $+$ CapEx $-$ D\&A $+\Delta$non-cash NWC & If you discount after-tax EBIT at the cost of capital, you assume **no reinvestment**: D\&A is reinvested to maintain existing assets. You can assume an **infinite life** but **cannot assume growth**.\\
\bottomrule
\end{tabularx}

> **Why these identities hold** *(added, not on slides)*
From FCFO $=$ EBIT$(1-\tau)$ $+$ D\&A $-$ CapEx $-\Delta$NWC:

  - EBIT$(1-\tau)$ $=$ FCFO $+$ (CapEx $-$ D\&A) $+\Delta$NWC: NOPAT is FCFO before net reinvestment. A perpetuity of NOPAT is coherent only with zero net reinvestment, hence zero growth.
  - EBITDA $=$ EBIT $+$ D\&A $=$ FCFO $+\tau\cdot$EBIT $+$ CapEx $+\Delta$NWC: EBITDA is FCFO before taxes and before *all* CapEx. Treating it as a perpetual cash flow means paying no taxes and never replacing the assets (the asset base shrinks), so the firm cannot live forever, let alone grow.

### Cost of Capital and Adjusted Present Value

[Figure: redrawn diagram, see PDF]

Depending on assumptions on **future growth**, both approaches can have 2-stage, 3-stage versions (same as with the DDM and FCFE models).

### Levering and Unlevering Beta

The formula to unlever (and relever) beta **depends on the assumed debt policy**. Two main alternatives:

> **Beta and debt policy**
**Assumption 1 -- debt as a \% of total capital, $D/(D+E)$, is fixed** (debt grows as the business grows):
\[
\beta_{\text{levered}} = \beta_{\text{unlevered}}\times\left[1+\frac{D}{E}\right]
\]
**Assumption 2 -- debt is fixed in \$ terms** (as in Modigliani--Miller): **Hamada formula**
\[
\beta_{\text{levered}} = \beta_{\text{unlevered}}\times\left[1+(1-\tau_C)\cdot\frac{D}{E}\right]
\]
Unlevering: invert the same formula, $\beta_u=\beta_l/[1+D/E]$ or $\beta_u=\beta_l/[1+(1-\tau_C)D/E]$.

> **Intuition for the two formulas** *(added, not on slides)*
With **fixed \$ debt** the tax shields are as safe as the debt (no risk from the business), so they reduce the risk borne by equity holders. The $(1-\tau_C)$ factor appears and the levered beta is *lower*. With a **constant leverage ratio** the debt (and hence the tax shields) moves up and down with firm value, so tax shields are as risky as the operating assets and no $(1-\tau_C)$ appears; the levered beta is *higher* for the same $D/E$. Both formulas assume a debt beta of zero.

> **Discussion Questions I -- F\&B firm (data)**
A privately held US firm in the food \& beverage business wants to estimate its cost of equity:

\begin{tabular}{@{}lr@{\hspace{1cm}}lr@{}}
Interest rate on \$ T-bonds & 3\% & Shareholders' equity & \$100m\\
ERP on US market & 6\% & Net debt & \$70m\\
Unlevered beta F\&B sector & 0.5 & Tax rate & 20\%\\
\end{tabular}

(i) The CFO aims at a constant debt policy in monetary terms (fixed debt): cost of equity?\\
(ii) The CFO aims at a constant leverage financing policy: cost of equity?

> **Solution -- \checkmark\ confirmed by the official class solution (Class 4 Excel)**
$D/E = 70/100 = 0.70$.
\begin{align*}
\text{(i) Fixed debt (Hamada):}\quad \beta_l &= 0.5\times[1+(1-0.20)\times0.70] = 0.5\times1.56 = \mathbf{0.78}\\
k_e &= 3\% + 0.78\times6\% = \mathbf{7.68\%}\\
\text{(ii) Constant leverage:}\quad \beta_l &= 0.5\times[1+0.70] = \mathbf{0.85}\\
k_e &= 3\% + 0.85\times6\% = \mathbf{8.10\%}
\end{align*}
The constant-leverage policy gives a higher cost of equity because the tax shields are risky.

% =====================================================================

## WACC: Financing Policy Inside the Discount Rate

### The Cost of Capital Approach: Stable Growth Model

A firm with FCFO growing at a stable rate (steady state) can be valued as:

> **Stable-growth firm value**
\[
\text{Firm Value}_0 = \frac{\text{FCFO}_1}{\text{WACC}-g_n}
\]

  - FCFO$_1$ = expected FCFO **next year**; WACC = weighted average cost of capital; $g_n$ = annual growth rate of FCFO forever.
  - Under stable growth: $\boxed{g_n = \text{Reinvestment rate}\times\text{Return on capital}}$.
  - The stable growth rate must be $\leq$ the growth rate of the economy (nominal or real, depending on CF and WACC).
  - Firm characteristics must be consistent with the assumptions of stable growth.

**Limitations**

  - Like all stable-growth models, it is **sensitive to assumptions about $g_n$**.
  - This sensitivity is **higher when using WACC** (which is lower than $k_e$).
  - It is also sensitive to assumptions about CapEx relative to depreciation.
  - The cost of capital should also reflect a stable-growth firm ($\beta$, $D/E$).

> **Why sensitivity is higher with WACC** *(added, not on slides)*
Value $=$ FCFO$_1$/(WACC $-g$). With FCFO$_1=100$ and $g=3\%$: at WACC $=8\%$ value $=2{,}000$; at WACC $=9\%$ value $=1{,}667$. With $g=4\%$: value $=2{,}500$ (WACC 8\%). The smaller the spread (WACC $-g$), the more a one-point change moves value. WACC $<k_e$, so the spread is smaller than for equity models.\\
**Reinvestment rate** $=$ (CapEx $-$ D\&A $+\Delta$NWC)/EBIT$(1-t)$; **FCFO** $=$ EBIT$(1-t)\times(1-\text{RR})$.

> **Discussion Questions II -- Telesp (data)**
Telesp provides telecommunication services to S\~ao Paulo:

\begin{tabular}{@{}lr@{\hspace{1cm}}lr@{}}
EBIT & R\$3,544m & BV equity (year $-1$) & R\$20,057m\\
Effective tax rate & 30.00\% & BV debt (year $-1$) & R\$8,042m\\
CapEx & R\$1,659m & Cash (year $-1$) & R\$4,277m\\
D\&A & R\$1,914m & Market value equity & R\$21,982m\\
$\Delta$ non-cash NWC & R\$1,119m & Market value net debt & R\$5,519m\\
\end{tabular}

(iii) Expected growth rate? Risk-free rate in Brazil 7\%, ERP 8\%, industry $\beta$ 0.8, pre-tax $k_d$ 9.50\%. (iv) WACC? (v) Enterprise and equity value?

> **Solution -- \checkmark\ confirmed by the official class solution (Class 4 Excel)**
**(iii) Growth.**
\begin{align*}
\text{NOPAT} &= 3{,}544\times(1-0.30) = 2{,}480.8\\
\text{Net reinvestment} &= \text{CapEx}-\text{D\&A}+\Delta\text{NWC} = 1{,}659-1{,}914+1{,}119 = 864\\
\text{Reinvestment rate} &= 864/2{,}480.8 = 34.83\%\\
\text{ROC} &= \frac{\text{NOPAT}}{\text{BV equity}+\text{BV debt}-\text{Cash}} = \frac{2{,}480.8}{20{,}057+8{,}042-4{,}277}\\
&= \frac{2{,}480.8}{23{,}822} = 10.41\%\\
g &= 34.83\%\times10.41\% = \mathbf{3.63\%}
\end{align*}
**(iv) WACC** (taking the industry $\beta=0.8$ as the equity beta of Telesp; market-value weights):
\begin{align*}
k_e &= 7\%+0.8\times8\% = 13.40\%\qquad k_d(1-t) = 9.50\%\times0.70 = 6.65\%\\
\tfrac{E}{V} &= \tfrac{21{,}982}{27{,}501}=79.93\%\qquad \tfrac{D}{V}=\tfrac{5{,}519}{27{,}501}=20.07\%\\
\text{WACC} &= 13.40\%\times0.7993+6.65\%\times0.2007 = \mathbf{12.05\%}
\end{align*}
**(v) Value.**
\begin{align*}
\text{FCFO}_0 &= 2{,}480.8-864 = 1{,}616.8\qquad \text{FCFO}_1 = 1{,}616.8\times1.0363 = 1{,}675.4\\
\text{EV} &= \frac{1{,}675.4}{0.12045-0.03627} = \mathbf{R\$19{,}902m}\\
\text{Equity} &= 19{,}902-5{,}519 = \mathbf{R\$14{,}383m}
\end{align*}
The model value is below the market value of equity (21,982): the market prices higher growth or lower risk than these inputs.\par
\footnotesize If instead $0.8$ is read as an *unlevered* industry beta (relevered with Hamada at $D/E=5{,}519/21{,}982$): $\beta_l=0.94$, $k_e=14.52\%$, WACC $=12.94\%$, EV $=17{,}982$, equity $=12{,}463$.

### The Cost of Capital Approach: General Model

In the most general case, firm value is the present value of expected FCFOs:

> **General and two-stage models**
\[
\text{Firm Value}_0=\sum_{t=1}^{\infty}\frac{\mathbb{E}[\text{FCFO}_t]}{(1+\text{WACC})^t}
\]
If the firm reaches steady state after $n$ years and then grows at a stable $g_n$:
\[
\text{Firm Value}_0=\sum_{t=1}^{n}\frac{\mathbb{E}[\text{FCFO}_t]}{(1+\text{WACC}_{hg})^t}+\frac{\dfrac{\mathbb{E}[\text{FCFO}_{n+1}]}{\text{WACC}_{st}-g_n}}{(1+\text{WACC}_{hg})^n}
\]
$hg$ = high growth; $st$ = stable growth. The terminal value at $n$ uses the *stable* WACC and is discounted at the *high-growth* WACC.

**Stable growth rate** (PRO): $g_n$ = reinvestment rate $\times$ return on capital; it must be reasonable relative to the nominal growth rate of the economy/industry; it should be linked to fundamentals.

**Limitations**

  - FCFEs are a much more intuitive measure of cash flows than FCFO. FCFE is a real cash flow that can be traced and analysed, whereas **FCFO is a theoretical construct**.
  - Its focus on pre-debt cash flows might **hide survival problems** if firms cannot raise additional equity to pay down debt.
  - Using a debt ratio in the cost of capital requires assuming that firms can **freely issue debt and equity and rebalance** their capital structure, which might not always be reasonable.

**The model works best for firms**

  - reaching steady state in several stages (two, three, $n$);
  - with either very high or very low leverage, or in the process of changing their leverage. In such cases computing FCFE is much more challenging because of the volatility induced by (net) debt payments.

### Using FCFO in the CoC Approach: Comparison with FCFE

  - The CoC model with FCFO, unlike FCFE or the DDM, **values the whole firm** rather than its equity alone. To extract equity value, subtract the market value of outstanding (net) debt.
  - Equity value under firm valuation (FCFO) and equity valuation (FCFE) will be the **same if we make consistent assumptions about financial leverage** (in practice, this is hard).
  - Advantage of FCFO: cash flows relating to debt need not be considered explicitly (FCFO is a pre-debt CF), whereas they must be in FCFE.
  - On the other hand, firm valuation requires information about (i) **debt ratios** and (ii) **interest rates** to estimate the WACC.

> **Discussion Questions III -- no-growth perpetual firm (data)**
No-growth, no-reinvestment perpetual firm: EBIT \$166.67m; effective tax rate 40\%; equity (market value) \$600m; $k_e$ 13.87\%; debt (market value) \$400m; $k_d$ (pre-tax) 7\%.\\
(vi) WACC? (vii) Enterprise value? (viii) Equity value by subtracting debt from EV? (ix) Equity value by discounting net income at $k_e$?

> **Solution -- \checkmark\ confirmed by the official class solution (Class 4 Excel)**
\begin{align*}
\text{(vi)}\quad \text{WACC} &= 13.87\%\times\tfrac{600}{1{,}000}+7\%\times(1-0.40)\times\tfrac{400}{1{,}000} = 8.322\%+1.680\% = \mathbf{10.00\%}\\
\text{(vii)}\quad \text{EV} &= \frac{\text{EBIT}(1-t)}{\text{WACC}} = \frac{166.67\times0.60}{0.10} = \frac{100}{0.10} = \mathbf{\$1{,}000m}\\
\text{(viii)}\quad \text{Equity} &= 1{,}000-400 = \mathbf{\$600m}\\
\text{(ix)}\quad \text{NI} &= (166.67-7\%\times400)\times0.60 = (166.67-28)\times0.60 = 83.20\\
\text{Equity} &= \frac{\text{NI}}{k_e} = \frac{83.20}{0.1387} = \mathbf{\$600m}
\end{align*}
No growth and no reinvestment $\Rightarrow$ FCFO $=$ NOPAT and FCFE $=$ NI (no net borrowing). Both routes give \$600m.

\textbf{Why the two routes agree here: three assumptions (PRO)}

  - **Values for debt and equity.** The debt and equity values used to compute the WACC are the same values obtained in the valuation. This circular reasoning (you need WACC to obtain the values in the first place) means that a WACC based on market-value weights will **not** give the same equity value as an equity model **if the firm is not fairly priced to begin with**.
  - **Extraordinary items.** No extraordinary or non-operating items affect net income but not operating income; so NI $=$ operating income $-$ interest $-$ taxes.
  - **Interest expenses.** Interest expense $=$ pre-tax cost of debt $\times$ market value of debt. If a firm has old debt on its books with interest differing from the current cost of debt, the two approaches diverge.

If there is **expected growth**, the potential for inconsistency increases: the firm must borrow enough to fund new investments so that the debt ratio stays at the level used in the WACC.

> **Discussion Questions IV -- DaimlerChrysler (data)**
DaimlerChrysler is a mature firm in a mature industry $\Rightarrow$ it is in stable growth $\Rightarrow$ it aims to keep a **constant leverage ratio**. Figures in DM million:

\begin{tabular}{@{}lr@{\hspace{1cm}}lr@{}}
EBIT (operating income) & 9,324 & Bottom-up unlevered $\beta$ (industry) & 0.61\\
Effective tax rate & 46.94\% & Daimler rating & AAA\\
ROC (after tax) & 7.15\% & Long-term German bond rate (DM) & 4.87\%\\
Equity (market value) & 62,300 & Default spread & 0.20\%\\
Debt (market value) & 64,500 & ERP & 4.00\%\\
Cash \& marketable securities & 18,068 & Long-term growth rate & 3.00\%\\
\end{tabular}

(x) Reinvestment rate? (xi) Cost of equity, cost of debt, WACC? (xii) Enterprise value and equity value?

> **Official solution (Class 4 Excel) -- uses NET debt**
The official solution measures leverage with **net debt** $D-\text{Cash}$ (cash is netted against debt), both in $\beta$ and in the WACC weights:
\begin{align*}
\text{(x)}\quad \text{RR} &= \frac{g}{\text{ROC}} = \frac{3\%}{7.15\%} = \mathbf{41.96\%}\\
\text{Net debt} &= 64{,}500-18{,}068 = 46{,}432\qquad \text{Net debt}+E = 46{,}432+62{,}300=108{,}732\\
\frac{D-C}{E} &= \frac{46{,}432}{62{,}300}=0.7453\qquad \frac{D-C}{D-C+E}=\frac{46{,}432}{108{,}732}=42.70\%\\
\text{(xi)}\quad \beta_l &= 0.61\times[1+0.7453] = \mathbf{1.0646}\quad\text{(constant leverage: no }(1-\tau)\text{)}\\
k_e &= 4.87\%+1.0646\times4\% = \mathbf{9.13\%}\\
k_d &= 4.87\%+0.20\% = \mathbf{5.07\%}\ \text{pre-tax};\qquad k_d(1-\tau)=5.07\%\times0.5306=2.69\%\\
\text{WACC} &= 9.13\%\times(1-0.4270)+2.69\%\times0.4270 = 5.231\%+1.149\% = \mathbf{6.38\%}\\
\text{(xii)}\quad \text{FCFO}_1 &= \text{EBIT}(1-\tau)\times(1-\text{RR})\times(1+g)\\
&= 9{,}324\times0.5306\times0.5804\times1.03 = \mathbf{2{,}957.7}\\
\text{EV} &= \frac{2{,}957.7}{0.0638-0.03} = \mathbf{87{,}527}\\
\text{Equity} &= \text{EV}-(\text{Debt}-\text{Cash}) = 87{,}527-46{,}432 = \mathbf{41{,}095}
\end{align*}
\footnotesize **Correction to our earlier version**: we had used *gross* debt in $\beta$ and in the weights ($\beta_l=1.2415$, WACC 6.20\%, EV 92,393, equity 45,961). The class convention is net debt: follow it in the exam. The model equity value (41,095) is well below the market value (62,300).

% =====================================================================

## APV: Financing Policy Valued Separately

### APV in One Line

> **APV**
\[
\boxed{V_l = V_u + TB - BC}
\]
$V_l$: value of the levered firm; $V_u$: value of the unlevered firm; $TB$: present value of the tax benefits of debt (tax shields); $BC$: present value of bankruptcy costs.

### APV: General Model

**1. Value of the unlevered firm, $V_u$**
\[
V_{u,0}=\frac{\mathbb{E}[\text{FCFO}_1]}{\rho_u-g_n}\qquad\text{or}\qquad
V_{u,0}=\sum_{t=1}^{n}\frac{\mathbb{E}[\text{FCFO}_t]}{(1+\rho_u)^t}+\frac{\dfrac{\mathbb{E}[\text{FCFO}_{n+1}]}{\rho_{u,st}-g_n}}{(1+\rho_{hg})^n}
\]
$\rho_u$: unlevered $k_e$ ($hg$ high growth, $st$ stable); $g_n$: stable growth rate.

**2. Expected tax benefit from borrowing, $TB$**. Two cases:

> **Tax benefits**
(i) **$D$ is low and fixed**:\quad $TB_0=\dfrac{\tau_C\cdot k_d\cdot D}{k_d}=\tau_C\cdot D$\\[6pt]
(ii) **$D$ is high and/or $D/E$ is predetermined**:
\[
TB_0=\sum_{t=1}^{n}\frac{\mathbb{E}[\tau_C\cdot k_d\cdot D_t]}{(1+\rho_u)^t}+\frac{\tau_C\cdot k_d\cdot D}{(\rho_u-g_n)\cdot(1+\rho_u)^n}
\]

**3. Expected bankruptcy costs, $BC$**

> **Bankruptcy costs**
\[
BC_0=\pi_d\times\text{LGD}
\]
$\pi_d$: probability of default; LGD: loss given default.

> **Reading the TB formulas** *(added, not on slides)*
Each year the firm saves taxes $=\tau_C\times$ interest $=\tau_C\,k_d\,D_t$. In case (i) the saving is a riskless perpetuity, as safe as the debt, so it is discounted at $k_d$ and the $k_d$ cancels: $TB=\tau_C D$. In case (ii) the debt path is set by the plan or by $D/E$, so the shields are as risky as the business and are discounted at $\rho_u$; after year $n$ they grow at $g_n$ (terminal value of the shields).\\
Example of case (i): $D=500$ permanent, $\tau=35\%$ $\Rightarrow$ $TB=175$.

**Estimating $\pi_d$**: two indirect ways:

  - estimate a **bond rating** and use the empirical default probabilities for that rating;
  - use a **statistical approach** (e.g., a probit) to estimate default probabilities from the firm's observable characteristics, at each debt level.

**Estimating the bankruptcy cost** (with considerable error) from studies of actual bankruptcies:

  - **direct** bankruptcy costs are small relative to firm value;
  - **indirect** costs can be substantial but vary widely across firms; Shapiro (1989) and Titman (1984) conclude that they could be as large as **25\%--30\% of firm value**, but provide no direct evidence.

\small
**Probability of default over 10 years by bond rating class (Altman, 2009)**\\[3pt]
\begin{tabular}{@{}lr@{\hspace{1cm}}lr@{\hspace{1cm}}lr@{}}
\toprule
**Rating** & **$\pi_d$** & **Rating** & **$\pi_d$** & **Rating** & **$\pi_d$**\\
\midrule
AAA & 0.07\% & BBB & 7.54\% & B$-$ & 45.00\%\\
AA & 0.51\% & BB+ & 10.00\% & CCC & 59.01\%\\
A+ & 0.60\% & BB & 16.63\% & CC & 70.00\%\\
A & 0.66\% & B+ & 25.00\% & C & 85.00\%\\
A$-$ & 2.50\% & B & 36.80\% & D & 100.00\%\\
\bottomrule
\end{tabular}

### APV: Stable Growth, Unlevered Cost of Equity, Limitations

  - **Stable growth rate**: $g_n$ = reinvestment rate $\times$ return on capital; reasonable relative to the nominal growth of the economy/industry; linked to fundamentals.
  - **Unlevered cost of equity, $\rho_u$**. First compute the firm's unlevered beta,
  \[
  \beta_{\text{unlevered}}=\beta_{\text{levered}}\Big/\left[1+\frac{D}{E}\right]\qquad\text{or}\qquad \beta_{\text{unlevered}}=\beta_{\text{levered}}\Big/\left[1+(1-\tau_C)\frac{D}{E}\right]
  \]
  depending on the financial policy; then \quad $\rho_u=r_f+\beta_u\cdot\text{ERP}$.
  - **Limitations**:
  
    - the tax rate should be the firm's **marginal** tax rate, assumed constant over time. If it changes you can still compute the PV of tax benefits year by year, but you cannot use the perpetual-growth equation;
    - the TB equation must be modified if current interest expenses do not reflect the current cost of debt;
    - estimating $\pi_d$ and BC is challenging and subject to errors.
  

### APV: Advantages and Challenges

**Advantages of APV**

  - It separates the effects of debt into their different components.
  - It allows the analyst to use different discount rates for each component.
  - We don't need to assume that the debt ratio stays constant forever, unlike CoC.
  - We can compute costs and benefits of debt keeping the dollar value of debt fixed.

**Challenges of APV**

  - It is hard to estimate the probabilities of default and the cost of bankruptcy.
  - As a result, many analyses ignore bankruptcy costs $\Rightarrow$ firm value always increases as firms borrow more $\Rightarrow$ the optimal debt ratio would be 100\% debt (is this realistic?).

> **CoC vs APV**
In general, **under the same assumptions, APV and CoC give very similar answers**. APV is more practical when firms evaluate a **stable dollar amount of debt**; CoC is more appropriate when firms keep **stable debt proportions $D/E$**.

**Why CoC and APV may sometimes give different values**

  - **Bankruptcy costs.** APV gives more flexibility to include *indirect* bankruptcy costs. To the extent these costs do not show up (or show up inadequately) in the pre-tax cost of debt, **APV gives a more conservative estimate** of value.
  - **Tax benefit.** APV computes the tax benefit from a **dollar debt value**, usually existing debt; CoC computes it from a **debt ratio** that may require the firm to borrow increasing amounts in the future.
  - **Financial leverage.** CoC is more practical for ongoing firms not going through sharp changes in leverage (easier to work with a ratio than with dollar debt levels). APV is more useful for **transactions funded disproportionately with debt** where repayments are negotiated or known.
  - **Discount rate.** APV often uses the **pre-tax cost of debt** to discount the tax savings; variations discount them at the WACC or the unlevered $k_e$, which gives values closer to CoC.

> **Discussion Questions V -- J.\ Crew (data)**
J.\ Crew is a US retailer selling clothes under its own brand through its own stores and online. It was acquired in a leveraged deal for \$2.7bn, with \$1.85bn of debt (rated BB) at a pre-tax $k_d$ of 7\%. Its $\beta_U$ is 1, $r_f$ 3.5\%, ERP 5\%, tax rate 35\%, $g$ 3.5\%. J.\ Crew generated \$230m of EBIT on revenues of \$1,722m before the acquisition, with a ROC of 14\%. Total bankruptcy costs are 30\% of firm value and the acquisition increased the probability of bankruptcy by 20\%. Debt schedule (\$m): year 1: 1,850; 2: 1,700; 3: 1,550; 4: 1,400; 5: 1,250; 6: 1,100; 7: 950; 8: 800; 9: 650; 10: 500; perpetuity: 500.\\
(xiii) Unlevered cost of equity $k_U$? (xiv) Unlevered value? (xv) Expected bankruptcy costs? (xvi) Levered value, compared with the \$2.7bn price?

> **Official solution (Class 4 Excel)**
**(xiii)** $k_U=r_f+\beta_U\times\text{ERP}=3.5\%+1\times5\%=\mathbf{8.5\%}$.

**(xiv)** Reinvestment rate $=g/\text{ROC}=3.5\%/14\%=25\%$.
\begin{align*}
\text{FCFO}_1 &= \text{EBIT}(1-\tau)(1-\text{RR})(1+g)=230\times0.65\times0.75\times1.035 = 116.05\\
V_U &= \frac{116.05}{0.085-0.035} = \mathbf{\$2{,}321.0m}
\end{align*}
**Tax benefits**: interest $=7\%\times$ debt due; tax shield $=35\%\times$ interest; **discounted at the pre-tax $k_d=7\%$**; after year 10 the shield on \$500m is a **perpetuity without growth**, valued as $TS/k_d$ and discounted back 10 years:

\small
\begin{tabular}{@{}crrrr@{}}
\toprule
Year & Debt due & Interest (7\%) & Tax shield (35\%) & PV at 7\%\\
\midrule
1 & 1,850 & 129.50 & 45.33 & 42.36\\
2 & 1,700 & 119.00 & 41.65 & 36.38\\
3 & 1,550 & 108.50 & 37.98 & 31.00\\
4 & 1,400 & 98.00 & 34.30 & 26.17\\
5 & 1,250 & 87.50 & 30.63 & 21.84\\
6 & 1,100 & 77.00 & 26.95 & 17.96\\
7 & 950 & 66.50 & 23.28 & 14.49\\
8 & 800 & 56.00 & 19.60 & 11.41\\
9 & 650 & 45.50 & 15.93 & 8.66\\
10 & 500 & 35.00 & 12.25 & 6.23\\
Perpetuity & 500 & 35.00 & 12.25 & $\frac{12.25}{0.07\times1.07^{10}}=$ 88.96\\
\midrule
\multicolumn{4}{@{}r}{**PV of tax benefits**} & **305.45**\\
\bottomrule
\end{tabular}

**(xv)** Expected bankruptcy costs are computed on the value *including* the tax benefits:
\[
BC=(V_U+TB)\times\text{BC\%}\times\pi_d=(2{,}321.0+305.45)\times30\%\times20\%=\mathbf{\$157.6m}
\]
**(xvi)** $V_L=V_U+TB-BC=2{,}321.0+305.45-157.6=\mathbf{\$2{,}468.9m}$, below the \$2.7bn price: the buyer **overpaid by about \$231m** (8.6\%), unless it expected operating improvements not in these inputs.

\footnotesize **Correction to our earlier version**: we had discounted the shields at $\rho_u=8.5\%$ with a growing terminal value (TB 313.3) and computed BC on $V_U$ only (139.3), giving $V_L=2{,}495$. The class conventions are: shields at $k_d$, final perpetuity without growth, BC on $V_U+TB$. The conclusion (overpayment) is the same.

### WACC or APV? A Practical Choice

\small
\begin{tabular}{@{}lll@{}}
\toprule
**Situation** & **Better tool** & **Why**\\
\midrule
Stable target $D/E$ or $D/(D+E)$ & WACC & Financing policy embedded in WACC\\
Known/predetermined debt schedule & APV & Tax shields can be valued directly\\
LBO/acquisition financing & APV & Debt repayment path is explicit\\
Changing leverage & APV or staged WACC & Single constant WACC misleading\\
Mature firm, stable leverage & WACC & Simpler and standard\\
Financial distress/high leverage & APV & Bankruptcy costs modelled explicitly\\
\bottomrule
\end{tabular}

% =====================================================================

## Conclusion

### Common Mistakes in WACC and APV Valuation (slide)

  - Discounting FCFO at the cost of equity.
  - Discounting FCFE at WACC.
  - Using book-value capital weights without justification.
  - Using today's leverage in WACC when the forecast assumes a different target leverage.
  - Applying a stable-growth terminal value while $\beta$, leverage, ROIC, or reinvestment assumptions are not stable.
  - Double-counting tax shields: once in WACC and again separately.
  - Treating WACC and APV as different answers rather than different implementations of financing assumptions.
  - Using APV but ignoring bankruptcy costs, mechanically making more debt always better.

### Takeaways

  - FCFO values the operating business; financing effects must be handled consistently.
  - WACC **embeds** financing effects in the discount rate.
  - APV values the unlevered business first and then **adds tax shields and subtracts expected distress costs**.
  - WACC works best with **stable target leverage ratios**.
  - APV works best with **known or changing dollar debt levels**, especially leveraged transactions.
  - WACC and APV should give similar answers **only under consistent assumptions**.
  - The main valuation errors come from mixing cash flows, discount rates, and financing-policy assumptions.

% =====================================================================

## Formula Summary Sheet

\small
\renewcommand{\arraystretch}{1.45}
\begin{longtable}{@{}p{4.8cm}p{10.2cm}@{}}
\toprule
**Concept** & **Formula**\\
\midrule
\endhead
WACC & $k_e\frac{E}{D+E}+k_d(1-\tau)\frac{D}{D+E}$ (market-value weights)\\
CAPM & $k_e=r_f+\beta_l\cdot\text{ERP}$;\quad $\rho_u=r_f+\beta_u\cdot\text{ERP}$\\
Cost of debt & $k_d=r_f+\text{default spread}$;\ after tax $k_d(1-\tau)$\\
Beta, constant $D/(D+E)$ & $\beta_l=\beta_u[1+D/E]$\\
Beta, fixed \$ debt (Hamada) & $\beta_l=\beta_u[1+(1-\tau)D/E]$\\
Stable growth value & $V_0=\text{FCFO}_1/(\text{WACC}-g_n)$\\
Two-stage value & $V_0=\sum_{t=1}^{n}\frac{\text{FCFO}_t}{(1+\text{WACC}_{hg})^t}+\frac{\text{FCFO}_{n+1}/(\text{WACC}_{st}-g_n)}{(1+\text{WACC}_{hg})^n}$\\
Stable growth & $g_n=\text{RR}\times\text{ROC}$;\quad RR $=g/\text{ROC}$\\
Reinvestment rate & $(\text{CapEx}-\text{D\&A}+\Delta\text{NWC})/\text{EBIT}(1-\tau)$\\
ROC & EBIT$(1-\tau)$/(BV equity $+$ BV debt $-$ cash)\\
FCFO from NOPAT & EBIT$(1-\tau)(1-\text{RR})$\\
NOPAT vs FCFO & EBIT$(1-\tau)=$ FCFO $+$ CapEx $-$ D\&A $+\Delta$NWC\\
EBITDA vs FCFO & EBITDA $=$ FCFO $+\tau\cdot$EBIT $+$ CapEx $+\Delta$NWC\\
No-growth firm & EV $=$ EBIT$(1-\tau)$/WACC;\quad Equity $=$ NI$/k_e$\\
APV & $V_l=V_u+TB-BC$\\
Unlevered value & $V_u=\text{FCFO}_1/(\rho_u-g_n)$ (or two-stage at $\rho_u$)\\
TB, fixed perpetual debt & $TB=\tau_C D$\\
TB, predetermined debt & $\sum_{t=1}^{n}\frac{\tau_C k_d D_t}{(1+\rho_u)^t}+\frac{\tau_C k_d D}{(\rho_u-g_n)(1+\rho_u)^n}$\\
Bankruptcy costs & $BC=\pi_d\times\text{LGD}$\\
Equity from EV & EV $-$ net debt (net debt $=$ debt $-$ cash; class convention)\\
TB, known schedule (class) & $\sum_{t}\frac{\tau k_d D_t}{(1+k_d)^t}+\frac{\tau k_d D_{\text{perp}}}{k_d(1+k_d)^{n}}$\\
BC (class) & $(V_U+TB)\times\text{BC\%}\times\pi_d$\\
\bottomrule
\end{longtable}

% =====================================================================

## Common Mistakes and Exam Traps

> **Exam traps -- Chapter 4**

  - FCFO at **WACC** gives the value of operating assets (add non-operating assets for firm value); FCFE at $k_e$ gives equity. Never mix them.
  - **Beta formula depends on debt policy**: constant leverage ratio $\Rightarrow$ $\beta_u(1+D/E)$; fixed \$ debt $\Rightarrow$ Hamada $\beta_u(1+(1-\tau)D/E)$. Constant leverage gives the *higher* levered beta (DQ I: 8.10\% vs 7.68\%).
  - WACC already contains the tax benefit (after-tax $k_d$) and the extra risk of debt (higher $k_e$, $k_d$). Do **not** add tax shields again (double counting).
  - In the stable-growth model use **FCFO$_1$** (next year), not FCFO$_0$; $g_n\leq$ growth of the economy; $g_n=$ RR $\times$ ROC.
  - In the two-stage model the terminal value uses \textbf{WACC$_{st}$} and is discounted at \textbf{WACC$_{hg}$}.
  - Sensitivity to $g$ is larger with WACC than with $k_e$, because WACC $-g$ is smaller.
  - Discounting EBITDA assumes no taxes and disinvestment (no growth, no infinite life); discounting NOPAT assumes no net reinvestment (infinite life, but no growth).
  - FCFO and FCFE equity values coincide only with **consistent leverage assumptions**, market-value weights equal to the resulting values (fair pricing), no extraordinary items, and interest $= k_d\times$ market value of debt.
  - APV: $V_l=V_u+TB-BC$; $V_u$ discounts FCFO at the **unlevered** $\rho_u$, not at WACC or $k_e$.
  - TB for fixed perpetual debt $=\tau_C D$. For predetermined/high debt the slide formula discounts the shields at $\rho_u$, but the **official J.\ Crew solution discounts them at $k_d$** (as the slide on CoC vs APV notes: ``APV often uses the pre-tax cost of debt''). If the exam gives a schedule without specifying, use $k_d$ as in class.
  - Ignoring bankruptcy costs in APV implies that 100\% debt is optimal, which is not realistic.
  - Direct bankruptcy costs are small; indirect costs may reach 25--30\% of firm value (Shapiro 1989, Titman 1984).
  - Use the **marginal** tax rate for tax shields.
  - Under the same assumptions APV $\approx$ CoC; APV is more conservative when indirect bankruptcy costs are not in $k_d$.
  - Tool choice: stable $D/E$, mature firm $\to$ WACC; known debt schedule, LBO, distress $\to$ APV; changing leverage $\to$ APV or staged WACC.
  - Market-value weights, not book values (unless justified); use target leverage, not today's, if the forecast assumes a change.
  - **Class convention (official solutions)**: leverage in $\beta$ and in the WACC weights is measured with **net debt** (debt $-$ cash) and market values; equity $=$ EV $-$ net debt (Daimler: EV 87,527, equity 41,095).
  - **J.\ Crew conventions**: tax shields of a known debt schedule discounted at the pre-tax $k_d$; residual debt as a no-growth perpetuity ($TS/k_d$); expected bankruptcy cost $=(V_U+TB)\times$ BC\% $\times\pi_d$.
  - Default probabilities rise steeply below investment grade (BBB 7.54\% $\to$ BB 16.63\% $\to$ B 36.80\% over 10 years).

