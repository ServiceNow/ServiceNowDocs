---
title: Email as an MFA factor
description: Multi-factor authentication \(MFA\) with email as a factor for your authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/mfa-with-email.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [MFA factor policies, MFA verification methods, Configuring MFA, Multi-factor authentication, Authentication, Access Management]
---

# Email as an MFA factor

Multi-factor authentication \(MFA\) with email as a factor for your authentication.

Admin can configure ServiceNow instance to require users who attempt to log in to the instance using email-based OTP.

**Note:** MFA with email is activated with the Integration - Multifactor Authentication \(`com.snc.integration.multifactor.authentication`\) plugin by default. You need to configure the policy inputs and conditions.

\[Omitted image "email-screen-mfa.png"\] Alt text: MFA-Email

When users attempt to log in to ServiceNow, Email OTP is sent to the email address associated. Users can enter the six-digit verification code that it sent to the email address and verify their identity.

