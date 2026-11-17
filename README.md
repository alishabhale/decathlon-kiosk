# StrideAI: In-store AI Shopping Agent (Decathlon concept)

PGPBL Group Assignment 1, IIM Kozhikode. An academic concept prototype that is not affiliated with Decathlon. Products and prices are illustrative.

## Run it
Open `index.html` in any browser. It needs no build step, no API key and no backend.

## Host on GitHub Pages
1. Create a public repo, for example `stride-kiosk`, and upload `index.html` (and this README).
2. Go to Settings → Pages → Source: *Deploy from a branch* → Branch `main`, folder `/ (root)` → Save.
3. After about a minute, it is live at `https://<username>.github.io/stride-kiosk/`.

## What the prototype demonstrates (maps to the 5 slides)
| Slide | Where to see it in the kiosk |
|---|---|
| 1. Customer | Beginner/returning sports shopper, budget-conscious, in-store. Guest vs member (opt-in) entry screen |
| 2. Tasks (≥3) | Starter kit builder · Size finder · Product comparison · Find in store · Free-text "Just ask" |
| 3. How it operates | Learns sport, level, budget (+ purchase history and saved size if member); searches store catalogue & live stock; ranks by rating, level-fit, stock, budget |
| 4. Autonomy | Right panel: Understand needs (asks) → Search, Shortlist (autonomous) → Compare (recommends) → Add to basket (customer tap only) → Payment (human only) |
| 5. Guardrails | Budget cap with consent to exceed · safety items never dropped · no medical advice · honest out-of-stock · child items need adult · no payment at kiosk · 90 s idle auto-erase · no dark patterns · call-staff override |

## Demo script (2 minutes)
1. Tap to start → **Scan my member QR** → keep Running/beginner, set budget ₹6,000 → Continue (shows the personal "replace your shoes" insight).
2. **Build my starter kit** → point at the budget meter and the decision log → *Add whole kit* (shows the confirmation step).
3. **Compare products** → the out-of-stock option is flagged, and the recommendation leaves the decision to you.
4. **Just ask** → "My knee hurts when I run" (medical guardrail) → "Can I pay here?" (payment guardrail).
5. Change sport to Cycling with a ₹3,000 budget → kit keeps the helmet and lights and drops the bike (safety-first guardrail).
6. Basket → **Send to billing counter** → session erased.
