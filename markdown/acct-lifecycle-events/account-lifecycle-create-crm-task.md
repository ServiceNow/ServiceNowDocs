---
title: Create a task in Microsoft Dynamics CRM
description: Create a task in the Microsoft Dynamics CRM platform from your ServiceNow instance and receive updates to the task in your ServiceNow instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using customer success, Customer success, Customer Success Management]
---

# Create a task in Microsoft Dynamics CRM

Create a task in the Microsoft Dynamics CRM platform from your ServiceNow instance and receive updates to the task in your ServiceNow instance.

## Before you begin

Role required: sn\_acct\_lc.ale\_success\_agent

## Procedure

1.  Navigate to **All** &gt; **Customer Success** &gt; **All Risks and Issues**.

2.  Open the risk record for which you want to create a task.

3.  If you have configured the **Create CRM task** option, you can see it on the Risk and Issue page.

    See [Integrating with Microsoft Dynamics CRM](../concept/account-lifecycle-crm-integration.md) for details on configuring this option.

    ![MS Dynamics CRM: Create CRM task](../image/account-lifecycle-crm-create-task-1.png)

4.  Select **Create CRM task**.

    A new task is created in the Microsoft Dynamics CRM platform. The details of the account, engagement, and contracts associated with the risk record are displayed.

    **Note:** If you modify or update Priority or Status fields in the task that was created, the updates are displayed as work notes in your ServiceNow instance.

5.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.

6.  Navigate to **Customer Success** &gt; **All Risks and Issues** and open a risk record.

    You can see the work notes that show how the task was updated.

    ![CRM Task work notes](../image/account-lifecycle-crm-create-task-2.png)

    Work notes are displayed if you have configured:

    -   The Microsoft Dynamics CRM update mechanism \(so that Microsoft Dynamics CRM can access the Microsoft Dynamics spoke webhook\) when the configured event occurs in the task table. See [Set up Microsoft Dynamics CRM spoke](https://www.servicenow.com/docs/access?context=setup-ms-dynamics-crm&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) for details.
    -   Microsoft Dynamics CRM spoke \(see [Microsoft Dynamics CRM Spoke](https://www.servicenow.com/docs/access?context=microsoft-dynamics-crm-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)\).
        -   Decision table as per the requirement
        -   Webhook \(Dynamics Webhook Callbacks\)
    -   Customer Success Management application has been configured for Microsoft Dynamics CRM integration. See [Integrating with Microsoft Dynamics CRM](../concept/account-lifecycle-crm-integration.md) for details.

