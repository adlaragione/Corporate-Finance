<!-- Markdown notes generated from the LaTeX chapter; tables and formulas kept in LaTeX syntax. The PDF is the reference version. -->
# Growth and Value

*Based on Lecture L08 (34 slides): ``Growth \& Value''. Workflow step: forecasts and cash flows $\to$ **terminal value**.*

% =====================================================================

## Estimating Growth

### Definition and Approaches

\small
\begin{tabular}{@{}lp{5.2cm}|ll@{}}
\multicolumn{2}{c|}{**Assets**} & \multicolumn{2}{c}{**Liabilities**}\\
\midrule
**Assets in place** & Existing investments: generate cash flows **today** & (Net) Debt & Borrowed money\\
**Growth opportunities** & Investments to be made: generate cash flows **tomorrow** & Equity & Owners' funds\\
\end{tabular}

Value of the firm (equity or asset side) with the DCF approach:

> **DCF with terminal value**
\[
\text{Value}_0=\sum_{t=1}^{n}\frac{\mathbb{E}[CF_t]}{(1+k_c)^t}+\frac{\text{Terminal Value}_n}{(1+k_c)^n},\qquad\text{under stable growth } \text{TV}_n=\frac{\mathbb{E}[CF_{n+1}]}{k_c-g}
\]
$CF_t$: expected cash flow (equity or asset side); $k_c$: cost of capital (equity or asset side); $g$: long-run growth of CF.

Three main approaches to estimate $g$:

  - **Historical**: based on historical growth in EPS.
  - **Analysts' estimates**: based on analysts' estimates of EPS growth.
  - **Fundamental**: based on the fundamentals of EPS growth: **reinvestment** (non-cash WC and net CapEx) and **return on investment** (the returns those projects earn).

### Historical Approach

> **Ways to measure historical growth**

  - **Arithmetic average**: \ $g_t=\frac1n\sum_{i=1}^{n}g_{t-i}=\frac1n\sum_{i=1}^{n}\frac{NI_{t-i}-NI_{t-i-1}}{NI_{t-i-1}}$
  - **Geometric average**: \ $g_t=\left[\prod_{i=1}^{n}(1+g_{t-i})\right]^{1/n}-1=\left(\frac{NI_t}{NI_{t-n}}\right)^{1/n}-1$
  - **Log-linear OLS regression**: $\ln(\text{EPS})=a+b\cdot t$; $\hat b$ is the percentage change in EPS per unit of time.
  - **Time-series models** (Box and Jenkins 1976; Foster 1977; Griffin 1977).

Historical rates are sensitive to:

  - the **estimation period** (to be chosen carefully, especially for young/high-growth firms);
  - **negative earnings**: if some EPS are negative, $\ln(\text{EPS})$ cannot be computed for the log-linear regression;
  - **earnings volatility**, high especially for young/high-growth industries. Revenue growth is more stable and more serially correlated than earnings growth, so it is a useful check;
  - **size effect**: growth is ``convex'': it falls as size increases;
  - changes in EPS not driven by earnings (e.g., stock splits).

> **Historical approach: Motorola (\$ million) -- verified**
\small
\begin{minipage}[t]{0.48\linewidth}
\begin{tabular}{@{}lrr@{}}
\toprule
Year & Revenues & \% change\\
\midrule
X & 22,245 & \\
X+1 & 27,037 & 21.54\%\\
X+2 & 27,973 & 3.46\%\\
X+3 & 29,794 & 6.51\%\\
X+4 & 29,398 & $-1.33\%$\\
X+5 & 30,931 & 5.21\%\\
\midrule
\multicolumn{2}{@{}l}{Arithmetic average} & 7.08\%\\
\multicolumn{2}{@{}l}{Geometric average} & 6.82\%\\
\multicolumn{2}{@{}l}{Standard deviation} & 8.61\%\\
\bottomrule
\end{tabular}

