---
title: Admin APIs: Authentication using a Salesforce-connected app
description: We recommend that you use admin API keys to authenticate admin API calls. An older method is documented here.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [API overview and resources, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Admin APIs: Authentication using a Salesforce-connected app

We recommend that you use admin API keys to authenticate admin API calls. An older method is documented here.

CPQ administration APIs are useful to facilitate new product introduction, data transfer, test-to-production operations, and so on. For use cases in which CPQ leverages Salesforce for user authentication, this article walks you through the steps required to build a Salesforce connected app and retrieve a JSON web token \[JWT\] that can be used to authenticate calls to CPQ administration APIs.

**Note:**

-   The release of admin API Keys has made this setup unnecessary and is now the recommended method of authentication of admin API calls. See [Intro to admin API keys](cpq-admin-api-keys.md).
-   The JWT method that was recommended before February 2025 has been deprecated by Salesforce. Instead, follow the updated steps in this article.

The JWT can be used as a bearer token to authenticate CPQ administration APIs to manipulate managed tables, write rules, deploy blueprints, and more.

## Creating or updating a connected app for JWT authentication

If youʼre updating an existing app, these instructions assume that youʼve created a connected app following the instructions in the legacy asset token flow.

1.  Go to Salesforce Setup, Apps → App Manager.
2.  Create a new connected app, or update your existing JWT app to match the image below.

    ![API settings](../images/cpq-apis-enable-oauth-settings.png)

3.  Click **Manage** in your JWT connected app.
4.  Edit policies.
    -   There will be a new section labeled Client Credentials Flow. Select your integration user in the **Run As** option.
    -   There will be a second new section labeled JWT-Based Access Token Settings for Named Users. Check **Issue JSON Web Token \(JWT\)-based access tokens**, and select a default timeout.
    -   Click **Save**. Your policies should resemble the following:

        ![OAuth Policies](../images/cpq-apis-policies.png)


## Generating the JWT

The following Postman collection can be used to generate a JWT for your instance:

[https://logikio.atlassian.net/wiki/spaces/CS/pages/1615036449/Admin+APIs+Authentication+via+Salesforce+Connected+App](https://logikio.atlassian.net/wiki/spaces/CS/pages/1615036449/Admin+APIs+Authentication+via+Salesforce+Connected+App)

For in-depth instructions, see:

[OAuth 2.0 Client Credentials Flow for Server-to-Server Integration](https://help.salesforce.com/s/articleView?id=xcloud.remoteaccess_oauth_client_credentials_flow.htm&type=5)

You can find the client ID and secret by viewing the Consumer Key and Secret → Manage Consumer Details field in the connected app you created above.

Note that a single call to Salesforce generates a token. Based on the **Issue JSON Web Token \(JWT\)-based access tokens for named users** setting in your connected app, the access token returned here is a JWT that you can use as a bearer token for CPQ APIs.

