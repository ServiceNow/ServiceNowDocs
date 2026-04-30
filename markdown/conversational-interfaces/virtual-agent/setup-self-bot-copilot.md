---
title: Setting up the Self-configured bot for using Microsoft Copilot
description: Using your Self-configured bot with Microsoft Copilot for Now Assist conversations requires you to complete a few additional setup actions.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 3
keywords: [Integrating, Now Assist, Virtual Agent, Microsoft, Copilot, Conversational Integration, Teams, MSTeams, sn\_va\_teams]
breadcrumb: [Integrating Now Assist in Virtual Agent with Microsoft Copilot, Conversational Integration with Microsoft Teams, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Setting up the Self-configured bot for using Microsoft Copilot

Using your Self-configured bot with Microsoft Copilot for Now Assist conversations requires you to complete a few additional setup actions.

However, if you want to use a self-configured bot for Microsoft Copilot, you must complete the following additional setup:

-   Provide the Self-configured bot a name while creating it. Providing a name for the bot improves the reliability of the bot responses within Copilot conversations.
-   Enable Copilot integration with Now Assist in Virtual Agent. For more information, see [Enable Now Assist experience in Virtual Agent API](enable-now-assist-in-virtual-agent-experience-in-virtual-agent-api.md).
-   Migrate any relevant topics to the Now LLM Service for Now Assist large language model \(LLM\) conversations with Copilot. To migrate your topics to LLM, you must enable LLM. For more information, see [Migrate NLU topics to LLM topics](../task/migrate-nlu-llm.md).

    **Note:** After enabling LLM, you don't need to do anything specific for the Copilot as it pertains to LLM topics. As long as the Self-configured bot is discoverable by the LLM, it's also discoverable by the Copilot and verifies that the plugin or bot responds when it’s used.

-   Enable AI Search on your ServiceNow Now Assist instance to use Now Assist with Microsoft Copilot. For more information about enabling AI Search, see [Enable AI Search for Next Experience](https://www.servicenow.com/docs/access?context=enable-ais-next-exp-app&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   Update the following fields within the manifest file that is downloaded from Admin experience to configure the Self-configured bot and use it for the Copilot integration.

    ![Update the description, semantic description, and sample prompts on the manifest.json file to reflect your Self-configured bot name.](../images/manifest-json-changes-copilot.png "manifest.json changes for Copilot integration")

    -   **Full Description**:
        -   Update the bot name in the full description to your Self-configured bot name.

            **Note:** Update the bot name in all the instances in the full description. Updating the bot name helps Copilot to identify the bot that the request must be routed to.

        -   Update the generic description that ServiceNow provides with a specific use case that you may have in your topics.

            For example, if you have unique LLM skills that accomplish scenarios unique to your environment, such as reserving a hotel desk or ordering food for a meeting, be sure to add that to your description so that Copilot will be able to recognize the skill and be able to process it.

    -   **View Prompts**: Add the prompts with your bot name.

        **Note:** The JSON prompts aren’t available in the manifest file by default. You must add them yourself and update the bot name with your Self-configured bot name.

        ```
        {
        "Sana What is our laptop replacement policy?"
        },
        ```

        **Note:** Updating the bot name on the prompt helps the utterance work with Copilot.

        ![Prompts are displayed while you connect with the Copilot using your plugin or bot name.](../images/view-prompts.png "View Prompts")

    For more information, refer to [App manifest scheme](https://learn.microsoft.com/en-us/microsoftteams/platform/resources/schema/manifest-schema) in the Microsoft Teams Developer documentation.

-   Enable Message Extension for the Self-configured bot, generate the new manifest file, and upload it to Microsoft Teams.

    -   **Message Extension in Microsoft Copilot Integration**

        The Microsoft Copilot integration is built on top of the existing Message Extension feature. For more information about enabling Message Extension for your bot on your ServiceNow instance, see [Auto-generate the manifest file for uploading on Microsoft Teams](../task/generate-manifest-file-msteams.md).

        When the message extension is enabled, you see the list of message extension-enabled apps when you select the Plugins icon \(![Plugins icon.](../images/plugin-bot-copilot.png)\). You can select the app of your choice from the list of plugins.

        ![Microsoft Copilot displaying the Message Extension-enabled apps.](../images/message-extension-teams.png "Message Extension in Copilot")

    **Note:** Users can update the manifest file to enhance the Copilot's Orchestration.

-   Edit, customize, and enhance the bot behavior to meet your needs. For more information, see [Guidelines to create or upgrade Copilot extensions](https://learn.microsoft.com/en-us/microsoftteams/platform/messaging-extensions/high-quality-message-extension?tabs=tasks).

