---
title: Soft PIN authentication
description: Soft PIN is a six-digit numeric PIN that verifies a caller's identity during an AI voice agent session.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/softpin-authentication.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Soft PIN Authentication, ServiceNow, low-risk scenarios, self-service features, security risks]
breadcrumb: [Configure authentication factors for AI voice agents, Authentication factors, Authentication, Access Management]
---

# Soft PIN authentication

Soft PIN is a six-digit numeric PIN that verifies a caller's identity during an AI voice agent session.

## When to use Soft PIN

Soft PIN is appropriate for low-risk caller verification, such as confirming a returning user before granting access to self-service tasks.

Soft PIN can be configured as a single factor, the first factor in a multi-factor authentication flow, or a second factor.

Soft PIN is a medium-assurance factor and is not suitable as the only authentication factor for sensitive operations. For those flows, combine Soft PIN with a higher-assurance factor such as Okta Verify push notification or a time-based one-time password \(TOTP\). For guidance on combining factors, see [Explore authentication factors for AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/explore-authentication-factors.md).

## How Soft PIN works

Each user enrolls a Soft PIN before it can be used for authentication. Users can change their PIN by re-enrolling at any time.

When Soft PIN is selected as an authentication factor for an AI voice agent service, the agent prompts the caller for the PIN during the session. The platform validates the response against the user's enrolled PIN and returns the result to the orchestrator.

**Note:** Soft PIN supports both Text and Voice input.

## Enrollment rules

The system enforces the following rules on the chosen PIN:

|Rule|Behavior|
|----|--------|
|Length|Exactly six digits.|
|Repetition|No single digit can repeat more than twice consecutively. For example, `111234` is rejected.|
|Sequences|Ascending or descending numeric sequences longer than two digits aren't allowed. For example, `123456` and `987654` are rejected.|
|History|The new PIN can't match any of the user's previous five PINs.|

## Limitations

A six-digit numeric PIN provides lower assurance than time-based codes or push notifications. PINs are vulnerable to reuse, observation, and social engineering.

## Availability

The administrator manages the following conditions on the instance. Soft PIN enrollment is available when both are met:

-   Install Now Assist for Platform `sn_genai_platform` for activating AI voice agents.
-   The system property `glide.auth_factors.Soft PIN.enrollment.enabled` is set to `true` \(default\).

When the plugin is not installed, no Soft PIN module exists on the instance and the enrollment URL is not available. When the plugin is installed but the property is set to false, the enrollment option is hidden from the user profile, the navigation menu, and the Service Portal. Users who navigate directly to the enrollment URL see the following message:

`Soft PIN enrollment is not available at this time. Please contact your administrator for more details.`

|Property|Description|Default state|
|--------|-----------|-------------|
|`glide.auth_factors.Soft PIN.enrollment.enabled`|Controls whether the Soft PIN enrollment option appears in the user profile, the navigation menu, and the Service Portal. Requires the AI Voice Agents plugin.|true|

**Related topics**  


[Configure Soft PIN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/configure-soft-pin.md)

[Authentication factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/authentication-factors.md)

