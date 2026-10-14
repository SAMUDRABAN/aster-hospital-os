# Aster Hospital OS

A responsive hospital EHR, CRM and operations frontend demo built with Next.js 16, React 19, TypeScript, Geist and Phosphor icons.

## Try the connected stories

Open **Explore the demo** from the sidebar (navigation menu on mobile).

1. **Clinic recovery:** compare alternatives, prepare a proposal, preview as the patient, and accept. The original appointment changes only on acceptance; availability is rechecked.
2. **From booking to follow-up:** book an available slot, open the patient record, prepare and sign a demo encounter, then complete it. Follow-up tasks, billing and communication update together. Select Follow-up as the visit type when booking the next visit.
3. **A coordinated discharge:** complete transport and document dependencies, record discharge, then confirm cleaning. Only then does the bed become available.

Other workspaces include a searchable directory of 120 fictional patients, calendar/list scheduling and waitlist, 48-bed capacity board, referrals, shared inbox, workflow studio with execution receipts, revenue queue, supplies and roster, and a patient companion.

## Run locally

Requires Node 20.9+ (verified on Node 24).

```sh
npm ci
npm run dev
```

Open http://127.0.0.1:3000. Production export: `npm run build` produces `out/`. Checks: `npm test` and `npm run typecheck`.

## Demo boundaries

All records are fictional. State persists only in this browser using localStorage. Workspace preferences → Reset demo restores the seed. There is no production backend, clinical AI, authentication/role enforcement, message delivery, scheduled job, insurance integration or payment processing. Role selection changes the starting workspace only. USD amounts and dates are illustrative. Do not enter real patient information.

## Verification

- Production build and TypeScript passed.
- 11 domain tests passed: clinician/patient collisions, cancellation, stale proposal acceptance, connected rescheduling, discharge sequencing, signed notes and future-visit preservation, duplicate suppression, paused retry, consent and reset.
- gstack Playwright browser checks exercised discharge/cleaning, proposal acceptance, duplicate suppression, missing consent, failed delivery retry, unsigned-note blocking, signing/completing an encounter, booking and persistence across reload.
- Production preview: no console errors; mobile companion measured no horizontal overflow and 16px body copy.
- Desktop and mobile reviewed. An independent initial design review requested five fixes, all implemented. Its follow-up hit the account usage limit; the final five-fix verdict and documentation were completed inline, not independently certified.

Source of truth: `src/lib/domain.ts`; interface: `src/components/HospitalApp.tsx`; styling: `src/app/globals.css`. Product direction is in PRODUCT.md and DESIGN.md. The research and implementation plan is in the parent outputs folder.
