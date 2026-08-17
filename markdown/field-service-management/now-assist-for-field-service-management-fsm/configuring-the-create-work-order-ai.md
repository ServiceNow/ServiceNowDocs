---
title: Configuring the Create Work Order AI agent
description: Configure the Create Work Order AI agent to appear in the ServiceNow Otto panel and ServiceNow Otto Virtual Agent on the ServiceNow Agent mobile application.Configure the Create Work Order AI agent and agentic workflow to appear in the ServiceNow Otto panel.Configure the Create Work Order AI agent to appear in the ServiceNow Otto Virtual Agent on the ServiceNow Agent mobile application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/now-assist-for-field-service-management-fsm/configuring-the-create-work-order-ai.html
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, ServiceNow Otto for FSM]
---

# Configuring the Create Work Order AI agent

Configure the Create Work Order AI agent to appear in the ServiceNow Otto panel and ServiceNow Otto Virtual Agent on the ServiceNow Agent mobile application.

## Configure Create Work Order agentic workflow for ServiceNow Otto

Configure the Create Work Order AI agent and agentic workflow to appear in the ServiceNow Otto panel.

### Before you begin

Role required: wm\_admin

### About this task

The Create Work Order agentic workflow allows users to create work orders from the ServiceNow Otto panel. The Create Work Order AI agentic workflow is not activated by default, and must be configured to appear in the ServiceNow Otto panel.

### Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

2.  Select the **Agentic workflows** tab.

3.  Select **Create work order**.

4.  Select **Select channels and status**.

5.  Allow the agentic workflow to be available through the ServiceNow Otto panel.

    The agentic workflow is enabled in the ServiceNow Otto panel. If the option isn't available, you must enable the panel first. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).

6.  Select **Save and test**.


### Result

The Create Work Order agentic workflow will appear in the ServiceNow Otto panel. The workflow can be triggered by asking ServiceNow Otto to create a work order, or by selecting the Create Work Order option. For more information, see [Create a work order using ServiceNow Otto for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/create-work-order-now-assist-fsm.md).

## Configure the Create Work Order AI Agent for the ServiceNow Otto Virtual Agent

Configure the Create Work Order AI agent to appear in the ServiceNow Otto Virtual Agent on the ServiceNow Agent mobile application.

### Before you begin

Role required: wm\_admin

### About this task

The Create Work Order AI agent allows users to create work orders in the ServiceNow Agent mobile application using ServiceNow Otto Virtual Agent. The Create Work Order AI agent is not activated by default, and must be configured to appear in the ServiceNow Agent mobile application.

### Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI Agent**.

2.  Select **Create work order**.

3.  Select **Select channels and status**.

4.  Toggle the **Allow** slider for the Virtual Agent assistants so that it's turned on.

5.  In the **Chat assistants** field, select **ServiceNow Otto Virtual Agent for FSM**.

6.  Select **Save and test**.


### Result

The Create Work Order AI agent will appear in the ServiceNow Agent mobile application. The agent can be triggered by asking ServiceNow Otto to create a work order, or by selecting the Create Work Order button. For more information, see [Create a work order on ServiceNow Agent using ServiceNow Otto for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/create-work-order-mobile-now-assist-fsm.md).

