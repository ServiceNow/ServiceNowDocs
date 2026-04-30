---
title: Manage AI models
description: Access and select the LLM \(large language model\) provider used for various Now Assist skills. The selection impacts all the skills within the capability.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Manage, LLM, Large language model]
breadcrumb: [Now Assist Admin Settings, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Manage AI models

Access and select the LLM \(large language model\) provider used for various Now Assist skills. The selection impacts all the skills within the capability.

## Before you begin

Role required: admin, sn\_nowassist\_admin.nsa\_admin

This feature is available in Now Assist Admin version 6.2 and Yokohama patch 6 onwards.

To enable the model provider selection, ensure that the skill is available in that region. The configuration controls for the approved model providers and corresponding compliant skills for specific regions are approved in AI Control Tower by the AI steward. For example, to update the model provider for Now Assist Q&amp;A Genius Results, ensure that all the skills under Conversational skills are available and active in the region.

As per the AI Control Tower settings, the model provider selection is available at multiple levels, including skill, skill group, and instance levels in Now Assist Admin. Therefore, in a situation where a skill is not compliant or a model provider is unavailable in a particular region, Now Assist Admin console presents the admin persona with alternate region scope options seeking approval permissions to proceed with model provider selection. For example: You opt to switch to another model provider to use a particular Now Assist skill. Consider, the region scope must be changed to global location for the skill to work. Here, you can proceed only after consenting to the region scope change.

**Note:** For regulated markets:

-   The **Manage LLM** option will not be available to customers on the Now Assist Admin user interface.
-   Only Now LLM Service skills will be available to customers. Any skill that leverages external providers \(e.g., Azure\) will be hidden on the Now Assist Admin console. With the exception of NSC region, skills leveraging Azure OpenAI is available to the users.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  Navigate to **Settings** &gt; **Manage model providers**.

    ![Now Assist admin settings - Manage model providers](../image/na-admin-settings-manage-llm.png)

3.  Review these on the **Manage model providers** page:

    -   Policy Summary set by your organization about skills using non-compliant model providers.

        **Note:** Note the routing and fallback exception details. These details are also derived from the AI Control Tower configurations.

    -   Model providers assigned to the Now Assist skills and skill groups.
    -   Policy and skill updates by the AI steward in AI Control Tower under the **Change History** tab.

-   **[Manage model providers](edit-model-providers.md)**  
Edit or customise the model provider for a skill or skill group at the instance level from the list of supported third party model providers, including the default Now LLM Service. You can also review the model policy set by your organisation, and view the change history here.
-   **[Manage Integration](manage-integration.md)**  
Choose the preferred integration type for configuring the available model providers. There are two ways to configure a model provider in Now Assist Admin. You can either select Original Equipment Manufacturer \(OEM\) or Bring Your Own Key \(BYOK\).
-   **[Manage version](manage-version.md)**  
Manage the version of the model providers across skills and instance levels. You can change and update versions for the out-of-box and custom skills.

**Parent Topic:**[Now Assist Admin Settings](configure-now-assist-admin-settings.md)