\medskip
\begin{tabular}{@{}lrr@{}}
\toprule
Year & EBIT & \% change\\
\midrule
X & 2,604 & \\
X+1 & 2,931 & 12.56\%\\
X+2 & 1,960 & $-33.13\%$\\
X+3 & 1,947 & $-0.66\%$\\
X+4 & 822 & $-57.78\%$\\
X+5 & 3,216 & 291.24\%\\
\midrule
\multicolumn{2}{@{}l}{Arithmetic average} & 42.45\%\\
\multicolumn{2}{@{}l}{Geometric average} & 4.31\%\\
\multicolumn{2}{@{}l}{Standard deviation} & 141.78\%\\
\bottomrule
\end{tabular}
\end{minipage}\hfill
\begin{minipage}[t]{0.48\linewidth}
\begin{tabular}{@{}lrr@{}}
\toprule
Year & EBITDA & \% change\\
\midrule
X & 4,151 & \\
X+1 & 4,850 & 16.84\%\\
X+2 & 4,268 & $-12.00\%$\\
X+3 & 4,276 & 0.19\%\\
X+4 & 3,019 & $-29.40\%$\\
X+5 & 5,398 & 78.80\%\\
\midrule
\multicolumn{2}{@{}l}{Arithmetic average} & 10.89\%\\
\multicolumn{2}{@{}l}{Geometric average} & 5.39\%\\
\multicolumn{2}{@{}l}{Standard deviation} & 41.56\%\\
\bottomrule
\end{tabular}

\medskip
\begin{tabular}{@{}lrr@{}}
\toprule
Year & EPS & \% change\\
\midrule
X & 0.88 & \\
X+1 & 0.98 & 11.36\%\\
X+2 & 0.65 & $-33.67\%$\\
X+3 & 0.66 & 1.54\%\\
X+4 & 0.14 & $-78.79\%$\\
X+5 & 0.45 & 221.43\%\\
\midrule
\multicolumn{2}{@{}l}{Arithmetic average} & 24.37\%\\
\multicolumn{2}{@{}l}{Geometric average} & $-12.55\%$\\
\multicolumn{2}{@{}l}{Standard deviation} & 115.69\%\\
\bottomrule
\end{tabular}
\end{minipage}

\medskip
**How to compute (e.g., revenues):** arithmetic $=(21.54+3.46+6.51-1.33+5.21)/5=7.08\%$; geometric $=(30{,}931/22{,}245)^{1/5}-1=1.3905^{0.2}-1=6.82\%$.

> **Lesson of the Motorola table** *(added, not on slides)*
The further down the income statement, the more volatile growth becomes (SD 8.6\% for revenues vs 141.8\% for EBIT). With volatile data the arithmetic average is badly inflated by one large rebound: EBIT +42.45\% arithmetic vs +4.31\% geometric; EPS +24.37\% arithmetic vs $-12.55\%$ geometric (EPS actually fell from 0.88 to 0.45). Use the geometric average and check against revenue growth.

### Analysts' Estimates Approach

  - Consensus growth estimates are available from online providers (e.g., I/B/E/S).
  - Analysts forecast EPS based on: (1) historical growth; (2) public information other than earnings affecting EPS growth; (3) recent firm-specific information updating the historical estimate; (4) recent market/industry information; (5) information revealed by competitors and/or private information.
  - Estimates are sensitive to: (1) the number of analysts covering the firm (increasing in market cap, institutional holdings and trading volume); (2) the extent of disagreement; (3) the independence of estimates; (4) analysts' quality.

**Analysts' five ``deadly sins''**:

  - **Tunnel vision**: too focused on the industry.
  - **``Lemmingitis''** (herding): the urge to revise when others do, in the same direction and magnitude.
  - **Stockholm syndrome**: identification with the managers.
  - **Factophobia**: relying on ``stories'' rather than facts.
  - **Dr.\ Jekyll/Mr.\ Hyde**: bringing business to investment banks.

### Fundamentals' Approach I: EPS Growth
The fundamentals' approach estimates growth as an **endogenous** variable.

> **EPS growth**
\[
g=\text{Retention ratio}\ (b)\times\text{ROE}
\]

