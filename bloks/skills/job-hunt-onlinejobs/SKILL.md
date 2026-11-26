---
name: job-hunt-onlinejobs
description: Scout OnlineJobs.ph and remote job listings, catch hidden attention checks and red flags, and draft tailored proposals.
license: MIT
metadata:
  title: OnlineJobs.ph & Remote Job Scout + Proposal Drafter
  version: "1"
  author: AORG
  tags: assistant, workflow
---

Use this when the user needs to scout OnlineJobs.ph and remote job listings, catch hidden attention checks and red flags, and draft tailored proposals.

1. Confirm the requested scope and available evidence, then follow the workflow below. Reuse answers already supplied.

# OnlineJobs.ph & Remote Job Scout + Proposal Drafter

## Use this when

The user asks to look for job postings on OnlineJobs.ph (or Upwork, LinkedIn, WeWorkRemotely, etc.), evaluate a job description, or write a tailored cover letter/application.

## Process

1. **Confirm Target Criteria:** Match listings against the user's target roles (Full-Stack, Backend, Frontend, AI/Automation, DevOps, and strictly technical/operational VA roles), tech stack, minimum hourly/monthly rate (USD/PHP), weekly hours (part-time, full-time, gig), and timezone overlap.
2. **Job Evaluation & Fit Table:** Extract Job Title, Employer/Company name, Offered Rate & Hours, Required Stack, Match Score (`Strong Match` / `Worth Considering` / `Skip` / `NOT SUITABLE`), and Source URL.
3. **Hard Role Exclusions & VA Scope Limit:**
   - **Strict NO Marketing, Sales, or Community Roles:** Immediately mark `NOT SUITABLE` / `Skip` and NEVER auto-apply to ALL marketing, sales, creator/affiliate management, social media management, ad/SEO outreach, email/SMS marketing, funnel building, cold/warm outreach, lead-gen, appointment setting, and community manager/moderator roles (including Discord/Slack "Community Superstar", hype, or member engagement roles)—even if the listing mentions Discord, Slack, Google Sheets, KPIs, or CRM.
   - **Strict VA Scope Limit (Transferable Technical/Ops Only):** Limit VA roles strictly to duties backed by verified technical/operational transferable skills: Technical VA, Automation/Webhook VA, Data/SQL/Reporting/Sheet-ops VA, Internal Portal/System Admin VA, and QA/Bug-Triage VA. Exclude generic VA, executive/personal VA, creator/community VA, e-commerce store-hype VA, and marketing/sales-ops VA. Daily Discord, Slack, or Google Sheets usage does NOT make community or marketing VA roles transferable. Borderline VA or marketing-adjacent roles must be marked `Skip` / `NOT SUITABLE` (or at most `NEEDS REVIEW`, NEVER `AUTO-APPLY ELIGIBLE`).
4. **Hidden Attention-Check Detector:** Scan the full listing text for secret screening instructions buried by employers (e.g., *"Put the word MANGO in your subject line"* or *"Answer these 3 questions in the first line"*) and call them out at the top.
5. **Red-Flag & Scam Filter:** Flag lowball rates for 5-in-1 roles, unpaid "trial projects" that build real production features, requests to move immediately to Telegram/WhatsApp, or invasive screen-monitoring demands.
6. **Anti-AI-Slop Proposal Drafter:** Write a short, direct, human-sounding OnlineJobs.ph subject line and message that obeys any attention-check keyword first, maps 2-3 concrete past outcomes to their stack, asks one smart technical/workflow question, and avoids generic AI openings.

## Output

Use: Job Match Table, Hidden Attention-Check Alert, Red-Flag Assessment, and Copy-Ready Subject Line + Proposal Draft.

## Guardrails

- Never draft an auto-apply pitch or submit an application for excluded marketing, sales, community-mod/hype, generic VA, or marketing-adjacent VA roles; mark them `NOT SUITABLE` / `Skip` (or at most `NEEDS REVIEW` for genuinely ambiguous technical/ops cases, NEVER `AUTO-APPLY ELIGIBLE`).
- Never bypass logins, CAPTCHAs, or anti-bot gates, and never submit a job application automatically without explicit user action.

Not for: Acting outside the requested scope or presenting unverified work as completed.
Return: The requested draft or result, supporting evidence where relevant, and any unresolved assumptions or blockers.
Approval: Ask before sending, publishing, purchasing, booking, cancelling, deleting, changing live systems, installing dependencies, committing or pushing, or enabling recurring automation. Drafts and reviews alone do not authorize those actions.
