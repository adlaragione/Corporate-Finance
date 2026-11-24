<!-- Markdown notes generated from the LaTeX chapter; tables and formulas kept in LaTeX syntax. The PDF is the reference version. -->
# Dividend Discount Models (DDM)

\emph{Based on Lecture L09 (21 slides): ``Dividend Discount Models (DDM)'', 14--15 October 2026, and on the official solution file \texttt{20127\_DQ\_6\_SOL.xlsx} (sheets 6.1--6.5 solve the slide examples; Ex\_1 and Ex\_2 are two additional exercises). Workflow step: equity valuation.}

## Plan for the Day
**Last time**: estimating future growth of earnings and cash flows; the relationship between growth and TV (Chapter~\ref{ch:growth}).\\
**Today**: how to implement a DDM valuation; the impact of different growth scenarios on a DDM valuation.\\
**Agenda**: (1) DDM: Gordon growth model, two-stage, three-stage, buybacks and payout ratio; (2) the value of growth; (3) ABN example (two-stage DDM); (4) takeaways.

% =====================================================================

## Dividend Discount Models

> **General DDM**
**The DDM is the simplest (and most intuitive) model for valuing equity**: the value of a stock is the PV of its expected dividends.
\[
\text{EqV}_t=\sum_{t=1}^{\infty}\frac{\mathbb{E}(\text{DPS}_t)}{(1+K_e)^t}
\]
EqV$_t$: equity value per share; $\mathbb{E}(\text{DPS})_t$: expected dividend per share; $K_e$: cost of equity.

  - When an investor buys a stock, s/he expects two types of cash flows: **dividends** during the holding period and the **price** at the end of the holding period.
  - Three versions: the **Gordon growth model**, the **two-stage DDM**, the **three-stage DDM**.

> **Key point**
**The choice of the model depends on the growth expectation for the firm.**

> **Why a finite holding period gives the same value** *(added, not on slides)*
The end-of-period price is itself the PV of the dividends after that date: $P_n=\sum_{t>n}\mathbb{E}(\text{DPS}_t)/(1+K_e)^{t-n}$. Substituting it back gives the infinite sum, so the value does not depend on the holding period.

% =====================================================================

## The Gordon Growth Model

> **Gordon growth model**
For **steady-state** firms with DPS growing at a constant rate forever:
\[
\text{EqV}_t=\frac{\mathbb{E}(\text{DPS}_{t+1})}{K_e-g}
\]
**Stable growth rate**: $g=\text{Retention ratio }(b)\cdot\text{ROE}$; growth of DPS $=$ growth of EPS (constant $b$).

  - **Limitations**: extremely (exponentially) sensitive to assumptions about $g$.
  - **Works best for**: firms growing at a rate $\leq$ the nominal growth rate of the economy (otherwise they would not be in steady state yet); firms with well-established payout policies they intend to continue.

### Implied Cost of Equity and P/E

> **$K_e$ from the Gordon model**
\[
\text{EqV}_t=\frac{\mathbb{E}(\text{DPS}_{t+1})}{K_e-g}\ \rightarrow\ K_e=\frac{\mathbb{E}(\text{DPS}_{t+1})}{\text{EqV}_t}+g=\frac{\text{DPS}_t(1+g)}{\text{Price per share}_t}+g
\]
Substituting DPS $=$ EPS $\cdot$ Payout and dividing by EPS:
\[
K_e=\frac{\text{EPS}_t\cdot\text{Payout}\,(1+g)}{\text{Price per share}_t}+g=\frac{\text{Payout}(1+g)}{P_t/\text{EPS}_t}+g
\]

  - $P_t/\text{EPS}_t$ is the firm's **P/E** on the profits of the last available period.
  - The main difference between DDM and P/E: the DDM is based on the growth of **DPS**, the P/E on the growth of **EPS**. If $g$ is estimated from historical earnings or dividends, major differences may arise.

