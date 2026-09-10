---
title: Configure human-assisted SMS OTP
description: Configure the HA SMS OTP service to enable human agents to generate and validate one-time pass codes during live interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/configure-human-assisted-sms-otp.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [configure human-assisted SMS OTP, HA SMS OTP service configuration, delivery mode, phone number resolution]
breadcrumb: [Human-assisted SMS OTP authentication, Authentication factors, Authentication, Access Management]
---

# Configure human-assisted SMS OTP

Configure the HA SMS OTP service to enable human agents to generate and validate one-time pass codes during live interactions.

## Before you begin

Role required: `sn_auth_ha_sms_otp_admin`

Perform the following:

-   Install the HA SMS OTP plugin \(`sn_auth_ha_sms_otp`\). This also installs the dependent Multi-factor authentication with SMS plugin \(`com.snc.authentication.sms_mfa`\) if not already present.
-   Enable human-assisted SMS OTP using the `glide.auth_factors.ha_sms_otp.enabled` property. Set it to `false` to turn the feature off; the default is `true`. Read and write access to this property is restricted to users with the `sn_auth_ha_sms_otp_admin` or `security_admin` role.
-   For OOB delivery mode: configure an SMS provider \(Twilio, Infobip, or Custom\) under **All** &gt; **Multi-factor Authentication** &gt; **Providers**. To know more, see [SMS One-time passcode \(OTP\) authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/sms-otp-authentication.md) for provider setup instructions.
-   Grant the `sn_auth_ha_sms_otp_caller` role to any user or integration that will call the HA SMS OTP API.
-   Grant the consuming application scope explicit permission to execute the HA SMS OTP API methods.

## Procedure

1.  Navigate to All &gt; Authentication Factors &gt; Human-Assisted SMS OTP &gt; Configuration.

2.  Select an existing configuration record to edit, or select **New** to create one.

    \[Omitted image "humar-assisted-sms-otp-list-view.png"\] Alt text: Human Assisted SMS OTP Service Configuration list view

3.  Fill in the following fields.

    \[Omitted image "humar-assisted-sms-otp.png"\] Alt text: Human Assisted SMS OTP Service Configuration

<table><thead><tr><th>

Field

</th><th>

Description

</th><th>

Default

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

Label for this configuration \(for example, HR Helpdesk SMS OTP\).

</td><td>

Default HA SMS OTP

</td></tr><tr><td>

**Global User Retry Window \(days\)**

</td><td>

The rolling time window, in days, over which a user's OTP retry attempts are counted. Attempts made within this window accumulate toward the user's retry limit; once the window elapses, the count resets.

</td><td>

7 \(range: 1 to 30\)

</td></tr><tr><td>

**Global User Lockout Duration \(days\)**

</td><td>

The number of days a user is prevented from requesting further OTPs after exhausting their allowed retry attempts.

</td><td>

1 \(range: 1 to 15\)

</td></tr><tr><td>

**Active**

</td><td>

When unchecked, this configuration is skipped at runtime. If no active configuration exists, OTP requests fail.**Note:** Only one active record can exist per domain.

</td><td>

true

</td></tr><tr><td>

**Delivery Mode**

</td><td>

-   OOB: the platform sends the SMS via the configured provider.
-   BYO: the platform generates and validates the OTP; the consuming application handles delivery.


</td><td>

OOB

</td></tr><tr><td>

**Phone Number Resolution**

</td><td>

How the platform resolves the end user's phone number for OOB delivery. -   Provided by calling application: phone number is passed in the API request.
-   Resolved from configured table: platform looks up the phone from the table and column configured below.
Applies to OOB only.

</td><td>

Config-table lookup

</td></tr><tr><td>

**Phone Table**

</td><td>

Table used to look up the end user's phone number \(for example, `sys_user`\). Used with config-table lookup only.

</td><td>

—

</td></tr><tr><td>

**Phone Column**

</td><td>

Column on the Phone Table that stores the phone number in E.164 format \(for example, `mobile_phone`\). Used with config-table lookup only.

</td><td>

—

</td></tr><tr><td>

**User Column**

</td><td>

Column on the Phone Table used to match the end user to a record \(for example, `sys_id`\). Used with config-table lookup only.

</td><td>

—

</td></tr><tr><td>

**OTP Code Length**

</td><td>

Number of digits in the generated OTP.

</td><td>

6 \(range: 6 to 8\)

</td></tr><tr><td>

**OTP Expiry \(Minutes\)**

</td><td>

Minutes before an unverified OTP expires and a new one must be requested.

</td><td>

3 \(range: 1 to 10\)

</td></tr><tr><td>

**Retry Limit**

</td><td>

Maximum incorrect validation attempts per conversation. Counts failed validateCode calls only. Triggering a resend does not consume this budget.

</td><td>

3 \(range: 1 to 10\)

</td></tr><tr><td>

**Resend Cooldown \(seconds\)**

</td><td>

Minimum seconds between consecutive OTP generation requests within the same conversation.

</td><td>

60 \(range: 0 to 600\)

</td></tr><tr><td>

**Global User Retry Limit**

</td><td>

Maximum failed OTP verification attempts for a single end user within the configured retry window. When exhausted, the user is locked out for the configured lockout duration, after which the counter resets.

</td><td>

10 \(range: 1 to 100\)

</td></tr><tr><td>

**Rate Limit Per Minute Per Agent**

</td><td>

Maximum OTP requests a single agent can trigger per minute. Set to 0 to disable.

</td><td>

10 \(range: 0 to 100\)

</td></tr><tr><td>

**Rate Limit Per Minute Per Tenant**

</td><td>

Maximum OTP requests across all agents in the tenant per minute. Set to 0 to disable.

</td><td>

100 \(range: 0 to 1000\)

</td></tr><tr><td>

**Domain**

</td><td>

Domain this record belongs to. Controls visibility in domain-separated instances.

</td><td>

—

</td></tr></tbody>
</table>    **Note:** If Delivery Mode is set to OOB and your SMS provider is a Custom type, phone number resolution uses the table and field configured in your MFA Provider Custom config record, not the Phone Number Resolution selection. In case of a mismatch, the MFA Provider Custom config takes precedence.

4.  Select Submit.


## Result

The HA SMS OTP service configuration is active and available for use by the consuming application's scriptable API calls. The consuming application can now call generateCode and validateCode to authenticate end users during human-assisted interactions.

**Related topics**  


[Human-assisted SMS OTP authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/human-assisted-sms-otp.md)

[SMS One-time passcode \(OTP\) authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/sms-otp-authentication.md)

[Configure authentication factors for AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/configuring-authentication-factors-for-ai-voice-agents.md)

