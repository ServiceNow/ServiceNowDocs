---
title: Configure the Create Work Order AI Agent for the Now Assist Virtual Agent
description: Configure the Create Work Order AI agent to appear in the Now Assist Virtual Agent on the ServiceNow Agent mobile application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/field-service-management/work-order-management/configure-create-work-order-ai-agent.html
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-12-01"
reading_time_minutes: 1
breadcrumb: [Configure, Work orders and tasks, Configure, Field Service Management]
---

# Configure the Create Work Order AI Agent for the Now Assist Virtual Agent

Configure the Create Work Order AI agent to appear in the Now Assist Virtual Agent on the ServiceNow Agent mobile application.

## Before you begin

Role required: wm\_admin

## About this task

The Create Work Order AI agent allows users to create work orders in the ServiceNow Agent mobile application using Now Assist Virtual Agent. The Create Work Order AI agent is not activated by default, and must be configured to appear in the ServiceNow Agent mobile application.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI Agent**.

2.  Select **Create work order**.

3.  Select **Select channels and status**.

4.  Toggle the **Allow** slider for the Virtual Agent assistants so that it's turned on.

    \[Omitted image "now-assist-create-wo-nava-allow.png"\] Alt text: Create Work Order configuration screen with Allow set to active.

5.  In the **Chat assistants** field, select **Now Assist Virtual Agent for FSM**.

6.  Select **Save and test**.


## Result

The Create Work Order AI agent will appear in the ServiceNow Agent mobile application. The agent can be triggered by asking Now Assist to create a work order, or by selecting the Create Work Order button. For more information, see [Create a work order on ServiceNow Agent using ServiceNow Otto for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/work-order-management/create-work-order-mobile-now-assist-fsm.md).

