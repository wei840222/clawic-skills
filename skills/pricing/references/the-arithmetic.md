# The Arithmetic

Everything here is derivable; the point is to run it before the recommendation, not to defend the recommendation afterwards. `m` = contribution margin as a fraction of price.

| Question | Formula | Worked |
|---|---|---|
| How much volume can a price rise cost me? | `x / (m + x)` | +10% at m=0.70 → up to 12.5% of units can leave before profit falls |
| How much volume must a cut win back? | `d / (m − d)` | −10% at m=0.70 → +16.7% units needed just to stand still |
| What does a discount cost in profit? | `discount% ÷ margin%` | 20% off at 70% margin → 28.6% of that deal's gross profit |
| Is annual prepay worth two months free? | 12 × (1 − d) vs expected months paid, where expected months in a year at monthly churn `c` = `(1 − (1 − c)^12) / c` | d = 16.7% → break-even near 3% monthly logo churn; above it, annual prepay wins on cash and on retention |
| Can the free tier pay for itself? | monthly cost per free user ≤ `r × m$ × L` | 1%/month conversion, 20 USD monthly contribution, 24-month life → ceiling of 4.80 USD per free user per month |
| What does the processor take on a small ticket? | `(rate × p + fixed) / p` | 2.9% + 0.30 USD on a 5 USD charge = 8.9%; on 50 USD = 3.5% — the fixed fee is the whole argument for bundling and annual billing |
| What day rate clears my target? | `income × (1 + overhead) / (working days × utilization)` | 120k target, 30% overhead, 220 days, 60% utilization → 156,000 / 132 ≈ 1,180 per day |
| Is this price above the floor? | contribution = `price − variable cost`; floor = `variable cost / (1 − target_gross_margin_pct)` | 30 USD variable cost at a 70% margin target → floor of 100 USD; below it, volume is something you are paying for |
| What must a marketplace take rate cover? | `take × GMV per transaction ≥ payments + trust/support + blended CAC of both sides ÷ transactions per cohort` | Thin GMV per transaction is why low take rates only work at high repeat frequency (`marketplace.md`) |
