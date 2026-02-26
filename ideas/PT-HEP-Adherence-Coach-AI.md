---
title: "Physical Therapy HEP Adherence Coach AI"
naics: "62"
industry: "Ambulatory Health Care Services - Physical & Occupational Therapy"
slug: "PT-HEP-Adherence-Coach-AI"
created: "2026-02-25"
status: "draft"
replaces_role: "HEP Follow-Up Coordinator / Rehab Tech"
annual_salary_replaced: "$42,000"
score: 8.2
---

# PT HEP Adherence Coach AI

## Pain Point
Physical therapy clinics prescribe Home Exercise Programs (HEPs), but 60–70% of patients stop doing them within 2 weeks — leading to poor outcomes, re-injury, and lost revenue from early discharge. Most clinics rely on a front-desk staff or tech to make follow-up calls, which is inconsistent, unscalable, and expensive. There is no affordable AI-native solution purpose-built for outpatient PT/OT clinics.

## AI Workflow
1. **Auto-assign HEP from EMR** — integrates with WebPT, Prompt, or Jane App via API/webhook; pulls prescribed exercises per patient visit
2. **Daily check-in SMS/WhatsApp** — AI sends personalized morning nudge with exercise video link, asks 3-question adherence form (Did you do it? Pain level? Questions?)
3. **Smart escalation** — if pain spikes >3 points or patient skips 3+ days, AI flags the case to the therapist with a summary note drafted for the chart
4. **Outcome report at discharge** — auto-generates adherence percentage, symptom trend, and functional progress note for the PT to sign off

## Moat
- Deep EMR integration (clinic won't switch once connected)
- Exercise video library licensed per specialty (PT, OT, SLP)
- HIPAA Business Associate Agreement baked in — most generic AI tools can't touch PHI
- Network effect: aggregate anonymized adherence data → benchmark reports sold to PT chains

## Market Size
- ~40,000 outpatient PT/OT clinics in the US
- Each clinic spends ~$3,500/month on front-desk and rehab tech labor for follow-up
- TAM: $1.68B/year in addressable coordinator labor
- SOM (5% penetration): $84M ARR

## Pricing
- $299/month per clinic location (up to 150 active patients)
- $499/month for multi-location practices (up to 500 active patients)
- Setup fee: $500 one-time for EMR integration

## Competitors
- Keet Health, MedBridge (exercise delivery only, no AI follow-up)
- Generic chatbot platforms (not PT-specific, no EMR integration)
- No direct AI-native HEP adherence competitor identified as of Feb 2026

## Why Now
- CMS expanding remote therapeutic monitoring (RTM) CPT codes 98975-98977 — clinics can now bill insurance for digital check-ins, making this a revenue center, not just a cost saver
- RTM reimbursement ~$50-80/patient/month means product pays for itself if clinic has 10+ active RTM patients
