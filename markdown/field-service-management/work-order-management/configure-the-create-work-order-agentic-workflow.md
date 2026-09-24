---
title: Configure the Create Work Order agentic workflow for the ServiceNow Otto panel
description: Configure the Create Work Order AI agent and agentic workflow to appear in the ServiceNow Otto panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/configure-the-create-work-order-agentic-workflow.html
release: brazil
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Set up work orders and tasks, Configure, Field Service Management]
---

# Configure the Create Work Order agentic workflow for the ServiceNow Otto panel

Configure the Create Work Order AI agent and agentic workflow to appear in the ServiceNow Otto® panel.

## Before you begin

Role required: wm\_admin

## About this task

The Create Work Order agentic workflow allows users to create work orders from the ServiceNow Otto® panel. The Create Work Order AI agentic workflow is not activated by default, and must be configured to appear in the ServiceNow Otto® panel.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **Agentic workflows**.

2.  Select **Create work order**.

3.  Select **Select channels and status**.

4.  Toggle the **Display** for the ServiceNow Otto® panel so that it's turned on.

    \[Omitted image "work-order-otto-panel.png"\] Alt text: servicenow otto panel selection

    You have enabled the agentic workflow in the ServiceNow Otto® panel. If the option isn't available, you must enable the panel first. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activate-now-assist-panel.md).

5.  Select **Save and test**.


## Result

The Create Work Order agentic workflow will appear in the ServiceNow Otto® panel. The workflow can be triggered by asking ServiceNow Otto® to create a work order, or by selecting the Create Work Order button. For more information, see [Create a work order using ServiceNow Otto for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/create-work-order-now-assist-fsm.md).

