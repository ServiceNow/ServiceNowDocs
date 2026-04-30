---
title: Enable live agent connection on the primary instance
description: Enable live agent connection on the primary instance to route an interaction to a live agent on the secondary instance.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Enable live agent connection on the primary instance

Enable live agent connection on the primary instance to route an interaction to a live agent on the secondary instance.

## Before you begin

Be sure to enable **com.glide.cs.external.agent.chat.enabled** system property. It’s not enabled by default.

Role required: admin or virtual\_agent\_admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Live Agent Connections**.

2.  Select **New** to create a connection.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the connection|
    |Active|Check box to enable the connection|
    |Order|If there are multiple matching live agent connections, the value entered in this field determines the order in which the matching connections are displayed to the user.|
    |Advanced|Selecting this check box opens the **Script** field. You can specify conditions using JavaScript in the script editor.|
    |Condition Table|Table used for selecting the matching condition. **Interaction** table is selected by default.|
    |Matching Condition|Conditions to route the interaction to this live agent connection. Use the condition builder to add conditions. The fields used in the condition are from the Interaction table.|
    |Script|JavaScript script that specifies the conditions for the interaction to be routed to this live agent connection. The condition in the script editor must evaluate to true. This field is enabled only when you select the **Advanced** check box.|
    |Subflow|Subflow transforms the request into the secondary instance request format and routes the request to the secondary instance. Select **VA API Bot Interconnect Integration Handler**.|

    ![Live agent connection configuration with condition builder](../images/live-agent-connection-condition-builder.png)![Live agent connection configuration with JavaScript](../images/live-agent-connection-javascript-condition-editor.png)

4.  Click **Submit**.


**Parent Topic:**[Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect](using-sn-secondary-bot-with-sn-primary.md)

**Previous topic:**[Create a Virtual Agent Bot Interconnect shell topic to call Virtual Agent secondary topics](../task/create-va-topic-sn-primary-secondary-config.md)

**Next topic:**[Debug Virtual Agent Bot Interconnect with a ServiceNow Virtual Agent secondary bot](../task/debug-bot-sn-sn-configuration.md)

