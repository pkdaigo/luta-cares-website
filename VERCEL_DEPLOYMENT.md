# Vercel Deployment Guide

## Quick Deploy to Vercel

### Option 1: Via Vercel Dashboard (Recommended)

1. Go to [Vercel Dashboard](https://vercel.com/new)
2. Click "Import Project"
3. Select "Import Git Repository"
4. Choose: **pkdaigo/luta-cares-website**
5. Configure:
   - **Framework Preset:** Next.js (or leave auto-detect)
   - **Root Directory:** ./
   - **Build Command:** npm run build (or leave default)
   - **Output Directory:** .next (or leave default)
6. Click "Deploy"

### Option 2: Via Vercel CLI

`bash
# Install Vercel CLI globally
npm i -g vercel

# Navigate to project
cd C:\Users\PKPho\luta-cares-website

# Deploy
vercel

# Follow prompts:
# - Link to existing project? No
# - What's your project's name? luta-cares-website
# - Which directory is your code located? ./
# - Want to override the settings? No
`

### Option 3: One-Click Deploy

Click the button below to deploy:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/pkdaigo/luta-cares-website)

## Environment Variables (if needed)

Add these in Vercel Dashboard → Settings → Environment Variables:

`
NEXT_PUBLIC_API_URL=https://api.lutacares.com
DATABASE_URL=your_database_url
`

## Custom Domain Setup

1. Go to Vercel Dashboard → Your Project → Settings → Domains
2. Add your domain: **lutacares.com** or **www.lutacares.com**
3. Follow DNS configuration instructions
4. Typical DNS records:
   - **A Record:** @ → 76.76.21.21
   - **CNAME:** www → cname.vercel-dns.com

## Automatic Deployments

✅ **Production:** Push to master branch → auto-deploys to production
✅ **Preview:** Push to any branch → auto-deploys to preview URL
✅ **Pull Requests:** Automatic preview deployments with unique URLs

## Vercel Project Settings

**Recommended Settings:**
- **Node.js Version:** 18.x
- **Install Command:** npm install
- **Build Command:** npm run build
- **Output Directory:** .next (for Next.js) or dist
- **Development Command:** npm run dev

## Monitoring & Analytics

Enable in Vercel Dashboard:
- ✅ **Web Analytics:** Real-time visitor data
- ✅ **Speed Insights:** Performance metrics
- ✅ **Log Drain:** Error tracking

## Troubleshooting

**Build fails?**
- Check Node.js version (18+ required)
- Verify all dependencies in package.json
- Check build logs in Vercel Dashboard

**Domain not working?**
- Wait 24-48 hours for DNS propagation
- Verify DNS records in domain registrar
- Use Vercel's DNS checker tool

## Support

- Vercel Docs: https://vercel.com/docs
- GitHub Issues: https://github.com/pkdaigo/luta-cares-website/issues
- Vercel Support: https://vercel.com/support

---

**Repository:** https://github.com/pkdaigo/luta-cares-website
**Created:** 2026-06-25 15:22:26
