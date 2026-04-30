---
title: Time-based one-time password \(TOTP\) authentication
description: A time based one-time password \(TOTP\) is a secure authentication factor that verifies user identity by generating a unique, time-sensitive code.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-11-13"
reading_time_minutes: 1
keywords: [Time-based one-time password, TOTP, authenticator apps, ServiceNow, user authentication, authentication factor, Okta Verify]
breadcrumb: [Configure authentication factors, Authentication factors, Authentication, Access Management]
---

# Time-based one-time password \(TOTP\) authentication

A time based one-time password \(TOTP\) is a secure authentication factor that verifies user identity by generating a unique, time-sensitive code.

TOTP authenticator apps like **Okta Verify** generate temporary numeric codes on a registered device, usually a mobile phone. These codes are only valid for a short time and can’t be used more than once. This approach offers enhanced security compared to static passwords.

## Use case

TOTP authenticator apps are suitable for users who require stronger protection than standard multi-factor authentication \(MFA\) methods.

## Key strengths

The TOTP authenticator apps method offers the following advantages:

-   Local generation: One-time passwords are generated directly on the user's device and don’t require an internet or mobile network connection.
-   Security: TOTP is resistant to interception and SIM-swapping attacks, providing robust protection for the authentication process.

## Important considerations

While TOTP authenticator apps are a secure and convenient authentication method, there are few considerations to keep in mind:

-   Initial setup: Users must set up the authenticator app on a registered device.
-   Device management: Users must re-enroll when devices are replaced or reset.
-   Phishing risk: One-time codes can be compromised if entered on untrusted or malicious sites.

TOTP authenticator apps are an effective method to strengthen your organization’s security posture. For detailed configuration instructions, see [Authenticator Applications](mfa-auth-app.md).

