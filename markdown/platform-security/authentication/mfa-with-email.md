---
title: Multi-factor authentication with Email
description: Multi-factor authentication \(MFA\) with Email as a factor for your authentication.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [MFA verification methods, Configure Multi-factor authentication, Multi-factor authentication, Authentication, Access Management]
---

# Multi-factor authentication with Email

Multi-factor authentication \(MFA\) with Email as a factor for your authentication.

Admin can configure ServiceNow instance to require users who attempt to login to the instance using Email based OTP.

**Note:** MFA with Email is activated with the Integration - Multifactor Authentication \(`com.snc.integration.multifactor.authentication`\) plugin by default. You need to configure the policy inputs and conditions.

![MFA-Email](../images/email-screen-mfa.png)

When users attempt to login to ServiceNow, Email OTP is sent to the Email address associated. User's can enter the six-digit verification code that it sent to the email address and verify their identity.

