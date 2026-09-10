---
title: Human-assisted SMS OTP authentication
description: Human-assisted SMS OTP lets a human agent verify an end user's identity by sending a one-time passcode via SMS during a live interaction. The agent initiates OTP generation and validation through the platform's scriptable APIs, and the consuming application \(for example, CSM or FSO workspace\) handles the agent-facing workflow and user interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/human-assisted-sms-otp.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [human-assisted SMS OTP, SMS OTP, one-time passcode, agent identity verification, generateCode, validateCode]
breadcrumb: [Authentication factors, Authentication, Access Management]
---

# Human-assisted SMS OTP authentication

Human-assisted SMS OTP lets a human agent verify an end user's identity by sending a one-time passcode via SMS during a live interaction. The agent initiates OTP generation and validation through the platform's scriptable APIs, and the consuming application \(for example, CSM or FSO workspace\) handles the agent-facing workflow and user interface.

**Note:**

-   This capability is separate from the SMS OTP factor used in AI voice agent authentication. SMS OTP for AI voice agents is configured in AI Voice Assistant Designer and executed by the orchestrator during automated calls. Human-assisted SMS OTP is triggered by a human agent and is not part of the AI voice agent flow.
-   You can enable human-assisted SMS OTP using the `glide.auth_factors.ha_sms_otp.enabled` property. Set it to `false` to turn the feature off; the default is `true`. Read and write access to this property is restricted to users with the `sn_auth_ha_sms_otp_admin` or `security_admin` role.

## When to use human-assisted SMS OTP

Use human-assisted SMS OTP when a human agent needs to verify the end user's identity before performing a sensitive operation, and the interaction is not handled by an AI voice agent.

Examples:

-   A customer service agent verifies a caller's identity before authorizing a wire transfer or account change.
-   A support agent confirms the end user's identity during a live chat or phone interaction before processing a high-risk request.
-   A field service agent verifies a contact before sharing account-specific details over the phone.

## How human-assisted SMS OTP works

1.  The human agent identifies the end user in the consuming application.
2.  The agent triggers OTP generation. The consuming application calls the generateCode API.
3.  The platform generates a one-time code.
    -   In OOB mode, the platform dispatches the SMS directly to the end user's phone using the configured SMS provider.
    -   In BYO mode, the platform returns the code in the API response. The consuming application dispatches the SMS through its own provider.
4.  The end user receives the SMS and reads the code back to the agent.
5.  The agent submits the code. The consuming application calls validateCode.
6.  The platform validates the code and returns a result. The consuming application updates the interaction accordingly.

## Delivery modes

|Mode|Behavior|
|----|--------|
|OOB \(Out-Of-the-Box\)|The platform sends the SMS directly to the end user using the configured SMS provider \(Twilio, Infobip, or Custom\). Default delivery mode.|
|BYO \(Bring-your-own\)|The platform returns the OTP in the API response. The consuming application handles SMS delivery through its own infrastructure.|

## Phone number resolution

When delivery mode is OOB, the platform resolves the end user's phone number using one of two strategies.

|Strategy|Behavior|
|--------|--------|
|Provided by calling application|The phone number is supplied in the API request by the consuming application.|
|Resolved from configured table|The platform resolves the phone number from a table and column configured in the HA SMS OTP service configuration.|

When delivery mode is BYO, the consuming application handles delivery and determines the destination number. The platform does not resolve or use a phone number.

**Note:** If Delivery Mode is set to OOB and your SMS provider is a Custom type, phone number resolution uses the table and field configured in your MFA Provider Custom config record, not the Phone Number Resolution selection in the HA SMS OTP configuration. In case of a mismatch, the MFA Provider Custom config takes precedence.

## Rate limiting and retry behavior

|Limit|What it controls|Default|
|-----|----------------|-------|
|Per tenant per minute|Maximum OTP requests across all agents in the tenant.|100|
|Per agent per minute|Maximum OTP requests a single agent can trigger.|10|
|Per-Conversation User Retry Limit|Maximum failed validation attempts for a single end user within one conversation. Counts incorrect code submissions only.|3|
|Global User Retry Limit|Maximum failed verification attempts for a single end user within the configured retry window. When exhausted, the user is locked out for the configured lockout duration, after which the counter resets.|10|
|Resend cooldown|Minimum time between consecutive OTP generation requests within the same conversation.|60 seconds|

**Note:** Retry and resend are independent counters. Retry counts failed validation attempts \(incorrect code submitted\). Resend counts new OTP generation requests \(new code sent\). Triggering a resend does not consume the retry budget.

## Audit trail

Every generateCode and validateCode call is logged with the agent ID, end user ID, conversation ID, phone number \(for OOB\), result, and timestamp. Audit records are retained for 90 days by default. A table cleaner job manages retention.

## Limitations

-   Human-assisted SMS OTP is not available as a factor in AI Voice Assistant Designer. It operates independently through the scriptable APIs.
-   The platform does not provide an agent-facing UI for triggering or validating OTP. The consuming application must build and maintain the agent workflow.
-   In BYO mode, the platform has no visibility into whether or where the SMS was actually delivered. Audit records reflect only what was passed to the API.
-   The combination of BYO delivery mode with config-table-lookup phone number resolution is not supported and is blocked at save time.

## Availability

Human-assisted SMS OTP is available when the following conditions are met:

-   The HA SMS OTP plugin \(`sn_auth_ha_sms_otp`\) is installed. This plugin depends on the Multi-factor authentication with SMS plugin \(`com.snc.authentication.sms_mfa`\).
-   For OOB delivery: an SMS provider \(Twilio, Infobip, or Custom\) is configured and active under Multi-factor Authentication &gt; Providers.
-   The calling user or script has the `sn_auth_ha_sms_otp_caller` role.
-   The consuming application scope has been granted explicit permission to execute the HA SMS OTP API methods.

**Related topics**  


[Configure human-assisted SMS OTP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/configure-human-assisted-sms-otp.md)

[Configuring authentication factors for AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/configuring-authentication-factors-for-ai-voice-agents.md)

