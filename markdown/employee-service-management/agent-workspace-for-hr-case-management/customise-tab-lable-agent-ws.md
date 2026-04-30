---
title: Customize tab label in Agent Workspace for HR Case Management
description: Change the tab title for the HR Cases, in Agent Workspace for HR Case Management, based on any of the case field values enabling you to see more details on the tab when multiple tabs are open.
locale: en-US
release: xanadu
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Agent Workspace for HR Case Management, Agent Workspace for HR Case Management \(Configurable\), HR Service Delivery, Employee Service Management]
---

# Customize tab label in Agent Workspace for HR Case Management

Change the tab title for the HR Cases, in Agent Workspace for HR Case Management, based on any of the case field values enabling you to see more details on the tab when multiple tabs are open.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences**.

2.  Select HR Agent Workspace.

3.  Under the UX Page Properties tab, select **caseTabTitleField** property.

    The field value to be displayed on the tab title can be configured here.

4.  In the **Value** field, provide the key value pair.

    The key being the table name, and the value being the field value. For example, "sn\_hr\_core\_case": "opened\_for". The value field has to be a valid JSON.

    Tab titles can also contain multiple fields. The key value remains the table name, but the value can be a list of strings. For example: "sn\_hr\_core\_case": \["opened\_for", "number"\].

5.  Click **Update**.