> **The P/E implied by the Gordon model** *(added, not on slides)*
Rearranging: $\dfrac{P_t}{\text{EPS}_t}=\dfrac{\text{Payout}\,(1+g)}{K_e-g}$. The P/E rises with the payout and $g$ and falls with $K_e$. Example: payout 64\%, $g=3.5\%$, $K_e=7.5\%$ $\Rightarrow$ P/E $=0.64\times1.035/0.04=16.6\times$. Check with the example below: $57.44/3.47=16.55\times$.

### When to Use It, and Its Assumptions
The Gordon model is useful when:

  - the business model and industry are such that cash flows will grow constantly in the **long term** (at least 20--30 years);
  - the industry grows in line with the whole economy (e.g., **utilities, banks**, \dots);
  - otherwise, it is better to use models based on **limited** growth assumptions.

> **Assumptions of the Gordon model (and of every DDM)**
The **risk-adjusted discount rate**, the **growth rate** and the **payout ratio** are **constant** in the long term.

### Example (slide) -- Official Solution, Sheet 6.1

> **Gordon growth model -- confirmed by the official Excel**
During the last fiscal year a firm reported EPS of \$3.47 and DPS of \$2.22. $R_F=3.5\%$; $\beta=0.8$ (industry average); ERP $=5\%$; $g=R_F$; ROE $=9.8\%$.
\begin{align*}
\text{Cost of equity:}\quad K_e&=R_f+\beta\cdot\text{ERP}=0.035+0.8\times0.05=\mathbf{7.5\%}\\
\text{Value per share:}\quad \text{EqV}_t&=\frac{\mathbb{E}(\text{DPS}_{t+1})}{K_e-g}=\frac{2.22\times1.035}{0.075-0.035}\\&=\frac{2.2977}{0.04}=\mathbf{\$57.44}\\
\text{Payout}&=2.22/3.47=63.98\%\\ \text{Retention rate}\ RR&=1-\frac{2.22}{3.47}=\mathbf{36.0\%}\\
\text{Fundamental growth:}\quad \mathbb{E}(g)&=RR\cdot\text{ROE}=0.36\times0.098\\&=\mathbf{3.53\%}\approx3.5\%
\end{align*}
Official comment: ``very close to the estimated growth rate'': the assumed $g=3.5\%$ is consistent with the firm's fundamentals.

### Additional Exercise Ex\_1 (Official Excel): Sensitivity to $g$

> **Ex\_1 -- Gordon growth model and its sensitivity**
$\text{DPS}_t=2$, $K_e=15\%$, $g=5\%$: \ $\text{DPS}_{t+1}=2\times1.05=2.10$; \ $\text{EqV}=2.10/(0.15-0.05)=\mathbf{21.00}$.

\small
\begin{tabular}{@{}cr@{\hspace{1cm}}cr@{\hspace{1cm}}cr@{}}
\toprule
$g$ & EqV & $g$ & EqV & $g$ & EqV\\
\midrule
0\% & 13.33 & 6\% & 23.56 & 12\% & 74.67\\
1\% & 14.43 & 7\% & 26.75 & 13\% & 113.00\\
2\% & 15.69 & 8\% & 30.86 & 14\% & 228.00\\
3\% & 17.17 & 9\% & 36.33 & 14.99\% & 22{,}998\\
4\% & 18.91 & 10\% & 44.00 & & \\
5\% & **21.00** & 11\% & 55.50 & & \\
\bottomrule
\end{tabular}

EqV $=2(1+g)/(0.15-g)$. As $g\to K_e$ the value explodes (22,998 at $g=14.99\%$): this is the ``extremely (exponentially) sensitive to $g$'' limitation.

[Figure: redrawn diagram, see PDF]

% =====================================================================

## The Two-Stage DDM

