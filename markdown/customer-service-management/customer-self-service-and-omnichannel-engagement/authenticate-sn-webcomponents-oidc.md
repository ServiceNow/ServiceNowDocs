---
title: Authenticate the ServiceNow components using OIDC
description: Set up auto-login and log out using OpenID Connect \(OIDC\) authentication to enable single and simultaneous login and logout in your website and embedded components.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up Web Embeddables, Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Authenticate the ServiceNow components using OIDC

Set up auto-login and log out using OpenID Connect \(OIDC\) authentication to enable single and simultaneous login and logout in your website and embedded components.

## Before you begin

You must use the default global code to enable login and logout functions on your ServiceNow instance.

Role required: sn\_embeddable\_core.emb\_admin

## About this task

Once the embeddable components are integrated into your website, you’re automatically logged in to the ServiceNow instance when you access the website. Ensuring a secure and personalized experience. Similarly, logging out of the website should also log you out of the ServiceNow instance.

**Note:** The Identity Provider \(IdP\) application used on your website must be configured on ServiceNow® as well.

## Procedure

1.  Configure an OIDC IdP \(Identity Provider\) on your ServiceNow instance.

    **Note:**

    -   For more information, see [Multi-Provider single sign-on \(SSO\)](https://www.servicenow.com/docs/access?context=c_MultipleProviderSingleSignOn&version=australia&pubname=australia-platform-security&ft:locale=en-US).
    -   The OIDC IdP should match the IdP that you use to log in to the website.
2.  Synchronize user records on the IdP with your ServiceNow instance.

    Verify that each website user is registered on the IdP and ServiceNow instance.

3.  Implement code on the third-party website to trigger the login\(\) and logout\(\) functions for automatic login and logout.

    1.  Use the login\(\) function to authenticate the session on embedded components when you log in using IdP into the website.

    2.  Use the logout\(\) function to log out from an ServiceNow instance.


## Result

Auto-login and logout functions are configured and trigger each time you log in or log out from the ServiceNow instance and third-party website.

