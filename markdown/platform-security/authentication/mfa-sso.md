---
title: Multi-factor Authentication with Single Sign-On
description: You can use MFA with an SSO provider for your ServiceNow instance.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring MFA, Multi-factor authentication, Authentication, Access Management]
---

# Multi-factor Authentication with Single Sign-On

You can use MFA with an SSO provider for your ServiceNow instance.

Since many users in your organization are logging in to your corporate network and accessing your ServiceNow instance, there is a stronger need for a secure authentication.

MFA with the combination of SSO provides an enhanced security for your instance. This capability provides flexibility to conditionally enable MFA for users.

**Note:**

-   ServiceNow MFA is enforced after the user is redirected after the successful authentication at the Identity Provider.
-   MFA was not enforced with SSO prior to the San Diego release.

For example, if you would like to give your external users an extra security protocol, then you can enforce MFA to only those users. In this way, you can add additional authentication abilities and control your user access.

For SSO-based login such as SAML, OpenID Connect, and Digest, you can enforce MFA for authentication.

MFA with SSO can be configured on-demand based on your requirement. With the help of authentication schemes and identity providers, you can enforce MFA for specific users with a specific login mechanism.

You can enforce MFA for the following conditions:

-   Authentication Scheme
-   Identity Provider

MFA with SSO is offered as a part of the Adaptive Authentication plugin \(com.snc.adaptive\_authentication\). To know more on how to set up Adaptive Authentication, see [Adaptive authentication](adaptive-authentication.md).

