<!-- Markdown notes generated from the LaTeX chapter; tables and formulas kept in LaTeX syntax. The PDF is the reference version. -->
# Risky Debt and Put-Call Parity (C. Conti)

*Based on ``Special Issues on Valuation (3/3) -- Application of Put-Call Parity to the Valuation of Risky Debt'' (12 slides) by Cesare Conti, Bocconi University, Department of Finance. Part Two (professional extensions). Two parts: (1) put-call parity; (2) its application to the valuation of risky debt. It formalises the option view of the firm introduced in Chapter 0 and the ``YTM $\geq$ cost of debt'' rule of Chapters 5 and 7.*

\providecommand{\inpractice}[1]{\par\smallskip\noindent{\small\textcolor{keyred}{**In practice**}\quad*#1*}\par\smallskip}

% =====================================================================
## Put-Call Parity

### The Replicating Portfolio
Build a portfolio:
\begin{itemize}
  \item **buy** ($+$) the equity at spot price $S$;
  \item **sell** ($-$) a call on $S$ with strike $X$ and maturity $T$;
  \item **buy** ($+$) a put on $S$ with the same strike $X$ and maturity $T$.
\end{itemize}
\begin{keybox}[Put-call parity]
\[
+S-C(S,X,T)+P(S,X,T)=B(X,T)\qquad\Longleftrightarrow\qquad \boxed{\,+S=+C+B-P\,}
\]
The portfolio pays $X$ at maturity in **every** state. $B$ is a **risk-free zero-coupon bond** with face value $X$ (so $B=X/(1+r_f)^T$).
\end{keybox}

### How Put-Call Parity Works
\begin{exbox}[Example (slide): strike $X=40$, two scenarios for $S_T$ at maturity]
\begin{center}
\begin{tabular}{@{}lcc@{}}
\toprule
**Position** & $S_T=45$ & $S_T=35$\\
\midrule
Equity $S$ & 45 & 35\\
Short call $-C$ & $-5$ & 0\\
Long put $+P$ & 0 & $+5$\\
\midrule
**Portfolio value** & **40** & **40**\\
\bottomrule
\end{tabular}
\end{center}
Both scenarios deliver the strike price $X=40$.
\end{exbox}
\begin{addbox}[Why the portfolio is risk-free]
Above the strike the short call takes away the upside ($S_T-X$); below the strike the long put pays back the loss ($X-S_T$). The portfolio pays exactly $X$ whatever happens, so by no-arbitrage it must cost the same as a riskless zero-coupon bond paying $X$: $S-C+P=B$. This is valuation of *redundant securities* by replication, the least general of the three asset-pricing questions of Chapter 0.
\end{addbox}

% =====================================================================
## Application to the Valuation of Risky Debt

### From Put-Call Parity to Risky Debt
Apply the same identity to the **firm**, with the firm's assets in place of the stock and the face value of debt as the strike:
\begin{center}
\small
\begin{tabular}{@{}lp{11cm}@{}}
\toprule
$V$ & **Levered value of the corporation's assets**\\
$C_V$ & Call on $V$ with strike equal to the **debt face value $X$** and maturity $T$\\
$P_V$ & Put on $V$ with strike $X$ and maturity $T$\\
$B$ & Risk-free zero-coupon bond with face value $X$ and maturity $T$\\
\bottomrule
\end{tabular}
\end{center}

### The Risk Profiles of Equity and Debt
At maturity the firm (value $V_T$) must repay $X$. Shareholders have limited liability:
\begin{center}
\begin{tabular}{@{}lcc@{}}
\toprule
**State** & **Equity $E$** & **Risky debt $D$**\\
\midrule
$V_T\leq X$ (default) & 0 & $V_T$\\
$V_T>X$ & $V_T-X$ & $X$\\
\bottomrule
\end{tabular}
\end{center}
\begin{keybox}[The firm as options]
\[
V=\underbrace{C_V}_{E}+\underbrace{(B-P_V)}_{D}
\qquad\text{i.e.}\qquad E=\max(V_T-X,0)=C_V,\qquad D=\min(V_T,X)=B-P_V
\]
Below $X$, **debt absorbs changes in firm value**. Above $X$, **equity captures the upside**.
\end{keybox}

\begin{center}
\begin{tikzpicture}[x=0.4cm,y=0.4cm,>=Stealth]
\draw[->] (0,0) -- (12,0) node[right] {\small $V_T$};
\draw[->] (0,0) -- (0,10.5) node[above] {\small $V,D,E$};
\draw[dotted] (5,0) -- (5,5); \draw[dotted] (0,5) -- (5,5);
\node[below] at (5,0) {\small $X$}; \node[left] at (0,5) {\small $X$};
\draw[navy,thick] (0,0) -- (10.5,10.5) node[above right] {\small $E+D=V$};
\draw[addgreen,very thick] (0,0) -- (5,5) -- (11.5,5) node[right] {\small $D$};
\draw[keyred,very thick] (0,0.06) -- (5,0.06) -- (11.5,6.56) node[right] {\small $E$};
\end{tikzpicture}
\quad
\begin{tikzpicture}[x=0.4cm,y=0.4cm,>=Stealth]
\draw[->] (0,-5.5) -- (0,7) node[above] {\small payoff};
\draw[->] (0,0) -- (12,0) node[right] {\small $V_T$};
\node[above] at (5,0) {\small $X$};
\draw[addgreen,very thick] (0,5) -- (11.5,5) node[right] {\small $B$ (pays $X$)};
\draw[keyred,very thick] (0,-5) -- (5,0) -- (11.5,0) node[above left] {\small $-P_V$};
\draw[navy,thick,dashed] (0,0) -- (5,5) -- (11.5,5) node[below left] {\small $D=B-P_V$};
\node[left] at (0,5) {\small $X$}; \node[left] at (0,-5) {\small $-X$};
\end{tikzpicture}
\end{center}
\slidefig{Left: payoffs at maturity of equity (call on the assets) and risky debt (redrawn from the slide). Right: the risk profile of risky debt $=$ risk-free bond $B$ plus a short put $-P_V$ (redrawn from the slide).}

### The Risk Profile of Risky Debt
\begin{keybox}[Risky debt]
\[
\boxed{\,D=B-P_V\,}
\]
\begin{itemize}[leftmargin=*]
  \item $B$ is **risk-free debt**.
  \item $-P_V$ is the **put sold to equity holders**.
  \item $B-P_V$ is the risk profile of the risky debt.
\end{itemize}
\end{keybox}

### From Risk Profile to Risky-Debt Pricing
The bondholder:
\begin{itemize}
  \item **buys** a risk-free zero-coupon bond $B$ with face value $X$ and maturity $T$;
  \item **sells** a put $P_V$ to equity holders, who can **deliver the firm** when $V_T\leq X$ (limited liability $=$ the right to ``put'' the assets to the creditors at price $X$).
\end{itemize}
\begin{keybox}[Comparative statics (slide)]
**Higher leverage or higher asset volatility** raises $P_V$, **lowers** $D$ and **raises the promised yield**.

$D=B-P_V$: the option model prices **contractual** debt cash flows and therefore produces a **promised return**.
\end{keybox}
\begin{addbox}[Why leverage and volatility raise the put]
More leverage $=$ a higher strike $X$ relative to $V$: the put is closer to (or deeper) in the money. More asset volatility $=$ a higher probability that $V_T$ ends below $X$: every option, puts included, is worth more when volatility rises. In both cases the put sold by creditors is worth more, so the price of debt falls for the same promise $X$, and the promised yield $\left(X/D\right)^{1/T}-1$ rises. The mirror image: equity is a call, so shareholders *gain* from higher asset volatility at the expense of creditors (asset substitution, the agency cost of debt mentioned in Chapter 7).
\end{addbox}

\begin{exbox}[Illustration (not on slides): a one-year zero-coupon debt]
Face value $X=100$, $T=1$, $r_f=5\%$, firm assets $V=150$, put on the assets $P_V=7.24$.
\begin{align*}
B&=\frac{100}{1.05}=95.24 \qquad\qquad D=B-P_V=95.24-7.24=\mathbf{88.00}\\
E&=V-D=150-88=\mathbf{62.00}\\
C_V&=V-B+P_V=150-95.24+7.24=62\quad\text{(check)}\\
\text{Promised yield}&=\frac{100}{88}-1=13.64\%\\
\text{Promised spread}&=13.64\%-5\%=8.64\%
\end{align*}
If volatility rises and $P_V$ goes to 10: $D=85.24$, promised yield $=17.32\%$, and $E=150-85.24=64.76$: value moves from creditors to shareholders while $V$ is unchanged.
\end{exbox}

% =====================================================================
## Promised Return vs Expected Return

### A Simplified Example (slide)
\begin{exbox}[Promised return and expected return]
\begin{center}
\begin{tabular}{@{}lr@{}}
\toprule
Debt market value today & 88\\
Promised payment in one year & 100\\
Default probability & 10\%\\
Recovery in default & 40\\
\midrule
**Expected payoff** & \textcolor{keyred}{**94**}\\
**Promised return** & \textcolor{keyred}{**13.64\%**}\\
**Expected return** & \textcolor{keyred}{**6.82\%**}\\
\bottomrule
\end{tabular}
\end{center}
\begin{align*}
\text{Expected payoff}&=0.90\times100+0.10\times40=90+4=94\\
\text{Promised return}&=\frac{100}{88}-1=13.64\%\qquad\text{(uses the contractual face value)}\\
\text{Expected return}&=\frac{94}{88}-1=6.82\%\qquad\text{(uses the probability-weighted payoff)}\\
\text{Expected-loss yield}&=13.64\%-6.82\%=6.82\%=\frac{0.10\times(100-40)}{88}=\frac{6}{88}
\end{align*}
Expected return uses the **probability-weighted payoff**, not the contractual face value.
\end{exbox}

### The WACC Requires an Expected Cost of Debt
\begin{keybox}[Cost of debt in the WACC]
\[
k_{D,\text{expected}}\approx\text{promised yield}-\text{expected-loss yield}
\]
\begin{itemize}[leftmargin=*]
  \item The option-pricing model returns a **promised** yield because it uses contractual repayment.
  \item The CAPM cost of equity is an **expected** return that compensates only for non-diversifiable risk.
  \item Using the promised yield in the WACC can **overstate $k_D$, overstate the WACC and understate enterprise value**.
\end{itemize}
**Use a consistent expected-return convention for both debt and equity.**
\end{keybox}

\begin{exbox}[Illustration (not on slides): how much the convention matters]
$E/V=60\%$, $D/V=40\%$, $k_e=10\%$, $t=25\%$, FCFO$_1=100$, $g=2\%$.
\begin{align*}
\text{WACC}_{\text{promised }k_D=13.64\%}&=0.6\times10\%+0.4\times13.64\%\times0.75=10.09\%\\
\text{WACC}_{\text{expected }k_D=6.82\%}&=0.6\times10\%+0.4\times6.82\%\times0.75=8.05\%\\
\text{EV}_{\text{promised}}&=\frac{100}{0.1009-0.02}=1{,}236\\
\text{EV}_{\text{expected}}&=\frac{100}{0.0805-0.02}=1{,}653
\end{align*}
Using the promised yield understates EV by about 25\% in this (deliberately risky) example. The default risk would be counted twice: once in the high promised yield, and implicitly again in expected cash flows that already include the possibility of default.
\end{exbox}

\begin{addbox}[Links to the rest of the course]
\begin{itemize}[leftmargin=*]
  \item Chapters 5 and 7: ``(promised) YTM $\geq$ cost of debt, with equality iff the default probability is zero; YTM $-$ $k_d$ $=$ expected default loss''. This module gives the option-pricing reason: the market price of debt reflects $B-P_V$, and the promised yield is computed on the contractual $X$.
  \item Chapter 0: equity $=$ call on the assets $=$ assets $+$ put $-$ riskless bond; risky debt $=$ riskless bond $-$ put. Rearranging $V=C_V+B-P_V$ gives exactly these two lines.
  \item Chapter 4 (APV): the expected bankruptcy cost $\pi_d\times$LGD is the cash-flow counterpart of the same default risk.
  \item Practical rule of thumb used in class: pre-tax $k_d=r_f+$ default spread (Disney). For investment-grade firms expected loss is small and the two conventions are close; for high-yield debt the gap is large.
\end{itemize}
\end{addbox}

% =====================================================================
## Review Questions (slide) and Solutions
\inpractice{Answer through the economic identity, not by memorising the option sign.}

\begin{exbox}[Q1 -- To obtain risky-debt value under put-call parity, the put premium should be:]
(a) Subtracted from the value of risk-free debt\quad (b) Added to the value of risk-free debt\quad (c) Multiplied by the value of risk-free debt

**Answer: (a).** $D=B-P_V$: creditors hold a risk-free bond and have *sold* a put to shareholders (limited liability), so the put premium is subtracted.
\end{exbox}
\begin{exbox}[Q2 -- The cost of debt included in WACC should equal:]
(a) The promised yield\quad (b) The expected return: promised yield *minus* the yield due to expected default loss\quad (c) The expected return: promised yield *plus* the yield due to expected default loss

**Answer: (b).** Use the expected return in the WACC: promised yield minus the expected-default-loss yield. Using the promised yield can overstate the WACC and understate corporate value.
\end{exbox}

\begin{exbox}[Practice MCQs (ours, not on slides)]
**Q3.** Debt with face value 200 due in one year trades at 180; default probability 5\%, recovery 50\%. The expected return on the debt is closest to: (a) 11.1\% (b) 8.3\% (c) 5.6\% (d) 2.8\%.

*Solution*: expected payoff $=0.95\times200+0.05\times100=195$; expected return $=195/180-1=8.33\%$ **(b)**. (a) is the promised yield $200/180-1$.

**Q4.** Holding the face value of debt constant, an increase in the volatility of the firm's assets: (a) raises the value of debt (b) lowers the value of equity (c) lowers the value of debt and raises the promised yield (d) leaves debt unchanged.

*Solution*: **(c)**: higher volatility raises $P_V$, so $D=B-P_V$ falls and $X/D-1$ rises; equity (a call) gains.

**Q5.** Under put-call parity applied to the firm, equity is equivalent to: (a) $B-P_V$ (b) $V-B+P_V$ (c) $V+B-P_V$ (d) $P_V-B$.

*Solution*: **(b)**: $E=C_V=V-D=V-(B-P_V)$.
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
Put-call parity & $S-C+P=B$ $\iff$ $S=C+B-P$; $B=X/(1+r_f)^T$\\
Firm as options & $V=C_V+(B-P_V)$; $E=C_V=\max(V_T-X,0)$; $D=\min(V_T,X)$\\
Risky debt & $D=B-P_V$\\
Equity from parity & $E=V-B+P_V$\\
Promised yield (1 year) & $X/D-1$ (contractual payment)\\
Expected payoff & $(1-\pi_d)X+\pi_d\cdot\text{Recovery}$\\
Expected return on debt & Expected payoff$/D-1$\\
Expected-loss yield & $\pi_d(X-\text{Recovery})/D$ $=$ promised $-$ expected\\
Cost of debt in WACC & $k_{D,\text{exp}}\approx$ promised yield $-$ expected-loss yield\\
Comparative statics & Leverage $\uparrow$ or $\sigma_V\uparrow$ $\Rightarrow$ $P_V\uparrow$, $D\downarrow$, promised yield $\uparrow$, $E\uparrow$ (for given $V$)\\
\bottomrule
\end{tabular}
\end{center}

\needspace{12\baselineskip}
## Common Mistakes and Exam Traps
\begin{trapbox}[Exam traps -- Chapter 14]
\begin{enumerate}[leftmargin=*]
  \item Put-call parity: $S-C+P=B$; the portfolio (long stock, short call, long put) pays the strike in every state.
  \item Risky debt $=$ risk-free bond **minus** a put: $D=B-P_V$ (the put premium is **subtracted**, not added or multiplied).
  \item Equity $=$ call on the firm's assets with strike $=$ face value of debt; creditors have **sold** the put to shareholders (limited liability).
  \item Below $X$ debt absorbs changes in firm value ($D=V_T$, $E=0$); above $X$ equity captures the upside ($E=V_T-X$, $D=X$).
  \item Higher leverage or asset volatility $\Rightarrow$ higher $P_V$ $\Rightarrow$ lower $D$ $\Rightarrow$ higher promised yield.
  \item The option model prices **contractual** cash flows $\Rightarrow$ it gives a **promised** return, not an expected one.
  \item Slide example: price 88, promise 100, $\pi_d=10\%$, recovery 40 $\Rightarrow$ expected payoff 94, promised 13.64\%, expected 6.82\%.
  \item WACC needs the **expected** cost of debt $=$ promised yield $-$ expected-loss yield (**minus**, not plus). Using the promised yield overstates $k_D$ and WACC and **understates** EV.
  \item CAPM $k_e$ is an expected return (non-diversifiable risk only): debt and equity must use the same expected-return convention.
\end{enumerate}
\end{trapbox}
