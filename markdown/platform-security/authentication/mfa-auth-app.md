---
title: Authenticator Applications
description: Use third party authenticator applications to generate temporary MFA pass codes.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Multi-factor authentication \(MFA\), Multi-factor authentication \(MFA\), Authentication, Access Management]
---

# Authenticator Applications

Use third party authenticator applications to generate temporary MFA pass codes.

An authenticator application is third-party software that generates temporary pass-codes. You can use these pass-codes along with your password to login into an instance that requires multi-factor authentication \(MFA\).

If your administrator has enabled MFA on your instance, you see a prompt for a pass-code after entering your user and password during login.

![MFA Authenticator App set up screen](../images/mfa-authenticator-app.png)

ServiceNow requires authenticator applications that support Time-based One-time Passwords \(TOTP\).

ServiceNow tests MFA with the following authenticators:

-   Google Authenticator
-   Microsoft Authenticator
-   LastPass Authenticator
-   Authy
-   FreeOTP
-   Duo
-   Okta Verify

**Note:** Other authenticators not listed might also be compatible, but are not tested by ServiceNow.

