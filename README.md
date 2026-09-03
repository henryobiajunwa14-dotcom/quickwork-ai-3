# QuickWork AI v2

A production-oriented starter for an automated digital-product business.

## Included
- Customer accounts/dashboard
- Order history
- Downloadable PDF and DOCX output
- Email delivery through SMTP
- Referral codes and referral rewards
- Subscription plans through Paystack recurring payments
- Admin dashboard
- Paystack webhooks
- SQLite persistence
- Optional AI generation
- Optional Telegram notifications

## Install
Node.js 20+ recommended.

    npm install
    cp .env.example .env
    npm start

Open http://localhost:3000

## Production checklist
- Put the site behind HTTPS.
- Use strong random ADMIN_KEY and SESSION_SECRET.
- Configure Paystack live credentials after testing.
- Configure SMTP.
- Configure your AI provider.
- Set Paystack webhook to:
  https://YOUR-DOMAIN/api/paystack/webhook
- Set Paystack subscription plans in the admin/configuration process.
- Add a real transactional email provider.
- Add rate limiting, CAPTCHA, CSRF protection, audit logs, database backups and stronger session storage before high-volume production.
- Never expose PAYSTACK_SECRET_KEY, SMTP_PASS, AI_API_KEY or ADMIN_KEY to the browser.

## Referral model
A new customer may enter a referral code. When their first paid order succeeds, the referrer receives referral points. The starter uses points as an internal reward balance; you can later add cash-out rules.

## Subscriptions
The Starter and Pro subscription buttons initialize Paystack recurring plans by plan code. Set PLAN_*_CODE in your .env or change the codes in server.js to your real Paystack plan codes.

This is a business starter, not a guarantee of income.
