---
title: Debug Virtual Agent Bot Interconnect with a ServiceNow Virtual Agent secondary bot
description: Debug Workflow Studio executions of your Virtual Agent Bot Interconnect and Virtual Agent secondary bot integration.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Debug, Virtual Agent, Bot interconnect, Workflow studio, integration]
breadcrumb: [Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Debug Virtual Agent Bot Interconnect with a ServiceNow Virtual Agent secondary bot

Debug Workflow Studio executions of your Virtual Agent Bot Interconnect and Virtual Agent secondary bot integration.

## Before you begin

Enable the following system properties:

-   **sn\_va\_bot\_ic.bot\_interconnect.enable.logging** = true
-   **glide.outbound\_http\_log.override** = true
-   **glide.outbound\_http\_log.override.level** = all

For more information, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

Role required: admin

## Procedure

1.  In the Bot Interconnect instance, modify the shell topic you created in Virtual Agent:

    1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

    2.  Open the shell topic you created in a previous step.

    3.  On the **Flow** tab, select the Bot Interconnect Topic Block.

    4.  In the **Additional Params \(String\)** field, select the Script icon ![Script icon.](../images/icon-script.png), and then add the following code:

        ```
        (function execute() {
          return JSON.stringify({quick: false}); 
        })()
        ```

    5.  Select Save.

    6.  Save the topic.

2.  Enable execution context debugging in Workflow Studio.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Process Automation Designer** &gt; **Flow Administration** &gt; **Settings**.

    2.  On the Settings page, select **New**.

    3.  In the **Flow/Subflow/Action** field, select the Search icon ![Search icon.](../images/icon-search.png).

    4.  On the Select the document form, fill in the fields.

        Add the following Flow Designer document settings if your secondary bot is in synchronous mode.

        ![Document setting for the primary bot in Workflow Studio if secondary bot is synchronous. Table name is Flow, and Document is VA API Bot Interconnect Integration Handler.](../images/debug-sn-sn-select-document-primary.png) ![Document setting for the primary bot in Workflow Studio if secondary bot is synchronous. Table name is Action Type, and Document is Bot Interconnect Sync Integration Handler.](../images/debug-sn-sn-select-document-secondary.png)

        Add the following Flow Designer document settings if your secondary bot is in asynchronous mode.

        ![Document setting for the primary bot in Workflow Studio if secondary bot is synchronous. Table name is Flow, and Document is VA API Bot Interconnect Integration Handler.](../images/Document-setting-secondary-bot-async1.png) ![Document setting for the primary bot in Workflow Studio if secondary bot is asynchronous.](../images/Document-setting-secondary-bot-async2.png) ![Document setting for the primary bot in Workflow Studio if secondary bot is synchronous. Table name is Action Type, and Document is Bot Interconnect Sync Integration Handler.](../images/Document-setting-secondary-bot-async3.png)

    5.  Select **Ok**.

    6.  In the **Reporting** field, select **Developer Trace**.

    7.  Select **Submit**.


## Result

You can view additional logs and Workflow Studio executions for debugging purposes.

**Parent Topic:**[Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect](../concept/using-sn-secondary-bot-with-sn-primary.md)

**Previous topic:**[Enable live agent connection on the primary instance](../concept/enable-live-agent-connection-on-the-secondary-instance.md)

**Next topic:**[Localization options for Virtual Agent](../concept/multi-language-options-va.md)

