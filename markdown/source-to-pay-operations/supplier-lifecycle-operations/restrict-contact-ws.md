---
title: Restrict the primary contact role for a contact from the Source-to-Pay Workspace
description: Remove the primary contact role for a contact to prevent them from accessing all the contacts and tasks in the Supplier Collaboration Portal.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage supplier contacts from the Source-to-Pay Workspace, Using Source-to-Pay Workspace, Using Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Restrict the primary contact role for a contact from the Source-to-Pay Workspace

Remove the primary contact role for a contact to prevent them from accessing all the contacts and tasks in the Supplier Collaboration Portal.

## Before you begin

Role required: sn\_slm.owner, sn\_slm.manager, sn\_slm.admin

**Note:** Users with the sn\_slm.owner role can restrict access only for the contacts of the suppliers they own. Users with sn\_slm.manager and sn\_slm.admin roles can restrict access for any supplier.

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Under **Quick Actions**, select **Manage my suppliers**.

3.  Select the legal name of the supplier.

4.  On the supplier details page, select the **Stakeholders** tab.

5.  Select **Supplier contacts**.

6.  Select the supplier contact that you want to restrict.

7.  Select **Restrict access**.![Selected Restrict access button.](../image/restrict-access-primary-contact.png)


## Result

The Primary contact column is set to **false** for this contact on the new table page, and the contact no longer has the primary contact role.

**Parent Topic:**[Manage supplier contacts from the Source-to-Pay Workspace](../concept/managing-contacts-smw.md)

**Related topics**  


[Add a supplier contact from the Source-to-Pay Workspace](add-supplier-contact.md)

[Remove a supplier contact from the Source-to-Pay Workspace](remove-supp-contact-ws.md)

[Elevate a contact to the primary contact role from the Source-to-Pay Workspace](elevate-contact-ws.md)

