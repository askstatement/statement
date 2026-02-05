# Xero Integration

This module handles integration with Xero APIs.

---

## Prerequisites

- An active Xero account
- Access to create developer apps

---

## Step 1: Create a Xero App

1. Go to the Xero developer dashboard:  
   [Developer Dashboard](https://developer.xero.com/app/manage)

2. Log in with your account.

3. Create a new app.

4. Configure the following settings:
   - **App name**: `<your app name>`
   - **Integration type**: Web app
   - **Homepage URL**: `<your website url>`
   - **OAuth 2.0 redirect URI**: Add the redirect URI. Keep the following URL structure and replace the domain with your domain:
     
     ```text
     <domain>/chat?tab=chat&connect=true&xeroStatus=connected
     ```
     
     Example:
     ```text
     https://askstatement.com/chat?tab=chat&connect=true&xeroStatus=connected
     ```

---

## Step 2: Get API Credentials

After creating the app, you will receive the following credentials:

- Client ID
- Client Secret (You may need to generate this)

---

## Step 3: Add Environment Variables

Update your `.env` file:

```env
XERO_CLIENT_ID=your_client_id_here
XERO_CLIENT_SECRET=your_client_secret_here
XERO_REDIRECT_URI=http://localhost:3000/chat?tab=chat&connect=true&xeroStatus=connected
```

If you are managing frontend and backend environments separately:

**Frontend `.env`:**
```env
XERO_CLIENT_ID=your_client_id_here
```

**Backend `.env`:**
```env
XERO_CLIENT_ID=your_client_id_here
XERO_CLIENT_SECRET=your_client_secret_here
XERO_REDIRECT_URI=http://localhost:3000/chat?tab=chat&connect=true&xeroStatus=connected
```
