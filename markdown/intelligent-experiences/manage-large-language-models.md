---
title: Manage AI models
description: Access and select the LLM \(large language model\) provider used for various AI skills. The selection impacts all the skills within the capability.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/manage-large-language-models.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Manage, LLM, Large language model]
breadcrumb: [AI Admin Hub Settings, Exploring AI Admin Hub, AI Admin Hub, Enable AI experiences]
---

# Manage AI models

Access and select the LLM \(large language model\) provider used for various AI skills. The selection impacts all the skills within the capability.

## Before you begin

Role required: admin, sn\_nowassist\_admin.nsa\_admin

This feature is available in AI Admin Hub version 6.2 and Yokohama patch 6 onwards.

To enable the model provider selection, confirm that the skill is available in that region. The configuration controls for the approved model providers and corresponding conforming skills for specific regions are approved in AI Control Tower by the AI steward. For example, to update the model provider for ServiceNow Otto Q&amp;A Genius Results, confirm that all the skills under Conversational skills are available and active in the region.

As per the AI Control Tower settings, the model provider selection is available at multiple levels, including skill, skill group, and instance levels in AI Admin Hub. When a skill is not conforming or a model provider is unavailable in a particular region, AI Admin Hub console presents the admin persona with alternate region scope options. It seeks approval permissions to proceed with model provider selection. For example: You opt to switch to another model provider to use a particular AI skill. Consider, the region scope must be changed to global location for the skill to work. Here, you can proceed only after consenting to the region scope change.

**Note:** For regulated markets:

-   The **Manage LLM** option will not be available on the AI Admin Hub user interface.
-   Only Now LLM Service skills will be available. Any skill that leverages external providers \(e.g., Azure\) will be hidden on the AI Admin Hub console. With the exception of NSC region, skills leveraging Azure OpenAI is available to the users.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Settings**.

2.  Navigate to **Settings** &gt; **Manage model providers**.

    \[Omitted image "na-admin-settings-manage-llm.png"\] Alt text: ServiceNow Otto admin settings - Manage model providers

3.  Review these on the **Manage model providers** page:

    -   Policy Summary set by your organization about skills using non-conforming model providers.

        **Note:** Note the routing and fallback exception details. These details are also derived from the AI Control Tower configurations.

    -   Model providers assigned to the AI skills and skill groups.
    -   Policy and skill updates by the AI steward in AI Control Tower under the **Change History** tab.

-   **[Manage model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/edit-model-providers.md)**  
Edit or customise the model provider for a skill or skill group at the instance level from the list of supported third-party model providers, including the default Now LLM Service. You can also review the model policy set by your organisation, and view the change history here.
-   **[Manage Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/manage-integration.md)**  
Choose the preferred integration type for configuring the available model providers. There are two ways to configure a model provider in AI Admin Hub. You can either select Original Equipment Manufacturer \(OEM\) or Bring Your Own Key \(BYOK\).
-   **[Manage version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/manage-version.md)**  
Manage the version of the model providers across skills and instance levels. You can change and update versions for the out-of-box and custom skills.

**Parent Topic:**[AI Admin Hub Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/configure-now-assist-admin-settings.md)