> **Two-stage DDM**
Two periods of growth: (i) an initial phase where $g$ is **not** stable; (ii) a subsequent steady state:
\[
\text{EqV}_0=\sum_{t=1}^{n}\frac{\mathbb{E}(\text{DPS}_t)}{(1+K_{e,hg})^t}+\frac{\mathbb{E}(P_n)}{(1+K_{e,hg})^n}=\sum_{t=1}^{n}\frac{\mathbb{E}(\text{DPS}_t)}{(1+K_{e,hg})^t}+\frac{\mathbb{E}(\text{DPS}_{n+1})}{(K_{e,st}-g_n)(1+K_{e,hg})^n}
\]
$K_e$: cost of equity ($hg$ high growth, $st$ stable growth); $\mathbb{E}(P_n)$: expected price at the end of $n$ (terminal value); $g$: growth in the first $n$ periods; $g_n$: stable growth.\\[4pt]
**If $g$ and the payout in the first stage are constant** (growing annuity):
\[
\text{EqV}_0=\frac{\text{DPS}_0(1+g)\left[1-\dfrac{(1+g)^n}{(1+K_{e,hg})^n}\right]}{K_{e,hg}-g}+\frac{\mathbb{E}(\text{DPS}_{n+1})}{(K_{e,st}-g_n)(1+K_{e,hg})^n}
\]

  - **Stable growth rate**: $g=RR\cdot\text{ROE}=(1-\text{Payout})\cdot\text{ROE}$. The payout should be consistent with $g$: **stable firms have higher payouts**, all else equal. Long-run ROE should be consistent with industry perspectives.
  - **Cost of equity**: adjust $K_e$ in the different phases (adjustments to $\beta$ and capital structure).
  - **Limitations**: difficult to estimate the length of the first stage; the shift to stable growth is sudden (it should be progressive); the focus on dividends can skew the value of non-dividend-paying firms (or firms not paying out what they could).
  - **Works best for**: firms with a competitive advantage for a finite period (barriers to entry, patents, \dots); firms with modest growth in the initial phase; firms committed/able to pay out their residual cash.

### Additional Exercise Ex\_2 (Official Excel): Two-Stage DDM

> **Ex\_2, case A -- growth path changing every year**
$\text{DPS}_0=1.20$; $K_e=12.5\%$ in years 1--10; after year 10: $g=2\%$, $K_e=10\%$. The TV is discounted at the high-growth $K_e$ (12.5\%).

\scriptsize
\setlength{\tabcolsep}{3pt}
\begin{tabular}{@{}lrrrrrrrrrrr@{}}
\toprule
Year & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 & 9 & 10 & TV\\
\midrule
$g$ & 5\% & 6\% & 8\% & 10\% & 9\% & 7\% & 5.5\% & 4\% & 3\% & 2.5\% & 2\%\\
DPS & 1.2600 & 1.3356 & 1.4424 & 1.5867 & 1.7295 & 1.8506 & 1.9523 & 2.0304 & 2.0913 & 2.1436 & 2.1865\\
$K_e$ & 12.5\% & 12.5\% & 12.5\% & 12.5\% & 12.5\% & 12.5\% & 12.5\% & 12.5\% & 12.5\% & 12.5\% & 10\%\\
PV & 1.1200 & 1.0553 & 1.0131 & 0.9906 & 0.9597 & 0.9128 & 0.8560 & 0.7914 & 0.7245 & 0.6601 & 8.4166\\
\bottomrule
\end{tabular}

\[
\text{TV}_{10}=\frac{2.1865}{0.10-0.02}=27.33\qquad \text{PV(TV)}=\frac{27.33}{1.125^{10}}=8.4166\qquad **EqV**=\sum\text{PV}=\mathbf{17.50}
\]

