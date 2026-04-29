---
title: \(Workaround\) Enable service provider-initiated authentication
description: Use this workaround if authentication fails because you do not have SAML 2.0 Update 1. This issue can happen if users attempt to skip IdP authentication and navigate directly to the instance.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ADFS integration with SAML 2.0, Integrating SAML 2.0 with other features, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# \(Workaround\) Enable service provider-initiated authentication

Use this workaround if authentication fails because you do not have SAML 2.0 Update 1. This issue can happen if users attempt to skip IdP authentication and navigate directly to the instance.

## Before you begin

Role required: sso\_config\_admin, business\_rule\_admin, script\_include\_admin

## About this task

This error occurs when the instance doesn't provide ADFS with the needed definition and semantics for the SPNameQualifier attribute in the SAMLResponse.

Enable service provider-initiated authentication by doing one of the following actions:

## Procedure

-   Upgrade to SAML 2.0 Update 1 and clear the option to create an AuthnContextClass request.

-   Modify the **SAML2** script include to comment out the definitions of the `SPNameQualifier` attribute when you have SAML 2.0 active \(not SAML 2.0 Update 1\).

    Comment out these lines in the createNameID and createNameIDPolicy functions:

    ```
    //nid.setSPNameQualifier (serviceURL ) ;
    
     //nameIdPolicy. setSPNameQualifier (serviceURLStr ) ;
    ```


## What to do next

If you do not want the login prompt from your ADFS server to appear when you access the instance, set the following SAML 2.0 Update 1 property to false: **Create an AuthnContextClass request in the AuthnRequest** statement \(**glide.authenticate.sso.saml2.createrequestedauthncontext**\).

