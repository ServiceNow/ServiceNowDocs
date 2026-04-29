---
title: Setting up the Self-configured bot for using Microsoft Copilot
description: Using your Self-configured bot with Microsoft Copilot for Now Assist conversations requires you to complete a few additional setup actions.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Integrating, Now Assist, Virtual Agent, Microsoft, Copilot, Conversational Integration, Teams, MSTeams, sn\_va\_teams]
breadcrumb: [Integrating Now Assist in Virtual Agent with Microsoft Copilot, Use Now Assist in VA conversations with Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Setting up the Self-configured bot for using Microsoft Copilot

Using your Self-configured bot with Microsoft Copilot for Now Assist conversations requires you to complete a few additional setup actions.

**Note:** Custom Engine Agent \(CEA\) is replacing Declarative Agent \(DA\), the prior Microsoft Copilot integration. The CEA enables Virtual Agent to be discoverable by Microsoft Copilot, with full functional access to Now Assist in Virtual Agent and multi-turn conversations.

You must have version 10.1.1 or higher of the Microsoft Teams plugin to have CEA support. In version 10.2 of the Microsoft Teams plugin, streaming is inactive by default and CEA is active by default.

You can install the default Now Assist Virtual Agent bot from the Microsoft Teams app store. This bot deploys automatically, but you cannot customize its prompts or manifest description. You must still install the ServiceNow Microsoft Teams plugin from the ServiceNow app store.

For more information on Microsoft Teams and Now Assist in Virtual Agent installation and settings, see [.](ms-copilot-na-va.md)

As of October 2025, streaming is active by default for both Teams and Copilot. Configurations are shared by Teams and Copilot, and both apps are linked to the assistant.

You can use the self-configured bot or the default version to install Microsoft Copilot integration. The default bot automatically deploys in Copilot. If you want to use a self-configured bot for Microsoft Copilot, complete the following additional setup:

-   Provide the Self-configured bot a name while creating it. This name is also provided to the Custom Engine Agent \(CEA\).
-   Activate your assistant in the Conversational Interfaces configuration page. For more information, see [Configuring assistants overview](../../now-assist-in-va/task/configure-now-assist-va.md).
-   Migrate any relevant topics to the Now LLM Service for Now Assist large language model \(LLM\) conversations with Copilot. To migrate your topics to LLM, you must enable LLM. For more information, see [Migrate NLU topics to LLM topics](../task/migrate-nlu-llm.md).
-   Update the following fields within the manifest file that is downloaded from Admin experience to configure the Self-configured bot. You can update your agent's description and update its prompts if it has any unique capabilities.

    ![Use the Microsoft Teams channel page in Conversational Interfaces Channels and Integrations to create and manage app settings.](../images/ci-settings-msteams.png "Conversational Interfaces Microsoft Teams channel page")

    Update the generic description that ServiceNow provides with a specific use case that you may have in your topics.

    For example, if you have unique LLM skills that accomplish scenarios unique to your environment, such as reserving a hotel desk or ordering food for a meeting, add those skills to your description so that Copilot is able to recognize the skill and process it.

    For more information, refer to [App manifest scheme](https://learn.microsoft.com/en-us/microsoftteams/platform/resources/schema/manifest-schema) in the Microsoft Teams Developer documentation.

-   Activate the Copilot check box on the Conversational Interfaces admin page before uploading your manifest.

**Parent Topic:**[Integrating Now Assist in Virtual Agent with Microsoft Copilot](ms-copilot-na-va.md)

