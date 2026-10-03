# Handoff — Stripe Payment Link for Contract Clarity Review

**Status:** IN PROGRESS (user completing manually on phone)
**Created:** 2026-10-03 ~01:00 PDT
**Objective:** Create a live $295 Stripe Payment Link for the Contract Clarity Review service and wire it into the offer page.

---

## 1. Product spec (exact — use verbatim)

| Field | Value |
|---|---|
| Product name | `Contract Clarity Review — CATCHY INN LLC` |
| Price | **$295.00 USD**, one-time |
| Description | `Fixed-scope plain-English review of one business contract (under 25 pages): every financial obligation mapped with verbatim clause citations, delivered in 3 business days. Consulting only — not legal advice.` |
| Checkout fields | Customer name (required), email (required), phone (optional) |

Offer page (needs the link once live): https://josiahwilson-bit.github.io/catchyinn-website/contract-review.html

---

## 2. Current state (as of 2026-10-03 ~00:55 PDT)

- [x] Offer page published: https://josiahwilson-bit.github.io/catchyinn-website/contract-review.html
- [x] New **standard** Stripe account created: `acct_1UMNgZRA7QVsnLZb`
- [~] Stripe onboarding in progress on user's phone (was on business-description step at 00:52, then welcome checklist)
- [ ] Toggle Test → Live
- [ ] Create payment link (Payment Links → Create)
- [ ] Wire link URL into `contract-review.html`

---

## 3. Key facts (do not re-derive)

- **Correct Stripe login email:** `zppcurl@gmail.com` (z-p-p). The spelling `zzpcurl@gmail.com` (z-z-p) **does not exist** — Google confirmed "couldn't find this account."
- **Login method:** Google OAuth ("Continue with Google"), not password. All password attempts are doomed.
- **Old account** `acct_1ULzFMEIWaG4NPui` is **Stripe Express** (GitHub Sponsors payouts). Express dashboards **cannot** create Payment Links — do not waste time there.
- **New account** `acct_1UMNgZRA7QVsnLZb` is a standard account and the correct target.
- Payment Links must be created in **Live mode**, not Test mode.

---

## 4. Blockers encountered (2026-10-03, resolved by pivoting)

1. Six Stripe password attempts rejected — root cause: wrong email spelling (`zzpcurl` ≠ `zppcurl`).
2. Password reset triggered for the wrong address went nowhere (address doesn't exist).
3. Google password for `zppcurl@gmail.com` rejected from agent browser.
4. User's own `hillwinks@gmail.com` login rejected from agent browser.
5. Conclusion: agent-side authentication is not viable. User completes onboarding + link creation manually on phone (logged-in session lives there).

---

## 5. Next steps (whoever picks this up)

1. Confirm user finished Stripe onboarding and toggled to **Live** mode.
2. Get the payment link URL from the user.
3. Edit `contract-review.html` in https://github.com/josiahwilson-bit/catchyinn-website — replace the "payment via Stripe after fee confirmation" text with the live payment link button.
4. Commit + verify the page renders the link.
5. (Optional) Test the link with a $0.50 test charge or Stripe test clock — only with explicit approval.

---

## 6. Machine-readable state

See `STATE.json` in this repo.
