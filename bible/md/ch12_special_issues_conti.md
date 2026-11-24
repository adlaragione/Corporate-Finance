<!-- Markdown notes generated from the LaTeX chapter; tables and formulas kept in LaTeX syntax. The PDF is the reference version. -->
# Special Issues on Valuation (C.\ Conti)

\emph{Based on ``Special Issues on Valuation'' (28 slides) by Cesare Conti, Bocconi University, Department of Finance: ``From valuation mechanics to economic judgement''. Sessions 15--16 of Part Two (professional extensions). Each slide ends with an ``In practice'' rule, reported here after the red label *In practice*.}

\newcommand{\inpractice}[1]{\par\smallskip\noindent{\small\textcolor{keyred}{**In practice**}\quad*#1*}\par\smallskip}

## Course Map

> **One relevant question about valuation mechanics**
**When does a formally correct valuation become economically wrong?**

\small
\begin{tabular}{@{}p{7cm}p{7cm}@{}}
\toprule
**Focus 1 $\cdot$ Value, earnings and risk** (Session 1) & **Focus 2 $\cdot$ Industry, deals and judgement** (Session 2)\\
\midrule
Value configurations and acquisition value & Dynamic industry analysis\\
EBITDA quality and multiple dispersion & Buy-and-build and strategic vulnerability\\
Size, control and comparability adjustments & Valuation gaps and deal design\\
Competitive advantage and terminal value & Uncertainty, scenarios and defensibility\\
\bottomrule
\end{tabular}

\inpractice{Before modelling, classify each judgement as cash flow, risk, multiple or deal structure.}

% =====================================================================

## Focus 1: Value, Earnings and Risk

### Price and Value Answer Different Questions

\small
\begin{tabular}{@{}p{7cm}p{7cm}@{}}
\toprule
**Value** & **Price**\\
\midrule
A **conditional estimate** based on a defined perspective & An **observed outcome** of negotiation\\
Changes with the valuation premise and available synergies & Reflects bargaining power, financing and execution constraints\\
Requires a coherent income, growth and risk profile & Can lie above or below either party's value\\
\bottomrule
\end{tabular}

> **Key point**
A deal can create value for **both** parties even when they disagree on ``the'' value.

> **Added explanation (not on slides)**
The same message as the Ocado case in the Introduction: ``price is negotiated, value is argued''. If the seller values the business at 160 and the buyer at 190, any price between them leaves both better off.

### A Ladder of Value Configurations

[Figure: redrawn diagram, see PDF]

\inpractice{Build a bridge that identifies who can capture each increment of value.}

> **Reading the ladder** *(added, not on slides)*
150 $\to$ 175 ($+25$): what *any* informed market participant would pay (e.g., market-wide synergies or financing). 175 $\to$ 190 ($+15$): synergies only *this* buyer can capture. The price (185) lies below the buyer's investment value, so the buyer keeps $190-185=5$, while the seller captures $185-150=35$ above intrinsic value.

### Acquisition Value Belongs to the Buyer

> **Acquisition value**
\[
\text{Acquisition value}=\text{Value of the buyer after the deal}-\text{Value of the buyer before the deal}
\]
**Value creation test**: \qquad Acquisition value $>$ Price paid

  - Synergies matter **only if the buyer can capture them**.
  - **Integration costs and execution risk** reduce acquisition value.
  - The target can be excellent and the deal can still destroy value.

Investment bankers should reconcile the valuation bridge with the deal thesis.

> **Illustration (not on slides)**
Buyer worth 1,000 alone; after the deal 1,180 (target stand-alone 150 $+$ synergies 50 $-$ integration costs 20). Acquisition value $=180$. Price 185 $\Rightarrow$ NPV for the buyer $=180-185=-5$: an excellent target, but a value-destroying deal.

### Control Premiums Often Double Count Value

\small
\begin{tabular}{@{}p{7cm}p{7cm}@{}}
\toprule
**Defensible approach** & **Common error**\\
\midrule
Start from the cash flows available to the controlling owner & Apply a market premium mechanically to a control-level DCF\\
Model operating improvements and financing effects explicitly & Treat the premium as a universal percentage\\
Separate control benefits from buyer-specific synergies & Add a premium after using comparables that already reflect control\\
\bottomrule
\end{tabular}

\inpractice{Translate control rights into cash-flow or risk effects and test for double counting.}

> **Added explanation (not on slides)**
Two typical double counts: (i) a DCF built on the controlling owner's plan (with improvements) already contains the value of control; adding a 30\% premium counts it twice. (ii) Deal multiples (Chapter~\ref{ch:multiples}) already embed control premiums; adding a premium on top double counts.

### EBITDA Is Useful Because It Excludes Information

\small
\begin{tabular}{@{}p{7cm}p{7cm}@{}}
\toprule
**What EBITDA captures** & **What EBITDA omits**\\
\midrule
Revenue less cash operating costs & Working-capital absorption and CapEx\\
Operating efficiency before asset consumption & Taxes and financing costs\\
A common denominator for peer comparison & Capital intensity and accounting for asset consumption\\
\bottomrule
\end{tabular}

> **Key point**
**Comparability rises when detail disappears. Valuation risk rises for the same reason.**

\inpractice{Bridge EBITDA to cash flow, capex, taxes and debt before using the multiple.}

### Alpha and Beta: Same EBITDA and Net Income, Different Value

> **Even same EBITDA and net income do not imply equal value (slide)**

\begin{tabular}{@{}lrr@{}}
\toprule
**Income statement** & **Alpha** & **Beta**\\
\midrule
EBITDA & 5,000 & 5,000\\
Depreciation and amortisation & (1,500) & (1,700)\\
Financial charges & (600) & (300)\\
Taxes & (400) & (500)\\
\midrule
**Net income** & **2,500** & **2,500**\\
\bottomrule
\end{tabular}

The headline earnings measures are identical. The economic differences appear **below EBITDA** and **outside net income**.

> **Cash conversion separates Alpha from Beta (slide)**

\begin{tabular}{@{}lrr@{}}
\toprule
**Operating cash flow** & **Alpha** & **Beta**\\
\midrule
EBITDA & 5,000 & 5,000\\
Change in net working capital & (800) & (400)\\
Capital expenditure & (1,300) & (1,000)\\
Taxes & (400) & (500)\\
\midrule
**Operating cash flow** & **2,500** & **3,100**\\
**Cash conversion** (OCF/EBITDA) & **50\%** & **62\%**\\
\bottomrule
\end{tabular}

Beta converts $3{,}100/5{,}000=62\%$ of EBITDA into operating cash flow versus $2{,}500/5{,}000=50\%$ for Alpha.

\inpractice{Calculate cash conversion before selecting peers or adjusting a multiple.}

> **Discussion: cash conversion and leverage explain different multiples (slide)**
Assume both companies are valued at **10$\times$ operating cash flow**.

\begin{tabular}{@{}lrr@{}}
\toprule
**Valuation bridge** & **Alpha** & **Beta**\\
\midrule
Enterprise value ($10\times$ OCF) & 25,000 & 31,000\\
**Implied EV/EBITDA** & $25{,}000/5{,}000=\mathbf{5.0\times}$ & $31{,}000/5{,}000=\mathbf{6.2\times}$\\
Debt & 6,000 & 3,000\\
Equity value (EV $-$ debt) & 19,000 & 28,000\\
**Implied P/E** & $19{,}000/2{,}500=\mathbf{7.6\times}$ & $28{,}000/2{,}500=\mathbf{11.2\times}$\\
\bottomrule
\end{tabular}

**A multiple is the result of cash generation and risk. It is not an input chosen before the economic analysis.**

> **Added explanation (not on slides)**
Applying one peer EV/EBITDA (say 6$\times$) to both firms would overvalue Alpha (30,000 vs 25,000) and undervalue Beta (30,000 vs 31,000). P/E differs even more because leverage also differs: Alpha's higher debt (6,000) is a larger claim on its lower EV. This is the EV/EBITDA determinants formula of Chapter~\ref{ch:multiples} in action: higher reinvestment (WC + CapEx) $\Rightarrow$ lower EV/EBITDA.

### Small-Company Risk Needs Diagnosis

\small
\begin{tabular}{@{}p{6.5cm}p{7.5cm}@{}}
\toprule
**Economic sources** & **Valuation responses**\\
\midrule
Customer, supplier and key-person concentration & **Adjust forecasts** when the risk changes expected cash flows\\
Limited financing flexibility and weaker systems & **Adjust the discount rate** only for non-diversifiable systematic exposure\\
Greater sensitivity to single events & **Use scenarios** when events create asymmetric outcomes\\
\bottomrule
\end{tabular}

> **Key point**
A **mechanical size premium** can hide risk already captured elsewhere.

> **Added explanation (not on slides)**
Consistent with the CAPM logic of Chapter~\ref{ch:coc}: only systematic risk belongs in the discount rate. Firm-specific risks (losing a key customer) change *expected* cash flows (probability-weighted), as in Chapter~\ref{ch:forecast} (``expected, not most likely''). Adding a size premium on top of haircut cash flows counts the same risk twice.

### Competitive Advantage Sets the Forecast Horizon

> **Key point**
**Value does not increase because the business plan becomes longer.**

[Figure: redrawn diagram, see PDF]

> **Key point**
**Terminal value starts when economics stabilise, not when Excel runs out of columns.**

\inpractice{End the explicit forecast when the economics reach a sustainable steady state.}

### Strategic Assets Require Maintenance

\small
\begin{tabular}{@{}>{\bfseries}p{4.5cm}p{9.5cm}@{}}
\toprule
\textnormal{**Strategic asset**} & **Maintenance investment**\\
\midrule
Brand and customer trust & Commercial investment, service quality and consistency\\
Technology and know-how & R\&D, talent retention and learning\\
Distribution access & Partner economics and channel productivity\\
Operating routines & Systems, training and coordination capacity\\
\bottomrule
\end{tabular}

> **Key point**
**Maintenance CapEx includes investments that accounting may classify as operating expense.**

> **Added explanation (not on slides)**
This is the R\&D-capitalization logic of Chapter~\ref{ch:fcf}: marketing, training or R\&D needed to *keep* the advantage are economically CapEx. A terminal value that assumes a lasting advantage without these costs overstates value.

### Terminal Value Needs an Economic Steady State

\small
\begin{tabular}{@{}p{7cm}p{7cm}@{}}
\toprule
**Fading advantage** & **Renewable advantage**\\
\midrule
Returns move toward the cost of capital & Returns remain above the cost of capital\\
Terminal value may converge toward invested capital & Terminal cash flow must include renewal investment\\
Forecast the run-off of excess returns explicitly & Evidence must support the effectiveness of reinvestment\\
\bottomrule
\end{tabular}

\inpractice{Test whether terminal returns fade to the cost of capital or require renewal investment.}

> **Why TV $\to$ invested capital when returns fade** *(added, not on slides)*
With ROC $=k_C$ in perpetuity, TV $=$ EBIT$_{n+1}(1-t)/k_C$ (Chapter~\ref{ch:growth}). Since EBIT$(1-t)=$ ROC $\times$ invested capital $=k_C\times$ IC, TV $=$ IC: the firm is worth exactly the capital invested, because it earns no excess return.

### Focus 1 Synthesis (Discussion)

  - Which **value configuration** answers the assignment?
  - What does **EBITDA hide** in this business?
  - Which risks belong in **cash flows, scenarios or the discount rate**?
  - How long can the company earn **excess returns**?

> **Key point**
If these questions remain unanswered, the model is not ready for an investment committee.

% =====================================================================

## Focus 2: Industry, Deals and Judgement

### Industry Analysis Must Explain Future Economics

\small
\begin{tabular}{@{}p{7cm}p{7cm}@{}}
\toprule
**Static description** & **Dynamic analysis**\\
\midrule
Market size, growth and concentration & Likely strategic moves and countermoves\\
Current competitors and market shares & Drivers of consolidation, integration or globalisation\\
Historical margins & The target's capacity to gain, defend or lose position\\
\bottomrule
\end{tabular}

\inpractice{Convert each industry observation into a revenue, margin, reinvestment or risk assumption.}

### Three Questions for Fundamental Industry Analysis

  - **Will the sector consolidate?** Scale economies, access to capital, standardisation and acquisition capacity.
  - **Will the value chain reconfigure?** Vertical integration, disintermediation and bargaining power.
  - **Where will profit pools migrate?** Customer needs, technology and scarce capabilities.

### A Fragmented Sector Can Carry Hidden Strategic Risk

> **Key point**
**Fragmentation today does not imply fragmentation tomorrow.**

[Figure: redrawn diagram, see PDF]

> **Key point**
Historical stability may be the **weakest evidence** in a changing competitive structure.

\inpractice{Rebuild the peer set and downside case when consolidation changes the industry structure.}

### Buy-and-Build Creates Value Through a Platform and Add-Ons

\small
\begin{tabular}{@{}p{7cm}p{7cm}@{}}
\toprule
**Value-creation mechanisms** & **Failure modes**\\
\midrule
Acquire a platform, then add smaller businesses in the same or adjacent market & Platform overpayment and weak add-on discipline\\
Create operating gains through scale, shared systems and stronger management & Integration costs exceed operating synergies\\
Potential multiple uplift is credible only if integration improves the combined business & Leverage reduces strategic flexibility\\
\bottomrule
\end{tabular}

> **Key point**
Analyse returns separately: **operating improvement**, **leverage** and **entry-to-exit multiple change**.

### Customer Value Is the First Valuation Bridge

[Figure: redrawn diagram, see PDF]

> **Key point**
Revenue forecasts need an explicit theory of **customer value** and **value capture**.

\inpractice{Tie every revenue assumption to customer value, willingness to pay and value capture.}

> **Added explanation (not on slides)**
This is the revenue tree of Chapter~\ref{ch:forecast} (price $\times$ volume) seen from the customer side: price depends on willingness to pay, volume on the size of the customer problem, margin on how much of the created value the firm captures.

### Mini-Case: A ``Cheap'' Platform Acquisition (Discussion)

> **Mini-case (slide)**
A regional services platform trades at **7$\times$ EBITDA**. Add-ons trade at **5$\times$**.

  - The model assumes a **9$\times$ exit multiple** after five years.
  - Central costs rise before procurement synergies arrive.
  - Competitors backed by other funds are bidding for the same targets.

**Investment committee questions**: Which part of the return comes from operations, leverage and multiple expansion? What happens if the platform never earns a strategic premium?

\inpractice{Stress-test the exit multiple and the availability and price of add-on acquisitions.}

> **Suggested solution (ours, illustrative numbers; not on slides)**
Buy the platform (EBITDA 10) at 7$\times$ $=70$ and add-ons (EBITDA 5) at 5$\times$ $=25$: total cost 95 for EBITDA 15 (blended entry multiple $95/15=6.33\times$). Assume EBITDA grows to 18 by year 5 and ignore debt.

\small
\begin{tabular}{@{}lrr@{}}
\toprule
**Source of value gain** & **Computation** & **Gain**\\
\midrule
Operations (EBITDA growth at entry multiple) & $(18-15)\times6.33$ & 19\\
Multiple arbitrage (add-ons re-rated to the platform multiple) & $18\times(7-6.33)$ & 12\\
Multiple expansion (7$\times\to$ 9$\times$) & $18\times(9-7)$ & 36\\
\midrule
**Total** ($18\times9-95$) & $162-95$ & **67**\\
\bottomrule
\end{tabular}

More than half of the gain (36 of 67) comes from the assumed 9$\times$ exit multiple. If the platform never earns a strategic premium (exit at 7$\times$), the gain falls to 31; at the blended 6.33$\times$, only the operating 19 remains. Rising central costs and competing bidders (higher add-on prices than 5$\times$) erode both the operating and the arbitrage components. Leverage would amplify equity returns in both directions, but it is not value creation by the business.

### Deal Design Converts a Value Gap into an Allocation of Risk

\small
\begin{tabular}{@{}p{7cm}p{7cm}@{}}
\toprule
**Seller perspective** & **Buyer perspective**\\
\midrule
Values the stand-alone plan and transfer of future upside & Prices integration costs and execution risk\\
May attach value to identity, continuity or control & Values only synergies it expects to capture\\
Faces information asymmetry about buyer synergies & Must preserve an acceptable acquisition return\\
\bottomrule
\end{tabular}

> **Key point**
Deal design combines **price, payment timing, financing, governance and contingent terms** to decide **who bears each uncertainty**.

### Four Deal-Design Tools for Four Uncertainties

\small
\begin{tabular}{@{}>{\bfseries}l p{5.2cm}p{6cm}@{}}
\toprule
\textnormal{**Tool**} & **How it works** & **What must be negotiated**\\
\midrule
Earn-out & Part of the price depends on post-closing results & Metric, control of the business and measurement period\\
Rollover equity & Seller reinvests part of the proceeds in the new group & Governance, dilution, liquidity and exit rights\\
Vendor loan & Seller finances part of the purchase price & Interest, maturity, security, subordination and recovery\\
Price adjustment & Price updates for debt, cash or working capital at closing & Definitions, accounting consistency and dispute process\\
\bottomrule
\end{tabular}

\inpractice{Match each deal tool to one uncertainty and model its cash-flow and control consequences.}

> **Which uncertainty each tool addresses** *(added, not on slides)*
Earn-out: disagreement on *future performance* (the seller is paid if the plan materialises). Rollover equity: *alignment* and the seller's belief in upside. Vendor loan: *financing* capacity and the seller's confidence. Price adjustment: the *closing balance sheet* (net debt and WC at completion, linked to the EV-to-equity bridge). Example earn-out: buyer values the target at 160, seller at 200; agree 160 upfront $+$ 40 if year-2 EBITDA exceeds the seller's plan.

### Uncertainty Creates False Value Drivers

\small
\begin{tabular}{@{}p{7cm}p{7cm}@{}}
\toprule
**Real driver** & **False driver**\\
\midrule
A causal link to future cash flows & A metric correlated with past performance only\\
Observable leading indicators & A narrative that cannot be falsified\\
A credible capacity to adapt or defend economics & A generic ``resilience'' premium without operational evidence\\
\bottomrule
\end{tabular}

\inpractice{Accept a driver only when a causal mechanism and observable indicator support it.}

### Scenarios Separate Exposure from Response

\small
\begin{tabular}{@{}>{\bfseries}l ll@{}}
\toprule
\textnormal{**External state**} & **Operating response** & **Valuation effect**\\
\midrule
Demand shock & Variable cost flexibility & Margin and cash burn\\
Input disruption & Dual sourcing and inventory & Working capital and service\\
Regulatory change & Product redesign or exit & CapEx, timing and terminal value\\
Financing stress & Covenant headroom and liquidity & Equity risk and optionality\\
\bottomrule
\end{tabular}

\inpractice{Model the external shock and the company response in separate scenario steps.}

> **Illustration (not on slides): scenario-weighted value**
Base case value 200 (prob.\ 60\%); demand-shock scenario 140 (30\%); severe shock 80 (10\%). Expected value $=0.6\times200+0.3\times140+0.1\times80=120+42+8=\mathbf{170}$, below the base case: asymmetric downside belongs in scenarios, not in a higher discount rate.

### A Valuation Is a Reasoned Estimate

> **Key point**
**Credibility comes from the chain of reasoning, not the number of decimal places.**

\small
\begin{tabular}{@{}>{\bfseries}l p{11cm}@{}}
Purpose & The assignment determines the relevant value configuration\\
Evidence & Historical, market and strategic information must reconcile\\
Assumptions & Material judgements remain explicit and testable\\
Limitations & Uncertainty and information gaps remain visible\\
\end{tabular}

\inpractice{Make each material judgement explicit, testable and linked to evidence.}

### Red-Team the Valuation (Discussion)
Teams receive the same model and attack one assumption each:

\small
\begin{tabular}{@{}>{\bfseries}l p{11cm}@{}}
Cash flows & Which forecast depends on the weakest causal link?\\
Multiple & Which peer difference has been ignored?\\
Terminal value & What competitive advantage survives into perpetuity?\\
Deal bridge & Who captures the synergies and who bears execution risk?\\
\end{tabular}

\inpractice{Challenge the weakest assumption and state whether it changes value, price or deal terms.}

## Close: The Investment-Banking Checklist

[Figure: redrawn diagram, see PDF]

\inpractice{Use the checklist before the investment-committee or client-review meeting.}

% =====================================================================

## Formula Summary Sheet

\small
\renewcommand{\arraystretch}{1.5}
\begin{tabular}{@{}p{5cm}p{10cm}@{}}
\toprule
**Concept** & **Formula / rule**\\
\midrule
Value ladder & Intrinsic $\leq$ market participant $\leq$ investment value; price is negotiated\\
Acquisition value & Value of buyer after deal $-$ value of buyer before deal\\
Value creation test & Acquisition value $>$ price paid\\
Cash conversion & Operating cash flow / EBITDA (Alpha 50\%, Beta 62\%)\\
Operating cash flow & EBITDA $-\Delta$NWC $-$ CapEx $-$ taxes\\
Implied multiples & EV/EBITDA $=$ (EV/OCF) $\times$ cash conversion; P/E $=$ (EV $-$ debt)/NI\\
TV with fading advantage & ROC $\to k_C$ $\Rightarrow$ TV $\to$ invested capital\\
Return decomposition (B\&B) & Operations $+$ multiple arbitrage $+$ multiple expansion ($+$ leverage)\\
Scenario value & $\sum_s p_s V_s$\\
\bottomrule
\end{tabular}

## Common Mistakes and Exam Traps

> **Exam traps -- Chapter 12**

  - **Price $\neq$ value**: value is a conditional estimate from a perspective; price is a negotiated outcome and can lie above or below either party's value.
  - Value ladder: intrinsic (stand-alone) $\to$ market participant (market assumptions) $\to$ investment value (buyer-specific synergies) $\to$ transaction price (negotiated). Example: 150, 175, 190, 185.
  - Acquisition value belongs to the **buyer**: value after $-$ value before; a deal creates value only if acquisition value $>$ price paid. Synergies count only if the buyer can capture them; integration costs reduce value.
  - **Control premiums double count** when added to a control-level DCF or to comparables (deal multiples) that already reflect control; never treat the premium as a universal percentage.
  - EBITDA omits WC, CapEx, taxes, financing and capital intensity: same EBITDA and NI can hide different cash conversion (Alpha 50\% vs Beta 62\%).
  - At the same 10$\times$ OCF, implied EV/EBITDA is 5.0$\times$ vs 6.2$\times$ and P/E 7.6$\times$ vs 11.2$\times$: a multiple is an **output** of cash generation and risk, not an input.
  - Small-company risk: adjust **cash flows** for firm-specific risks, the **discount rate** only for systematic exposure, **scenarios** for asymmetric events; a mechanical size premium may double count.
  - A longer business plan does not create value; the explicit forecast ends when economics reach a steady state (``not when Excel runs out of columns'').
  - Maintenance of strategic assets (brand, R\&D, distribution, routines) is economically CapEx even if expensed.
  - Fading advantage $\Rightarrow$ returns $\to$ cost of capital, TV $\to$ invested capital; renewable advantage $\Rightarrow$ terminal cash flow must include renewal investment.
  - Dynamic industry analysis: consolidation, value-chain reconfiguration, profit-pool migration; fragmentation today does not imply fragmentation tomorrow.
  - Buy-and-build: separate operating improvement, leverage and multiple change; stress-test the exit multiple and add-on availability/price.
  - Deal tools: earn-out (performance), rollover equity (alignment/governance), vendor loan (financing), price adjustment (closing debt, cash, WC).
  - False value drivers: correlation with the past, unfalsifiable narratives, generic ``resilience'' premiums.
  - Scenarios model the external shock and the company's response in separate steps.

