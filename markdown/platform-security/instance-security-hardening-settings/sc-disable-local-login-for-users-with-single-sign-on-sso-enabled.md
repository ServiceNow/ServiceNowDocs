---
title: Disable local login for users with Single Sign-On \(SSO\) enabled
description: Update user records to disable local login for users with Single Sign-On \(SSO\) enabled.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Disable local login for users with Single Sign-On \(SSO\) enabled

Update user records to disable local login for users with Single Sign-On \(SSO\) enabled.

Users configured to use SSO authentication may be able to access the instance, or parts of the instance, with local credentials stored in the **user\_password** field of their User \[sys\_user\] record. This access applies to both interactive and non-interactive access for users who aren’t locked out. Help prevent SSO-configured users from using local credentials to reduce the chance that valid local login credentials are stolen and used by malicious users.

Review Now Support Knowledge Base article [KB1649420](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1649420) for instructions on identifying and addressing accounts with local login still enabled on an instance with SSO enabled.

## More information

|Attribute|Description|
|---------|-----------|
|Security risk|When SSO authentication is enabled for a user, it’s best practice to prevent that user from logging in locally. This reduces the chance that the valid local login credentials are stolen and used to login by a malicious user.|
|Common Vulnerability Scoring System \(CVSS\) score|4.2|
|Common Vulnerability Scoring System \(CVSS\) rating|Medium|
|Functional impact|SSO configured users are able to log in with local credentials.|
|Dependencies and prerequisites|Single Sign-On must be enabled \(the **glide.authenticate.multisso.enabled** system property set to **true**.\)|
|Data type|N/A|
|Base system value|N/A|
|Fallback value|N/A|
|Recommended value|N/A|

**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

