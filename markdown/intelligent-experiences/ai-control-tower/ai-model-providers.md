---
title: AI model providers
description: AI model providers in AI Control Tower enable you to manage third-party large language models \(LLMs\) and small language models \(SLMs\) and control data routing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/ai-model-providers.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Controls, Configurations, AI Control Tower dashboard, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# AI model providers

AI model providers in AI Control Tower enable you to manage third-party large language models \(LLMs\) and small language models \(SLMs\) and control data routing.

## Data routing and model providers

Data routing is a technology by which LLM and SLM requests are routed to the most suitable datacenter. This technology helps to optimize data traffic, which reduces latency and speeds up response time.

The Data routing and model providers section enables you to route AI model requests and select the allowed model providers.There are two types of data routing:

-   **Regional data routing**

    Regional data routing routes LLM and SLM requests to datacenters within your region. For example, if you’re in the APJC \(Asia Pacific, Japan, and China\) region, these requests could be routed to the most suitable datacenter in the APJC region. Regional data routing can sometimes be mandated by governments of specific regions.

-   **Global data routing**

    When you opt for Global data routing, LLM and SLM requests are routed to the most suitable datacenter globally.


To configure third-party LLM providers, select the edit option, choose either Regional or Global data routing, and select the allowed model providers.

There are two sections of AI model providers:

-   AI model providers supported by ServiceNow. For example, Now LLM Service, AWS Claude, Now LLM-LTS \(Long Term Stable\) model.
-   AI model providers configured by your organization. For example, Perplexity, IBM Watson.

**Note:** You can select the Now LLM Service- LTS model, which supports regulated industries such as financial institutions, with stronger AI lifecycle management, governance, transparency, and compliance tools.

For more information on Now LLM Service- LTS model, see [Long term stable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/long-term-stable-models.md)

For information on exploring the scenarios configuring third-party LLMs for all the regions, see [Explore the third-party LLMs and regions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/exploring-third-party-llms-and-data-routing-configuration.md)

For information about configuring third-party LLMs through Data routing configuration for APJC region, see [Configure third-party LLMs using AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/configure-third-party-llms-using-ai-control-tower.md)

## Fallback and spillover

-   **Fallback**

    If you have active AI systems in ServiceNow® that aren’t supported by your enabled model providers, the ‘fallback mechanism’ enables these systems to continue operating with their default providers. However, if you choose not to enable fallback, these AI systems must be deactivated. AI systems deployed on fallback providers conform with the list of approved providers.

    **Note:** The Fallback is activated by default and can be modified.

-   **Spillover**

    Regional deployments of AI models can experience limited capacity, which could lead to request rate limiting and impact performance. Enabling spillover can help prevent these performance issues. In ServiceNow®, only Azure OpenAI currently makes this switch.


**Note:** The Spillover feature gets active or enabled when Azure OpenAI gets selected.

## Impact summary

The Impact summary is determined by the chosen allowed model providers and the status of the fallback, which is either active or inactive. The Fallback significantly affects how the Impact Summary data appears in the Impact summary table.

\[Omitted image "ai-model-providers.png"\] Alt text: AI model providers screen.

Select the edit option to set Fallback to Yes or No. Before saving, select Preview impact to review and confirm your selections.

\[Omitted image "ai-preview-impact.png"\] Alt text: Preview Impact screen.

The following two scenarios illustrate how the Impact Summary table data changes based on the fallback status.

-   **Activate fallback- No**

    -   Total AI systems- Shows all AI systems that are supported by the allowed model providers.
    -   AI systems supported by allowed providers- Shows AI systems with skill sets that are supported by the providers.
    -   AI systems require deactivation- Lists all active AI systems that lack provider support and must be deactivated because the fallback option isn’t enabled.
    -   AI systems can’t be activated- Shows all those systems, which are currently inactive and aren’t supported by any provider.
    \[Omitted image "ai-activate-no.png"\] Alt text: Support matrix table showing AI systems and their model providers. \[Omitted image ""\] Alt text: Fallback activation screen.

-   **Activate fallback- Yes**
    -   Total AI systems- Shows all AI systems that are supported by the allowed model providers.
    -   AI systems supported by allowed providers- Shows all AI systems with skill sets that are supported by the providers.
    -   AI systems supported by fallback providers- Shows AI systems that are non-compliant as fallback providers aren’t permitted providers.

\[Omitted image "ai-activate-yes.png"\] Alt text: Activate fallback option screen.

**Note:** The entries in the Impact summary table change based on the fallback status.

When you select an entry from the table, the support matrix page appears with those selected entries, allowing you to update your personalized list.

## Support Matrix

The support matrix displays all AI systems and their respective AI model providers in a table. You can view details such as the AI system, type, activation status, and selected AI model provider.

If you select an AI provider supported by your organization or a third party, it appears in the AI systems and model provider support table.

\[Omitted image "ai-support-matrix.png"\] Alt text:

## Model Preview Program

Model Preview Program \(MPP\) is an opt-in program that gives eligible users early access to AI models that aren't yet generally available. These models may be labeled as preview, beta, pre-release, or experimental.

With the MPP, you can:

-   Experiment with upcoming AI models before general availability \(GA\).
-   Test new AI capabilities in their environment.
-   Build and validate custom skills and agents using the latest models on the platform.
-   Provide early feedback on new model offerings.

How it works in AI Control Tower:

-   A MPP toggle appears in AI Model Providers settings.
-   The toggle is off by default.
-   An administrator must accept the terms and conditions before enabling the toggle.
-   Once enabled, eligible preview models become available for use.
-   Acceptance is audited and recorded.

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

In a multi-instance setup, when a managed \(sub-prod\) instance is added to or removed from the syncing instances, the audit log displays two records. The first record shows all instances being removed. The second record shows the instance being added or removed.

\[Omitted image "audit-logs.png"\] Alt text: AI Control Tower Audit logs.

