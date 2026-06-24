---
title: Define trigger conditions
description: Define trigger conditions that start a sequence by configuring simple triggers or combining multiple triggers for initiating workflows from multiple record-based events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/define-trigger-conditions.html
release: zurich
topic_type: task
last_updated: "2025-11-11"
reading_time_minutes: 1
breadcrumb: [Create sequences, Customer Engagement Sequences, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Define trigger conditions

Define trigger conditions that start a sequence by configuring simple triggers or combining multiple triggers for initiating workflows from multiple record-based events.

## Before you begin

**Note:** Multi-trigger capability is available only with at least Playbooks version 28.1 on the Zurich release. For more information, see [Playbooks in Workflow Studio release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/release-notes/process-automation-designer-rn.md).

Delegated developer roles must be assigned to designated users. For more information, see [Grant delegated developer permissions for managing sequences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/grant-delegated-developer-permissions.md).

Role required: sn\_crm\_sequence.admin, sn\_crm\_sequence.writer

**Note:** If you're using Customer Engagement Sequences 1.0.0, then you need the playbook.admin or pd\_author role to create sequences.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon \[Omitted image "list-outline-24.svg"\] Alt text:.

3.  Navigate to **Sequences** &gt; **All Sequences**.

4.  Select a sequence that you're creating or updating.

5.  On the left sidebar, select the Triggers icon \[Omitted image "triggers-icon.png"\] Alt text:.

6.  Select an option that indicates when the playbook should run from the **Add trigger** drop-down list.

    The available options are:

    -   When record is created
    -   When record is updated
    -   When record is created or updated
7.  In the **Conditions** field, add conditions that must be met to trigger your playbook.

    To trigger the sequence when a new record is created in the Lead \[sn\_lead\_mgmt\_core\_lead\] table, you would set the condition **\[State\]****\[is\]****\[New\]**.

    For more information, see [Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-user-experiences/c_ConditionBuilder.md).

8.  Select **Save and close**.

9.  Create a multi-trigger sequence by selecting **Add triggers** from the Triggers pane and repeating the steps of defining the trigger conditions.

    When adding additional triggers, if you select a child table or any other table from the **Trigger table** field, you must use the data pill picker to select the parent record.

    **Tip:** You can add up to 10 triggers.


## Result

The new triggers appear in the Record based triggers section of the Triggers pane.

**Parent Topic:**[Create a customer engagement sequence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/create-customer-engagement-sequence.md)

**Related topics**  


[Triggers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio/process-automation-designer-triggers.md)

[Add and configure a trigger in a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio/add-configure-trigger.md)

