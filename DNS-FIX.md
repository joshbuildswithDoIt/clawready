# ClawReady.com DNS Fix — 2-Minute Guide

## Problem
`clawready.com` currently points to a **Vercel** IP (216.150.x.x) but was never deployed there.
The site is live at `clawready.netlify.app` ✅ — just need DNS to point to Netlify instead.

## Fix (wherever you registered the domain)

### Option A: CNAME (Recommended)
1. Log into your domain registrar (Namecheap, Cloudflare, etc.)
2. Go to DNS settings for `clawready.com`
3. Delete any existing A/CNAME records for `@` or `clawready.com`
4. Add: `CNAME` → `@` → `clawready.netlify.app`
   - If your registrar doesn't allow CNAME on root, use Option B

### Option B: Netlify DNS
1. In Netlify dashboard → Site settings → Domain management
2. Click "Add custom domain" → enter `clawready.com`
3. Follow the prompts — Netlify will give you nameservers
4. Update your registrar's nameservers to Netlify's

### Option C: A Record (if CNAME on root not supported)
1. Use Netlify's load balancer IP: `75.2.60.5`
2. Add: `A` → `@` → `75.2.60.5`
3. Also add: `CNAME` → `www` → `clawready.netlify.app`

## After DNS Change
- Propagation: 5-60 minutes
- Netlify auto-provisions HTTPS via Let's Encrypt
- Verify: `curl -I https://clawready.com` should return 200

## Current Status
- `clawready.netlify.app` → ✅ Working
- `clawready.com` → ❌ Vercel 404 (wrong DNS target)
