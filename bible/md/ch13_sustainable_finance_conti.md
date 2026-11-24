<!-- Markdown notes generated from the LaTeX chapter; tables and formulas kept in LaTeX syntax. The PDF is the reference version. -->
# Sustainable Finance and Enterprise Value (C. Conti)

*Based on ``Special Issues on Valuation (2/3) -- Sustainable finance and enterprise value'' (7 slides) by Cesare Conti, Bocconi University, Department of Finance. Part Two (professional extensions). The module has three parts: (1) the transition towards sustainable finance; (2) the shift from shareholder to stakeholder capitalism; (3) sustainable finance and value.*

\providecommand{\inpractice}[1]{\par\smallskip\noindent{\small\textcolor{keyred}{**In practice**}\quad*#1*}\par\smallskip}

% =====================================================================
## The Transition Towards Sustainable Finance

### Towards Sustainable Finance
\begin{itemize}
  \item **Traditional economic models** developed when natural resources appeared **abundant** and carbon emissions were **limited**.
  \item Those models often **ignored the pricing of many externalities** (the impact of corporate decisions on resources and environmental conditions), focusing mainly on **capital and labour**. Labour was also structurally underpaid in many contexts, and child labour was often exploited.
  \item The **transition** seeks sustainable economic, social and environmental development that preserves food, water, healthcare and energy resources for future generations without overstressing the Earth system.
\end{itemize}
\begin{keybox}[Definition (slide)]
**Sustainable finance** directs capital towards the investments required by this transition.
\end{keybox}
\begin{addbox}[What an externality is]
An **externality** is a cost (or benefit) of a firm's decision that falls on third parties and is *not* in the firm's own cash flows: e.g., pollution, carbon emissions, depletion of a common resource. If externalities are unpriced, a project can show a positive NPV for shareholders and still destroy value for society. Carbon taxes, emission permits or regulation ``price'' the externality, i.e.\ they bring it back into the firm's cash flows, and from that moment it becomes a valuation input (see Section~\ref{sec:sf-value}).
\end{addbox}

### Why Corporate Finance Becomes Involved
Traditional **shareholder-value** finance relies on **two assumptions**:
\begin{center}
\small
\begin{tabular}{@{}cp{12.5cm}@{}}
\toprule
**1** & Companies have **no comparative advantage** in socially responsible decisions, so **shareholders** should make those choices (e.g., by donating their own dividends).\\
**2** & **Governments** can control corporate externalities through effective **regulation and taxation**.\\
\bottomrule
\end{tabular}
\end{center}
\begin{keybox}[Key message (slide)]
When **either** assumption fails, corporate finance can allocate capital to sustainable firms and projects and accelerate the shift towards a **low-carbon, more circular economy**.
\end{keybox}
\begin{addbox}
This is the classic Friedman view (``the social responsibility of business is to increase its profits''): firms maximise shareholder value, governments fix externalities, shareholders pursue their own social goals. The argument for stakeholder-oriented finance is that in reality (i) firms are often better placed than dispersed shareholders to reduce an externality (they control the production process), and (ii) regulation is incomplete, slow or cross-border. Note the logic: only *one* of the two assumptions needs to fail.
\end{addbox}

% =====================================================================
## The Shift from Shareholder to Stakeholder Capitalism

### The Three Actors
\begin{center}
\begin{tikzpicture}[box/.style={draw=none,rounded corners=2pt,minimum height=2.7cm,text width=4.3cm,align=center,font=\small}]
\node[box,fill=boxblue] (a) at (0,0) {**Boards and CEOs**\\[4pt] Embed sustainability in business models and governance while preserving accountability and balancing stakeholder interests.};
\node[box,fill=teal!75!black,text=white] (b) at (4.8,0) {**Financial institutions**\\[4pt] Banks, insurers, public and private investors, and ESG and credit-rating agencies integrate sustainability into capital allocation.};
\node[box,fill=keyred!85!black,text=white] (c) at (9.6,0) {**Regulators**\\[4pt] Sustainability-reporting requirements broaden ESG information and the population of companies expected to report it.};
\end{tikzpicture}
\end{center}
\begin{keybox}[Key message (slide)]
The **competitive risk of being unprepared** for the transition can be substantial for both companies and financial institutions.
\end{keybox}
\begin{addbox}
Shareholder capitalism: the firm is run in the interest of shareholders (maximise equity value). Stakeholder capitalism: the firm also weighs the interests of employees, customers, suppliers, communities and the environment. For a valuation analyst the relevant point is not ideology but **transition risk**: a firm unprepared for stricter regulation, changing customer demand or the reallocation of capital by investors and banks faces lower future cash flows and/or more expensive funding.
\end{addbox}

### What Determines the Speed of the Transition
\begin{center}
\small
\begin{tabular}{@{}p{3.6cm}p{11cm}@{}}
\toprule
**Driver** & **Content**\\
\midrule
\textcolor{navy}{**Financing innovation**} & Green, social, sustainable and sustainability-linked bonds and loans, together with ESG risk-management instruments.\\
\textcolor{keyred}{**Integrated analysis**} & Traditional credit and equity analysis combined with ESG analysis and ratings.\\
\textcolor{navy}{**Integrated reporting**} & Financial and ESG performance, material KPIs, management incentives, stakeholder communication, and reliable comparable data.\\
\textcolor{keyred}{**Regulation and engagement**} & Reporting requirements and investor engagement reinforce market discipline.\\
\bottomrule
\end{tabular}
\end{center}
\begin{keybox}[Key message (slide)]
Effectiveness depends on **credible data** and on identifying the ESG dimensions that are **material** in each business context.
\end{keybox}
\begin{addbox}[The financing instruments in one line each]
\begin{itemize}
  \item **Green bond / loan**: the *proceeds* are earmarked for eligible environmental projects (use-of-proceeds instrument).
  \item **Social bond**: proceeds earmarked for social projects (housing, health, education); **sustainable bond**: a mix of green and social uses.
  \item **Sustainability-linked bond / loan**: proceeds are *not* earmarked; the *coupon* is linked to the issuer reaching ESG KPI targets (e.g., the coupon steps up if emissions are not cut by the target date).
\end{itemize}
**Materiality**: an ESG issue is material if it can affect the firm's cash flows or risk in *its* industry (carbon for a utility, data privacy for a bank, labour conditions for apparel). ESG, in short, stands for **E**nvironmental, **S**ocial and **G**overnance.
\end{addbox}

% =====================================================================
## Sustainable Finance and Value

### Sustainability and Enterprise Value
\begin{keybox}[The valuation identity (slide)]
\[
\text{Equity value}=\text{Enterprise value}-\text{Net financial debt}
\]
ESG affects value only through the three blocks of this identity.
\end{keybox}
\begin{center}
\begin{tikzpicture}[box/.style={rounded corners=2pt,minimum height=2.6cm,text width=4.3cm,align=left,font=\small}]
\node[box,fill=boxblue] at (0,0) {\centering\textcolor{navy}{**OPERATING CASH FLOW**}\par\smallskip
$\bullet$ EBITDA and operating costs\\ $\bullet$ Working-capital movements\\ $\bullet$ Investment and divestment};
\node[box,fill=boxblue] at (4.8,0) {\centering\textcolor{keyred}{**COST OF CAPITAL**}\par\smallskip
$\bullet$ Risk-free rate and credit spread\\ $\bullet$ Unlevered and levered beta\\ $\bullet$ Equity risk premium and leverage};
\node[box,fill=lightgrey] at (9.6,0) {\centering\textcolor{navy}{**NET FINANCIAL DEBT**}\par\smallskip
$\bullet$ Funding needs and liquidity\\ $\bullet$ Debt pricing and refinancing\\ $\bullet$ Cash generated by ESG initiatives};
\end{tikzpicture}
\end{center}
\begin{keybox}[Key message (slide)]
Empirical evidence often associates **high ESG ratings with lower risk**, but valuation still requires a **causal analysis** of cash flows and the cost of capital.
\end{keybox}

\begin{addbox}[How to put ESG into a DCF without errors]
\begin{enumerate}[leftmargin=*]
  \item **Cash flows (FCFO)**: model explicitly the ESG effects you can explain: carbon costs or taxes in operating costs; energy-efficiency savings in EBITDA; transition CapEx (e.g., new plants) in reinvestment; stranded assets as write-offs or shorter useful lives; demand shifts in revenue.
  \item **Cost of capital**: change it only for **systematic** (non-diversifiable) risk: e.g., a lower beta if the firm is less exposed to economy-wide regulatory or climate shocks, or a lower credit spread on sustainability-linked debt. Firm-specific ESG events (a single lawsuit, a spill) belong in expected cash flows or scenarios, not in the discount rate (Chapters 7 and 12).
  \item **Net debt / bridge**: environmental liabilities and litigation provisions are debt-like items (Chapter 1, after tax); ESG-linked financing changes debt pricing and refinancing risk.
  \item **Do not double count**: if ESG risk is already in the cash flows (scenarios, carbon costs), do not also add an ``ESG premium'' to the discount rate. And a correlation between ESG ratings and risk is not proof that improving the rating will lower *this* firm's cost of capital: you need the causal mechanism.
\end{enumerate}
\end{addbox}

\begin{exbox}[Illustration (not on slides): a carbon cost in a perpetuity]
A firm has NOPAT $=100$, no growth, WACC $=8\%$: EV $=100/0.08=1{,}250$. A carbon tax costs 15 per year pre-tax ($t=25\%$): NOPAT falls by $15\times0.75=11.25$ to $88.75$, so EV $=88.75/0.08=1{,}109$ ($-11\%$).

If, instead, the firm invests 60 today in abatement that eliminates the tax: EV $=1{,}250-60=1{,}190>1{,}109$. The investment creates $1{,}190-1{,}109=81$ of value (it is a positive-NPV project because the externality is now *priced*). This is the mechanism through which regulation turns sustainability into a valuation input.
\end{exbox}

% =====================================================================
## Formula Summary Sheet
\begin{center}
\small
\renewcommand{\arraystretch}{1.5}
\begin{tabular}{@{}p{5cm}p{10cm}@{}}
\toprule
**Concept** & **Formula / rule**\\
\midrule
Valuation identity & Equity value $=$ EV $-$ Net financial debt\\
ESG channel 1 & Operating cash flow: EBITDA and costs, working capital, investment/divestment\\
ESG channel 2 & Cost of capital: $r_f$ and credit spread, $\beta_u$ and $\beta_l$, ERP and leverage\\
ESG channel 3 & Net financial debt: funding needs, liquidity, debt pricing, refinancing, cash from ESG initiatives\\
Discount-rate rule & Adjust WACC only for systematic ESG risk; firm-specific ESG risk in cash flows/scenarios\\
Shareholder-value assumptions & (1) no corporate comparative advantage in CSR; (2) governments control externalities\\
\bottomrule
\end{tabular}
\end{center}

\needspace{12\baselineskip}
## Common Mistakes and Exam Traps
\begin{trapbox}[Exam traps -- Chapter 13]
\begin{enumerate}[leftmargin=*]
  \item Sustainable finance $=$ directing capital towards the investments required by the transition.
  \item Traditional models ignored the **pricing of externalities** and focused on capital and labour.
  \item Shareholder-value finance rests on **two** assumptions (no corporate comparative advantage in socially responsible decisions; governments control externalities). Corporate finance becomes involved when **either** fails, not only when both fail.
  \item Three actors of stakeholder capitalism: boards/CEOs, financial institutions (incl.\ ESG and credit-rating agencies), regulators (reporting requirements).
  \item Four drivers of the speed of the transition: financing innovation, integrated analysis, integrated reporting, regulation and engagement. Effectiveness depends on **credible data** and **materiality**.
  \item ESG affects value only via operating cash flow, cost of capital and net financial debt (Equity $=$ EV $-$ net debt).
  \item High ESG ratings are *associated* with lower risk, but valuation needs a **causal** analysis: correlation is not a valuation input.
  \item Do not double count ESG risk in both cash flows and the discount rate; only systematic risk goes into the discount rate.
  \item Green bonds earmark the *proceeds*; sustainability-linked instruments link the *coupon* to KPI targets.
\end{enumerate}
\end{trapbox}