**Proof.** Define $g=\frac{NI_t-NI_{t-1}}{NI_{t-1}}$ and $\text{ROE}_{t-1}=\frac{NI_{t-1}}{BV_{t-2}}$ (BV $=$ book value of equity). With no equity injections, $NI_t=BV_{t-1}\times\text{ROE}_t=(BV_{t-2}+\text{Retained earnings}_{t-1})\times\text{ROE}_t$. With constant ROE:
\[
NI_t-NI_{t-1}=\text{RE}_{t-1}\times\text{ROE}\ \Rightarrow\ g=\frac{\text{Retained earnings}_{t-1}}{NI_{t-1}}\times\text{ROE}=b\times\text{ROE}.\qquad\text{QED}
\]
Implicit assumptions: constant ROE; no equity issuance (so NI growth $=$ EPS growth); no other comprehensive income in book equity.

### Fundamentals' Approach II: Net Income Growth

> **NI growth with the equity reinvestment rate**
\[
\text{Equity reinvested}_t=(\text{CapEx}_t-\text{D\&A}_t)+\Delta\text{WC}_t-(\text{New debt issued}_t-\text{Debt repaid}_t)
\]
\[
b_t=\frac{\text{Equity reinvested}_t}{NI_t}\qquad\qquad g_{t+1}=b_t\times\text{ROE}
\]

Adjust all figures (R\&D, operating leases, etc.) consistently with the adjustments made to cash flows. Implicit assumptions: constant ROE; **equity issuance allowed**, so NI growth $\neq$ EPS growth; no OCI in book equity.

### Fundamentals' Approach: ROE and Leverage
Following Modigliani--Miller (with taxes):
\[
k_A=k_E\frac{E}{D+E}+k_D(1-\tau_C)\frac{D}{D+E}\iff k_E=k_A+[k_A-k_D(1-\tau_C)]\frac{D}{E}
\]

> **Accounting version**
\[
\text{ROE}=\text{ROC}+[\text{ROC}-i(1-\tau_C)]\frac{D}{E}
\]
\vspace{-6pt}
\begin{gather*}
\text{ROC}=\frac{\text{EBIT}(1-\tau_C)}{\text{BV debt}-\text{Cash}+\text{BV equity}}=\frac{\text{EBIT}(1-\tau_C)}{\text{BV net debt}+\text{BV equity}}\\
\frac{D}{E}=\frac{\text{BV net debt}}{\text{BV equity}}\qquad i=\frac{\text{Interest expenses on (net) debt}}{\text{BV of (net) debt}}
\end{gather*}

Implications: ROE depends on the returns on investments undertaken (ROC); **ROE changes with leverage** (and financial risk); the higher the cost of debt, the lower the ROE; marginal ROE differs from average ROE $\Rightarrow$ addition to expected growth $=\frac{\text{ROE}_t-\text{ROE}_{t-1}}{\text{ROE}_{t-1}}$.

> **Illustration (not on slides)**
ROC $=12\%$, $i=6\%$, $\tau=25\%$, $D/E=0.5$: ROE $=12\%+(12\%-4.5\%)\times0.5=15.75\%$. With $D/E=1$: 19.5\%. Leverage raises ROE as long as ROC $>$ after-tax cost of debt (but it also raises risk).

### Fundamentals' Approach: Growth in Operating Income (EBIT)
**1. Stable ROC scenario**

> **Key point**
\begin{gather*}
g=b\times\text{ROC}\\
b=\text{Reinvestment rate}=\frac{(\text{CapEx}_t-\text{D\&A}_t)+\Delta\text{WC}_t}{\text{EBIT}_t(1-\tau_C)}\\ \text{ROC}=\frac{\text{EBIT}_t(1-\tau_C)}{\text{BV equity}+\text{BV debt}-\text{Cash}}
\end{gather*}

Implicit assumptions: constant ROC and EBIT margins; $b$ from recent statements is forward-looking; accounting ROC is a good measure of required returns on assets (check against the industry average); no OCI in book equity.

