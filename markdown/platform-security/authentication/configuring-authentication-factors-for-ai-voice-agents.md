---
title: Configure authentication factors for AI voice agents
description: To secure voice agent environments, configure authentication factors that first identify the caller, then authenticate them before granting access.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-12-03"
reading_time_minutes: 2
breadcrumb: [Authentication factors, Authentication, Access Management]
---

# Configure authentication factors for AI voice agents

To secure voice agent environments, configure authentication factors that first identify the caller, then authenticate them before granting access.

Configuration involves:

-   [User identification](configuring-authentication-factors-for-ai-voice-agents.md#section_ftb_gmy_mhc)
-   [User authentication](configuring-authentication-factors-for-ai-voice-agents.md#section_gtb_gmy_mhc)

## User identification

User identification forms the foundational layer of security for AI voice agents. You can configure knowledge-based authentication \(KBA\) to establish the caller identity before any authentication steps.

## User authentication

After identification, authentication confirms the caller's identity before enabling access to sensitive resources or actions. ServiceNow AI Platform supports both single-factor and multi-factor authentication \(MFA\), enabling administrators to tailor security configurations according to assurance levels and user roles. Supported factors include numeric PINs, authenticator app codes, one-time passwords over SMS, push notifications, and knowledge-based questions.

## Recommendations

-   You’re encouraged to leverage multi-factor authentication as the default approach for optimal security.
-   You should regularly review and update authentication factor configurations to address evolving threats and maintain conformance.

The following matrix shows the authentication factor combinations based on assurance level and authentication strategy:

<table id="table_f1l_smy_mhc"><thead><tr><th>

Factor

</th><th>

Security Assurance

</th><th>

Recommended as Single Factor

</th><th>

Recommended as First Factor \(MFA\)

</th><th>

Recommended as Second Factor \(MFA\)

</th><th>

Learn more about configuration

</th></tr></thead><tbody><tr><td>

[Time-based one-time password \(TOTP\) authentication](totp-authenticator-apps.md)

</td><td>

High

</td><td>

Y

</td><td>

Y

</td><td>

Y

</td><td>

[Authenticator Applications](mfa-auth-app.md)

</td></tr><tr><td>

[Push notification - Okta Verify](push-notification-okta-verify.md)

</td><td>

High

</td><td>

Y

</td><td>

Y

</td><td>

Y

</td><td>

[Configure push notification \(Okta Verify\)](../task/configure-okta-verify-push-notification.md)

</td></tr><tr><td>

[SoftPIN authentication](softpin-authentication.md)

</td><td>

Medium

</td><td>

Sometimes

</td><td>

Y

</td><td>

Y

</td><td>

[Configure Soft PIN](../task/configure-soft-pin.md)

</td></tr><tr><td>

[SMS One-time passcode \(OTP\) authentication](sms-otp-authentication.md)

</td><td>

Medium

</td><td>

N

</td><td>

N

</td><td>

Y

</td><td>

[Multi-factor authentication Providers](multi-factor-authentication-providers.md)

</td></tr><tr><td>

[Knowledge-based authentication \(Security Questions\)](knowledge-based-authentication.md)

</td><td>

Low

</td><td>

N

</td><td>

Y

</td><td>

N

</td><td>

[Configure knowledge-based authentication](../task/configure-kba.md)

</td></tr></tbody>
</table>**Important:** Y = Recommended \| Sometimes = Use with Caution \| N = Not Recommended

