---
title: Remove a supplier contact from the My contacts widget
description: Remove a supplier contact that you no longer require.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Remove a supplier contact from the Supplier Collaboration Portal, Managing supplier contacts from the Supplier Collaboration Portal, Using Supplier Collaboration Portal, Using Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Remove a supplier contact from the My contacts widget

Remove a supplier contact that you no longer require.

## Before you begin

Role required: sn\_slm.contact or sn\_slm.admin

## About this task

The **Remove Contact** option is available only to the primary supplier contact and the supplier administrator.

## Procedure

1.  Navigate to the Supplier Collaboration Portal home page by accessing your instance URL and adding a /supplier suffix.

    For example, `https://example.com/supplier`.

    **Note:** If many-to-many \(M2M\) mapping between supplier contact and suppliers is enabled, you can see the list of all contacts associated with companies where you’re designated as the primary contact.

2.  In the My contacts widget, do one of the following:

    -   Select a contact to open the contact's profile page, and then select **Remove Contact**.
    -   Select the cross icon \(![](../image/cross-icon.png)\) next to the name of the contact that you want to remove.
    The Remove Contact dialog box is displayed.

3.  Select the supplier from the **Supplier** drop-down list.

    **Note:** The **Supplier** drop-down list is available after the Xanadu December 2024 release.

4.  In the **Delegate tasks to** field, search for and select a contact to whom you want to reassign the tasks that are currently assigned to the contact being removed.

5.  In the **Comments** field, enter the reason for removing the contact.

6.  Select **Remove**.

    The contact is removed and all the tasks that were assigned to that contact are reassigned to the alternate contact.


**Parent Topic:**[Remove a supplier contact from the Supplier Collaboration Portal](remove-supplier-contact.md)

