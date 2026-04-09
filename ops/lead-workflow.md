# Lead Workflow - Sacramento HVAC Quotes

## Overview
This is the internal ops workflow for receiving homeowner requests, qualifying them, and distributing them to contractors.

---

## Step 1: Homeowner submits request
- Via lead-form.html (email to mxjarvis.builds@gmail.com)
- Email subject: "HVAC Quote Request"

## Step 2: Jarvis receives and qualifies
On email receipt:
1. Check zip code is in service area (Sacramento, Elk Grove, Roseville, Folsom, Citrus Heights)
2. Check contact info is valid (name + phone or email)
3. Check job type is real (repair, replacement, install, maintenance)
4. Mark as: QUALIFIED or JUNK

## Step 3: Match to contractor
- Check contractor roster (ops/contractors.csv)
- Match by: zip code, job type, current availability
- Assign shared (up to 3) or exclusive (1) based on their plan

## Step 4: Send lead to contractor
- Email with homeowner name, phone, zip, job type, description
- Subject: "New HVAC Lead - [Job Type] - [Zip]"
- Include: time to contact, urgency level
- Log in ops/leads-log.csv

## Step 5: Follow up
- If contractor doesn't respond in 48h, reassign
- If homeowner reports no contact, flag contractor
- Log outcomes for quality scoring

---

## Lead Pricing (performance-based — pay only on closed jobs)
| Job Type | Fee |
|------|-------|
| Closed repair job | $75 |
| Closed install or replacement | $200 |
| Zip code monthly lock (optional) | $299/mo |

---

## Service Area Zip Codes
95814, 95815, 95816, 95817, 95818, 95819, 95820, 95821, 95822, 95823, 95824, 95825, 95826, 95827, 95828, 95829, 95831, 95832, 95833, 95834, 95835, 95838, 95841, 95842, 95843, 95864 (Sacramento)
95624, 95757, 95758, 95759 (Elk Grove)
95661, 95678, 95747 (Roseville)
95630, 95762 (Folsom)
95610, 95621 (Citrus Heights)
