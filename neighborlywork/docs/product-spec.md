# NeighborlyWork — Product Specification
*Version 1.0 | April 2026*

---

## Vision
A two-sided marketplace where homeowners post jobs and local workers complete them. Platform holds payment in escrow, releases on completion, and takes a cut automatically. Scales to every home service trade nationwide.

---

## Two Sides

### Posters (Homeowners)
- Post a job with description, photos, budget, and timeline
- Get matched with local workers
- Pay upfront (held in escrow)
- Confirm completion → payment releases
- Rate the worker

### Workers (Contractors / Gig workers)
- Browse and accept posted jobs in their area
- Complete the job
- Mark done + upload photo proof
- Get paid automatically after poster confirms (or 24h auto-release)
- Rate the poster

---

## Core Flow

1. **Poster creates job**
   - Title, description, category, photos
   - Zip code / location
   - Budget (fixed price or open to bids)
   - Timeline (ASAP, this week, flexible)

2. **Worker discovers job**
   - Browse by category and location
   - Accept fixed-price jobs OR submit a bid
   - Chat with poster to clarify

3. **Job accepted**
   - Poster pays upfront → funds held in escrow (Stripe Connect)
   - Worker gets notified, shows up, does the job

4. **Completion**
   - Worker taps "Job done" + optional before/after photo
   - Poster has 24 hours to confirm or dispute
   - If no response → auto-release payment
   - If confirmed → worker gets paid, both rate each other

5. **Platform takes cut**
   - 15% service fee on every transaction (charged to poster)
   - 5% processing fee to worker
   - Net: ~20% per transaction stays with platform

---

## Extra Work Handling (Ernesto's question)
- Worker taps "Request extra work" mid-job
- Describes additional scope + price
- Poster approves or declines in app
- If approved → additional escrow charge added
- If declined → worker completes original scope only
- Prevents scope creep disputes, keeps everything on-platform

---

## Keeping Users On Platform
- All communication via in-app chat (no phone numbers shown until job accepted)
- Payment only via platform (no cash bypass incentive)
- Reputation system — ratings tied to platform account
- Repeat booking button — "Book [Worker Name] again" keeps relationship on-platform
- Worker incentive: faster payment, insurance of getting paid, dispute protection

---

## Categories (Phase 1 — starting with HVAC)
- HVAC (heating, cooling, repair, install)
- Plumbing
- Electrical
- Landscaping / lawn care
- Pool service
- Roofing
- Gutters / windows
- Cleaning
- Handyman / general repair
- Painting

---

## Dispute System
- Poster disputes → funds freeze
- Both sides submit evidence (photos, chat log)
- Under $100 → auto-refund (not worth fighting)
- Over $100 → manual review by NeighborlyWork team (us)
- Over $500 → escalation path + refund policy

---

## Revenue Model
| Source | Rate |
|--------|------|
| Service fee (poster) | 15% of job value |
| Processing fee (worker) | 5% of payout |
| Featured listing (optional) | $9.99/month |
| Background check badge | $19.99 one-time |
| Pro subscription (workers) | $29.99/month for priority placement |

---

## Tech Stack (MVP)
| Layer | Tool |
|-------|------|
| Frontend | React or Next.js |
| Backend | Node.js + Express |
| Database | PostgreSQL (via Supabase) |
| Auth | Supabase Auth |
| Payments | Stripe Connect (escrow) |
| Storage | Supabase Storage (photos) |
| Hosting | Vercel (frontend) + Railway or Supabase (backend) |
| Maps | Google Maps API (job location) |
| Chat | Stream or simple Supabase realtime |

---

## MVP Feature List (Launch)
- [ ] User registration (poster + worker roles)
- [ ] Job posting form
- [ ] Job browse/search by category + zip
- [ ] Job acceptance
- [ ] In-app chat
- [ ] Stripe Connect escrow payment
- [ ] Job completion + photo upload
- [ ] 24h auto-release
- [ ] Dispute flag
- [ ] Star ratings (both sides)
- [ ] Worker profile page
- [ ] Poster dashboard
- [ ] Worker dashboard
- [ ] Email notifications (job posted, accepted, completed, paid)

---

## Phase 2 (post-launch)
- [ ] Bidding system (open bids vs fixed price)
- [ ] Extra work requests mid-job
- [ ] Background check integration
- [ ] Pro subscription tier
- [ ] Mobile app (React Native)
- [ ] Repeat booking
- [ ] Referral program

---

## Go-to-Market
1. **Start in Sacramento** — HVAC, handyman, lawn care
2. **Recruit workers first** — 20-30 workers before launch
3. **Recruit homeowners** — Nextdoor, Craigslist, Facebook Groups
4. **Use NeighborlyWork.com** as the marketing front door
5. **Expand by city** — Roseville, Elk Grove, Folsom, then Bay Area

---

## Milestones
| Milestone | Target |
|-----------|--------|
| Product spec complete | ✅ Done |
| MVP wireframes | Week 1 |
| MVP build start | Week 1-2 |
| MVP launch (Sacramento) | Week 4-6 |
| First transaction | Week 6 |
| 10 active workers | Month 2 |
| $1,000 GMV | Month 2 |
| $10,000 GMV | Month 3-4 |
| Expand to 3 cities | Month 6 |
