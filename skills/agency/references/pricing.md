# Pricing and Proposals

## Rate Card Structure

Maintain in <state_root>/config.md:

```markdown
### Hourly Rates
- Strategy/Senior: $X
- Execution/Mid: $Y
- Junior/Support: $Z

### Project Minimums & Margin Targets
- Discovery call: $0 or a configured qualification fee
- Standard Project Minimum: [configured amount]
- Retainer Minimum: [configured monthly amount]
- Target Gross Margin: [configured range]
- Target Net Margin: [configured range]

### Multipliers and Risk Adjustments
- Rush: [configured uplift based on available capacity]
- Complex integration or unknown technology: [configured risk buffer]
- Enterprise client (extra compliance or meetings): [configured uplift]
- Retainer volume discount: [configured discount tied to a defined commitment]
```

## Estimation Process

Given a scope:

1. **Break into phases:**
   - Discovery/intake
   - Strategy/planning
   - Execution/production
   - Review/revision rounds
   - Delivery/handoff

2. **Estimate hours per phase:**
   - Be specific: "Homepage design: 6h, inner page template: 3h"
   - Apply the configured contingency for uncertainty and approved scope risk
   - Account for client communication time

3. **Apply multipliers:**
   - Check complexity indicators
   - Check timeline pressure
   - Check client type

4. **Compare to historical:**
   - Search `<state_root>/knowledge/` for similar projects
   - Adjust if past estimates were off

## Proposal Structure

Generate PDF with:

```
1. CONTEXT
   - Why they came to us
   - What we heard as the core problem

2. APPROACH
   - How we'll solve it (methodology)
   - Why this approach works

3. DELIVERABLES
   - Specific items they receive
   - Format and quantity

4. TIMELINE
   - Phases with dates
   - Client dependencies/approvals needed

5. INVESTMENT
   - Price (or range)
   - What's included
   - What's not included
   - Payment terms

6. NEXT STEPS
   - How to proceed
   - What we need from them
```

## Pricing Models

- **Hourly:** Best for maintenance, ambiguous scopes, and consulting. Limits scale.
- **Project-based (Fixed):** Best for well-defined deliverables. Requires strict scope management.
- **Retainer:** Best for ongoing support, SEO, or continuous marketing. Provides predictable MRR.
- **Value-based:** Best for high-impact projects (e.g., pricing based on % of revenue generated). Highest margin, highest risk.

## Pricing Requirements

- Complete discovery and understand scope fully before providing a quote.
- Reduce scope proportionally when applying a discount to train clients appropriately.
- State revision limits clearly and prominently in the proposal.
- Account for client communication time using the agency's historical estimate data.
- Include handoff and documentation time in the final estimate.

## Version Control

When client requests changes to proposal:
- Save v1 before editing
- Track what changed and why
- Note who requested the change
- If scope reduced, reduce price explicitly

## Historical Comparison

Before finalizing estimate, search:
```
Similar projects in <state_root>/knowledge/:
- What was estimated vs actual
- What caused overruns
- What would we do differently
```
