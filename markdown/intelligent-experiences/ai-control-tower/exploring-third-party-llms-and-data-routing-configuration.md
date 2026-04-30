---
title: Explore Third-party LLMs and regions
description: Explore all the scenarios for configuring third party LLMs and SLMs based on the regions.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Explore Third-party LLMs and regions

Explore all the scenarios for configuring third party LLMs and SLMs based on the regions.

## Configuration overview

These are the few scenarios to consider when configuring LLMs:

-   **APJC region**

    The Data routing configuration is available for both regional and global routing. All the allowed providers are visible, and you can edit data routing settings

-   **Regulated markets**

    The Data routing configuration isn’t available, and the list of allowed providers is limited. You can view the allowed provider, but only in a read-only format.

-   **AMS &amp; EMEA regions**

    LLMs follow regional data routing configurations, as there’s no global routing option and you can view all the allowed providers.


Activating Fallback enables AI systems supported by your approved providers to stay active by using their default providers. Manually deactivating Fallback ensures that these AI systems remain inactive.

For information about Data routing, Fallback, Spillover and Impact summary, see [Explore AI model providers](ai-model-providers.md)

For information on configuring of third party LLMs for APJC region, see [Configure third-party LLMs using AI Control Tower](../task/configure-third-party-llms-using-ai-control-tower.md)

