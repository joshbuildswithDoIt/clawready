# ClawReady — Account Setup Guide

## 1. Calendly (Booking)
- **URL:** https://calendly.com/signup
- **What to set up:**
  - Free account is fine to start
  - Create 3 event types:
    - "ClawReady Starter Setup" — 60 min, $99
    - "ClawReady Pro Setup" — 120 min, $199
    - "ClawReady VIP Setup" — 180 min, $299
  - Enable Stripe integration inside Calendly for payment collection
  - Set availability: your preferred hours (ET)
  - Grab your Calendly link (e.g. `calendly.com/josh-clawready`)

## 2. Stripe (Payments)
- **URL:** https://dashboard.stripe.com/register
- **What to set up:**
  - Business name: ClawReady
  - Business type: Individual/Sole proprietor
  - Connect to your bank account for payouts
  - Once created, connect Stripe to Calendly:
    - Calendly → Integrations → Stripe → Connect
  - This lets Calendly collect payment at booking time

## 3. Domain (Optional but recommended)
- **Suggested:** clawready.com or getclawready.com
- **Where:** Namecheap, Cloudflare, or Google Domains
- **Cost:** ~$10-15/year
- Can connect custom domain to Netlify after deployment

## 4. After Setup
- Give DoIt your Calendly link → I'll update the site
- Give DoIt your custom domain (if purchased) → I'll connect it to Netlify
- Everything else is handled

## Status
- [ ] Calendly account created
- [ ] Stripe account created
- [ ] Stripe connected to Calendly
- [ ] Event types created
- [ ] Domain purchased (optional)
- [ ] Links provided to DoIt
