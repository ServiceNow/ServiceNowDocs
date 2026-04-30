---
title: Restrict the primary contact role for a contact from the Source-to-Pay Workspace
description: Remove the primary contact role for a contact to prevent them from accessing all the contacts and tasks in the Supplier Collaboration Portal.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing supplier contacts from the Source-to-Pay Workspace, Using Source-to-Pay Workspace, Using Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Restrict the primary contact role for a contact from the Source-to-Pay Workspace

Remove the primary contact role for a contact to prevent them from accessing all the contacts and tasks in the Supplier Collaboration Portal.

## Before you begin

Role required: sn\_slm.owner

**Note:**

-   The sn\_slm.owner role can restrict access only for the contacts of the suppliers they own.
-   This functionality is not available in Xanadu December 2024 release.

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Under My suppliers, select the legal name of the supplier.

    The supplier details page is displayed.

3.  On the **About** tab, under Supplier Contacts, select the supplier contact that has the Admin label next to their name.

    **Note:** Each supplier must have at least one primary contact. You cannot restrict access for a primary contact if that contact is the only primary contact for the supplier.

4.  Select **Restrict access**.

    The Primary contact column is set to **false** for this contact on the new table page, and the contact no longer has the primary contact role.


**Parent Topic:**[Managing supplier contacts from the Source-to-Pay Workspace](../concept/managing-contacts-smw.md)