**2. Positive and changing ROC scenario**
\[
g=b\times\text{ROC}+\Delta\%\text{ROC},\qquad \Delta\%\text{ROC}=\frac{\text{ROC}_t-\text{ROC}_{t-1}}{\text{ROC}_{t-1}}
\]

> **Illustration (not on slides)**
RR $=40\%$, new ROC $=15\%$; ROC on existing assets rises from 12\% to 13\%: $g=0.40\times15\%+(13\%-12\%)/12\%=6\%+8.33\%=14.33\%$ (the improvement on existing assets adds growth for one year only).

**3. Negative ROC / changing margins scenario**

  - Estimate revenue growth over time: use historical revenue growth for the near future; decrease the rate as the firm becomes larger (convexity); keep track of absolute revenues to make sure growth is feasible.
  - Estimate expected operating margins every year: set a target margin, move the current margin towards it, use the target in perpetuity.
  - Estimate the capital to be invested to generate the expected revenue growth/margins via the **sales-to-capital ratio**: \ Investment needs $=$ Revenue growth / Sales-to-capital ratio.
  - Check that the implied ROC is consistent with sustainable long-run growth in the industry/economy.

### Estimating Growth: Recap

\small
\setlength{\tabcolsep}{4pt}\begin{tabular}{@{}llll@{}}
\toprule
& **General** & **Stable growth** & **Reinvestment in stable growth**\\
\midrule
Dividend approach & $g=b\cdot\text{ROE}+\Delta\%\text{ROE}$ & $g=b\cdot\text{ROE}$ & $b=g/\text{ROE}$\\
FCFE approach & $g=\text{ERR}\cdot\text{ROE}+\Delta\%\text{ROE}$ & $g=\text{ERR}\cdot\text{ROE}$ & ERR $=g/\text{ROE}$\\
FCFF approach & $g=\text{RR}\cdot\text{ROC}+\Delta\%\text{ROC}$ & $g=\text{RR}\cdot\text{ROC}$ & RR $=g/\text{ROC}$\\
\bottomrule
\end{tabular}

In stable growth, firms must reinvest to deliver the forecast growth ($\Delta\%$ROE and $\Delta\%$ROC go to zero), and the reinvestment rate is a function of growth and return.

> **Key point**
$\Longrightarrow$ Need to estimate **both** $g$ and ROE/ROC: **assumptions' consistency is key**.

% =====================================================================

## Terminal Value

### Explicit Projections

  - Any asset's value is a function of (1) the **cash flows** it can generate and (2) their **time distribution**.
  - The time horizon of the projections should: show CF dynamics linked to corporate financial restructuring; show CF dynamics linked to extraordinary investment cycles; analyse growth phases due to competitive imbalances; describe performance in cyclical industries.
  - When the project's duration is tied to irreplaceable resources, renewals or concessions, the horizon can correspond to (i) the **exhaustion** of the resources or (ii) the **maturity** of the concession contracts.
  - International practice: explicit period of **7--10 years** in low-capital-intensive sectors; up to **10--15 years** in industries whose assets have long economic/technical lives (hydroelectric, petrochemical, \dots).
  - Analysts usually begin with a business plan of **3--5 years**, extended as necessary. The extension must fulfil a **double requirement**: (1) cover the entire business cycle; (2) the share of value from the explicit CFs should be reasonable relative to the discounted TV (this share varies by business area).

### Cash-Flow Valuation and the Two Meanings of TV
A firm potentially has an infinite life, so its value is the PV of CF forever ($n\to\infty$). Since we cannot estimate FCF forever, we estimate them explicitly for a ``growth period'' and add a TV:
\[
V_t=\sum_{s=t+1}^{n}\frac{\mathbb{E}_t[\text{FCF}_s]}{(1+k_C)^{s-t}}+\frac{\text{TV}_n}{(1+k_C)^n}
\]
The TV can mean:

  - the **breakup value** (liquidation value): for firms operating with contracts or concessions with a low possibility of renewal; the value realized by breaking up the assets and selling them separately;
  - the **equilibrium value**: the common case, since the time horizon of a business cannot be defined in advance; the value of ``equilibrium'' for the firm's overall operations.

