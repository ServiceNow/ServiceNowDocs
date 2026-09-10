---
title: Configure the Create Work Order agentic workflow for the Now Assist panel
description: Configure the Create Work Order AI agent and agentic workflow to appear in the Now Assist panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/field-service-management/work-order-management/configure-the-create-work-order-agentic-workflow.html
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-12-01"
reading_time_minutes: 1
breadcrumb: [Configure, Work orders and tasks, Configure, Field Service Management]
---

# Configure the Create Work Order agentic workflow for the Now Assist panel

Configure the Create Work Order AI agent and agentic workflow to appear in the Now Assist panel.

## Before you begin

Role required: wm\_admin

## About this task

The Create Work Order agentic workflow allows users to create work orders from the Now Assist panel. The Create Work Order AI agentic workflow is not activated by default, and must be configured to appear in the Now Assist panel.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **Agentic workflows**.

2.  Select **Create work order**.

3.  Select **Select channels and status**.

4.  Toggle the **Display** for the Now Assist panel so that it's turned on.

    \[Omitted image "now-assist-create-wo-nap-display.png"\] Alt text: Create Work Order configuration screen with Display set to active.

    You have enabled the agentic workflow in the Now Assist panel. If the option isn't available, you must enable the panel first. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/activate-now-assist-panel.md).

5.  Select **Save and test**.


## Result

The Create Work Order agentic workflow will appear in the Now Assist panel. The workflow can be triggered by asking Now Assist to create a work order, or by selecting the Create Work Order button. For more information, see [Create a work order using ServiceNow Otto for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/work-order-management/create-work-order-now-assist-fsm.md).

