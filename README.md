# Snowvixa Labs - Vercel + Backend

## Setup
1. `npm install`
2. Create Stripe products: $199/mo, $599/mo, $1889/mo recurring. Copy Price IDs to Vercel env vars.
3. Get Resend API key from resend.com and add to env vars.
4. Create HubSpot Private App with crm.objects.contacts.write scope. Add token to env vars.
5. Replace Calendly URL in index.html: search `REPLACE WITH YOUR CALENDLY URL`
6. `vercel --prod` or push to GitHub and import to Vercel

## Environment Variables in Vercel
Set these in Project Settings > Environment Variables:
- RESEND_API_KEY
- STRIPE_SECRET_KEY  
- STRIPE_PRICE_STARTER
- STRIPE_PRICE_GROWTH
- STRIPE_PRICE_SCALE
- HUBSPOT_ACCESS_TOKEN

## Deploy
Connect repo to Vercel. Framework: Other. It will auto-detect API routes.

Contact form POSTs to /api/contact. Pricing buttons POST to /api/checkout.
