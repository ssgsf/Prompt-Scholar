# PromptScholar - Complete Setup Guide

## 🎓 What You Have

A complete web application for PromptScholar with:
- Professional landing page
- Prompt improvement tool
- Prompt library (18+ prompts to start)
- Pricing page
- Legal pages (Terms, Privacy)
- Stripe payment integration setup
- Responsive design
- SEO-optimized

## 📦 Files Included

```
promptscholar/
├── index.html          # Landing page (MAIN)
├── library.html        # Prompt library  
├── improve.html        # Prompt improvement tool
├── pricing.html        # Pricing & signup
├── style.css           # All styling
├── script.js           # Functionality
├── prompts-data.json   # Prompt database
├── terms.html          # Terms of Service
├── privacy.html        # Privacy Policy
├── ethical-use.html    # Ethical AI guide
└── README.md           # This file
```

## 🚀 DEPLOYMENT STEPS (30 Minutes)

### Step 1: Register Domain (5 minutes)

1. Go to **Namecheap.com** or **GoDaddy.com**
2. Search: "promptscholar.com"
3. If available → Buy it ($12/year)
4. If taken → Try promptscholar.io or promptscholar.ai

### Step 2: Deploy to Vercel (10 minutes)

1. Go to **vercel.com**
2. Click "Sign Up" (use GitHub, Google, or Email)
3. Click "Add New Project"
4. Choose "Import Git Repository" OR "Deploy from folder"
5. **Upload these files** (drag the entire promptscholar folder)
6. Click "Deploy"
7. Your site is now live at: `yourproject.vercel.app`

### Step 3: Connect Custom Domain (5 minutes)

1. In Vercel dashboard → Click your project
2. Go to "Settings" → "Domains"
3. Add your domain: `promptscholar.com`
4. Follow Vercel's instructions to update DNS at Namecheap
5. Wait 10-60 minutes for DNS propagation

### Step 4: Set Up Stripe (10 minutes)

1. Go to **stripe.com** → Sign up
2. Go to "Products" → Create new product:
   - Name: "PromptScholar Premium"
   - Price: $4.99/month recurring
3. Get your **Publishable Key** and **Secret Key**
4. In pricing.html, replace:
   ```javascript
   // Line ~50
   const stripe = Stripe('pk_test_YOUR_KEY_HERE');
   ```
5. For production: Switch to live keys in Stripe dashboard

## 💳 PAYMENT SETUP (Detailed)

### Stripe Checkout Integration

Your app uses Stripe Checkout (easiest method). Here's what happens:

1. User clicks "Subscribe" button
2. Redirected to Stripe's secure checkout
3. After payment → Redirected back to success page
4. You manage access manually at first

### Managing Subscribers (Manual - Month 1)

**Simple Approach:**
1. When someone subscribes, Stripe sends you an email
2. You manually give them access (share a password or login)
3. Track subscribers in a spreadsheet

**Better Approach (Later):**
- Set up Stripe webhooks to auto-update user access
- Use Firebase for user database
- Automate everything
- (Come back to me for help with this!)

## 📧 CUSTOMER SUPPORT SETUP

### Create Support Email

**Option A: Gmail (Free)**
1. Create: support@gmail.com  
2. Use for inquiries
3. Forward to your personal email

**Option B: Custom Domain Email (Professional)**
1. Use Zoho Mail (free for 1 address)
2. Set up: support@promptscholar.com
3. Much more professional

### FAQ Page
Add common questions to reduce support volume:
- "Is this cheating?" → No, it's learning
- "Which AI works best?" → Claude, ChatGPT, any
- "Refund policy?" → 30-day money back
- "How to cancel?" → Email us anytime

## 📊 ANALYTICS SETUP

### Google Analytics (Free)

1. Go to **analytics.google.com**
2. Create account → Add property
3. Get tracking ID: `G-XXXXXXXXXX`
4. Add to ALL HTML files before `</head>`:
   ```html
   <!-- Google Analytics -->
   <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
   <script>
     window.dataLayer = window.dataLayer || [];
     function gtag(){dataLayer.push(arguments);}
     gtag('js', new Date());
     gtag('config', 'G-XXXXXXXXXX');
   </script>
   ```

