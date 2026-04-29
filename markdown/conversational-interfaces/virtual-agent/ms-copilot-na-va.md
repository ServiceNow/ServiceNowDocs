---
title: Integrating Now Assist in Virtual Agent with Microsoft Copilot
description: Integrate your Now Assist Virtual Agent with Microsoft Copilot using Conversational Integration with Microsoft Teams to leverage the generative AI conversational experience.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Integrating, Now Assist, Virtual Agent, Microsoft, Copilot, Conversational Integration, Teams, MSTeams, sn\_va\_teams]
breadcrumb: [Use Now Assist in VA conversations with Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrating Now Assist in Virtual Agent with Microsoft Copilot

Integrate your Now Assist Virtual Agent with Microsoft Copilot using Conversational Integration with Microsoft Teams to leverage the generative AI conversational experience.

**Note:** Custom Engine Agent \(CEA\) is replacing Declarative Agent \(DA\), the prior Microsoft Copilot integration. The CEA enables Virtual Agent to be discoverable by Microsoft Copilot, with full functional access to Now Assist in Virtual Agent and multi-turn conversations.

You must have version 10.1.1 or higher of the Microsoft Teams plugin to have CEA support. In version 10.2 of the Microsoft Teams plugin, streaming is inactive by default and CEA is active by default.

Microsoft Copilot and Now Assist are generative AI assistants that work together. The Microsoft Copilot integration with Now Assist in Virtual Agent enables users to get answers and take actions straight from Copilot. Meanwhile, Copilot can hand off requests to Now Assist in Microsoft Teams.The Microsoft Copilot integration uses the existing setup and configuration experience for Microsoft Teams through the Conversational Integration with Microsoft Teams application, because the primary use case for Copilot is an extension of Microsoft Teams.

You can install the default Now Assist Virtual Agent bot from the Microsoft Teams app store. This bot deploys automatically, but you cannot customize its prompts or manifest description. You must still install the ServiceNow Microsoft Teams plugin from the ServiceNow app store.

The default Conversational Integration with Microsoft Teams plugin \(sn\_va\_teams\) automatically integrates with Copilot. For the integration to work automatically, verify that you have:

-   The Xanadu version of the Conversational Integration with Microsoft Teams application installed and configured. If you have a previous version of the application, upgrade it to the Xanadu release.
-   Either a Microsoft Copilot license or the free Copilot chat license.

    **Note:**

    -   Before the integration, make sure that Copilot is enabled on your Microsoft Teams tenant.
    -   No configuration changes are required on your ServiceNow instance to integrate with Microsoft Copilot.
    -   There are no additional configurations required for Copilot.
-   The Now Assist license and verify that the Now Assist in Virtual Agent is configured. For more information, see [Configuring assistants overview](../../now-assist-in-va/task/configure-now-assist-va.md).
-   Enable the teams bot \(the Now Virtual Agent bot or the Self-configured bot, which you would like to use for Copilot integration\) for the Now Assist Conversations in the **All** &gt; **Conversational Interfaces** &gt; **Assistants** &gt; **Display experience** &gt; **Channels** section.

    For more information, see [Configuring assistants overview](../../now-assist-in-va/task/configure-now-assist-va.md).


## Integrate Microsoft Copilot with Now Virtual Agent bot

If you're using the default Now Virtual Agent bot, no additional setup is required. The process of integrating the Now Virtual Agent bot with Microsoft Copilot is similar to that of integrating the Now Virtual Agent bot with Microsoft Teams.

For more information, see [Integrating Virtual Agent with Microsoft Teams](va-integ-msteams.md).

To interact with the Now Virtual Agent bot within Copilot, you can either @-mention the bot name and invoke it or navigate to the Agents section on the right panel within Copilot to select it for direct interaction.

![Select the Now Virtual Agent bot within Copilot for your interaction.](../images/copilot-select-now-bot.png "Selecting the Now Virtual Agent bot within Copilot")

The default Now Virtual Agent app that is compatible with Microsoft Copilot integration is available on the Microsoft Teams store for use.

## Integrate Microsoft Copilot with Self-configured bot

Use your Self-configured bot to connect with Microsoft Copilot. The process of integrating the Self-configured bot with Microsoft Copilot is similar to that of integrating the Self-configured bot with Microsoft Teams. For more information, see [Integrating Virtual Agent with Microsoft Teams using the self-configured bot](va-integ-teams-self-configured-bot.md).

The self-configured bot will support the latest Copilot CEA experience. The out-of-the-box production bot will continue to provide support until October 2025. For more information, see [Setting up the Self-configured bot for using Microsoft Copilot](setup-self-bot-copilot.md) and

-   **[Setting up the Self-configured bot for using Microsoft Copilot](setup-self-bot-copilot.md)**  
Using your Self-configured bot with Microsoft Copilot for Now Assist conversations requires you to complete a few additional setup actions.
-   **[Now Assist in Virtual Agent conversations with Microsoft Copilot](na-ms-copilot-conversations.md)**  
Use Now Assist plugins in Microsoft Copilot to connect with the Copilot by providing your bot or plugin name during your generative AI conversations.

**Parent Topic:**[Using Now Assist in Virtual Agent conversations with Microsoft Teams](na-va-llm-teams.md)

