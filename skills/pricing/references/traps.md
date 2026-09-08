# Traps

| Trap | Why it fails | Do instead |
|---|---|---|
| Cost-plus pricing on software | Marginal cost is near zero, so the method returns a number unrelated to value and usually far too low | Value metric plus a researched range; cost only sets the floor (Rule 1, `value-metric.md`) |
| Matching a competitor's price | Their price encodes their cost base, funding, and segment, none of which you have | Reference price plus quantified differentiation value (`elasticity.md`) |
| A flat percentage raise "across the board" | The cohorts differ in tolerance, and the most valuable ones absorb the least attention | Segment the raise, sequence it, budget the churn (Rule 7) |
| Grandfathering with no end date | The legacy plan becomes a permanent second product with its own support cost and its own migration project later | Fixed term with the expiry recorded in `## Price History` (`price-increase.md`) |
| Discounting to close the quarter | Teaches every buyer to wait for the last week, permanently | Trade the discount for term, prepay, or scope; hold the floor (`discounting.md`) |
| Deep annual discounts to "lock people in" | Past roughly two months free, the discount usually exceeds the churn it prevents | Run the prepay break-even (→ The Arithmetic) before setting `annual_discount_pct` |
| Per-seat pricing on a product used by one person per company | Revenue caps out on day one regardless of the value delivered | Pick a metric that grows (`value-metric.md`) |
| A free tier generous enough to be the product | Conversion remains low because the free tier fulfills all their needs | Limit on the success path; check the free-user cost ceiling (`freemium.md`) |
| Uncapped usage pricing with no alerts | The first surprise invoice ends the account, and the customer tells other buyers | Soft cap, 80% alert, commit tier below the overage rate (`usage-based.md`) |
| Reading a price test on conversion rate | A cheaper price converts better and can still earn less | Revenue per visitor over a full billing cycle, churn at 90 days (Rule 8) |
| Same-page A/B on identical shoppers | Screenshots travel; the trust cost outlives the learning | Cohort, geo, or new-traffic splits, price honored either way (`testing.md`) |
| Converting prices at the spot rate for a new country | Produces prices like 47.13 and ignores purchasing power and local expectations | Country bands with local rounding (`international.md`) |
| Removing a feature people already pay for to build a higher tier | Reads as a price rise plus a downgrade, and it is the version customers post about | Gate new capability upward; leave the existing entitlement intact (`packaging.md`) |
| A pricing decision that lives only in the chat | Re-argued every quarter, and the rejected options get re-proposed by name | `artifacts/` with the date, the rationale, and what was rejected (`memory-template.md`) |