> **Ex\_2, case B -- constant 5\% growth for 10 years (check with the growing annuity)**
DPS grows 5\% per year: 1.26, 1.3230, 1.3892, 1.4586, 1.5315, 1.6081, 1.6885, 1.7729, 1.8616, 1.9547; $\text{DPS}_{11}=1.9547\times1.02=1.9938$.\\
PV of dividends year by year: 1.1200, 1.0453, 0.9756, 0.9106, 0.8499, 0.7932, 0.7404, 0.6910, 0.6449, 0.6019 (sum $=8.3729$).
\begin{align*}
\text{Growing annuity}&=\frac{1.20\times1.05\times\left[1-\frac{1.05^{10}}{1.125^{10}}\right]}{0.125-0.05}=\frac{1.26\times(1-0.5017)}{0.075}=\mathbf{8.3729}\\
\text{PV(TV)}&=\frac{1.9938/(0.10-0.02)}{1.125^{10}}=\frac{24.92}{3.2473}=\mathbf{7.6747}\\
**EqV**&=8.3729+7.6747=\mathbf{16.05}\quad(\text{same as the year-by-year sum: ``Ok''})
\end{align*}

% =====================================================================

## The Three-Stage DDM

> **Three-stage DDM**
Three periods: (i) high $g$; (ii) declining $g$ (transition); (iii) final stable $g$:
\[
\text{EqV}_0=\sum_{t=1}^{n_1}\frac{\text{EPS}_0(1+g_a)^t\cdot\Pi_a}{(1+K_{e,hg})^t}+\sum_{t=n_1+1}^{n_2}\frac{\mathbb{E}(\text{DPS}_t)}{(1+K_{e,tr})^t}+\underbrace{\frac{\mathbb{E}(\text{EPS}_{n_2})(1+g_n)\Pi_n}{(K_{e,st}-g_n)(1+K_{e,tr})^{n_2}}}_{\text{Terminal value}}
\]
$g_a$: growth in the first $n_1$ periods; $g_n$: stable growth; $\Pi_a$, $\Pi_n$: payout in high and stable growth; $n_2-n_1$: periods in transition; $K_e$: $hg$ high growth, $tr$ transition, $st$ stable.

  - **Stable growth rate**: $g=RR\cdot\text{ROE}=(1-\text{Payout})\cdot\text{ROE}$; payout consistent with $g$; long-run ROE consistent with the industry.
  - **Cost of equity**: adjust $K_e$ across phases.
  - **Limitations**: requires more inputs; focus on dividends can skew the value of firms not paying out what they could.
  - **Works best for**: firms changing growth and other dimensions (payout, risk, \dots) over time; firms whose competitive advantage is expected to decline gradually after a period; firms committed/able to pay out residual cash.

### Example (slide) -- Official Solution, Sheet 6.2-3

> **Three-stage DDM -- confirmed by the official Excel**
Last fiscal year: EPS \$3.56 (\$3.5535 unrounded in the Excel), DPS \$2.26; $K_e=8.45\%$. The firm reinvests 36.4\% of its earnings at ROE $=25\%$.\\
\textcolor{keyred}{**Slide typo**}: the slide says ``reinvest 36.5\%''; the number used everywhere (payout $1-0.364$, $g=9.10\%$) is **36.4\%**: $g=0.364\times0.25=\mathbf{9.10\%}$.

**Stage 1 (years 1--5)**: EPS grows at 9.10\%; payout $=1-0.364=63.6\%$; $K_e=8.45\%$.

\small
\begin{tabular}{@{}lrrrrr@{}}
\toprule
Year & 1 & 2 & 3 & 4 & 5\\
\midrule
EPS & 3.88 & 4.23 & 4.61 & 5.03 & 5.49\\
Payout & 63.6\% & 63.6\% & 63.6\% & 63.6\% & 63.6\%\\
DPS & 2.47 & 2.69 & 2.93 & 3.20 & 3.49\\
$(1.0845)^t$ & 1.0845 & 1.1761 & 1.2755 & 1.3833 & 1.5002\\
PV of DPS & 2.27 & 2.29 & 2.30 & 2.31 & 2.33\\
\bottomrule
\end{tabular}

