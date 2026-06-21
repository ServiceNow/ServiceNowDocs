---
title: Multi-factor authentication with Email
description: Multi-factor authentication \(MFA\) with Email as a factor for your authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-security/authentication/mfa-with-email.html
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring MFA, supported methods, and workflow, Multi-factor authentication \(MFA\), Authentication, Access Management]
---

# Multi-factor authentication with Email

Multi-factor authentication \(MFA\) with Email as a factor for your authentication.

Admin can configure ServiceNow instance to require users who attempt to login to the instance using Email based OTP.

**Note:** MFA with Email is activated with the Integration - Multifactor Authentication \(`com.snc.integration.multifactor.authentication`\) plugin by default. You need to configure the policy inputs and conditions.

\[Omitted image "email-screen-mfa.png"\] Alt text: MFA-Email

When users attempt to login to ServiceNow, Email OTP is sent to the Email address associated. User's can enter the six-digit verification code that it sent to the email address and verify their identity.

