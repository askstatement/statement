# PayPal Integration

This module handles integration with PayPal APIs.

---

## Prerequisites

- An active PayPal Developer account
- Access to create developer apps

---

## Step 1: Create a PayPal App

1. Go to the PayPal developer dashboard:  
   [Developer Dashboard](https://developer.paypal.com/dashboard/applications/sandbox)

2. Log in with your account.

3. Create a new app (select **Platform** or **Merchant**).

4. Configure the following settings:
   - **App name**: `<your app name>`
   - **Sandbox or Business Account**: Select a sandbox account for testing.

---

## Step 2: Get API Credentials

After creating the app, you will receive the following credentials:

- Client ID
- Secret (Click "Show" under the Secret field)

---

## Step 3: Add Environment Variables

Update your backend `.env` file:

```env
PAYPAL_ENV=sandbox
PAYPAL_LIVE_URL=https://api-m.paypal.com
PAYPAL_SANDBOX_URL=https://api-m.sandbox.paypal.com
```

use PAYPAL_ENV=live for live environment
use PAYPAL_ENV=sandbox for sandbox environment

## Step 4: Connect Directly via the above credentials

Use your Client ID and Secret key to connect PayPal via the UI.