### Estimation Approaches

\small
\begin{tabular}{@{}p{4.3cm}p{4.3cm}p{5.6cm}@{}}
\toprule
**Breakup value** & **Multiple approach** & **Stable growth model**\\
\midrule
Most useful when assets are separable and marketable & Easiest approach, but makes the valuation a **relative** valuation & Technically soundest, but requires judgments about when the firm will grow at a stable rate it can sustain forever, and the excess returns (if any) it will earn\\
\bottomrule
\end{tabular}

\subsubsection*{Liquidation value approach}
The firm ceases operations and sells its assets to the highest bidder; the estimated assets value is the **liquidation value**.

  - **Book-value approach**: BV of assets at the end of the estimation period, adjusted for inflation ($\pi$) over the average age of the assets ($s$):
  \[
  \text{Expected liquidation value}_t=\text{BV of assets}_t\cdot(1+\pi)^s
  \]
  Subtract the estimated debt to get equity. Limitation: based on accounting BV, not on earnings power.
  - **Earnings-power approach**: PV at rate $r$ of the expected CF from the assets over their remaining useful life $j$:
  \[
  \text{Expected liquidation value}_t=CF\cdot a_{\overline{j}|r}=CF\cdot\frac{1-(1+r)^{-j}}{r}
  \]
  Subtract debt. Limitation: it is a growth model with zero growth.

> **Illustration (not on slides)**
BV of assets 500, inflation 2\%, average age 5 years: liquidation value $=500\times1.02^5=552$. Earnings power: CF 80 for 6 remaining years at 9\%: $80\times\frac{1-1.09^{-6}}{0.09}=80\times4.486=358.9$.

\subsubsection*{Multiples approach}
Value in a future year $=$ multiple $\times$ earnings or revenues in that year; e.g., asset side: $\text{TV}_n=\text{Revenue}_n\cdot(\text{EV}/\text{Sales})_n$; subtract debt for equity, or use equity multiples (P/E).

  - Simple, but obtaining the right multiple is crucial: from **comparables** it becomes a **relative** valuation, not DCF; from **fundamentals** it converges to the stable growth model.
  - Using comparables' multiples for the TV is a **dangerous mix of relative and DCF valuation**: a DCF should give intrinsic value, not relative value.

> **Key point**
The only consistent ways of estimating the TV in a DCF valuation: (i) a **liquidation value** or (ii) a **stable growth model**.

\subsubsection*{Stable growth model}
Unlike liquidation value (finite life), the stable growth model assumes the firm **reinvests** CF into new assets (firm value $=$ assets in place $+$ future assets).

  - **Two-stage model**: beyond year $n$, FCF grow at a constant $g$ forever (Gordon growth from $n+1$):
  \[
  V_t=\sum_{s=t+1}^{n}\frac{\mathbb{E}_t[\text{FCF}_s]}{(1+k_C)^{s-t}}+\frac{\mathbb{E}_t[\text{FCF}_{n+1}]}{(k_C-g)(1+k_C)^n}
  \]
  Equity side: $\text{TV}_n=\frac{\mathbb{E}[\text{FCFE}_{n+1}]}{k_{e,n+1}-g}$ or $\frac{\mathbb{E}[\text{Dividends}_{n+1}]}{k_{e,n+1}-g}$; asset side: $\text{TV}_n=\frac{\mathbb{E}[\text{FCFO}_{n+1}]}{\text{WACC}_{n+1}-g}$.
  - **Three-stage model**: after the explicit period, (i) high growth, (ii) a transition of converging growth, (iii) constant growth forever.
  - **N-stage model**: the growth rate changes every year until the final period.

% =====================================================================

## Stable Growth Rate