**Stable phase** (after year 10): $g=3\%$, ROE $=15\%$, $K_e=9\%$ $\Rightarrow$ \textbf{Payout $=1-g/\text{ROE}=1-0.03/0.15=80\%$}.\\
**Stage 2 (years 6--10)**: each figure moves **linearly** from its stage-1 value to its stable value (step $=\frac{\text{target}-\text{start}}{5}$): $g$ falls by $(9.10\%-3\%)/5=1.22\%$ per year; payout rises by $(80\%-63.6\%)/5=3.28\%$; $K_e$ rises by $(9\%-8.45\%)/5=0.11\%$.

\small
\begin{tabular}{@{}lrrrrr@{}}
\toprule
Year & 6 & 7 & 8 & 9 & 10\\
\midrule
Expected $g$ & 7.88\% & 6.66\% & 5.44\% & 4.22\% & 3.00\%\\
EPS & 5.93 & 6.32 & 6.66 & 6.95 & 7.15\\
Payout & 66.88\% & 70.16\% & 73.44\% & 76.72\% & 80.00\%\\
DPS & 3.96 & 4.43 & 4.89 & 5.33 & 5.72\\
$K_e$ & 8.56\% & 8.67\% & 8.78\% & 8.89\% & 9.00\%\\
Cumulative $K_e$ & 1.6286 & 1.7698 & 1.9252 & 2.0964 & 2.2850\\
PV of DPS & 2.43 & 2.51 & 2.54 & 2.54 & 2.50\\
\bottomrule
\end{tabular}

**Cumulative discount factor** (changing $K_e$): e.g., year 7: $(1.0845)^5\times1.0856\times1.0867=1.7698$.
\begin{align*}
\text{TV}_{10}&=\frac{\mathbb{E}(\text{DPS}_{11})}{K_{e,st}-g_{st}}=\frac{7.15\times1.03\times0.80}{0.09-0.03}=\mathbf{\$98.24}\\
\text{EqV}&=\text{PV(DPS)}+\text{PV(TV)}=24.03+\frac{98.24}{2.2850}=24.03+42.99=\mathbf{\$67.03}
\end{align*}
(PV of the 10 dividends $=2.27+2.29+2.30+2.31+2.33+2.43+2.51+2.54+2.54+2.50=24.03$.)

% =====================================================================

## The Value of Growth (Two-Stage DDM)

In any model, the value can be split into the part attributable to **growth**, further broken down into **high growth** and **stable growth**:

> **Decomposition of value**
\begin{align*}
\text{EqV}=&\underbrace{\left[\sum_{t=1}^{n}\frac{\mathbb{E}(\text{DPS}_t)}{(1+k_{e,hg})^t}+\frac{\mathbb{E}(\text{DPS}_{n+1})}{(k_{e,st}-g_n)(1+k_{e,hg})^n}-\frac{\mathbb{E}(\text{DPS}_1)}{k_{e,st}-g_n}\right]}_{\text{Value of high growth}}\\
&+\underbrace{\left(\frac{\mathbb{E}(\text{DPS}_1)}{k_{e,st}-g_n}-\frac{\text{DPS}_0}{k_{e,st}}\right)}_{\text{Value of stable growth}}+\underbrace{\frac{\text{DPS}_0}{k_{e,st}}}_{\text{Value of assets in place}}
\end{align*}

  - **Value of high $g$** $=$ total value $-$ value of the firm as a stable-growth firm.
  - **Value of stable $g$** $=$ value as a stable-growth firm $-$ value with no growth.
  - **Value of assets in place** $=$ value with **no growth** (DPS $=$ EPS: with no growth there is nothing to reinvest, so all earnings are paid out).

% =====================================================================

## Case: ABN -- Two-Stage DDM

> **ABN: inputs (slide)**
Long-term $R_f$ (euro) $=5.02\%$; risk premium $=4\%$ (US premium: the Netherlands is AAA rated). Current EPS $=$ \euro1.60; current DPS $=$ \euro0.60.

