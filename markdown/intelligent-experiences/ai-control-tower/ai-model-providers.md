---
title: Explore AI model providers
description: Explore the AI model providers section in AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/ai-model-providers.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Controls, Configurations, AI Control Tower dashboard, Explore, AI Control Tower, Enable AI experiences]
---

# Explore AI model providers

Explore the AI model providers section in AI Control Tower.

Role required: AI steward

AI model providers enable you to select data routing, manage third-party LLMs \(Large Language Models\) and SLMs \(Small Language Models\), and configure the third-party LLMs by selecting the allowed model providers.

## Data routing and model providers

Data routing is a technology by which LLM and SLM requests are routed to the most suitable datacenter. This technology helps to optimize data traffic, which reduces latency and speeds up response time.

The Data routing and model providers section enables you to route AI model requests and select the Allowed model providers.

There are two types of data routing:

-   **Regional data routing**

    Regional data routing routes LLM and SLM requests to datacenters within your region. For example, if you’re in the APJC \(Asia Pacific, Japan, and China\) region, these requests could be routed to the most suitable datacenter in the APJC region. Regional data routing can sometimes be mandated by governments of specific regions.

-   **Global data routing**

    When you opt for Global data routing, LLM and SLM requests are routed to the most suitable datacenter globally.


You can configure the third-party LLM providers using the edit option by choosing either Regional or Global data routing and select all the Allowed model providers.

There are two sections of AI model providers:

-   AI model providers supported by ServiceNow
-   AI model providers configured by your organization

The AI model providers supported by ServiceNow contain providers such as Now LLM Service, AWS Claude, Now LLM-LTS model and so on.

The AI model providers configured by your organization such as Perplexity, IBM Watson and so on.

[AI asset lifecycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-asset-lifecycle.md)

**Note:** You can select Now LLM Service- LTS \(Long term stable\) Model, which supports regulated industries, such as financial institutions, with stronger AI lifecycle management, governance, transparency, and compliance tools.

For more information on Now LLM Service- LTS model, see [Long term stable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/long-term-stable-models.md)

For information on exploring the scenarios configuring third-party LLMs for all the regions, see [Explore the third-party LLMs and regions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/exploring-third-party-llms-and-data-routing-configuration.md)

For information about configuring third-party LLMs through Data routing configuration for APJC region, see [Configure third-party LLMs using AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/configure-third-party-llms-using-ai-control-tower.md)

## Fallback and Spillover

-   **Fallback**

    If you have active AI systems in ServiceNow® that aren’t supported by your enabled model providers, the ‘fallback mechanism’ enables these systems to continue operating with their default providers. However, if you choose not to enable fallback, these AI systems must be deactivated. AI systems deployed on fallback providers conform with the list of approved providers.

    **Note:** The Fallback is activated by default and can be modified.

-   **Spillover**

    Regional deployments of AI models can experience limited capacity, which could lead to request rate limiting and impact performance. Enabling spillover can help prevent these performance issues. In ServiceNow®, only Azure OpenAI currently makes this switch.


**Note:** The Spillover feature gets active or enabled when Azure OpenAI gets selected.

## Impact Summary

The Impact Summary is determined by the chosen Allowed model providers and the status of the fallback, which is either active or inactive. The Fallback significantly affects how the Impact Summary data appears in the Impact Summary table.

\[Omitted image "ai-model-providers.png"\] Alt text: AI model providers screen.

You can use the edit option to select Yes or No for activating the Fallback. Before saving, you can select Preview impact to review and confirm all your selections.

\[Omitted image "ai-preview-impact.png"\] Alt text: Preview Impact screen.

Let's review the Impact Summary table data for the following two scenarios.

-   **Activate fallback- No**

    -   Total AI systems- Shows all AI systems that are supported by the allowed model providers.
    -   AI systems supported by allowed providers- Shows AI systems with skill sets that are supported by the providers.
    -   AI systems require deactivation- Lists all active AI systems that lack provider support and must be deactivated because the fallback option isn’t enabled.
    -   AI systems can’t be activated- Shows all those systems, which are currently inactive and aren’t supported by any provider.
    \[Omitted image "ai-activate-no.png"\] Alt text: \[Omitted image ""\] Alt text: Fallback activation screen.

-   **Activate fallback- Yes**
    -   Total AI systems- Shows all AI systems that are supported by the allowed model providers.
    -   AI systems supported by allowed providers- Shows all AI systems with skill sets that are supported by the providers.
    -   AI systems supported by fallback providers- Shows AI systems that are non-compliant as fallback providers aren’t permitted providers.

\[Omitted image "ai-activate-yes.png"\] Alt text: \[Omitted image ""\] Alt text: Activate fallback option screen.

**Note:** The entries in the Impact summary table change based on the fallback status.

When you select an entry from the table, the support matrix page appears with those selected entries, allowing you to update your personalized list.

The support matrix presents all AI systems in a table format, along with their respective AI model providers. You are able to view the support matrix table and categories such as AI system, type, activation status and more, as well as the selected AI model provider.

If you have selected an AI provider, which is supported by your organization or a third party provider, the selected provider will show up in the AI systems and model provider support table.

\[Omitted image "ai-support-matrix.png"\] Alt text: Support matrix.

## Audit logs

Audit logs show configuration changes made on Data, Approvals, and AI model providers categories in AI Control Tower. You can select the **View audit logs** option to view the Audit logs.

\[Omitted image "view-audit-logs.png"\] Alt text: Audit logs.

The Audit logs page displays all the configuration changes details organized in the following categories:

-   Timestamp
-   User
-   Changed category
-   Changed setting
-   After change
-   Before change

You can also filter the changes by selecting a date range, starting with the last 90 days.

**Note:**

In the Multi-instance setup, when a managed \(sub-prod\) instance is added or removed from the syncing instances in the AI inventory information to synchronize with a specific manager \(prod\) instance, the audit logs first display a record of all instances being removed, followed by a separate record indicating the instance being added or removed.

\[Omitted image "audit-logs.png"\] Alt text: AI Control Tower Audit logs.

