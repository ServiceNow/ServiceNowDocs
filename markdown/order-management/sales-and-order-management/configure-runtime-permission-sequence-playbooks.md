---
title: Assign runtime permissions while creating sequences
description: Use permission sets to control access to sequence records such as sequence tasks and steps.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create sequences, Customer Engagement Sequences, Lead and opportunity apps, Use, Sales and Order Management]
---

# Assign runtime permissions while creating sequences

Use permission sets to control access to sequence records such as sequence tasks and steps.

## Before you begin

Delegated developer roles must be assigned to designated users. For more information, see [Grant delegated developer permissions for managing sequences](grant-delegated-developer-permissions.md).

**Note:** Runtime permissions are available only with at least Playbooks version 28.1 on the Zurich release. For more information, see [Playbook release notes](https://www.servicenow.com/docs/access?context=process-automation-designer-rn&version=australia&pubname=australia-release-notes&ft:locale=en-US).

Role required: sn\_crm\_sequence.admin, sn\_crm\_sequence.writer

**Note:** If you're using Customer Engagement Sequences 1.0.0, you need the playbook.admin or pd\_author role to create sequences.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Sequences** &gt; **All Sequences**.

4.  Select a sequence that you're creating or updating.

5.  On the Workflow Studio page, select **Properties** from the More actions menu icon ![](../image/icon-three-dot-menu.png).

6.  On the Playbook properties window, select **Runtime permissions**.

7.  Grant fine-grained access to sequence records by selecting a permission set from the **Add permission set** menu.

    The available permission sets are:

    -   Users
    -   User groups
    -   User criteria
8.  Use the data pill picker to establish a connection between a user, user group, or criteria with a column on the parent table.

    To allow agents to view only their own assigned sequence tasks for a sequence based on the Lead table, you would select Parent Record as Lead and then its **Owner** column. For instance, if user Max Blaze is overlooking a lead, only Max Blaze will be able to view the sequence steps and complete activities.

9.  Confirm your selection and set the permission by selecting the Add permission set icon![](../../../reuse/icons/product-icons/circle-check-outline-24.svg).

10. Grant the level of access by selecting View or Manage or both.

11. Add additional permission sets as needed.

12. Select **Save and close**.


**Parent Topic:**[Create a customer engagement sequence](create-customer-engagement-sequence.md)