\small
\begin{tabular}{@{}lll@{}}
\toprule
**Variable** & **High-growth phase** & **Stable-growth phase**\\
\midrule
Length & 5 years & Forever after year 5\\
ROE & 15.56\% & 15\% (industry average)\\
Payout & 37.5\% & 66.67\%\\
Retention & 62.5\% & 33.33\% ($b=g/\text{ROE}$)\\
Expected $g$ & $0.1556\times0.625=9.73\%$ & 5\%\\
$\beta$ & 0.95 & 1.00\\
$K_e$ & $5.02\%+0.95\times4\%=8.82\%$ & $5.02\%+1.00\times4\%=9.02\%$\\
\bottomrule
\end{tabular}

> **ABN: valuation -- official solution (sheet 6.4)**

\small
\begin{tabular}{@{}lrrrrr|r@{}}
\toprule
Year & 1 & 2 & 3 & 4 & 5 & 6\\
\midrule
EPS ($\times1.0973$) & 1.7556 & 1.9263 & 2.1137 & 2.3192 & 2.5448 & 2.6720\\
DPS (payout 37.5\%; yr 6: 66.67\%) & 0.6584 & 0.7224 & 0.7926 & 0.8697 & 0.9543 & 1.7813\\
PV at 8.82\% & 0.6050 & 0.6100 & 0.6151 & 0.6202 & 0.6254 & \\
\bottomrule
\end{tabular}

\begin{align*}
\text{EPS}_6&=2.5448\times1.05=\text{\euro}2.672\qquad \text{DPS}_6=2.672\times0.6667=\text{\euro}1.7813\\
\text{TV}_5&=\frac{1.7813}{0.0902-0.05}=\text{\euro}44.31\qquad \text{PV(TV)}=\frac{44.31}{1.0882^5}=\text{\euro}29.04\\
\text{EqV}&=0.605+0.610+0.615+0.620+0.625+29.04=\mathbf{\text{\euro}32.11}\quad\text{(slide: \euro32.12)}
\end{align*}
Official comment: ``stock undervalued'' (at its market price, not shown on the slide).

