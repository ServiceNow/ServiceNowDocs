---
title: Configuring the Create Work Order AI agent
description: Configure the Create Work Order AI agent to appear in the Now Assist panel \(NAP\) and Now Assist Virtual Agent \(NAVA\) on the ServiceNow Agent mobile application.Configure the Create Work Order AI agent and agentic workflow to appear in the Now Assist panel.Configure the Create Work Order AI agent to appear in the Now Assist Virtual Agent on the ServiceNow Agent mobile application.
locale: en-US
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for FSM]
---

# Configuring the Create Work Order AI agent

Configure the Create Work Order AI agent to appear in the Now Assist panel \(NAP\) and Now Assist Virtual Agent \(NAVA\) on the ServiceNow Agent mobile application.

## Configure the Create Work Order agentic workflow for the Now Assist panel

Configure the Create Work Order AI agent and agentic workflow to appear in the Now Assist panel.

### Before you begin

Role required: wm\_admin

### About this task

The Create Work Order agentic workflow allows users to create work orders from the Now Assist panel. The Create Work Order AI agentic workflow is not activated by default, and must be configured to appear in the Now Assist panel.

### Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **Agentic workflows**.

2.  Select **Create work order**.

3.  Select **Select channels and status**.

4.  Toggle the **Display** for the Now Assist panel so that it's turned on.

    ![Create Work Order configuration screen with Display set to active.](../image/now-assist-create-wo-nap-display.png)

    You have enabled the agentic workflow in the Now Assist panel. If the option isn't available, you must enable the panel first. For more information, see Activate the Now Assist panel standard chat.

5.  Select **Save and test**.


### Result

The Create Work Order agentic workflow will appear in the Now Assist panel. The workflow can be triggered by asking Now Assist to create a work order, or by selecting the Create Work Order button. For more information, see [Create a work order using Now Assist for Field Service Management \(FSM\)](../task/create-work-order-now-assist-fsm.md).

## Configure the Create Work Order AI Agent for the Now Assist Virtual Agent

Configure the Create Work Order AI agent to appear in the Now Assist Virtual Agent on the ServiceNow Agent mobile application.

### Before you begin

Role required: wm\_admin

### About this task

The Create Work Order AI agent allows users to create work orders in the ServiceNow Agent mobile application using Now Assist Virtual Agent. The Create Work Order AI agent is not activated by default, and must be configured to appear in the ServiceNow Agent mobile application.

### Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI Agent**.

2.  Select **Create work order**.

3.  Select **Select channels and status**.

4.  Toggle the **Allow** slider for the Virtual Agent assistants so that it's turned on.

    ![Create Work Order configuration screen with Allow set to active.](../image/now-assist-create-wo-nava-allow.png)

5.  In the **Chat assistants** field, select **Now Assist Virtual Agent for FSM**.

6.  Select **Save and test**.


### Result

The Create Work Order AI agent will appear in the ServiceNow Agent mobile application. The agent can be triggered by asking Now Assist to create a work order, or by selecting the Create Work Order button. For more information, see [Create a work order on ServiceNow Agent using Now Assist for Field Service Management \(FSM\)](../task/create-work-order-mobile-now-assist-fsm.md).

