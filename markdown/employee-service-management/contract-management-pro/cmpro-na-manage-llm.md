---
title: Select large language models for use cases in ServiceNow Otto for Contract Management Pro
description: Select a large language model \(LLM\) provider for a contract analysis or metadata extraction use case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-na-manage-llm.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Set LLM for Now Assist skills, Set LLM for ServiceNow Otto skills, Set LLM at skill level]
breadcrumb: [Configure, ServiceNow Otto for Contract Management Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Select large language models for use cases in ServiceNow Otto for Contract Management Pro

Select a large language model \(LLM\) provider for a contract analysis or metadata extraction use case.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_admin

## About this task

You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all generative AI skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md).

In ServiceNow Otto for Contract Management Pro, you can select the LLM provider at the use case level. This selected LLM is applicable only for the use case and overrides the LLM selected at the skill level.

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **AI Admin Hub** to access the **AI Skills** tab of the AI Admin Hub console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  On the tile of your activated skill that you want to modify, select **Edit Configuration** in the options menu \(\[Omitted image "cmpro-na-three-dot-icon.png"\] Alt text: Options menu icon.\).

    \[Omitted image "cmpro-na-active-skills.png"\] Alt text: AI skills in Contract Management Pro.

4.  In the skill guided setup, select **Use cases**.

5.  Open the use case for which you want to set the LLM.

6.  Select the settings icon \(\[Omitted image "gear-icon.png"\] Alt text: Settings icon.\).

    \[Omitted image "cmpro-na-use-case-gear.png"\] Alt text: Settings in the Use case page.

7.  In the Settings window, select **Manage LLMs**.

    \[Omitted image "cmpro-na-llm-setting.png"\] Alt text: Manage LLM Provider in use case settings.

8.  From the LLM provider drop-down list, select the LLM provider.

9.  In the Settings window, select **Save**.

10. In the use cases page, select **Save and continue**.

11. In the Review and activate page, select **Done**.


## Result

The LLM provider is set for the use case and is used for contract analysis or metadata extraction where this use case is applicable.

**Parent Topic:**[Configure ServiceNow Otto for Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/confg-na-in-cmpro.md)

**Related topics**  


[Configure data permissions for AI skills]()

[Configuring contract metadata extraction]()

[Configuring contract analysis]()

[Configuring contract obligation extraction]()

[Configuring agentic workflows in ServiceNow Otto for Contract Management Pro]()

[Post-upgrade steps for ServiceNow Otto for Contract Management Pro]()

[Configure ServiceNow Otto for Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/confg-na-in-cmpro.md)

[Create use cases for contract metadata extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-na-usecase-me.md)

[Create use cases for contract analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-na-usecase-ca.md)

