# NeighborlyWork Last Audit — Not-Done Check

Date: 2026-04-26

## Agent-fixable items Zayith named
All seven named agent-fixable audit items are done in the NeighborlyWork repo, with local verification already passing:

1. Patch `transition_lead_status` authorization — **done** in `supabase/004_lead_transitions_v1.sql`.
2. Commit admin RLS policies — **done** in `supabase/007_admin_rls_policies.sql`.
3. Escape DB/user fields in admin surfaces / XSS — **done** across dynamic render paths and covered by tests.
4. Add ops SOP docs + monitoring/reconciliation scripts — **done** in `docs/ops/` and `scripts/run-launch-reconciliation.mjs`.
5. Abuse/rate-limit/CAPTCHA-style controls on intake/signup — **done** via honeypot, minimum-fill-time, and local rate limiting in `app/abuse-guard.mjs` integrated into intake/signup.
6. Quote/verification/change-order timeout automation — **done** in `app/timeout-automation.mjs` and `scripts/run-timeout-automation.mjs`.
7. Draft both contractor vetting options — **done** in `docs/ops/contractor-vetting-options.md` for soft-launch checkbox/manual review and verified CSLB + insurance path.

## Last audit items not done
No additional **agent-fixable local code/docs items** from the last audit remain undone.

Remaining not-done items from the audit are user/provider/product-decision gates:
- Netlify production restoration: blocked by billing/usage decision.
- Resend DNS/domain verification: blocked by DNS action.
- Live production E2E/admin/mobile validation: blocked until Netlify production serves instead of `503 usage_exceeded` and provider readiness exists.
- Supabase live SQL/RPC/Edge Function deployment: blocked by authenticated deploy path/access.
- Twilio SMS validation: only needed if SMS launch validation is required; blocked by login/sender setup.
- Live Stripe: intentionally blocked until explicit approval.
- Business mailing address: required before marketing/cold outreach email sends.
- Analytics/monitoring vendor: product/privacy decision; no hidden tracking installed.
- Contractor vetting path choice: Zayith must choose soft-launch/manual path vs verified CSLB + insurance path.
