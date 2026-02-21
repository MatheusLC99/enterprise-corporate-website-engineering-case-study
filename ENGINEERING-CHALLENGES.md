# Engineering Challenges & Solutions

## Legacy System Constraints

The previous website suffered from:

- outdated UI
- poor performance
- limited extensibility

Solution:
Rebuilt architecture using a monorepo full-stack approach.

---

## Form Reliability vs Email Failures

Challenge:
SMTP delivery could fail.

Solution:
Implemented resilient submission flow:
data persists even if email sending fails.

---

## Shared Validation

Problem:
Duplicated validation between frontend and backend.

Solution:
Created shared schemas using Drizzle + Zod,
eliminating mismatches entirely.

---

## UX Conversion Strategy

Challenge:
Institutional websites often lack clear conversion funnels.

Solution:
Designed hero-driven navigation and persistent WhatsApp CTA.