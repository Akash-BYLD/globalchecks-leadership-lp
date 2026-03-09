# GlobalChecks Leadership Verification - Landing Page

## Overview
Lead generation landing page for GlobalChecks Leadership Verification service.
Deployed on Vercel with Formspree form backend.

## Tech Stack
- **Frontend:** Static HTML/CSS/JS (no framework, fast load)
- **Hosting:** Vercel (free tier)
- **Form Backend:** Formspree (free, 50 submissions/month)
- **Analytics:** GA4 + GTM + Microsoft Clarity (all free)
- **CDN:** Vercel Edge Network (automatic)

## Setup Instructions

### Step 1: Create Formspree Account
1. Go to https://formspree.io and sign up (free)
2. Click "New Form" → name it "Leadership Verification Leads"
3. Copy your form endpoint (looks like: `https://formspree.io/f/xABcDeFg`)
4. In `public/index.html`, find `YOUR_FORMSPREE_ID` and replace with your form ID

### Step 2: Push to GitHub
```bash
git init
git add .
git commit -m "Initial commit - Leadership Verification LP"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/globalchecks-leadership-lp.git
git push -u origin main
```

### Step 3: Deploy on Vercel
1. Go to https://vercel.com and sign up with your GitHub account
2. Click "Add New Project"
3. Import the `globalchecks-leadership-lp` repository
4. Framework Preset: Select "Other"
5. Click "Deploy" — that's it. Live in ~30 seconds.

### Step 4: Custom Domain (Optional but Recommended)
1. In Vercel dashboard → Project → Settings → Domains
2. Add: `leadership.globalchecks.in`
3. Vercel will show you DNS records to add
4. Go to your domain registrar (GoDaddy/Namecheap/Cloudflare)
5. Add CNAME record: `leadership` → `cname.vercel-dns.com`
6. Wait 5-10 minutes for DNS propagation
7. Vercel auto-provisions SSL certificate

### Step 5: Analytics Setup
1. **GA4:** Replace `G-XXXXXXXXXX` in index.html with your GA4 Measurement ID
2. **GTM:** Replace `GTM-XXXXXXX` in index.html with your GTM Container ID
3. **Clarity:** Replace `CLARITY_ID` in index.html with your Clarity project ID
4. Get Clarity ID from https://clarity.microsoft.com (free signup)

### Step 6: Test
- [ ] Submit test form entry
- [ ] Verify email notification received
- [ ] Check Formspree dashboard for submission
- [ ] Test on mobile (iPhone + Android)
- [ ] Verify GA4 is receiving events (GA4 Realtime report)
- [ ] Verify Clarity is recording sessions

## Making Changes
1. Edit files locally
2. `git add . && git commit -m "description" && git push`
3. Vercel auto-deploys in ~10 seconds
4. Changes are live immediately

## File Structure
```
globalchecks-leadership-lp/
├── vercel.json          # Vercel config (routing, headers, security)
├── README.md            # This file
└── public/
    ├── index.html       # The landing page (everything in one file)
    └── favicon.ico      # Site favicon (add your own)
```

## Form Submissions
- **Dashboard:** https://formspree.io/forms (login to view all submissions)
- **Email:** Notifications sent to your registered email on every submission
- **Export:** CSV export available from Formspree dashboard
- **Upgrade path:** When you exceed 50/month, upgrade Formspree ($8/mo for 100) or migrate to a CRM integration

## Performance Targets
- LCP: < 1.5s (no heavy images, fonts preloaded)
- CLS: < 0.05 (all elements have explicit dimensions)
- INP: < 100ms (minimal JS, no framework overhead)
