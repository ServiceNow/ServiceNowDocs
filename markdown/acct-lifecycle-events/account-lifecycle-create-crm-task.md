---
title: Create a task in Microsoft Dynamics CRM
description: Create a task in the Microsoft Dynamics CRM platform from your ServiceNow instance and receive updates to the task in your ServiceNow instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft Dynamics CRM integration, Customer success, Customer Success Management, Customer Success Management]
---

# Create a task in Microsoft Dynamics CRM

Create a task in the Microsoft Dynamics CRM platform from your ServiceNow instance and receive updates to the task in your ServiceNow instance.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_agent

## Procedure

1.  Navigate to **All** &gt; **Customer Success** &gt; **All Risks and Issues**.

2.  Open the risk record for which you want to create a task.

3.  If you have configured the **Create CRM task** option, you can see it on the Risk and Issue page.

    See [Enable integration with Microsoft Dynamics CRM](../concept/account-lifecycle-crm-integration.md) for details on configuring this option.

4.  Select **Create CRM task**.

    A new task is created in the Microsoft Dynamics CRM platform. The details of the account, engagement, and contracts associated with the risk record are displayed.

    **Note:** If you modify or update Priority or Status fields in the task that was created, the updates are displayed as worknotes in your ServiceNow instance.

5.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.

6.  Navigate to **Customer Success** &gt; **All Risks and Issues** and open an risk record.

    You can see the worknotes that show how the task was updated.

    ![CRM Task worknotes](../image/account-lifecycle-crm-create-task-2.png)

    Worknotes are displayed if you have configured:

    -   The Microsoft Dynamics CRM update mechanism \(so that Microsoft Dynamics CRM can access the Microsoft Dynamics spoke webhook\) when the configured event occurs in the task table. See [Set up Microsoft Dynamics CRM spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-ms-dynamics-crm.md) for details.
    -   Microsoft Dynamics CRM spoke \(see [Microsoft Dynamics CRM Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/microsoft-dynamics-crm-spoke.md)\).
        -   Decision table according to the requirement
        -   Webhook \(Dynamics Webhook Callbacks\)
    -   Customer Success Management application has been configured for Microsoft Dynamics CRM integration. See [Enable integration with Microsoft Dynamics CRM](../concept/account-lifecycle-crm-integration.md) for details.

**Parent Topic:**[Enable integration with Microsoft Dynamics CRM](../concept/account-lifecycle-crm-integration.md)

