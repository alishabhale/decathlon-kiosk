# StrideAI: in-store AI shopping agent

**Live demo:** https://alishabhale.github.io/decathlon-kiosk/

PGPBL Group Assignment 1, IIM Kozhikode · PGPBL/07/033. This is an academic concept prototype. It is **store-neutral**: the demo loads a sports and outdoor catalogue, and the same agent works for fashion, footwear or electronics if you swap the catalogue. Products, prices and return statistics are illustrative.

## Why AI when customers still try things on
Trying on stays human. The AI takes over the costly decisions around it:

| Pain in a big store today | What the agent does |
|---|---|
| Thousands of SKUs and no idea what a beginner needs | Builds a complete, budget-fitted set of essentials, with safety items first |
| Generic size charts, so people carry 2 or 3 sizes into the trial room | Predicts the size **for each product** from measurements, the product's fit and return data, and the shopper's history, then shows its confidence |
| Wrong size means getting dressed, queueing and searching again | **Trial-room loop:** tap "too tight" and a runner brings the next size or a close alternative to the cubicle |
| Stock-outs found only at the shelf | Shows stock honestly, suggests alternatives, offers home delivery |
| Overspending and upselling | A hard budget cap, and it asks before going over |

The agent learns within the session. For example, after "too tight in a shoe that runs small", it adjusts the next prediction. It saves anything to the member profile only if the shopper agrees.

## Maps to the 5 slides
| Slide | Where it shows in the kiosk |
|---|---|
| 1. Customer | A beginner or returning shopper, budget-conscious, in store. They choose guest mode or member mode (opt-in) |
| 2. Tasks | Build my kit · Get my size right first time · Trial-room assistant · Compare · Find in store · Just ask |
| 3. How it operates | Learns needs, budget, measurements, purchase and return history, and trial-room feedback. Searches the store catalogue, per-size stock and product fit data. Ranks by rating, level fit, stock and budget |
| 4. Autonomy | Understand (asks) → Search, Shortlist (autonomous) → Size and compare (recommends) → Trial-room re-size (acts, undoable) → Basket (customer tap only) → Payment (human only) |
| 5. Guardrails | Budget cap · safety items never dropped · honest stock · confidence always shown · no camera in the trial room · runner queue capped at 3 · no medical advice · adult confirms children's items · no payment at the kiosk · 90 s idle erase · call staff at any time |

## Demo script (3 minutes)
1. Tap to start → **Scan my member QR** → budget ₹9,000 → Continue.
2. **Get my size right first time** → pick *Running shoe, responsive foam*. It shows EU 43 at high confidence and explains why (runs small, history agrees). → Add to trial-room list.
3. **Trial-room assistant** → *Too tight*. A runner request goes out automatically, and the "learned" panel updates. After about 5 s it arrives → *Fits* → add to basket in EU 44.
4. Try *Not my style* to get alternatives. On a size that is out of stock, it says so honestly and offers delivery.
5. **Just ask** → "My knee hurts when I run" (medical guardrail) · "Can I pay here?" (payment guardrail).
6. Basket → **Send to billing counter** → session erased.

## Run locally
Open `index.html` in a browser. There is no build step, API key or backend.
