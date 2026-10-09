---
title: Configure step-up authentication
description: Configure step-up authentication to require an additional challenge before callers reach AI voice agents that handle sensitive requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/configure-step-up-authentication.html
release: brazil
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-10-09"
reading_time_minutes: 1
keywords: [configure step-up authentication, step-up factor, Caller verification, AI Voice Assistant Designer]
breadcrumb: [Step-up authentication, Configure authentication factors for AI voice agents, Authentication factors, Authentication, Access Management]
---

# Configure step-up authentication

Configure step-up authentication to require an additional challenge before callers reach AI voice agents that handle sensitive requests.

## Before you begin

Role required: `auth_factors_admin`

The `glide.conv_ai_voice.step_up.enabled` system property is set to `true`.

The factor you select must be configured at the platform level before you can use it for step-up authentication. For more information, see [Authentication factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/explore-authentication-factors.md).

Whether an AI voice agent requires step-up authentication is set in AI Agent Studio. For more information, see [AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aias-landing.md).

## Procedure

1.  Open the voice assistant in AI Voice Assistant Designer.

2.  Select **Settings**, then select **Caller verification**.

3.  On the step-up authentication card, select **Add**.

4.  Select one of the following factors:

    -   Okta Verify push notification
    -   SMS verification code
    -   Authenticator app time-based One Time Password \(TOTP\)
    The factor you select applies to every AI voice agent in this voice assistant that requires step-up authentication. The factor selected as the **First factor** or **Second factor** can be selected again here.

5.  Select **Save and continue**.


## Result

Callers who reach an AI voice agent that requires step-up authentication complete a challenge using the selected factor. After the caller completes the challenge, the elevated state applies for the rest of the call.

## What to do next

-   **Update the step-up authentication factor**

    To change the factor, select **Edit** on the step-up authentication card. To clear it, select **Remove**. If an AI voice agent still requires step-up authentication, callers reaching that agent are directed to the configured fallback method until a factor is selected again.


**Related topics**  


[Step-up authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/step-up-authentication.md)

[identify-and-authenticate-the-caller]

