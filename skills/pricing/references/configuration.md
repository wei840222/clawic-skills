# Configuration

User-dependent variables. Defaults apply until the user states a preference; store them in `<state_root>/pricing/config.yaml`.

| Variable | Type | Default | Effect |
|---|---|---|---|
| business_model | saas-subscription \| usage-based \| one-time \| marketplace \| services \| physical-goods | saas-subscription | Which guide is authoritative and which value metrics are even candidates (`value-metric.md`) |
| currency | text (ISO 4217) | `profile.yaml`, else USD | Currency of every price, floor, and quote, and the code written into every stored amount (Rule 6) |
| target_gross_margin_pct | number (0-100) | 70 | The `m` in every Arithmetic row, and the floor a cost-plus price or a discount must clear |
| discount_floor_pct | number (0-100) | 20 | Largest discount emitted without routing to the approval ladder in `discounting.md` |
| annual_discount_pct | number (0-100) | 17 | The monthly-to-annual prepay discount used in every plan table (two months free = 16.7%) |
| grandfather_policy | forever \| fixed-term \| next-renewal \| none | next-renewal | How every price-increase plan treats existing customers, and what expiry date gets recorded (Rule 7) |
| price_endings | charm \| round \| whole | charm | The final digits of every price emitted: 49 vs 50 vs 47 (`pricing-page.md`) |
| tax_display | exclusive \| inclusive | exclusive | Whether quoted prices include VAT/GST; consumer selling in several markets requires inclusive (`international.md`) |
| price_review_cadence | quarter \| half \| year \| none | year | The row written into `## Due`, and how often a full review is proposed unprompted |

Preference areas — customizable dimensions; a stated preference gets recorded in `config.yaml` and applied from then on:

- **Tooling** — billing platform and whether it is a merchant of record, survey and conjoint tooling, analytics source for cohort reads — affects what a migration can actually execute (`price-increase.md`, `international.md`)
- **Conventions** — tier names, SKU and plan naming, how prices are written in copy, seat versus "editor" versus "member" vocabulary — affects every table and page produced
- **Platform** — markets and countries sold into, purchasing-power posture, payment methods offered, self-serve versus sales-led — affects `international.md` and `pricing-page.md`
- **Risk posture** — appetite for testing on live traffic, willingness to lose customers to a raise, whether discounts are permitted at all, floor rigidity — affects Output Gates, `testing.md`, `discounting.md`
- **Output register** — one number versus a range, table versus deck versus memo, how much of the derivation to show — affects the shape of every answer
- **Cadence** — competitor sweep, discount audit, post-change churn checkpoints, research refresh — every accepted cadence becomes a row in the `## Due` table of `memory.md`
- **Constraints** — channel and advertised-price obligations, investor or board commitments about revenue shape, contractual price protection already given, data covered by an NDA — affects what may be proposed at all