### Three Key Assumptions

  - **Length of the high-growth period**
  
    - **Longevity**: a matter of when, not whether: either the firm becomes stable/large or it is liquidated.
    - **Firm size**: smaller firms are more likely to earn excess returns than similar larger firms.
    - **Ability to earn excess returns**: growth depends on investing in new projects whose marginal return exceeds the cost of capital.
    - **Competitive advantages**: the bigger and more sustainable (barriers to entry, management quality), the longer the excess returns.
  
  - **Characteristics of stable-growth firms**
  
    - **Equity risk**: lower $\beta$ than high-growth firms (e.g., Fama--French).
    - **Project returns**: excess returns decline when reaching stable growth.
    - **Debt ratios**: stable firms use **more debt**, since debt capacity increases as firms mature ($\to$ cost of capital).
  
  - **The transition to stable growth**: two-stage (abrupt), three-stage (gradual transition), N-stage (characteristics change each year).

### Which Scenario to Choose

\begin{tabular}{@{}ll@{}}
\toprule
**Model** & **Best for**\\
\midrule
Two-stage & Firms with **moderate** growth rates, where the shift will not be too dramatic\\
Three-stage & Firms with **very high** growth rates in operating income\\
N-stage & **Very young** firms or firms with **negative operating margins**\\
\bottomrule
\end{tabular}

### Qualitative Aspects
Growth is also determined by qualitative factors (quality of management, marketing strength, capacity to form partnerships, strategic vision, \dots). **They matter, but they must ultimately show up in one or more of the quantitative inputs**:

  - **Quality of management** affects (i) the ROC on new investments and (ii) how long it is sustained $\Rightarrow$ one reason why ROC can stay above the cost of capital.
  - **Marketing strength** affects operating margins and turnover ratios $\Rightarrow$ typically a trade-off between lower margins and higher turnover; consider its implications for value.
  - **Partnerships** (acquisitions, R\&D, \dots) affect the projected ROC.
  - **Strategic vision** shapes (and is shaped by) competition; it determines the size of excess returns (ROC $-$ CoC) and how quickly they fade to zero.

Otherwise, remain skeptical about whether these factors truly affect value. Why impose this structure? One of the biggest dangers in valuing tech firms is using **story-telling** to justify growth rates that are neither **reasonable** nor **sustainable**: ``Tesla will grow 100\% a year because the green movement is strong''; ``Coca-Cola will grow 20\% a year because it has a great brand''. There is a kernel of truth, but: to what extent do the stories translate into the model? Do they support higher growth than competitors? An analyst who knows the firms better $\Rightarrow$ more precise growth estimates, but this does **not** imply better returns from investing in them.

### Main Constraints

  - The stable growth rate **cannot exceed the growth rate of the economy**, but it can be lower; it can even be negative (the TV is then lower and you assume the firm will ``disappear'' over time).
  - In the long term, the real risk-free rate converges to the real growth rate of the economy, and the nominal risk-free rate to the nominal growth rate.
  - $\text{Nominal } R_f=\text{Real } R_f+\mathbb{E}[\pi]$. **Rule of thumb: the stable growth rate should not exceed the riskless rate used.**
  - **Nominal vs real consistency** (nominal CF and discount rates with nominal growth) and **currency consistency** (growth in the currency of the valuation).

### Reinvestment Rate

  - Linking the reinvestment rate (and retention ratio) to the stable growth rate makes the valuation **less sensitive** to assumptions about $g$.
  - Increasing $g$ (all else constant) increases value directly, but the higher reinvestment rate needed reduces cash flows: the gain is partially or completely offset.
  - Whether value rises depends on **excess returns** in stable growth: \ ROC $>k_C\Rightarrow$ higher $g$ increases value; \ ROC $=k_C\Rightarrow$ higher $g$ has **no effect** on value (and ROC $<k_C\Rightarrow$ growth destroys value).

> **TV for a firm with after-tax operating income of \$100m in year $n+1$ and a cost of capital of 10\% -- verified**
\[
\text{TV}=\frac{\text{EBIT}_{n+1}(1-\tau)\times(1-g/\text{ROC})}{k_C-g}=\frac{100\times(1-g/\text{ROC})}{0.10-g}
\]

