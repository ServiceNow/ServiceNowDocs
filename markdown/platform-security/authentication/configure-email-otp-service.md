---
title: Configure Email OTP
description: Configure the Email one-time password \(OTP\) to enable OTP-based authentication for users in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/configure-email-otp-service.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 1
keywords: [email OTP, one-time password, authentication]
breadcrumb: [Email OTP authentication, Configure authentication factors for AI voice agents, Authentication factors, Authentication, Access Management]
---

# Configure Email OTP

Configure the Email one-time password \(OTP\) to enable OTP-based authentication for users in your instance.

## Before you begin

Role required: `auth_factors_admin`

Install Now Assist for Platform `sn_genai_platform` for activating AI voice agents before Email OTP can be configured.

## Procedure

1.  Navigate to **All** &gt; **Authentication Factors** &gt; **Email OTP Factor** &gt; **Email OTP Service Configuration**.

2.  Select **New**.

3.  Specify the following fields on the form:

    |Field|Description|
    |-----|-----------|
    |Service Profile Table|Select the table associated with the AI voice agent service profile. For example, `sys_now_assist_d...` \(Now Assist Deployment\).|
    |Service Profile|Select the specific AI voice agent service profile to associate with the Email OTP configuration. For example, `Now Assist Deployment: Auth Factors Voice`.|
    |Table|Select the table that contains the user records. Defaults to `User [sys_user]`.|
    |Active|Select to enable the Email OTP configuration. Enabled by default.|
    |Email Column|Select the column from the user table that contains the email address used to send the OTP. Defaults to `Email`.|
    |User Column|Select the column used to identify the user record. Defaults to `Sys ID`.|

    \[Omitted image "kba-email-otp-service-config.png"\] Alt text: Email OTP Service Configuration form

4.  Select **Submit**.


## Result

The Email OTP configuration is saved. During an AI voice agent session, a one-time passcode is sent to the user's registered email address for authentication.

**Related topics**  


[Email One-time passwords \(OTP\) authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/email-otp-authentication.md)

[Explore authentication factors for AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/explore-authentication-factors.md)

