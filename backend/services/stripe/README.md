# Stripe Integration

This module handles integration with Stripe APIs.

---

## Prerequisites

- An active Stripe account
- Access to create developer apps
- Stripe SDK installed (added to requirements.txt)

---

## Step 1: Login with Stripe

1. Go to the Stripe developer dashboard:  
   [Developer Dashboard](https://dashboard.stripe.com)

2. Log in with your account.

---

## Step 2: Get API Credentials

After logging in, you need to get the following credentials:

- Client ID
- Secret Key

To find these credentials in the Stripe Dashboard:

Try the following URLs for getting the above credentials:

Client ID - https://dashboard.stripe.com/test/settings/connect/onboarding-options/oauth

Secret Key - https://dashboard.stripe.com/test/apikeys

or try the below method:

- **Client ID**: Navigate to **Settings > Connect settings**. Look for the "Onboarding options" section and under the OAuth tab you can find your Client ID (it starts with `ca_`).
- **Secret Key**: Navigate to **Developers > API keys**. You'll see both your publishable key and secret key; copy the secret key.

---

## Step 3: Add Environment Variables

Update your `.env` file:

```env
STRIPE_CLIENT_ID=your_client_id_here
STRIPE_SECRET_KEY=your_secret_key_here
```

If you are managing frontend and backend environments separately:

**Frontend `.env`:**
```env
STRIPE_CLIENT_ID=your_client_id_here
```

**Backend `.env`:**
```env
STRIPE_SECRET_KEY=your_secret_key_here