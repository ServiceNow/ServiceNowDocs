---
title: AI model providers
description: AI model providers enable you to select data routing and manage third-party LLMs \(Large language models\) and SLMs \(Small language models\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-model-providers.html
release: australia
topic_type: concept
last_updated: "2026-08-14"
reading_time_minutes: 5
breadcrumb: [Configure ServiceNow AI settings, Configure, AI Control Tower, Enable AI experiences]
---

# AI model providers

AI model providers enable you to select data routing and manage third-party LLMs \(Large language models\) and SLMs \(Small language models\).

## Overview of AI model providers

The AI Control Tower provides an AI model providers section where administrators can configure how AI requests are routed and which model providers are permitted on the instance. There are two categories of AI model providers:

-   AI model providers supported by ServiceNow. For example, Now LLM Service, AWS Claude, Now LLM-LTS \(Long Term Stable\) model.
-   AI model providers configured by your organization. For example, Perplexity, IBM Watson.

**Note:** You can select the Now LLM-LTS \(Long Term Stable\) model, which supports regulated industries such as financial institutions with stronger AI lifecycle management, governance, transparency, and conformance tools.

For more information on the Now LLM-LTS \(Long Term Stable\) model, see [Long term stable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/long-term-stable-models.md)

## Data routing and model providers

Data routing is a technology by which LLM and SLM requests are routed to the most suitable datacenter. This technology helps to optimize data traffic, which reduces latency and speeds up response time.

The Data routing and model providers section enables you to route AI model requests and select the allowed model providers. There are two types of data routing:

|Data routing type|Description|
|-----------------|-----------|
|Regional data routing|Routes LLM and SLM requests to datacenters within your region. For example, if you're in the APJC \(Asia Pacific, Japan, and China\) region, requests are routed to the most suitable datacenter in the APJC region. Regional data routing can be mandated by governments of specific regions.|
|Global data routing|Routes LLM and SLM requests to the most suitable datacenter globally, regardless of the region where the request originates.|

You can configure third-party LLM providers using the edit option by choosing either Regional or Global data routing and selecting all the Allowed model providers.

## Model Preview Program

Model Preview Program \(MPP\) is an opt-in program that gives eligible users early access to AI models that aren't yet generally available. These models may be labeled as preview, beta, pre-release, or experimental.

With the MPP, you can:

-   Experiment with upcoming AI models before general availability.
-   Test new AI capabilities in their environment.
-   Build and validate custom skills and agents using the latest models on the platform.
-   Provide early feedback on new model offerings.

How MPP works in AI Control Tower:

-   An MPP toggle appears in AI Model Providers settings.
-   The toggle is off by default.
-   An administrator must accept the terms and conditions before enabling the toggle.
-   When enabled, eligible preview models are set to available for use.
-   Acceptance is audited and recorded.

## Fallback and spillover

|Feature|Description|
|-------|-----------|
|Fallback|If you have active AI systems that aren't supported by your enabled model providers, the fallback mechanism enables these systems to continue operating with their default providers. If you choose not to enable fallback, these AI systems must be deactivated. AI systems deployed on fallback providers conform with the list of approved providers. The Fallback is activated by default and can be modified.|
|Spillover|Regional deployments of AI models can experience limited capacity, which could lead to request rate limiting and impact performance. Enabling spillover can help prevent these performance issues. In ServiceNow, only Azure OpenAI currently makes this switch. The Spillover feature is set to active when Azure OpenAI is selected.|

## Impact summary

The Impact Summary is determined by the chosen allowed model providers and the status of the fallback \(active or inactive\). The Fallback significantly affects how the Impact summary data appears in the Impact summary table.

You can use the edit option to select **Yes** or **No** for activating the Fallback. Before saving, you can select Preview impact to review and confirm all your selections.

**Activate fallback: No**

When Fallback is set to No, the Impact summary table shows:

-   Total AI systems — all AI systems supported by the allowed model providers.
-   AI systems supported by allowed providers — AI systems with skill sets supported by the providers.
-   AI systems require deactivation — all active AI systems that lack provider support and must be deactivated because the fallback option is not enabled.
-   AI systems can't be activated — all systems currently inactive and not supported by any provider.

**Activate fallback: Yes**

When Fallback is set to Yes, the Impact Summary table shows:

-   Total AI systems — all AI systems supported by the allowed model providers.
-   AI systems supported by allowed providers — all AI systems with skill sets supported by the providers.
-   AI systems supported by fallback providers — AI systems that are non-conforming because fallback providers aren't permitted providers.

**Note:** The entries in the Impact summary table change based on the fallback status. When you select an entry from the table, the support matrix page appears with those selected entries, allowing you to update your personalized list.

## Support matrix

The support matrix presents all AI systems in a table format, along with their respective AI model providers. The support matrix table includes categories such as AI system, type, activation status, and the selected AI model provider.

When you select an AI provider, it appears in the AI systems and model provider support table.

## Audit logs

Audit logs show configuration changes made on Data, Approvals, and AI model providers categories in the AI Control Tower Workspace. Select the View audit logs option to view the Audit logs page.

The Audit logs page displays all configuration change details organized in the following categories:

-   Timestamp
-   User
-   Changed category
-   Changed setting
-   After change
-   Before change

You can also filter the changes by selecting a date range, starting with the last 90 days.

**Note:** In a Multi-instance setup, when a managed \(sub-prod\) instance is added to or removed from the synchronizing instances, the audit log displays two records. The first record shows all instances being removed and the second record shows the instance being added or removed.

**Parent Topic:**[Configure ServiceNow AI settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-servicenow-ai-settings.md)

