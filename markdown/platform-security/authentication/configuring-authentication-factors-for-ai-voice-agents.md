---
title: Authentication factor configuration for AI voice agents
description: To secure voice agent environments, configure authentication factors that first identify the caller, then authenticate them before granting access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/configuring-authentication-factors-for-ai-voice-agents.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Authentication factors, Authentication, Access Management]
---

# Authentication factor configuration for AI voice agents

To secure voice agent environments, configure authentication factors that first identify the caller, then authenticate them before granting access.

Configuration involves:

-   [User identification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/configuring-authentication-factors-for-ai-voice-agents.md)
-   [User authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/configuring-authentication-factors-for-ai-voice-agents.md)

## User identification

User identification forms the foundational layer of security for AI voice agents. You can configure knowledge-based authentication \(KBA\) to establish the caller identity before any authentication steps.

## User authentication

After identification, authentication confirms the caller's identity before enabling access to sensitive resources or actions. ServiceNow AI Platform supports both single-factor and multi-factor authentication \(MFA\), enabling administrators to tailor security configurations according to assurance levels and user roles. Supported factors include numeric PINs, authenticator app codes, one-time passwords over SMS and email, push notifications, and knowledge-based questions.

## General guidelines

-   Use multi-factor authentication as the default approach for stronger security.
-   Regularly review and update authentication factor configurations to address evolving threats and maintain conformance.

The following matrix shows the authentication factor combinations based on assurance level and authentication strategy.

|Factor|Security assurance|Recommended as single factor|Recommended as first factor \(MFA\)|Recommended as second factor \(MFA\)|Learn more about configuration|
|------|------------------|----------------------------|-----------------------------------|------------------------------------|------------------------------|
|[Time-based one-time password \(TOTP\) authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/totp-authenticator-apps.md)|High|Y|Y|Y|[Authenticator applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/mfa-auth-app.md)|
|[Push notification - Okta Verify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/push-notification-okta-verify.md)|High|Y|Y|Y|[Configure Push notification - Okta Verify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/configure-okta-verify-push-notification.md)|
|[Soft PIN authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/softpin-authentication.md)|Medium|Sometimes|Y|Y|[Configure Soft PIN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/configure-soft-pin.md)|
|[SMS one-time passcode \(OTP\) authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/sms-otp-authentication.md)|Medium|N|N|Y|[Multi-factor authentication providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/multi-factor-authentication-providers.md)|
|[Email one-time passwords \(OTP\) authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/email-otp-authentication.md)|Medium|N|Sometimes|Y|[Configure Email OTP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/configure-email-otp-service.md)|
|[Knowledge-based authentication \(security questions\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/knowledge-based-authentication.md)|Low|N|Y|N|[Configure knowledge-based authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/configure-kba.md)|

**Important:** Y = Recommended \| Sometimes = Use with Caution \| N = Not Recommended

