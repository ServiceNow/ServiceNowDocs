---
title: Authenticating CPQ API calls
description: Secure CPQ API calls with admin API keys, JWT tokens, session cookies, or Google IdP for runtime and Admin tasks.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [API overview and resources, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Authenticating CPQ API calls

Secure CPQ API calls with admin API keys, JWT tokens, session cookies, or Google IdP for runtime and Admin tasks.

## Authenticating runtime API calls

When using CPQ in a headless manner, you authenticate your configuration session by using a runtime client. To create a runtime client, navigate to the CPQ Admin UI, click **Utilities** in the sidebar, and then click **Runtime Clients**. From here, specify the origin of your call, whether it is an external URL or an origin specified in the header of your call. You can also give your client an expiration date. After you save your client, you can copy the token and use it as the bearer token in other runtime API calls.

![Menu](../images/cpq-menu-runtime-clients.png)

![Edit Run time client](../images/cpq-edit-runtime-client-dialog.png)

For more information on CPQ runtime calls, see [Intro to runtime API calls](intro_to_runtime_api_calls.md).

## Authenticating admin API calls

There are four ways to authenticate your admin API calls:

-   Admin API keys

    Admin API keys are the recommended way of authenticating admin API calls. For information about setting up admin API Keys, see:

    [CPQ: admin API Keys](https://logikio.atlassian.net/wiki/spaces/CS/pages/1615331503).

-   JWT token

    To ensure tighter security for long-term admin API authentication, we leverage the Salesforce JWT web token. For steps to initialize this access flow, see:

    [Admin APIs: Authentication using a Salesforce-connected app](admin-apis-authentication-via-salesforce-connected-app.md)

-   Session cookies

    To authenticate a short term admin session, you can leverage your browser’s session cookie. Navigate to the cookies in your browser’s console, and take the session cookie. Enter the cookie in your request header as a keyed pair: `"Cookie”:”SESSION=<yourSessionCookie>"`

    ![Session cookie in Google Chrome browser](../images/cpq-matrix-loader-select-cookie.png)

-   Google IdP

    If you are not connected to a Salesforce environment and choose not to use admin API keys, you can use Google IdP to authenticate. If you do not use Google IdP, open a support case or email support@logik.io to discuss options for admin API authentication.

    For information on setting up a Google IdP JWT token, see:

    [Setting up a Google IdP JWT Token for Headless admin API Authentication](https://logikio.atlassian.net/wiki/spaces/CS/pages/1614479620/Setting+up+a+Google+IdP+JWT+Token+for+Headless+Admin+API+Authentication)


