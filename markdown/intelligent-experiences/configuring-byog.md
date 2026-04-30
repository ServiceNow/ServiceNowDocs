---
title: Configuring a Guardrail Service Provider
description: Now Assist Guardian supports default guardrails and third-party or custom guardrail service providers to extend AI content monitoring with your organization's AI governance policies.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-02-13"
reading_time_minutes: 2
breadcrumb: [Now Assist Guardian, Now Assist Admin Settings, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Configuring a Guardrail Service Provider

Now Assist Guardian supports default guardrails and third-party or custom guardrail service providers to extend AI content monitoring with your organization's AI governance policies.

## Guardrail Service Provider overview

Now Assist Guardian includes default guardrails to detect offensive content, block prompt injection attacks, and filter sensitive topics. In addition to these guardrails, Now Assist Guardian supports third-party guardrail service providers. You can also create your own custom guardian using the Bring Your Own Guardrail \(BYOG\) feature to monitor and detect malicious content.

Custom guardian evaluates prompts and responses in real time, just like the default guardrails. You can set each custom guardrail to log events, block content, or both based on your specific security or content policies.

## ServiceNow supported third-party guardrail service providers

Now Assist Guardian supports the following cloud AI service providers:

-   ServiceNow guardrail: The default provider built into the platform. No additional configuration is required.
-   Third-party providers: Integrate with supported cloud AI safety services. Following are the supported providers:
    -   Microsoft Azure Content Safety
    -   Amazon Bedrock
    -   Google Model Armor
-   Custom \(BYOG\): Create your own guardrail to apply your organization's specific compliance, security, or content policies.

Only one guardrail service provider can be active at a time. The selected provider monitors and evaluates all Now Assist interactions for harmful, offensive, or prompt injection content.

## Custom guardrails for Now Assist Guardian

The Bring Your Own Guardrail \(BYOG\) feature lets you create and connect a custom guardrail in Now Assist Guardian. A custom guardrail connects to an external endpoint that you control, allowing you to apply policies specific to your organization. It evaluate prompts and responses in real time, the same as default guardrails. You can configure each custom guardrail to log events, block content, or both.

Setting up a custom guardrail involves three steps:

1.  Create a connection and credential alias for the custom guardian and complete its setup. The alias supports Basic Auth, OAuth 2.0, and API Key credential types.

    For more information, see [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

2.  Create a custom guardian in the Generative AI Custom Guardian Transformer \[sys\_generative\_ai\_custom\_guardian\_transformer\_list.do\] table.

    For more information, see [Create a custom guardian](../task/create-custom-guardian.md).

3.  Select your preferred guardrail service providers to monitor content.

    For more information, see [Setup a Guardrail Service Provider](../task/configure-guardrail-model.md).


-   **[Create a custom guardian](../task/create-custom-guardian.md)**  
Create your own custom guardian to monitor and detect requests sent to LLM.
-   **[Setup a Guardrail Service Provider](../task/configure-guardrail-model.md)**  
Select a guardrail service provider of your choice in Now Assist Guardian to monitor and detect Now Assist interactions for harmful, offensive, and prompt injection content.

**Parent Topic:**[Now Assist Guardian](../../now-assist-platform/concept/now-assist-guardian.md)

