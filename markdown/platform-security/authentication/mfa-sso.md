---
title: Configure Multi-factor authentication with Single Sign-On
description: Configure Multi-factor authentication \(MFA\) with a Single Sign-On \(SSO\) provider for your ServiceNow instance.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Multi-factor authentication, Multi-factor authentication, Authentication, Access Management]
---

# Configure Multi-factor authentication with Single Sign-On

Configure Multi-factor authentication \(MFA\) with a Single Sign-On \(SSO\) provider for your ServiceNow instance.

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

