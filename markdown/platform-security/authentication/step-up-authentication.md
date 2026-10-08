---
title: Step-up authentication
description: Step-up authentication requires a caller who is already authenticated to complete an additional challenge before reaching an AI voice agent that handles a sensitive request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/step-up-authentication.html
release: brazil
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-10-08"
reading_time_minutes: 5
keywords: [step-up authentication, AI voice agent, AI Voice Assistant Designer, caller verification]
breadcrumb: [Configure authentication factors for AI voice agents, Authentication factors, Authentication, Access Management]
---

# Step-up authentication

Step-up authentication requires a caller who is already authenticated to complete an additional challenge before reaching an AI voice agent that handles a sensitive request.

## When to use step-up authentication

Without step-up authentication, every caller is verified once at the start of the call and keeps the same level of access for the rest of it. The verification required at the start therefore has to be strong enough for the most sensitive request the caller might make later.

Step-up authentication separates the two. Callers complete a lighter verification to reach general requests, and complete an additional challenge only when the call reaches an AI voice agent that handles a sensitive request, such as a password reset or access to bank account details.

## How step-up authentication works

A caller must already be authenticated before step-up authentication can run. If the caller's first request reaches an AI voice agent that requires step-up authentication, the caller must first complete configured identification and authentication. The step-up challenge runs only after that authentication is complete.

Step-up authentication behaves as follows:

<table><thead><tr><th>

Behavior

</th><th>

Detail

</th></tr></thead><tbody><tr><td>

Trigger

</td><td>

On entry to an AI voice agent that requires step-up authentication. It applies to all the actions the agent performs.

</td></tr><tr><td>

Attempts

</td><td>

One attempt. If the caller doesn't complete the challenge, the request is blocked. The caller is then directed to the fallback method configured on the **Safeguards** screen in AI Voice Assistant Designer.

</td></tr><tr><td>

Factor reuse

</td><td>

The first or second authentication factor can be selected again for step-up. A new challenge is issued.

 For example, if SMS OTP is the configured authentication factor and the step-up factor, the caller receives a new code during step up attempt. The earlier code is not reused.

</td></tr><tr><td>

Scope

</td><td>

One step-up factor per voice assistant, shared by every AI voice agent in that assistant that requires step-up authentication.

</td></tr><tr><td>

Duration

</td><td>

Applies for the rest of the call.

</td></tr><tr><td>

System property

</td><td>

`glide.conv_ai_voice.step_up.enabled`, by default set to `true`.

</td></tr></tbody>
</table>## Configuration

Step-up authentication requires two settings, configured on different screens.

-   Which AI agents require step-up authentication is set in the **Access rules** section of AI Agent Studio. Step-up authentication is set per agent, in the Access rules section of AI Agent Studio, where agents are configured and built. For more information, see [AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aias-landing.md).
-   Which factor callers use for step-up authentication is set on the **Caller verification** screen in AI Voice Assistant Designer. For more information, see [Configure step-up authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/configure-step-up-authentication.md).

If an AI voice agent requires step-up authentication and no step-up factor is selected for the voice assistant, callers reaching that agent are directed to the configured fallback method.

## Supported factors

-   Okta Verify push notification
-   SMS verification code
-   Authenticator app time-based One Time Password \(TOTP\)

**Note:** Knowledge-based authentication \(KBA\), Soft PIN, and Email one-time password \(OTP\) aren't supported for step-up authentication.

## Combining step-up authentication with other factors

Step-up authentication is an additional layer on top of the factors configured for the voice assistant. It doesn't replace the configured authentication factor. It runs after them, and only when the call reaches an AI voice agent that requires it.

The step-up factor is selected separately from the first factor and second factor:

-   A factor used as the first factor or second factor can also be selected as the step-up factor. The caller receives a new challenge each time.
-   A factor that isn't supported for step-up authentication isn't excluded from the earlier steps. Soft PIN, for example, can be the first authentication factor even though it isn't supported as the step-up factor.

The following examples show how the three can be combined.

|Example|First factor|Second factor|Step-up factor|What the caller experiences|
|-------|------------|-------------|--------------|---------------------------|
|A different factor at each step|Soft PIN|SMS verification code|Okta Verify push notification|The caller completes the step-up challenge with an Okta Verify push notification after reaching an AI voice agent that requires it.|
|The same factor reused for step-up authentication|SMS verification code|Okta Verify push notification|SMS verification code|The caller receives a new verification code rather than reusing the code sent earlier in the call.|

## Limitations

-   Step-up authentication applies at the AI voice agent level. It can't be applied to individual actions within an agent.
-   One step-up factor is configured per voice assistant. Every AI voice agent in that assistant that requires step-up authentication uses the same factor.
-   Step-up authentication is one attempt. The retry setting in **Advanced options** applies to first factor and second factor authentication only.
-   The elevated state applies for the duration of the call and can't be configured to expire earlier.
-   The elevated state isn't carried across voice assistants and isn't transferred when the call is handed off to a live agent.

## Availability

Step-up authentication is available for AI voice agents when the following conditions are met:

-   The `glide.conv_ai_voice.step_up.enabled` system property is set to `true`.
-   The factor you want to use for step-up authentication is configured at the platform level. For more information, see [Authentication factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/explore-authentication-factors.md).
-   The AI voice agent is set to require step-up authentication in the **Access rules** section of AI Agent Studio.
-   A step-up factor is selected for the voice assistant on the **Caller verification** screen in AI Voice Assistant Designer. To make this selection, you need the `auth_factors_admin` role.

**Related topics**  


[Configure step-up authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/configure-step-up-authentication.md)

[Authentication factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/explore-authentication-factors.md)

[Identify and authenticate the caller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-voice-assistants.md)

