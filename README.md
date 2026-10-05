# Fieldstone Marketing Site

A single, self-contained landing page — no build step, no dependencies. Just `index.html`.

## Deploying later (when you're ready)

This is a **separate site** from the CRM app itself (your `claude-crm-project` deployment) — it's meant to live at your main domain (e.g. `fieldstone.com`) and link out to the actual app for login/signup (e.g. `app.fieldstone.com` or wherever the CRM is hosted).

**Easiest path — Vercel, same as the CRM app:**
1. Push this folder to its own GitHub repo (or a subfolder of an existing one).
2. In Vercel: "Add New Project" → select the repo → Framework Preset: **Other** (it's static HTML, no build command needed) → Deploy.
3. Once live, update the `/login` and `/signup` links in `index.html` to point at your actual CRM app's URL (currently they're relative links assuming this site and the app share a domain).

## What to customize before going live

- The two `/login` and `/signup` href attributes (search for them — there are a few) should point at your real app URL if this ends up on a different domain than the CRM itself.
- Pricing (₹4,999/seat/year) is pulled from what's actually in your billing system — update both places if that price changes.
- Swap the logo mark/wordmark if you ever rename the product away from "Fieldstone."