### Track Key Metrics

Monitor these in Google Analytics:
- Daily visitors
- Page views
- Time on site
- Conversion funnel: Home → Library → Pricing → Purchase

## 🎯 LAUNCH CHECKLIST

### Pre-Launch (Do This Before Going Public)

- [ ] Domain purchased and connected
- [ ] All pages load correctly
- [ ] Mobile responsive (test on phone)
- [ ] Stripe test payment successful
- [ ] Support email set up
- [ ] Google Analytics added
- [ ] Social media accounts created (@promptscholar)
- [ ] 10 beta testers lined up
- [ ] Legal pages reviewed

### Launch Day

- [ ] Post on Reddit (r/college, r/GetStudying)
- [ ] Post on ProductHunt
- [ ] Email beta testers
- [ ] Post on LinkedIn
- [ ] Create 3 TikToks
- [ ] Monitor analytics obsessively
- [ ] Respond to ALL comments/questions

### Week 1 Post-Launch

- [ ] Daily content posting (TikTok/Instagram)
- [ ] Respond to customer inquiries <24hrs
- [ ] Fix any bugs reported
- [ ] Add 10-20 more prompts
- [ ] Review metrics: signups, conversions, churn

## 🐛 TROUBLESHOOTING

### Site Not Loading
- Check Vercel deployment logs
- Ensure all file names are correct
- Test in incognito mode (clear cache)

### Stripe Not Working
- Verify API keys are correct
- Check Stripe dashboard for errors
- Test in test mode before live mode

### Mobile Display Issues
- CSS is responsive, but test on actual devices
- Use Chrome DevTools → Mobile view
- Fix any overflow or sizing issues

## 📈 GROWTH STRATEGIES

### Month 1: Validation
- Goal: 100 signups, 20 paying
- Focus: Reddit, organic content
- Budget: $0-300 (optional ads)

### Month 2-3: Traction
- Goal: 300 signups, 75 paying
- Focus: TikTok, influencer outreach
- Budget: $300-500/month ads

### Month 4-6: Scale
- Goal: 1,000 signups, 250 paying
- Focus: Paid ads, partnerships
- Budget: $500-1,000/month ads

## 🔄 UPDATING PROMPTS

### Come Back to Claude Every 2-4 Weeks

**Say this:**
"I need to add 30 new prompts to PromptScholar. Topics: [Biology genetics, Psychology disorders, etc]. Use the same format as existing prompts."

I'll generate them, you copy-paste into prompts-data.json, redeploy. Takes 15 minutes total.

## 💰 REVENUE TRACKING

### Simple Spreadsheet

Track monthly:
- New signups
- Paid conversions
- Churn (cancellations)
- MRR (Monthly Recurring Revenue)
- CAC (Customer Acquisition Cost)
- LTV (Lifetime Value)

### Stripe Dashboard

Shows automatically:
- Total revenue
- Active subscriptions
- Failed payments
- Refunds

## 🎓 NEXT STEPS

### Immediately (Today)
1. Download all files from this chat
2. Test locally (open index.html in browser)
3. Make sure everything looks good

### This Week
1. Deploy to Vercel
2. Buy domain
3. Set up Stripe
4. Recruit beta testers

### Next 2 Weeks
1. Beta test with 10-20 people
2. Gather feedback
3. Fix bugs
4. Get testimonials
5. Prepare launch content

### Launch (Week 3)
1. Go public
2. Execute marketing plan
3. Monitor metrics
4. Iterate based on data

## 🆘 NEED HELP?

### Come Back to Claude

For:
- Adding more prompts
- Fixing bugs
- Adding features
- Marketing advice
- Technical issues

### Useful Resources

- Vercel Docs: vercel.com/docs
- Stripe Docs: stripe.com/docs
- Web Dev Help: stackoverflow.com
- Design Inspiration: dribbble.com

## 🎉 YOU'VE GOT THIS!

Remember:
- Done is better than perfect
- Launch and iterate
- Listen to users
- Stay consistent with marketing
- Don't give up in month 2-3 (slow growth is normal)

Your MVP is ready. Time to ship it! 🚀

---

© 2026 PromptScholar | Built with Claude
