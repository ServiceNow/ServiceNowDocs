---
title: Create an identity provider \(IdP\) for Engagement Messenger
description: Create an IdP for your Engagement Messenger so that you can enable customer authentication. You can create an IdP for either the OpenID Connect \(OIDC\) or Security Assertion Markup Language \(SAML\) authentication type.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up Engagement Messenger, Enable communication channels, Configure, Customer Service Management]
---

# Create an identity provider \(IdP\) for Engagement Messenger

Create an IdP for your Engagement Messenger so that you can enable customer authentication. You can create an IdP for either the OpenID Connect \(OIDC\) or Security Assertion Markup Language \(SAML\) authentication type.

## Before you begin

Role required: admin

## About this task

If you previously configured an IdP, you can ignore this task and reuse the existing IdP.

**Note:** If you have configured multiple IdPs on your instance and want to select a specific IdP for your Engagement Messenger module, do the following:

-   [Enable Engagement Messenger on a website when third-party application cookies are blocked](../task/allowlist-em-third-party-website.md)
-   [Custom URL with Identity Provider](https://www.servicenow.com/docs/access?context=custom-url-with-multiple-identity-providers&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   If you have multiple IdPs on your instance:

    -   In case of OIDC authentication type, the generated ID token should contain the client ID of a IdP record against which authentication is required.
    -   In case of SAML authentication type, set the particular IDP record as Auto-redirect IdP.
    **Note:** For more information, see [Setting up auto login and logout for Engagement Messenger](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1560205).


## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

2.  Select **New**.

3.  Select either **OpenID Connect** or **SAML**.

    -   If you select **OpenID Connect**, follow the procedure in [Create an OpenID Connect \(OIDC\) configuration for Single Sign-On \(SSO\)](https://www.servicenow.com/docs/access?context=create-OIDC-configuration-SSO&version=australia&pubname=australia-platform-security&ft:locale=en-US).
    -   If you select **SAML**, follow the procedure from step 3 in [Create and update identity providers](https://www.servicenow.com/docs/access?context=t_CreateUpdateIdentityProvider&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## What to do next

-   When customers sign in to your website where the Engagement Messenger module is deployed, they must also be authenticated within the messenger. User authentication is done by using the same IdP that authenticated the customer's login into your website.

    You must verify that the customers of your website are also added in your OIDC or SAML authentication provider for the ServiceNow instance.

-   Enable cross-domain requests between Engagement Messenger and your website. For more information, see [Configure a CORS rule for Engagement Messenger](../task/create-cors-for-rest-api-ec.md).

**Related topics**  


[How to set up OIDC provider on ServiceNow instance](https://support.servicenow.com/kb_view.do?sysparm_article=KB0778342)