\small
\begin{tabular}{@{}c|rrrrr@{}}
\toprule
& \multicolumn{5}{c}{**ROC in perpetuity**}\\
**$g$ forever** & 6\% & 8\% & 10\% & 12\% & 14\%\\
\midrule
0.0\% & 1,000 & 1,000 & 1,000 & 1,000 & 1,000\\
0.5\% & 965 & 987 & 1,000 & 1,009 & 1,015\\
1.0\% & 926 & 972 & 1,000 & 1,019 & 1,032\\
1.5\% & 882 & 956 & \fcolorbox{navy}{boxblue}{1,000} & 1,029 & 1,050\\
2.0\% & 833 & 938 & 1,000 & 1,042 & 1,071\\
2.5\% & 778 & 917 & 1,000 & 1,056 & 1,095\\
3.0\% & 714 & 893 & 1,000 & 1,071 & 1,122\\
\bottomrule
\end{tabular}

Example cell ($g=3\%$, ROC $=6\%$): RR $=3/6=50\%$, FCF $=100\times0.5=50$, TV $=50/0.07=714$. Cell ($g=3\%$, ROC $=14\%$): RR $=21.4\%$, FCF $=78.6$, TV $=78.6/0.07=1{,}122$.

**Proof that growth is irrelevant when ROC $=k_C$.**
\begin{align*}
\text{TV}_n=\frac{\mathbb{E}_t[\text{FCF}_{n+1}]}{k_C-g}&=\frac{\mathbb{E}_t[\text{EBIT}_{n+1}(1-\tau_C)-\text{Net CapEx}_{n+1}-\Delta\text{WC}_{n+1}]}{k_C-g}\\
&=\frac{\mathbb{E}_t[\text{EBIT}_{n+1}(1-\tau_C)(1-\text{RR})]}{k_C-g}\\
&=\frac{\mathbb{E}_t[\text{EBIT}_{n+1}(1-\tau_C)(1-\text{RR})]}{k_C-\text{RR}\cdot\text{ROC}}
\end{align*}
If $k_C=$ ROC:
\[
\text{TV}_n=\frac{\text{EBIT}_{n+1}(1-\tau_C)(1-\text{RR})}{k_C-\text{RR}\cdot k_C}=\frac{\text{EBIT}_{n+1}(1-\tau_C)(1-\text{RR})}{k_C(1-\text{RR})}=\frac{\text{EBIT}_{n+1}(1-\tau_C)}{k_C}
\]
Similar arguments apply to the DDM and FCFE.

% =====================================================================

## Takeaways

  - Assumptions of the constant-growth perpetuity model: positive cash flow next period; constant discount rate (implies constant capital-structure ratios); constant growth rate lower than the discount rate.
  - Reasonable range of perpetual growth: positive but sustainable (long-run inflation, growth of the economy in inflation and real terms, productivity gains); it can be negative (falling margins from price pressure, higher costs or loss of competitive advantage).
  - Assess reasonableness of growth: basic financial analysis of underlying assumptions; growth rates of comparables (analysts or FCF forecasts); implied market multiples vs current multiples of comparables; how current multiples will evolve up to the continuing-value date.

% =====================================================================

## Formula Summary Sheet

