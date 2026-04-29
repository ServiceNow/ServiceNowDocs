---
title: Define trigger conditions
description: Define trigger conditions that start a sequence by configuring simple triggers, or combining multiple triggers for initiating workflows from multiple record-based events.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create sequences, Customer Engagement Sequences, Lead and opportunity apps, Use, Sales and Order Management]
---

# Define trigger conditions

Define trigger conditions that start a sequence by configuring simple triggers, or combining multiple triggers for initiating workflows from multiple record-based events.

## Before you begin

**Note:** Multi-trigger capability is available only with Playbooks versions 28.1 and higher on the Zurich release. For more information, see [Playbook release notes](https://www.servicenow.com/docs/access?context=process-automation-designer-rn&version=australia&pubname=australia-release-notes&ft:locale=en-US).

Assign delegated developer roles to designated users. For more information, see [Grant delegated developer permissions for managing sequences](grant-delegated-developer-permissions.md).

Role required: sn\_crm\_sequence.admin, sn\_crm\_sequence.writer

**Note:** If you're using Customer Engagement Sequences 1.0.0, then you need the playbook.admin or pd\_author role to create sequences.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Sequences** &gt; **All Sequences**.

4.  Select a sequence that you're creating or updating.

5.  On the left sidebar, select the Triggers icon ![](../image/triggers-icon.png).

6.  Select an option that indicates when the playbook should run from the to**Add trigger** drop-down list.

    The available options are:

    -   When record is created
    -   When record is update
    -   When record is created or updated
7.  In the **Conditions** field, add conditions that must be met to trigger your playbook.

    To trigger the sequence when a new record is created in the Lead \[sn\_lead\_mgmt\_core\_lead\] table, you would set the condition **\[State\]****\[is\]****\[New\]**.

    For more information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

8.  Select **Save and close**.

9.  To create a multi-trigger sequence, select **Add triggers** from the Triggers pane and repeat the steps of defining the trigger conditions.

    When adding additional triggers, if you select a child table or any other table from the **Trigger table** field, then you must use the data pill picker to select the parent record.

    **Tip:** You can add up to 10 triggers.


## Result

The triggers that you've created appear under the Record based triggers section on the Triggers pane.

**Parent Topic:**[Create a customer engagement sequence](create-customer-engagement-sequence.md)

**Related topics**  


[Triggers](https://www.servicenow.com/docs/access?context=process-automation-designer-triggers&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

[Add and configure a trigger in a playbook](https://www.servicenow.com/docs/access?context=add-configure-trigger&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