\textcolor{keyred}{**Slide inconsistencies**}: the slide table shows a year-1 PV of 0.65 (correct: 0.61, as used in the slide's own sum), and writes PV(TV) $=44.31/(1.09)^5$, whereas 29.04 is obtained by discounting at the **high-growth** $K_e$: $44.31/1.0882^5$. Rule: the TV is computed with the stable $K_e$ (9.02\%) but discounted back with the high-growth $K_e$ (8.82\%).

> **ABN: value of growth -- official solution**
\begin{align*}
\text{Value as a stable-growth firm}&=\frac{\text{EPS}_0(1+g_n)\times\text{Payout}_{st}}{K_{e,st}-g_n}\\&=\frac{1.60\times1.05\times0.6667}{0.0902-0.05}=\text{\euro}27.86\\
\text{Assets in place (no growth, payout 100\%)}&=\frac{\text{EPS}_0}{K_{e,st}}=\frac{1.60}{0.0902}=\text{\euro}17.74\\[3pt]
\text{Value of high growth}&=32.11-27.86=\mathbf{\text{\euro}4.25}\\
\text{Value of stable growth}&=27.86-17.74=\mathbf{\text{\euro}10.12}\\
\text{Value of assets in place}&=\mathbf{\text{\euro}17.74}\\
\text{Check}&=17.74+10.12+4.25=\text{\euro}32.11\ \checkmark
\end{align*}
\footnotesize Note: the class solution computes the stable-firm value from EPS$_0$ times the *stable* payout (not the current DPS of 0.60), and the no-growth value with payout $=100\%$ (DPS $=$ EPS), as the slide states.

> **Reading the decomposition** *(added, not on slides)*
Over half of ABN's value (17.74/32.11 $=55\%$) comes from assets in place; stable growth adds 32\%; the 5 years of high growth add only 13\%. This is typical of mature firms like banks, and it is why the DDM is used for FIG valuations.

% =====================================================================

## Buybacks and Payout

US firms have increasingly turned to **buybacks** to return cash to shareholders (also because capital gains are taxed less than dividends). Focusing only on DPS may miss an important portion of the cash returned.

> **Augmented payout**
\[
\text{Augmented payout}=\frac{\text{Dividends}+\text{Buybacks}}{\text{Net income}}
\]
Buybacks can be **smoothed** (averaged) over time. If buybacks were financed with debt to increase leverage:
\[
\text{Modified augmented payout}=\frac{\text{Dividends}+\text{Buybacks}-\text{Debt issues}}{\text{Net income}}
\]
\[
\text{Augmented growth rate}=(1-\text{Augmented payout})\cdot\text{ROE}
\]

### Example (slide) -- Official Solution, Sheet 6.5

> **S\&P 500: dividends only**
On 1 January the S\&P 500 trades at 1,257.64; last year's DPS on the index $=\$23.12$. Expected growth in EPS and DPS for 5 years $=6.95\%$, then 3.29\% forever; cost of capital $=8.5\%$.

\small
\begin{tabular}{@{}lrrrrr|r@{}}
\toprule
Year & 1 & 2 & 3 & 4 & 5 & TV$_5$\\
\midrule
$\mathbb{E}(\text{DPS})$ & 24.73 & 26.45 & 28.28 & 30.25 & 32.35 & 641.38\\
PV at 8.5\% & 22.79 & 22.46 & 22.14 & 21.83 & 21.52 & 426.54\\
\bottomrule
\end{tabular}

\[
\text{EqV}=\frac{24.73}{1.085}+\frac{26.45}{1.085^2}+\frac{28.28}{1.085^3}+\frac{30.25}{1.085^4}+\frac{32.35}{1.085^5}+\frac{32.35\times1.0329}{(0.085-0.0329)\times1.085^5}=\mathbf{537.28}
\]
(TV$_5=32.35\times1.0329/0.0521=641.38$.) Was the index fairly priced? **It looks overvalued** (1,257.64 vs 537.28), but this valuation does not consider buybacks.

> **S\&P 500: augmented dividends (dividends + buybacks)**
Buybacks last year $=\$30.84$ $\Rightarrow$ cash returned $=23.12+30.84=\$53.96$ per share. Same parameters:

\small
\begin{tabular}{@{}lrrrrr|r@{}}
\toprule
Year & 1 & 2 & 3 & 4 & 5 & TV$_5$\\
\midrule
Div.\ + buybacks & 57.71 & 61.72 & 66.01 & 70.60 & 75.51 & 1{,}496.91\\
PV at 8.5\% & 53.19 & 52.43 & 51.68 & 50.94 & 50.21 & 995.51\\
\bottomrule
\end{tabular}

\[
\text{EqV}=\frac{57.71}{1.085}+\dots+\frac{75.51}{1.085^5}+\frac{75.51\times1.0329}{(0.085-0.0329)\times1.085^5}=\mathbf{1{,}253.97}
\]
With buybacks incorporated, the index looks **(almost) fairly priced** (1,253.97 vs 1,257.64).

% =====================================================================

## Takeaways

  - The DDM is widely used to value **financial institutions (FIG)**, especially **banks**, since they pay predictable/constant DPS.
  - The DDM is very sensitive to assumptions, particularly the **perpetuity growth rate**.
  - To smooth the impact of $g$ on value, use models allowing for **different growth rates** (two-stage, three-stage).
  - **Consistency is key**: payouts consistent with growth (stable firms have higher payout ratios, all else equal); long-run ROE consistent with the industry perspective.

% =====================================================================

## Formula Summary Sheet

\small
\renewcommand{\arraystretch}{1.5}
\begin{longtable}{@{}p{4.6cm}p{10.4cm}@{}}
\toprule
**Concept** & **Formula**\\
\midrule
\endhead
General DDM & $\text{EqV}_0=\sum_{t\geq1}\mathbb{E}(\text{DPS}_t)/(1+K_e)^t$\\
Gordon & $\text{EqV}_t=\text{DPS}_t(1+g)/(K_e-g)$\\
Stable growth & $g=b\cdot\text{ROE}=(1-\text{Payout})\cdot\text{ROE}$;\ stable payout $=1-g/\text{ROE}$\\
Implied $K_e$ & $K_e=\text{DPS}_t(1+g)/P_t+g=\frac{\text{Payout}(1+g)}{P/E}+g$\\
Implied P/E & $P/E=\text{Payout}(1+g)/(K_e-g)$\\
Two-stage & $\sum_{t=1}^n\frac{\text{DPS}_t}{(1+K_{hg})^t}+\frac{\text{DPS}_{n+1}}{(K_{st}-g_n)(1+K_{hg})^n}$\\
Growing annuity & $\text{DPS}_0(1+g)\frac{1-(1+g)^n/(1+K)^n}{K-g}$\\
Three-stage TV & $\text{EPS}_{n_2}(1+g_n)\Pi_n/(K_{st}-g_n)$, discounted with the cumulative factor\\
Linear transition & step $=($target $-$ start$)/$(number of transition years)\\
Cumulative factor & $\prod_{s=1}^{t}(1+K_{e,s})$\\
Value of assets in place & $\text{EPS}_0/K_{e,st}$ (no growth, payout 100\%)\\
Value of stable growth & $\frac{\text{EPS}_0(1+g_n)\Pi_{st}}{K_{e,st}-g_n}-\frac{\text{EPS}_0}{K_{e,st}}$\\
Value of high growth & Total value $-$ stable-growth-firm value\\
Augmented payout & (Dividends $+$ Buybacks)/NI\\
Modified augmented payout & (Dividends $+$ Buybacks $-$ Debt issues)/NI\\
Augmented growth & $(1-\text{Augmented payout})\cdot\text{ROE}$\\
\bottomrule
\end{longtable}

## Common Mistakes and Exam Traps

> **Exam traps -- Chapter 9**

  - Gordon uses **next year's** dividend: $\text{DPS}_0(1+g)$, not DPS$_0$ (example: $2.22\times1.035$).
  - Gordon requires $g<K_e$ and $g\leq$ nominal growth of the economy; value explodes as $g\to K_e$ (Ex\_1: 21 at 5\%, 228 at 14\%, 22,998 at 14.99\%).
  - Every DDM assumes a constant discount rate, growth and payout in the long run.
  - Retention $=1-$ DPS/EPS; fundamental check $g=RR\times$ ROE (example: $0.36\times9.8\%=3.53\%\approx3.5\%$).
  - Stable payout $=1-g/\text{ROE}$ (three-stage: 80\%; ABN: 66.67\%). Stable firms pay out more.
  - Two-stage: the TV uses the **stable** $K_e$ and stable payout, but is discounted with the **high-growth** $K_e$ (ABN: $44.31/1.0882^5=29.04$; Ex\_2: $27.33/1.125^{10}$).
  - EPS in the first stable year $=$ EPS$_n(1+g_n)$, then apply the **stable** payout (ABN: $2.672\times0.6667=1.78$).
  - With changing $K_e$ use the **cumulative** discount factor $\prod(1+K_{e,s})$, not $(1+K_{e,t})^t$.
  - Three-stage transition: $g$, payout and $K_e$ move **linearly** (equal steps) to the stable values.
  - Value of growth: assets in place $=$ EPS$_0/K_{e,st}$ (payout 100\%); stable-growth value uses EPS$_0\times$ stable payout; high growth $=$ total $-$ stable-firm value (ABN: 17.74 $+$ 10.12 $+$ 4.25 $=$ 32.11).
  - P/E is driven by EPS growth, the DDM by DPS growth: historical $g$ estimates can make them diverge.
  - Ignoring buybacks undervalues firms that return cash via repurchases (S\&P: 537 vs 1,254 with augmented payout). Debt-financed buybacks: subtract debt issues (modified augmented payout).
  - DDM is the standard for banks/FIG; it misvalues firms that pay out less than they could.
  - Slide typos: three-stage reinvestment is 36.4\% (not 36.5\%); ABN year-1 PV is 0.61 (not 0.65).

