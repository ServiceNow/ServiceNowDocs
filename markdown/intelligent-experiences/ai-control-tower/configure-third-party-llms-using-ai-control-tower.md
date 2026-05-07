---
title: Configure third-party LLMs using AI Control Tower
description: Use the AI Control Tower to configure third-party LLMs based on the data routing configuration for the APJC region..
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Configure, AI Control Tower, Enable AI experiences]
---

# Configure third-party LLMs using AI Control Tower

Use the AI Control Tower to configure third-party LLMs based on the data routing configuration for the APJC region..

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\]

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Configurations** &gt; **Controls** &gt; **AI model providers**.

2.  Select **Edit**.

    You can configure AI model requests through these types of data routing configuration:

    1.  Regional
    2.  Global
3.  Configure LLMs through Regional data routing.

    1.  Select **Regional**.

        All allowed model providers are displayed:

        -   Now LLM Service
        -   AWS Claude
        -   Azure OpenAI
        -   Google Gemini
    2.  Select the model providers according to your organizational policies.

        When Azure OpenAI is selected, you’re asked to Allow Spillover, which redirects the traffic to Global data routing.

    3.  Enable spillover by selecting **Yes**.

    4.  Select **Save**.

        The Data routing confirmation consent request appears informing you to provide the consent.

    5.  Select **Agree and proceed**.

    6.  Select **Save**.

        The third-party LLMs are configured with Regional data routing configuration for the APJC region.

4.  Configure LLMs through Global data routing.

    1.  Select **Global**.

        All allowed model providers are displayed:

        -   AWS Claude
        -   Azure OpenAI
        -   Google Gemini
        -   Now LLM Service
        **Note:** Selecting global data routing redirects your data processing location to a global datacenter.

    2.  Select all the model providers.

    3.  Select **Save**.


## Result

The third-party LLMs are configured with the Global data routing configuration for the APJC region.

For information about Data routing, Fallback, and Spillover, see [Explore AI model providers](../concept/ai-model-providers.md)

For information about scenarios for configuring third-party LLMs for regulated markets and AMS &amp; EMEA regions, see [Explore the third-party LLMs and regions](../concept/exploring-third-party-llms-and-data-routing-configuration.md)

