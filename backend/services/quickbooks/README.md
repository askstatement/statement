# Quickbooks Integration

This module handles integration with Quickbooks Online APIs.

---

## Prerequisites

- An active Intuit Developer account
- Access to create developer apps

---

## Step 1: Create a Quickbooks App

1. Go to the Intuit developer dashboard:  
   [Developer Dashboard](https://developer.intuit.com/workspaces)

2. Log in with your account.

3. Create a new app.

4. Configure the following settings:
   - **App name**: `<your app name>`
   - **Scopes**: QuickBooks Online and Payments (com.intuit.quickbooks.accounting, com.intuit.quickbooks.payment)
   - **Redirect URIs**: Add the redirect URIs (under **Settings**). Keep the following URL structure and replace the domain with your domain:
     
     ```text
     <domain>/chat?tab=chat&connect=true&qbStatus=connected
     ```
     
     Example:
     ```text
     https://askstatement.com/chat?tab=chat&connect=true&qbStatus=connected
     ```

---

## Step 2: Get API Credentials

Navigate to **Keys and credentials** to find:

- Client ID
- Client Secret

---

## Step 3: Add Environment Variables

Update your `.env` file:

```env
QUICKBOOKS_ENVIRONMENT=sandbox
QUICKBOOKS_CLIENT_ID=your_client_id_here
QUICKBOOKS_CLIENT_SECRET=your_client_secret_here
QUICKBOOKS_REDIRECT_URI=http://localhost:3000/chat?tab=chat&connect=true&qbStatus=connected
```

If you are managing frontend and backend environments separately:

**Frontend `.env`:**
```env
QUICKBOOKS_CLIENT_ID=your_client_id_here
```

**Backend `.env`:**
```env
QUICKBOOKS_ENVIRONMENT=sandbox
QUICKBOOKS_CLIENT_ID=your_client_id_here
QUICKBOOKS_CLIENT_SECRET=your_client_secret_here
QUICKBOOKS_REDIRECT_URI=http://localhost:3000/chat?tab=chat&connect=true&qbStatus=connected
```
