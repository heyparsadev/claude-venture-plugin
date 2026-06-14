# Unit Economics Guide — Formulas & Health Checks

Every output shows formula + inputs + result. Inputs labeled `measured / sourced / assumption (confidence)`.

## Core formulas

```
ARPU            = revenue / active customers (per month)
Gross margin %  = (revenue − COGS) / revenue
                  COGS: hosting/API per user, payment fees, support cost per user,
                  delivery/fulfillment — NOT founder salary or marketing
Monthly churn % = customers lost in month / customers at month start
Lifetime (mo)   = 1 / monthly churn          (simple; fine early)
LTV             = ARPU × gross margin × lifetime
                = (ARPU × gross margin) / monthly churn
CAC             = total sales+marketing spend / new customers acquired (same period)
                  blended AND per-channel where data allows; founder time priced in at
                  a stated hourly rate (ignoring it flatters services badly)
LTV : CAC       = LTV / CAC
CAC payback     = CAC / (ARPU × gross margin)        → months
Contribution    = price − variable cost per unit      (per order/booking for non-subscription)
Break-even      = fixed costs / contribution per customer  → # customers; map to month via projection
```

## Health thresholds (rules of thumb — cite as such)

| Metric | Trouble | OK | Healthy |
|---|---|---|---|
| LTV:CAC | <1.5 | ~2 | ≥3 (>>5 = likely under-spending on growth) |
| CAC payback | >18 mo | 12–18 | ≤12 (B2B) / ≤6 (consumer) |
| Gross margin | <40% (software) | 40–70% | >70% software · >20–30% e-commerce/services |
| Monthly churn | >7% B2B / >12% B2C | 4–7% / 8–12% | <3% B2B / <6% B2C |

## Type-specific notes

- **Marketplace:** unit = transaction. Take-rate revenue only (GMV is not revenue). Compute CAC per *side*; LTV on the constrained side.
- **Service/agency:** unit = client or engagement. Capacity ceiling is part of the model (hours available). Utilization % drives everything.
- **E-commerce:** unit = order, then customer. First-order contribution after CAC is the survival number; LTV needs repeat-rate evidence, not hope.
- **Freemium:** model free users as COGS; conversion % free→paid is the assumption to stress hardest.

## Scenario discipline

Pessimistic / base / optimistic varying the 2–3 lowest-confidence inputs. Base case uses uncomfortable defaults: early churn high, CAC rising with scale, conversion below hope. Then one **sensitivity line**: "result is most sensitive to <variable>: ±20% moves payback by <X> months → validate that variable next."

## High-inflation / local-currency contexts (e.g. Iran)

- State the inflation and FX assumption; show money columns in local currency AND a hard-currency reference.
- Annual prepay (common locally) changes payback math — model the cash timing, not just accrual.
- Repricing cadence is part of the model: if costs are USD-linked and prices are local, margin erodes monthly — show it.
