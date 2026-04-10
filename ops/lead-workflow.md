# Lead Workflow - NeighborlyWork Sacramento Leads

## Overview
This is the internal ops workflow for receiving homeowner requests, qualifying them, and routing them into either Community Jobs or Pro Installs.

---

## Step 1: Homeowner submits request
- Via homepage lead forms
- Community Jobs or Pro Installs path selected
- Data captured into lead intake sheet / email / form tool

## Step 2: Jarvis receives and qualifies
For Community Jobs:
1. Check zip code is in service area
2. Check contact info is valid
3. Check job is small, affordable, and clear
4. Mark as: QUALIFIED or JUNK

For Pro Installs:
1. Check zip code is in service area
2. Check contact info is valid
3. Check job is a real HVAC / roof / plumbing install or replacement
4. Mark as: QUALIFIED or JUNK

## Step 3: Match to contractor
- Community Jobs: match by trade, zip, and price fit
- Pro Installs: match by zip, trade, and availability
- Assign shared (up to 3 for Pro Installs) or exclusive (1 for small jobs)

## Step 4: Send lead to contractor
- Community Jobs: email worker with job, price, zip, and contact info
- Pro Installs: email 3 contractors with homeowner name, phone, zip, job details
- Subject: "New Lead - [Path] - [Zip]"
- Include urgency and time to contact
- Log in ops/leads-log.csv

## Step 5: Follow up
- If contractor doesn't respond in 48h, reassign
- If homeowner reports no contact, flag contractor
- Log outcomes for quality scoring

---

## Revenue Model
| Path | Fee |
|------|-----|
| Community Jobs under $200 | 10% |
| Community Jobs $200 - $1,000 | 8% |
| Community Jobs over $1,000 | 5% |
| Pro Installs closed repair | $75 |
| Pro Installs closed install / replacement | $350 |

---

## Service Area Zip Codes
95814, 95815, 95816, 95817, 95818, 95819, 95820, 95821, 95822, 95823, 95824, 95825, 95826, 95827, 95828, 95829, 95831, 95832, 95833, 95834, 95835, 95838, 95841, 95842, 95843, 95864 (Sacramento)
95624, 95757, 95758, 95759 (Elk Grove)
95661, 95678, 95747 (Roseville)
95630, 95762 (Folsom)
95610, 95621 (Citrus Heights)
