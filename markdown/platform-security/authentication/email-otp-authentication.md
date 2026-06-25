---
title: Email One-time passwords \(OTP\) authentication
description: Email OTP for AI voice agents sends a one-time numeric code to the caller's email address. The caller retrieves the code from their email and provides it to the agent to verify their identity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/email-otp-authentication.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Email One-time Passcode, OTP, authentication, ServiceNow, secondary factor, identity verification, medium-risk scenarios, phishing, email account compromise, delivery delays, email service availability]
breadcrumb: [Configure authentication factors for AI voice agents, Authentication factors, Authentication, Access Management]
---

# Email One-time passwords \(OTP\) authentication

Email OTP for AI voice agents sends a one-time numeric code to the caller's email address. The caller retrieves the code from their email and provides it to the agent to verify their identity.

## When to use Email OTP

Email OTP is appropriate for caller verification when the caller has access to their email during the session and SMS delivery is not preferred or available. Email OTP can be configured as a single factor, the first factor in a multi-factor authentication flow, or a second factor.

Email OTP is a medium-assurance factor and is not suitable as the only authentication factor for sensitive operations. For those flows, combine Email OTP with a higher-assurance factor such as Okta Verify push notification or a time-based one-time password \(TOTP\). For guidance on combining factors, see [Explore authentication factors for AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/explore-authentication-factors.md)

## How Email OTP works

During an AI voice agent session, the platform generates a one-time numeric code and sends it to the caller's email address. The caller retrieves the code from their email and provides it to the agent. The platform validates the code and returns the result to the orchestrator. Email OTP supports both **Text** and **Voice** input.

## Email source configuration

Email OTP determines which email address to send the code to by reading from a configuration record in the Email OTP Service Configurations table. Each record specifies a user record location: which table to look in, which column holds the email, and which column links that record back to the user's identity in sys\_user. The table is domain-separated.

By default, the ServiceNow AI Platform ships an instance-level configuration base system that reads the Email field from the User \(sys\_user\) table, keyed by Sys ID. Administrators can override this by pointing to a different table — for example, a custom contact table or a group table — as long as the table has an email field and a column that references sys\_user. Service profile-specific configurations take precedence over the instance-level default.

## Limitations

Email OTP requires the caller to have access to their email during the session. Latency depends on email delivery times.

## Availability

Email OTP is available base system on ServiceNow AI Platform. No plugin installation or system property change is required to use Email OTP.

**Related topics**  


[Configure Email OTP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/configure-email-otp-service.md)

[Explore authentication factors for AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/explore-authentication-factors.md)

