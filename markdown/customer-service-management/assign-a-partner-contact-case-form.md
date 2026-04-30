---
title: Assign a partner contact on the case form
description: Enable Customer Service Management agents to assign partner contacts for an account that is associated to an install base item on the case form. By adding partner contacts, you can provide access to multiple partners to access their accounts.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Case form, Customer Service forms, Reference, Customer Service Management]
---

# Assign a partner contact on the case form

Enable Customer Service Management agents to assign partner contacts for an account that is associated to an install base item on the case form. By adding partner contacts, you can provide access to multiple partners to access their accounts.

## Before you begin

Role required: customer service agent

## Procedure

1.  Navigate to **CSM/FSM Configurable Workspace** &gt; **Cases** &gt; **My Cases**.

2.  Select **New**.

3.  In the **Install Base** field, use the search icon ![Search icon.](../image/search_icon.png) to add an install base item on the Create Case form.

    The **Account** and **Contact** fields are automatically filled from the install base form. For a description of the field values, see [Case task form](../reference/csm-case-task-form.md).

4.  In the **Partner** field, use the search icon to ![Search icon.](../image/search_icon.png) search for a partner associated with the selected account.

    The partner in the **Partner** field is the partner account that is associated with the account.

5.  In the **Partner Contact** field, enter an eligible partner contact who has the following criteria:

    -   All partner contacts of the partner account are eligible if the **Restrict Account Access** isn't enabled.
    -   All partner contacts with the partner admin role are eligible if **Restrict Account Access** is enabled.
    -   Partner contacts that are added as an Authorized Representative through the related party list for the install base item.
    -   Partner contacts that are added as an Authorized Account through the related party list for the install base item.
    To add a related party to an install base item, see [Add related parties to an install base item](add-related-party-install-base.md).

6.  Select **Submit**.


## Result

A partner contact is assigned to the case.