\small
\renewcommand{\arraystretch}{1.45}
\begin{longtable}{@{}p{4.8cm}p{10.2cm}@{}}
\toprule
**Concept** & **Formula**\\
\midrule
\endhead
DCF + TV & $V_0=\sum_{t=1}^n\frac{CF_t}{(1+k)^t}+\frac{\text{TV}_n}{(1+k)^n}$;\ $\text{TV}_n=\frac{CF_{n+1}}{k-g}$\\
Arithmetic growth & $\frac1n\sum g_{t-i}$\\
Geometric growth & $(X_t/X_{t-n})^{1/n}-1$\\
Log-linear & $\ln\text{EPS}=a+bt$, growth $=\hat b$\\
EPS growth & $g=b\times\text{ROE}$, $b=1-$ payout\\
Equity reinvested & (CapEx $-$ D\&A) $+\Delta$WC $-$ (new debt $-$ repaid)\\
NI growth & $g=\frac{\text{Equity reinvested}}{NI}\times\text{ROE}$\\
ROE and leverage & $\text{ROE}=\text{ROC}+[\text{ROC}-i(1-\tau)]\,D/E$\\
MM cost of equity & $k_E=k_A+[k_A-k_D(1-\tau)]\,D/E$\\
ROC & EBIT$(1-\tau)$/(BV equity $+$ BV debt $-$ cash)\\
Reinvestment rate & (CapEx $-$ D\&A $+\Delta$WC)/EBIT$(1-\tau)$\\
EBIT growth & $g=\text{RR}\times\text{ROC}\ (+\Delta\%\text{ROC})$\\
Sales-to-capital & Investment needs $=\Delta$Revenue / (Sales/Capital)\\
Stable growth reinvestment & $b=g/\text{ROE}$;\ RR $=g/\text{ROC}$\\
Liquidation value (BV) & BV assets $\times(1+\pi)^s$\\
Liquidation value (earnings) & $CF\times\frac{1-(1+r)^{-j}}{r}$\\
TV with multiple & Revenue$_n\times$(EV/Sales)$_n$\\
TV from fundamentals & $\frac{\text{EBIT}_{n+1}(1-\tau)(1-g/\text{ROC})}{k_C-g}$\\
TV if ROC $=k_C$ & $\text{EBIT}_{n+1}(1-\tau)/k_C$\\
Nominal rate & Nominal $R_f=$ Real $R_f+\mathbb{E}[\pi]$;\ $g\leq R_f$\\
\bottomrule
\end{longtable}

## Common Mistakes and Exam Traps

> **Exam traps -- Chapter 8**

  - Three approaches to growth: historical, analysts, fundamentals. Fundamentals: growth $=$ reinvestment $\times$ return.
  - Geometric average $\leq$ arithmetic; with volatile data the arithmetic average is misleading (Motorola EPS: $+24.37\%$ arithmetic vs $-12.55\%$ geometric).
  - The log-linear regression cannot be used with negative EPS.
  - Revenue growth is more stable and more serially correlated than earnings growth.
  - $g=b\times\text{ROE}$ assumes constant ROE and **no** equity issuance (NI growth $=$ EPS growth). With the equity reinvestment rate, issuance is allowed and NI growth $\neq$ EPS growth.
  - Equity reinvested **subtracts** net debt issued.
  - ROE $=$ ROC $+$ [ROC $-i(1-\tau)$] $D/E$: leverage raises ROE only if ROC $>$ after-tax cost of debt.
  - Changing ROC adds $\Delta\%$ROC to growth; in stable growth $\Delta\%$ROC $\to0$.
  - Match pairs: dividends $\leftrightarrow$ retention ratio $\times$ ROE; FCFE $\leftrightarrow$ equity reinvestment rate $\times$ ROE; FCFF $\leftrightarrow$ reinvestment rate $\times$ ROC.
  - Explicit period: 7--10 years (low capital intensity), 10--15 (long-lived assets); start from a 3--5 year plan; must cover the whole business cycle.
  - TV via comparables' multiples turns DCF into relative valuation. The only consistent DCF TVs: liquidation value or stable growth.
  - Liquidation value (earnings power) implies zero growth; liquidation value (BV) ignores earnings power.
  - Two-stage for moderate growth; three-stage for very high growth; N-stage for young firms or negative margins.
  - Stable firms: lower $\beta$, lower excess returns, **higher** debt ratios.
  - Stable $g\leq$ growth of the economy and $\leq$ the risk-free rate; $g$ can be negative.
  - If ROC $=k_C$, growth adds no value: TV $=$ EBIT$(1-\tau)/k_C$ whatever $g$. If ROC $<k_C$, growth destroys value (TV table, ROC $=6\%$).
  - Qualitative factors (management, marketing, partnerships, vision) count only through quantitative inputs (ROC, margins, turnover, duration of excess returns).
  - Analysts' five sins: tunnel vision, lemmingitis, Stockholm syndrome, factophobia, Dr.\ Jekyll/Mr.\ Hyde.

