# Market Sizing Guide — TAM / SAM / SOM

## Definitions

- **TAM** — total demand for the *job* if everyone who has it bought a solution. Upper bound, not a target.
- **SAM** — TAM filtered to who you can actually serve: geography, segment, channel, language, regulation.
- **SOM** — the share of SAM realistically winnable in ~3 years given competition and your resources. The only number that matters for early decisions.

## Method 1 — Top-down

Industry report total → successive filters.

```
TAM = industry market size (cited report)
SAM = TAM × geography% × segment% × serviceable%
SOM = SAM × realistic share% (justify vs competitor count & strength)
```

Weaknesses: inflated analyst numbers, mismatched category definitions. Always note what the source actually measured (revenue? users? bookings?).

## Method 2 — Bottom-up (more credible — always include)

Build from countable units:

```
SOM = (# target customers reachable) × (adoption %) × (price/yr)
```

Each factor needs grounding:
- **# customers:** census/statistics bureaus, business registries, app store install counts, association member lists.
- **adoption %:** analogous product penetration; early-market default 1–5% of reachable, not 10%+.
- **price:** what alternatives cost today; what discovery interviews suggest people pay.

## Worked example (illustrative format — numbers are placeholders, never reuse them as data)

Venture: appointment no-show reduction SaaS for dental clinics, Iran.

```
# clinics:        ~X dental clinics nationwide [source: ministry/association stats, year]
reachable:        urban, digitized clinics ≈ 40% → 0.4X      (med confidence: proxy = % using any practice software)
adoption (3yr):   3% of reachable (early B2B SaaS norm)      (low confidence)
price:            $Y/mo ≈ 12Y/yr (anchored to current admin-staff cost & competitor pricing) (med)
SOM ≈ X × 0.4 × 0.03 × 12Y per year
```

Present as a **range** (pessimistic/base/optimistic varying the weakest factor), and show which factor the result is most sensitive to.

## Rules

1. Never present a single point number — always a range + confidence.
2. The math must be re-derivable from the report alone.
3. If TAM < ~10× your revenue ambition, say loudly that the market may be too small.
4. Sanity-check against analogous companies: if the claimed SOM exceeds the actual revenue of the market leader, something's wrong.
